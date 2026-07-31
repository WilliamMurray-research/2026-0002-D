Document Reference: `2026-001-spec`
# Versioning Specification - General Reference Standard
### Technical Standard v1.0
### Governance & Architecture Specification  
---
#### William Murray 
#### 21 July 2026
---
| **Status** | Stable |
| **Scope** | Applicable to software systems, platforms, kernels, and governance engines requiring structured version control |
| **Versioning Model** | Semantic Versioning (MAJOR.MINOR.PATCH) |
---

---

## **Scope**
Applicable to software systems, platforms, kernels, and governance engines requiring deterministic, auditable, constitutionally governed version control.

## **Versioning Model**
All governed systems **shall** use:

```
MAJOR.MINOR.PATCH
```

Version identifiers are architectural artefacts encoding structural evolution, capability expansion, and stability refinement.

---

# **1. Introduction**
This Standard defines the normative requirements for version identification, classification, governance, and lifecycle management. Version progression is treated as a constitutional mechanism ensuring deterministic evolution, architectural integrity, and governance traceability.

---

# **2. Normative References**
This specification is self‑contained. Optional alignment:

- ISO/IEC 27001 — Information Security Management  
- ISO/IEC/IEEE 42010 — Architecture Description  
- Semantic Versioning 2.0.0 (informative reference only)

---

# **3. Terms and Definitions**

**Version Identifier**  
A structured label consisting of MAJOR, MINOR, and PATCH components.

**Architectural Epoch**  
A system‑wide structural change requiring a MAJOR increment.

**Capability Expansion**  
A backward‑compatible functional enhancement requiring a MINOR increment.

**Stability Refinement**  
A non‑behavioural improvement requiring a PATCH increment.

**Design Corpus**  
The authoritative set of documents defining system architecture, governance, and operational boundaries.

**Roadmap (Corpus‑Versioned)**  
A version‑controlled artefact defining intended system evolution.

---

# **4. Versioning Model**
Each component of the version identifier **shall** reflect the class of change introduced:

- **MAJOR** — architectural epoch  
- **MINOR** — capability expansion  
- **PATCH** — stability refinement  

---

# **5. Version Classes (Normative)**

## **5.1 MAJOR Version — Architectural Epochs**
A MAJOR increment **shall** be applied when changes introduce structural or constitutional modifications.

A MAJOR increment is required when any of the following occur:

- Introduction of a new architectural runtime or execution model  
- Introduction of enterprise‑grade envelopes (multi‑tenancy, RBAC, compliance frameworks)  
- Schema‑breaking changes  
- Redefinition of module or subsystem boundaries  
- Modification of constitutional architecture or governance primitives  

MAJOR versions represent **architectural epochs**.

---

## **5.2 MINOR Version — Capability Expansion**
A MINOR increment **shall** be applied when new capabilities are added without breaking compatibility.

A MINOR increment is required when any of the following occur:

- Addition of new modules or subsystems  
- Introduction of new CRUD or operational features  
- Addition of synchronisation or integration capabilities  
- Security enhancements  
- **Any backward‑compatible schema expansion, including addition of optional or minor fields**  
- Addition of new UI pages, workflows, or operational refinements  

MINOR versions represent **functional growth**.

---

## **5.3 PATCH Version — Stability & Polish**
A PATCH increment **shall** be applied when changes do not alter system behaviour or structure.

A PATCH increment is required when any of the following occur:

- Defect correction  
- UI/UX polish  
- Documentation improvements  
- Refactoring without behavioural change  

PATCH versions represent **stability improvements**.

**Note:**  
Schema changes **shall not** be classified as PATCH under v1.1.

---

# **6. Version Governance Requirements (Normative)**

1. **Documentation Requirement**  
   All changes shall be recorded in a changelog.

2. **Justification Requirement**  
   Each increment shall reference an ADR.

3. **ADR Placement Requirement**  
   ADR identifiers **shall** appear in:  
   - Git tag annotation  
   - Changelog entry  
   - Release metadata  

4. **Compatibility Requirement**  
   Backward compatibility shall be preserved unless a MAJOR increment is declared.

5. **Corpus Integrity Requirement**  
   All changes shall maintain the integrity of the design corpus.

Versioning is a **constitutional mechanism**, not an operational convenience.

