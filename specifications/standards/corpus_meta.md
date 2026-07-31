# **CLASSIFICATION: D**  
Document Reference: `2026-000-meta`  
# **Unified Corpus Meta‑Standard (U‑CMS)**  
### Constitutional Governance Specification v1.0  
### Corpus‑Level Governance & Architecture Standard  
---  
#### William Murray  
#### 31 July 2026  
---  
**Status:** Stable  
**Scope:** Governs the entire design corpus, including all standards, templates, and governance engines.  
**Primary Model / Scheme:** Corpus Governance Model (CGM)  

---

# **Scope**
This Meta‑Standard defines the **constitutional governance rules** for the entire design corpus.  
It establishes:

- corpus boundaries  
- corpus‑integrity rules  
- corpus‑level roadmap governance  
- corpus‑level transition rules  
- justification and audit requirements  
- structural expectations for subordinate standards  

Applicability:

- All standards within the governed corpus  
- All governance engines  
- All architectural specifications  
- All title‑page standards  
- All versioning standards  
- All future standards derived from the Technical Standard Template  

Exclusions:

- Artefacts outside the governed corpus  
- Operational documentation not governed by constitutional rules  

---

# **Primary Model / Scheme: CGM**  
The **Corpus Governance Model (CGM)** defines the constitutional layer that all subordinate standards must obey.

CGM comprises:

1. **Corpus Constitution Layer**  
2. **Corpus Roadmap Layer**  
3. **Corpus Integrity Layer**  
4. **Corpus Transition Layer**  
5. **Corpus Audit Layer**  

---

# **1. Introduction**
The governed corpus requires a **single constitutional authority** ensuring deterministic evolution, structural coherence, and governance integrity across all standards.

This Meta‑Standard defines that authority.

It ensures:

- all standards evolve coherently  
- all standards obey the same governance primitives  
- all standards share a unified roadmap  
- all standards remain internally compatible  
- all changes are justified, auditable, and reproducible  

The U‑CMS is the **root governance document** for the entire corpus.

---

# **2. Normative References**
This Meta‑Standard is self‑contained. Optional alignment:

- ISO/IEC/IEEE 42010 — Architecture Description  
- Semantic Versioning 2.0.0 (informative)  
- Corporate governance frameworks  
- Constitutional design principles  

---

# **3. Terms and Definitions**

**Corpus**  
The complete set of governed standards, specifications, and architectural artefacts.

**Subordinate Standard**  
Any standard governed by the U‑CMS (e.g., Versioning Standard, SC‑TPGM).

**Corpus Roadmap**  
A version‑controlled artefact defining intended evolution of the entire corpus.

**Corpus Integrity**  
The property ensuring all standards remain structurally coherent, aligned, and non‑contradictory.

**Corpus Transition**  
A state change affecting standards, versions, or corpus structure.

**ADR**  
Architectural Decision Record used to justify changes.

---

# **4. Corpus Constitution Layer**
The corpus shall be governed by a single constitutional authority defined in this Meta‑Standard.

Constitutional rules:

- All standards must conform to U‑CMS.  
- All standards must inherit corpus‑integrity rules.  
- All standards must reference the corpus roadmap.  
- All standards must use the Technical Standard Template (TST) structure.  
- All standards must be version‑controlled.  

Subordinate standards include:

1. **SV‑GOV** — Versioning Specification  
2. **SC‑TPGM** — Title‑Page & Classification Standard  
3. **TST** — Technical Standard Template  
4. Any future standards approved via ADR  

---

# **5. Corpus Roadmap Layer (Normative)**

## **5.1 Roadmap Requirements**
- The corpus roadmap **shall** be part of the design corpus.  
- The roadmap **shall** be version‑controlled.  
- Deviations **shall** require ADR justification.  
- All standards must align with the roadmap.  

## **5.2 Roadmap Invalidation Rule**
A standard or version is **invalid** if it contradicts the corpus‑versioned roadmap.

---

# **6. Corpus Integrity Layer (Normative)**

A standard is **invalid** if it:

- contradicts another standard  
- contradicts the corpus roadmap  
- omits mandatory structural elements  
- violates corpus‑level compatibility rules  
- introduces undocumented behaviour  
- alters architectural boundaries without MAJOR justification  
- fails to use the Technical Standard Template  

Corpus integrity is constitutional, not optional.

---

# **7. Corpus Transition Layer (Normative)**

## **7.1 Allowed Transitions**
- Draft → Stable  
- Stable → Deprecated  
- Standard vX → Standard vX+1  
- Corpus vX → Corpus vX+1  

## **7.2 Forbidden Transitions**
- Deprecated → Stable without ADR  
- Structural change → MINOR increment  
- Any transition contradicting the roadmap  
- Any transition bypassing ADR justification  

## **7.3 Preconditions**
- **MAJOR:** structural or constitutional change  
- **MINOR:** capability expansion  
- **PATCH:** stability refinement  

These preconditions apply to **all subordinate standards**.

---

# **8. Corpus Tagging Requirements (Normative)**

All standards shall be tagged with:

- corpus identifier  
- standard identifier  
- version identifier  
- ADR reference  

Tagging shall be consistent across:

- title pages  
- metadata blocks  
- changelogs  
- release notes  

Tagging forms part of the constitutional audit trail.

---

# **9. Corpus Change Protocol (Normative)**

- All changes require ADR justification.  
- Boundary‑altering changes require MAJOR increments.  
- Corpus changes are versioned independently of subordinate standards.  
- Corpus integrity must be preserved across all transitions.  

---

# **10. Corpus Audit Layer (Normative)**

The corpus shall support:

- architectural decision traceability  
- governance auditability  
- compliance alignment  
- deterministic evolution  

All changes must be reviewable, reproducible, and justified.

---

# **11. Subordinate Standards (Informative)**

The following standards are governed by U‑CMS:

### **11.1 SV‑GOV — Versioning Specification**  
Defines MAJOR/MINOR/PATCH, version integrity, roadmap alignment.

### **11.2 SC‑TPGM — Title‑Page & Classification Standard**  
Defines classification (A–D), title‑page structure, typography, signalling.

### **11.3 TST — Technical Standard Template**  
Defines canonical structure for all future standards.

### **11.4 Future Standards**  
Must be approved via ADR and conform to U‑CMS.

---

# **12. Document Control**

**Document Owner:** Corpus Governance Authority  
**Change Authority:** Architectural Decision Records (ADRs)  
**Review Cycle:** Per MAJOR corpus change  

---

# **v1.0 Summary of Changes**
- Established constitutional corpus governance  
- Defined corpus roadmap rules  
- Defined corpus integrity rules  
- Defined corpus transition state machine  
- Defined subordinate standard structure  
- Unified governance primitives across all standards  

---

# **Changelog**
| Version ID | Date | Key Changes |
|-----------|------|-------------|
| 1.0 | 2026‑07‑31 | Initial constitutional release |

---

