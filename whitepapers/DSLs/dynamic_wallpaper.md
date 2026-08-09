# **Dynamic Island Wallpaper: Scene DSL Technical Whitepaper**  
**Version 0.1**

---

## **Abstract**  
Dynamic Island Wallpaper introduces a deterministic, symbolic Scene Domain‑Specific Language (Scene DSL) designed to describe environmental state for a small island vignette. The DSL acts as a semantic contract between a Prolog‑based inference engine and any rendering backend—deterministic or generative. This whitepaper formalizes the DSL’s purpose, structure, semantics, and versioning strategy, ensuring long‑term stability and renderer independence.

---

# **1. Introduction**

Modern ambient experiences often rely on complex rendering pipelines tightly coupled to telemetry or procedural logic. This coupling reduces portability, increases maintenance cost, and complicates deterministic behavior. Dynamic Island Wallpaper addresses these issues by introducing a **minimal, declarative, symbolic DSL** that abstracts environmental state into finite categories.

The Scene DSL is intentionally constrained:

- **No numeric telemetry**  
- **No rendering instructions**  
- **No procedural directives**  
- **No generative hints**

Instead, it provides a stable symbolic description of sky, weather, tide, wind, waves, palette, and daily rhythm. Renderers—whether deterministic compositors or non‑deterministic diffusion models—consume the same DSL and interpret it according to their own capabilities.

---

# **2. Design Goals**

The Scene DSL is engineered to be:

- **Deterministic** — identical input yields identical symbolic output  
- **Declarative** — describes *what is*, not *how to render it*  
- **Finite** — all fields use closed enumerations  
- **Renderer‑agnostic** — compatible with procedural and generative pipelines  
- **Minimal** — no extraneous fields or telemetry  
- **Stable & versionable** — future‑proof without breaking older scenes  

These constraints ensure predictable behavior across devices, runtimes, and renderer implementations.

---

# **3. DSL Structure**

A valid Scene DSL document is a JSON object containing all required symbolic fields:

```json
{
  "version": "0.0.1",

  "sunposition": "<enum>",
  "sun_height": "<enum>",
  "sky_mode": "<enum>",
  "weather": "<enum>",
  "moon": "<enum>",
  "stars": "<boolean>",

  "tide_state": "<enum>",
  "wind_strength": "<enum>",
  "wave_intensity": "<enum>",
  "island_palette": "<enum>",

  "daily_state": "<enum>"
}
```

All fields are mandatory in v0.0.1.

---

# **4. Sky & Weather Model**

The DSL abstracts solar, lunar, and atmospheric conditions into symbolic buckets.

## **4.1 Solar Position**

### `sunposition`  
Symbolic azimuth bucket:

- `"none"`  
- `"bottomleft" | "bottomright"`  
- `"midleft" | "midright"`  
- `"topleft" | "topright"`

### `sun_height`  
Symbolic altitude bucket:

- `"none"`  
- `"low"`  
- `"medium"`  
- `"high"`

### `sky_mode`  
Time‑of‑day category:

- `"night"`  
- `"dawn"`  
- `"day"`  
- `"dusk"`

## **4.2 Atmospheric Conditions**

### `weather`  
Symbolic weather state:

- `"clear"`  
- `"cloudy"`  
- `"approaching_rain"`  
- `"rain"`

### `moon`  
Visible lunar phase:

- `"none"`  
- `"crescent"`  
- `"half"`  
- `"gibbous"`  
- `"full"`

### `stars`  
Star visibility:

- `true`  
- `false`

Stars are visible only when:

- `moon = "none"`  
- `sky_mode = "night"`

---

# **5. Island Environmental Model**

## **5.1 Tide**

`tide_state`:

- `"low"`  
- `"medium"`  
- `"high"`

## **5.2 Wind**

`wind_strength`:

- `"none"`  
- `"breeze"`  
- `"windy"`  
- `"strong"`

## **5.3 Waves**

`wave_intensity`:

- `"calm"`  
- `"gentle"`  
- `"rough"`  
- `"storm"`

Wave intensity is derived from wind + weather.

## **5.4 Palette**

`island_palette`:

- `"day"`  
- `"sunset"`  
- `"night"`

Palette is derived from `sky_mode`.

---

# **6. Daily Rhythm Model**

The DSL includes symbolic cues for character behavior and ambient rhythm. These cues do not specify animation frames or rendering logic.

`daily_state`:

- `"morning_start"` — coffee animation  
- `"work_start"` — sitting animation  
- `"day_progress"` — neutral scene  
- `"break_time"` — callisthenics animation  
- `"evening"` — wave animation  
- `"sleep_time"` — campfire extinguish animation  

These states are derived from user schedule + solar telemetry.

---

# **7. Semantic Rules (Telemetry → DSL)**

The Prolog engine converts raw telemetry into symbolic categories.

## **7.1 Solar Altitude → `sun_height`**

- alt < 0° → `"none"`  
- alt < 10° → `"low"`  
- alt < 35° → `"medium"`  
- alt ≥ 35° → `"high"`

## **7.2 Solar Azimuth + Altitude → `sunposition`**

Hemisphere‑aware symbolic buckets.

## **7.3 Sky Mode**

- alt < −6° → `"night"`  
- −6° ≤ alt ≤ 6° → `"dawn"` or `"dusk"`  
- alt > 6° → `"day"`

## **7.4 Moon Visibility**

- moon_alt < 0° → `"none"`  
- otherwise → bucketed phase

## **7.5 Stars**

Visible only when:

- `moon = "none"`  
- `sky_mode = "night"`

## **7.6 Tide**

- < 0.5 m → `"low"`  
- 0.5–1.2 m → `"medium"`  
- > 1.2 m → `"high"`

## **7.7 Wind**

- < 2 m/s → `"none"`  
- 2–5 m/s → `"breeze"`  
- 5–10 m/s → `"windy"`  
- > 10 m/s → `"strong"`

## **7.8 Waves**

Derived from wind + weather.

## **7.9 Palette**

Derived from sky_mode.

## **7.10 Daily Rhythm**

Derived from user schedule + sunrise/sunset.

---

# **8. Renderer Independence**

The DSL is intentionally renderer‑agnostic. Two renderer classes exist:

## **8.1 Deterministic Procedural Compositor**

- Same DSL → identical PNG  
- Byte‑for‑byte reproducible  
- No randomness  
- No diffusion  
- No sampling  

## **8.2 Non‑Deterministic Generative Renderer**

- Uses diffusion or img2img  
- Output varies even with fixed seeds  
- GPU nondeterminism applies  
- Not byte‑for‑byte reproducible  

The DSL remains stable and deterministic regardless of renderer choice.

---

# **9. Versioning Strategy**

- DSL versions are immutable  
- Renderers must ignore unknown fields  
- Prolog rules may evolve independently  
- Telemetry sources may change without affecting DSL structure  

This ensures long‑term compatibility and forward evolution.

---

# **10. Conclusion**

The Scene DSL v0.0.1 provides a deterministic, symbolic, renderer‑agnostic foundation for Dynamic Island Wallpaper. Its minimal, finite structure ensures stability across rendering technologies while enabling expressive environmental storytelling. As telemetry sources and rendering techniques evolve, the DSL remains a stable semantic backbone.

---