---

# **7. Target Maturity Framework (Informative)**

This section describes a **reference lifecycle** for typical system evolution.  
It does **not** constrain version arithmetic, which is governed solely by Section 5.

## **7.1 Pre‑Functional Scaffolding (v0.x)**
Characteristics:
- No functional logic  
- No persistence  
- No workflows  
- No authentication  
- No automation  
- No symbolic reasoning  

Purpose: Define membranes, module boundaries, and structural scaffolding.

---

## **7.2 Local Functional Kernel (v1.x)**
Capabilities:
- CRUD operations  
- Standards or document attachments  
- Local persistence  
- Local execution environment  

Purpose: Provide a deterministic, self‑contained operational kernel.

---

## **7.3 Symbolic or Advanced Runtime Integration (v2.x)**
Capabilities:
- Symbolic or logic‑based runtimes  
- Event‑driven architecture  
- Immutable logs  
- Cryptographic signing  
- Advanced reasoning or automation modules  

Purpose: Enable neurosymbolic or advanced governance capabilities.

---

## **7.4 Enterprise Envelope (v3.x)**
Capabilities:
- Multi‑tenancy  
- Role‑based access control  
- Compliance integrations  
- Environmental or operational monitoring  
- Distributed or microservice architectures  

Purpose: Provide enterprise‑grade governance and compliance.

---

# **8. Tagging Requirements (Normative)**

All releases **shall** be tagged using a version identifier matching all documentation references.

Tagging shall be consistent across:

- Versioning documentation  
- Changelog  
- System status or release notes  

Tagging forms part of the audit trail.

---

# **9. Pre‑Release Identifiers (Normative)**

Pre‑release suffixes shall follow semantic versioning conventions:

- **alpha** — unstable, experimental  
- **beta** — feature‑complete but unrefined  
- **rc** — release candidate  

Examples:
- `1.0.0-alpha`  
- `1.0.0-rc.1`  

---

# **10. Version Integrity Rules (Normative)**

A version shall be considered **invalid** if it:

- Introduces undocumented behaviour  
- Violates structural or compliance alignment  
- Changes architecture without a MAJOR increment  
- Adds features without a MINOR increment  
- Fixes behaviour without a PATCH increment  
- **Contradicts the corpus‑versioned roadmap**

---

## **10.1 Roadmap Governance (Normative)**

- The roadmap **shall** be part of the Design Corpus.  
- The roadmap **shall** be version‑controlled.  
- Deviations from the roadmap **shall** be justified via ADR.  
- A version is invalid if it contradicts the **current corpus‑versioned roadmap**.

---

# **11. Corpus Change Protocol (Normative)**

- Corpus changes require ADR justification.  
- Corpus changes altering architectural boundaries require MAJOR increments.  
- Corpus changes shall be versioned independently of software releases.  
- Corpus integrity shall be preserved across all version transitions.

---

# **12. Version Transition State Machine (Normative)**

### **Allowed Transitions**
- `MAJOR → MINOR → PATCH`  
- `MAJOR → PATCH` (if no new capabilities are added)  
- `MINOR → PATCH`  
- `PATCH → PATCH`  

### **Forbidden Transitions**
- `PATCH → MINOR` without ADR justification  
- `PATCH → MAJOR` without ADR justification  
- `MINOR → MAJOR` without structural change  
- Any transition contradicting the corpus‑versioned roadmap  

### **Preconditions**
- MAJOR: structural or constitutional change  
- MINOR: capability expansion  
- PATCH: stability refinement  

This state machine ensures deterministic version progression.

---

# **13. Compliance & Audit**

Versioning shall support:

- Architectural decision traceability  
- Governance auditability  
- Compliance alignment  
- Deterministic evolution of the system  

All version changes shall be reviewable, reproducible, and justified.

---

# **14. Document Control**

**Document Owner:** Governance Authority  
**Change Authority:** Architectural Decision Records (ADRs)  
**Review Cycle:** Per MAJOR release or structural amendment  

---

## **v1.1 Summary of Changes**
- Consolidated all schema additions under MINOR  
- Clarified Section 7 as a Target Maturity Framework  
- Added Roadmap Governance rules  
- Added ADR placement requirements  
- Added Corpus Change Protocol  
- Added Version Transition State Machine  

---

