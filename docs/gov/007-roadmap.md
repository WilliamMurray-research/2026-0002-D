# **CLASSIFICATION: D**  
Document Reference: `2026-007-roadmap`  

---
# **Corpus Roadmap v1.1 — Governed Corpus Architecture**  

#### William Murray  
#### 31 July 2026  
---

### **Status:** Stable  
### **Maintainer:** Corpus Governance Authority  

---

## **1. Purpose**
This roadmap defines the planned evolution of the governed corpus architecture.  
It provides a deterministic, constitutional pathway for:

- new standards  
- amendments  
- ADR‑driven changes  
- structural evolution  
- governance extensions  

All future corpus changes must align with this roadmap.  
Contradictions invalidate documents under U‑CMS §6 (Corpus Integrity).

---

## **2. Scope**
This roadmap applies to:

- the Unified Corpus Meta‑Standard (U‑CMS)  
- all governed standards (`spec`)  
- all ADRs (`adr`)  
- all governance notices (`notice`)  
- all corpus‑level artefacts (`roadmap`)  

It governs both structural and semantic evolution.

---

## **3. Corpus Architecture Overview**
The corpus consists of:

- **2026‑001‑meta_spec** — Unified Corpus Meta‑Standard  
- **2026‑002‑spec** — SC‑TPGM  
- **2026‑003‑spec** — TST  
- **2026‑004‑spec** — SV‑GOV  
- **2026‑005‑adr** — ADR‑010 (Suffix Schema Formalization)  
- **2026‑006‑notice** — Contributions Disabled Notice  
- **2026‑007‑roadmap** — This document  

These artefacts form the constitutional foundation of the corpus.

---

## **4. Roadmap Principles**
All roadmap items must adhere to:

1. **Determinism** — No ambiguous evolution.  
2. **Traceability** — All changes justified via ADR.  
3. **Integrity** — No contradictions across standards.  
4. **Consistency** — All documents follow SC‑TPGM + TST.  
5. **Auditability** — All changes are reviewable and reproducible.

These principles are binding.

---

## **5. Planned Standards**
### **5.1 SV‑GOV v1.1 (2026‑004‑spec)**
The Versioning Governance Standard will be expanded to include:

- suffix‑aware versioning rules  
- corpus‑level lifecycle governance  
- ADR placement rules  
- pre‑release identifiers  
- version transition state machine  
- corpus‑aligned version semantics  

### **5.2 Future Standards (Reserved)**
Document references reserved for future standards:

- `2026-008-spec`  
- `2026-009-spec`  

These require ADR justification before use.

---

## **6. Structural Evolution**
### **6.1 SC‑TPGM Amendments**
SC‑TPGM will be updated to include:

- §8.4 — Normative suffix schema  
- vocabulary harmonization (“without ADR justification”)  

### **6.2 TST Amendments**
TST will be updated to include:

- §5.11 — Reference to suffix schema  
- canonical stub for unused mandatory sections  

### **6.3 Corpus Index**
A corpus‑level index will be introduced to unify:

- standards  
- ADRs  
- notices  
- roadmap entries  

---

## **7. Governance Extensions**
### **7.1 Corpus Linter**
A deterministic validation engine will be developed to enforce:

- SC‑TPGM metadata correctness  
- TST section topology  
- suffix schema compliance  
- ADR linkage  
- versioning rules  
- roadmap alignment  

### **7.2 Corpus Registry Automation**
Automated generation of:

- registry tables  
- suffix‑validated filenames  
- document reference sequences  

---

## **8. ADR Roadmap**
Planned ADRs include:

- **ADR‑011** — Corpus Index Specification  
- **ADR‑012** — Corpus Linter Specification  
- **ADR‑013** — Versioning Semantics Extension (SV‑GOV)  
- **ADR‑014** — Corpus Registry Automation  

All ADRs must use suffix `adr` and follow TST.

---

## **9. Governance Notices**
Future notices may include:

- corpus deprecation policies  
- corpus archival policies  
- corpus release cadence  

These require ADR justification.

---

## **10. Versioning Plan**
### **10.1 Roadmap Versioning**
Roadmap versions follow SV‑GOV rules:

- **MAJOR** — structural or constitutional change  
- **MINOR** — capability expansion  
- **PATCH** — stability refinement  

This document is **v1.1** (MINOR).

---

## **11. Transition State Machine**
Allowed transitions:

- Draft → Stable  
- Stable → Deprecated  
- vX → vX+1  

Forbidden transitions:

- Deprecated → Stable without ADR  
- any transition contradicting roadmap  
- structural change → MINOR increment  

---

## **12. Dependencies**
This roadmap depends on:

- U‑CMS v1.0  
- SC‑TPGM v1.0  
- TST v1.0  
- ADR‑010 (suffix schema)  

All future changes must maintain compatibility.

---

## **13. Risks**
- inconsistent suffix usage  
- ungoverned document creation  
- roadmap drift  
- missing ADR justification  
- structural divergence across standards  

These risks are mitigated by the corpus linter.

---

## **14. Assumptions**
- corpus remains closed to external contributions  
- standards evolve deterministically  
- ADRs remain the sole justification mechanism  
- suffix schema remains stable  

---

## **15. Constraints**
- no structural changes without MAJOR increment  
- no suffix changes without ADR  
- no new standards without roadmap alignment  
- no contradictions across corpus artefacts  

---

## **16. Milestones**
- **M1:** SV‑GOV v1.1  
- **M2:** SC‑TPGM §8.4 update  
- **M3:** TST §5.11 update  
- **M4:** Corpus Index  
- **M5:** Corpus Linter  
- **M6:** Registry Automation  

---

## **17. Document Control**

**Document Owner:** Corpus Governance Authority  
**Change Authority:** Standards Board  
**Review Cycle:** Per MAJOR corpus change  

---

## **18. Version History**

| Version | Date | Type | Summary |
|---------|-------|--------|---------|
| v1.1 | 31 Jul 2026 | MINOR | Added suffix schema alignment, governance extensions, ADR roadmap |
| v1.0 | 31 Jul 2026 | MAJOR | Initial roadmap release |

---

## **19. Summary**
This roadmap defines the deterministic evolution of the governed corpus architecture.  
It ensures:

- structural consistency  
- constitutional alignment  
- suffix‑aware identity governance  
- ADR‑driven change  
- machine‑readable determinism  

It is binding under U‑CMS.

---

