# **CLASSIFICATION: D**  
Document Reference: `2026-007-spec-D`  
Version: `1.0`  
Status: `ACTIVE`  
Effective Date: `2026-08-01`  
Next Review: `2027-08-01`  
Owner / Custodian: `William Murray`  
Classification Authority: `Founding Chief Architect`  
Distribution: `OPEN`  
Supersedes: `—`  

# **IDM-01 — Information Disclosure Matrix Specification**  

---

## 1. Purpose & Scope

This specification defines the **Information Disclosure Matrix (IDM)** protocol for the Corpus. It establishes a deterministic, multi-level security (MLS) projection mechanism that dynamically transforms the **Master Asset Registry** into clearance-restricted view catalogs based on authenticated user clearance grades (`D`, `C`, `B`, `A`).

The objective is to enforce mandatory access control (MAC) and prevent spillage while maintaining cryptographic chain-of-custody, system-wide auditability, and deterministic structural verification.

---

## 2. Security Clearance Tiers & Information Barriers

System principals and computational assets are categorized into four explicit security clearance tiers:

| Clearance Code | Name | Handling Constraints | Access Boundary |
| --- | --- | --- | --- |
| **`D`** | Public / Unrestricted | Standard web protocols; open distribution. | Unrestricted public interface. |
| **`C`** | Internal / Restricted | Authenticated internal network session. | Internal operations & contributors. |
| **`B`** | Confidential / Commercial | Encrypted channel; multi-factor authentication. | Authorized, role-bounded personnel. |
| **`A`** | Air-Gapped / Isolated | Physically isolated / air-gapped compute node. | Local sovereign environment only. |

---

## 3. Projection Transformation Matrix

When a catalog view is generated for a principal operating at clearance level $C_{user}$, every master registry entry $E$ with classification grade $G_{asset}$ MUST undergo field-level transformation according to the following matrix:

```
           ┌─────────────────────────────────────────────────────────┐
           │                   Asset Grade (G_asset)                 │
┌──────────┼───────────────┬───────────────┬───────────────┬─────────┤
│ User (C) │       D       │       C       │       B       │    A    │
├──────────┼───────────────┼───────────────┼───────────────┼─────────┤
│    D     │ Full + Link   │ Full (NoLink) │ Partial (Red) │ RefOnly │
│    C     │ Full + Link   │ Full + Link   │ Full (NoLink) │ RefOnly │
│    B     │ Full + Link   │ Full + Link   │ Full + Link   │ Partial │
│    A     │ Full + Link   │ Full + Link   │ Full + Link   │ Full    │
└──────────┴───────────────┴───────────────┴───────────────┴─────────┘

```

### Transformation Field Logic

1. **`Full + Link` (Unrestricted View):**
* All metadata fields rendered (`Document Ref`, `Class`, `Type`, `Version`, `Status`, `Effective Date`, `Next Review`, `Owner`, `Distribution`, `Supersedes`, `Canonical Title`).
* Payload payload URL / path active.


2. **`Full (NoLink)` (Existence Aware, Payload Redacted):**
* All metadata fields rendered.
* `Canonical Title` appended with `(Restricted Access)`.
* Payload URI omitted or pointed to access request endpoint.


3. **`Partial (Red)` (Redacted Metadata View):**
* `Document Ref`, `Class`, `Type`, `Version`, `Status`, `Effective Date`, `Next Review`, `Owner`, `Distribution`, `Supersedes` rendered.
* `Canonical Title` replaced with literal string `[REDACTED]`.
* Payload link omitted.


4. **`RefOnly` (Minimal Existence Ledgering):**
* `Document Ref` rendered.
* `Class` rendered.
* All other fields replaced with static null indicator `—`.
* `Canonical Title` replaced with literal string `[REDACTED]`.
* Payload link omitted.



---

## 4. Deterministic Transformation Rules (Prolog Spec)

The transformation logic MUST be implemented as a deterministic rule set. The following symbolic reference rules define the core filtering engine:

```prolog
:- module(idm_projection, [project_registry_entry/3]).

% project_registry_entry(+UserClearance, +MasterEntry, -ProjectedEntry)

% Grade D Assets are always fully visible across all clearance tiers
project_registry_entry(_UserClearance, entry(Ref, 'D', Type, Ver, Stat, Eff, Rev, Own, Dist, Sup, Title, Link),
                       projected(Ref, 'D', Type, Ver, Stat, Eff, Rev, Own, Dist, Sup, Title, Link)) :- !.

% Same-level or higher clearance gets full document access
project_registry_entry(UserC, entry(Ref, AssetG, Type, Ver, Stat, Eff, Rev, Own, Dist, Sup, Title, Link),
                       projected(Ref, AssetG, Type, Ver, Stat, Eff, Rev, Own, Dist, Sup, Title, Link)) :-
    clearance_gte(UserC, AssetG), !.

% Grade C Asset requested by Grade D User -> Full Metadata, Link Redacted
project_registry_entry('D', entry(Ref, 'C', Type, Ver, Stat, Eff, Rev, Own, Dist, Sup, Title, _Link),
                       projected(Ref, 'C', Type, Ver, Stat, Eff, Rev, Own, Dist, Sup, RedactedTitle, '—')) :-
    atom_concat(Title, ' (Restricted Access)', RedactedTitle), !.

% Grade B Asset requested by Grade D or C User -> Metadata Visible, Title Redacted
project_registry_entry(UserC, entry(Ref, 'B', Type, Ver, Stat, Eff, Rev, Own, Dist, Sup, _Title, _Link),
                       projected(Ref, 'B', Type, Ver, Stat, Eff, Rev, Own, Dist, Sup, '[REDACTED]', '—')) :-
    member(UserC, ['D', 'C']), !.

% Grade A Asset requested by lower clearance -> Reference ID Only
project_registry_entry(_UserClearance, entry(Ref, 'A', _Type, _Ver, _Stat, _Eff, _Rev, _Own, _Dist, _Sup, _Title, _Link),
                       projected(Ref, 'A', '—', '—', '—', '—', '—', '—', '—', '—', '[REDACTED]', '—')) :- !.

% Helper: Clearance Hierarchy Evaluation
clearance_level('A', 4).
clearance_level('B', 3).
clearance_level('C', 2).
clearance_level('D', 1).

clearance_gte(C1, C2) :-
    clearance_level(C1, V1),
    clearance_level(C2, V2),
    V1 >= V2.

```

---

## 5. Security & Verification Invariants

1. **Title Confidentiality:** Canonical titles of Class `B` and Class `A` assets MUST NOT be rendered or leaked in build artifacts destined for public environment deployment.
2. **Reference Integrity:** Reference sequence IDs (e.g., `2026-001-kernel-A`) MUST remain preserved across all projection views to maintain global sequence auditability.
3. **No Inference Vector:** Error responses for direct payload requests at invalid clearance levels MUST return `404 Not Found` rather than `403 Forbidden` to prevent resource enumeration.

---
