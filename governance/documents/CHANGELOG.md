# Classification: D  
Document Reference: `2026-CHG`
# **Corpus Changelog — Governed Corpus Architecture**  
  

### Status: Stable  
### Maintainer: Corpus Governance Authority  
### Review Cycle: Per MAJOR corpus change  

---

## **Purpose**
This changelog records **all corpus‑level changes**, including:

- updates to the Corpus Constitution (CC)  
- releases of governed standards (SC‑TPGM, SV‑GOV, TST)  
- structural amendments  
- roadmap‑aligned transitions  
- ADR‑justified modifications  

It forms part of the constitutional audit trail.

---

# **Changelog Entries**

---

## **2026‑07‑31 — Corpus Constitution v1.0 Released**
**Type:** MAJOR  
**ADR:** ADR‑001  
**Summary:**  
- Established the **Unified Corpus Meta‑Standard (U‑CMS)** as the constitutional authority.  
- Defined corpus boundaries, integrity rules, transition state machine, and roadmap governance.  
- Introduced corpus‑level tagging, justification, and audit requirements.  
- Formalized the hierarchical structure for subordinate standards.

---

## **2026‑07‑31 — Standard 1: SC‑TPGM v1.0 Released**
**Type:** MAJOR  
**ADR:** ADR‑002  
**Summary:**  
- Introduced the **Security Classification & Title‑Page Governance Model**.  
- Added classification taxonomy (A–D).  
- Added title‑page schema, typography rules, and security signalling requirements.  
- Added classification‑validity rules and semantic line‑break guidance.  
- Integrated corpus‑level governance and roadmap alignment.

---

## **2026‑07‑31 — Standard 2: SV‑GOV v1.1 Released**
**Type:** MINOR  
**ADR:** ADR‑003  
**Summary:**  
- Updated versioning rules under corpus governance.  
- Consolidated schema additions under MINOR increments.  
- Added version transition state machine.  
- Added ADR placement requirements.  
- Added corpus‑aligned integrity rules.  
- Clarified Target Maturity Framework.

---

## **2026‑07‑31 — Standard 3: TST v1.0 Released**
**Type:** MAJOR  
**ADR:** ADR‑004  
**Summary:**  
- Formalized the **Technical Standard Template** as a governed artefact.  
- Added mandatory section taxonomy for all future standards.  
- Added normative layout schema and metadata requirements.  
- Added integrity rules and transition state machine.  
- Ensured full alignment with SC‑TPGM and U‑CMS.

---

## **2026‑07‑31 — Repository Structure Formalized**
**Type:** PATCH  
**ADR:** ADR‑005  
**Summary:**  
- Added recommended directory layout for corpus organization.  
- Introduced root‑level README.  
- Added placeholders for roadmap and corpus‑level changelog.  
- No behavioural or structural changes to standards.

---

## **2026‑07‑31 — Licensing Decision: Apache 2.0**
**Type:** MINOR  
**ADR:** ADR‑006  
**Summary:**  
- Adopted Apache License 2.0 for the entire corpus.  
- Added licence declaration to README.  
- Added root‑level `LICENSE` file.  
- Ensured compatibility with corpus‑level governance and Class D classification.

---

# **Version Summary Table**

| Component | Version | Date | Change Type | ADR | Notes |
|----------|---------|------|-------------|-----|-------|
| Corpus Constitution (CC) | 1.0 | 2026‑07‑31 | MAJOR | ADR‑001 | Initial constitutional release |
| SC‑TPGM | 1.0 | 2026‑07‑31 | MAJOR | ADR‑002 | Title‑page & classification standard |
| SV‑GOV | 1.1 | 2026‑07‑31 | MINOR | ADR‑003 | Versioning governance standard |
| TST | 1.0 | 2026‑07‑31 | MAJOR | ADR‑004 | Technical standard template |
| Repository Structure | 0.1 | 2026‑07‑31 | PATCH | ADR‑005 | Structural scaffolding |
| Licensing | 1.0 | 2026‑07‑31 | MINOR | ADR‑006 | Apache 2.0 adoption |

---

