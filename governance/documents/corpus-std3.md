# **CLASSIFICATION: D**  
Document Reference: `2026-003-spec`  
# **TST – Technical Standard Template**  
### Technical Standard v1.0  
### Corpus Governance & Architecture Specification  
---  
#### William Murray  
#### 31 July 2026  
---  
**Status:** Stable  
**Scope:** Defines the canonical structure, mandatory sections, metadata schema, and normative layout for all technical standards within the governed corpus.  
**Primary Model / Scheme:** TST (Technical Standard Template)

---

# **Scope**
This Standard defines the **mandatory structure, section taxonomy, metadata schema, and normative layout** for all technical standards within the governed corpus.

Applicability:

- All new standards  
- All revised standards  
- All corpus‑level specifications  
- All governance and architecture documents  

Exclusions:

- Non‑standard operational documentation  
- Artefacts outside the governed corpus  

This Standard inherits all corpus‑level rules defined in the **Unified Corpus Meta‑Standard (U‑CMS)**.

---

# **Primary Model / Scheme: TST**
The **Technical Standard Template (TST)** defines the structural and semantic rules for constructing governed standards.

It comprises:

1. **Title‑Page Layer**  
2. **Metadata Layer**  
3. **Normative Section Layer**  
4. **Informative Section Layer**  
5. **Document Control Layer**

TST ensures that all standards are:

- structurally consistent  
- machine‑readable  
- corpus‑aligned  
- governance‑compliant  

---

# **1. Introduction**
The governed corpus requires **uniform, predictable, and structurally coherent standards**.  
TST provides the canonical structure that all standards must follow, ensuring:

- deterministic layout  
- consistent governance signalling  
- predictable section boundaries  
- corpus‑level compatibility  
- auditability and reproducibility  

TST is the **root structural template** for all standards.

---

# **2. Normative References**
This specification is self‑contained. Optional alignment:

- ISO‑style technical standard structures  
- Corporate governance documentation frameworks  
- APA/IEEE formatting conventions (informative only)

---

# **3. Terms and Definitions**

**Technical Standard**  
A governed document defining normative rules, models, or specifications.

**Normative Section**  
A section containing mandatory rules or requirements.

**Informative Section**  
A section providing guidance, examples, or non‑mandatory context.

**Corpus Constitution (CC)**  
The root governance authority defined in U‑CMS.

---

# **4. TST Core Framework**

## **4.1 Mandatory Section Structure**
All standards **shall** contain the following sections in order:

1. **Title Page**  
2. **Scope**  
3. **Primary Model / Scheme**  
4. **Introduction**  
5. **Normative References**  
6. **Terms and Definitions**  
7. **Core Model / Framework**  
8. **Normative Classes / Categories**  
9. **Governance Requirements**  
10. **Target Maturity Framework (Informative)**  
11. **Tagging Requirements**  
12. **Pre‑Release Identifiers**  
13. **Integrity Rules**  
14. **Corpus Change Protocol**  
15. **Transition State Machine**  
16. **Compliance & Audit**  
17. **Document Control**  
18. **Summary of Changes**  
19. **Changelog**

No section may be omitted unless explicitly justified via ADR.

---

## **4.2 Title‑Page Requirements**
Title pages **shall** conform to the SC‑TPGM Standard.

Mandatory elements:

- Classification marker  
- Document reference  
- Primary title  
- Standard name  
- Version identifier  
- Author  
- Date  
- Status  
- Scope line  
- Primary model / scheme  

Class A documents must include top and bottom banners.

---

## **4.3 Metadata Requirements**
Metadata blocks **shall** include:

- Status  
- Scope  
- Primary model / scheme  
- Document reference  
- Author  
- Date  

Metadata must be machine‑readable and corpus‑consistent.

---

## **4.4 Normative Section Requirements**
Normative sections **shall**:

- contain mandatory rules  
- use “shall”, “must”, or “required” language  
- avoid ambiguity  
- align with corpus‑level governance rules  

Normative sections define the constitutional behaviour of the standard.

---

## **4.5 Informative Section Requirements**
Informative sections **may**:

- provide examples  
- describe maturity frameworks  
- offer guidance  
- clarify intent  

Informative sections **shall not** introduce mandatory rules.

---

# **5. Section‑by‑Section Template (Normative)**

Below is the canonical template that all standards must follow.

---

## **5.1 Title Page**
```
CLASSIFICATION: [A/B/C/D]

Document Reference: `YYYY-XXX-spec`
# [Primary Title] – [Standard Name]
### Technical Standard vX.Y
### Governance & Architecture Specification
---
#### [Author Name]
#### [Document Date]
---
Status: Draft / Stable / Deprecated
Scope: [Short scope line]
Primary Model / Scheme: [Model]
```

---

## **5.2 Scope**
Defines applicability, boundaries, and exclusions.

---

## **5.3 Primary Model / Scheme**
Defines the governing model (e.g., versioning, classification, architecture).

---

## **5.4 Introduction**
Explains purpose, context, and rationale.

---

## **5.5 Normative References**
Lists optional external references.

---

## **5.6 Terms and Definitions**
Defines all key terms used in the standard.

---

## **5.7 Core Model / Framework**
Describes the main conceptual or architectural model.

---

## **5.8 Normative Classes / Categories**
Defines classes, categories, or types with triggers and semantic summaries.

---

## **5.9 Governance Requirements**
Defines documentation, justification, placement, compatibility, and corpus‑integrity rules.

---

## **5.10 Target Maturity Framework (Informative)**
Describes typical lifecycle stages.

---

## **5.11 Tagging Requirements**
Defines tagging rules for identifiers and metadata.

---

## **5.12 Pre‑Release Identifiers**
Defines alpha, beta, rc conventions.

---

## **5.13 Integrity Rules**
Defines invalidation conditions.

---

## **5.14 Corpus Change Protocol**
Defines justification and versioning rules for corpus changes.

---

## **5.15 Transition State Machine**
Defines allowed/forbidden transitions and preconditions.

---

## **5.16 Compliance & Audit**
Defines traceability, auditability, and compliance alignment.

---

## **5.17 Document Control**
Defines owner, authority, and review cycle.

---

## **5.18 Summary of Changes**
Summarizes changes for the current version.

---

## **5.19 Changelog**
Tabular record of all changes.

---

# **6. Governance Requirements (Normative)**

1. **Structural Consistency Requirement**  
   All standards shall conform to TST without deviation.

2. **Justification Requirement**  
   Deviations require ADR justification.

3. **Placement Requirement**  
   Sections shall appear in the order defined in Section 5.

4. **Compatibility Requirement**  
   Standards shall remain compatible with U‑CMS and SC‑TPGM.

5. **Corpus Integrity Requirement**  
   Standards shall not contradict each other or the corpus roadmap.

---

# **7. Integrity Rules (Normative)**

A standard is **invalid** if it:

- omits mandatory sections  
- misorders sections  
- contradicts corpus‑level rules  
- contradicts the corpus roadmap  
- omits classification markers  
- omits document control metadata  

---

# **8. Transition State Machine (Normative)**

### Allowed Transitions
- Draft → Stable  
- Stable → Deprecated  

### Forbidden Transitions
- Deprecated → Stable without ADR  
- Any transition contradicting corpus roadmap  

### Preconditions
- Draft: initial development  
- Stable: corpus‑aligned and validated  
- Deprecated: superseded or retired  

---

# **9. Compliance & Audit**

TST supports:

- structural auditability  
- governance traceability  
- corpus‑level consistency  
- deterministic evolution  

All standards must be reviewable and reproducible.

---

# **10. Document Control**

**Document Owner:** Corpus Governance Authority  
**Change Authority:** Standards Board  
**Review Cycle:** Per MAJOR corpus change  

---

# **v1.0 Summary of Changes**
- Formalized TST under U‑CMS  
- Added mandatory section taxonomy  
- Added normative layout schema  
- Added integrity rules  
- Added transition state machine  

---

# **Changelog**
| Version ID | Date | Key Changes |
|-----------|------|-------------|
| 1.0 | 2026‑07‑31 | Initial governed release |

---

