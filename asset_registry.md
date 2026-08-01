# Asset Registry

---

## /governance/documents/

| **Document Ref** | **Class** | **Type** | **Version** | **Status** | **Effective Date** | **Next Review** | **Owner** | **Distribution** | **Supersedes** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `2026-001-meta_spec` | `D` | `meta_spec` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | Unified Corpus Meta‑Standard (U‑CMS) |
| `2026-002-spec` | `D` | `spec` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | SC‑TPGM — Security Classification & Title‑Page Governance Standard |
| `2026-003-spec` | `D` | `spec` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | TST — Technical Standard Template |
| `2026-004-spec` | `D` | `spec` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | SV‑GOV — Versioning Governance Standard |
| `2026-005-adr` | `D` | `adr` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | ADR‑010 — Suffix Schema Formalization |
| `2026-006-notice` | `D` | `notice` | 1.0 | `ACTIVE` | 2026-01-01 | — | Corpus Authority | OPEN | — | Contributions Disabled — Corpus Governance Notice |

---

## /papers/

| **Document Ref** | **Class** | **Type** | **Version** | **Status** | **Effective Date** | **Next Review** | **Owner** | **Distribution** | **Supersedes** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `2025-001-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2025-01-01 | — | — | OPEN | — | Cognitive Minimalism in Programming: Applying Occam's Razor and Cognitive Load Theory to Software Development Best Practices |
| `2026-001-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | The Architecture of Plausibility: Reconceptualising Large Language Models Beyond the Knowledge Base Paradigm |
| `2026-002-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | A Multi-Model, Syntax-Preserving, Drift-Resistant Conjecture-to-Proof Pipeline |
| `2026-003-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | The First Honest Machine |
| `2026-004-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | The Latency–Accuracy Exchange Principle |
| `2026-005-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | Prototyping as an Epistemic Taxonomy in Software Systems |

---

## /whitepapers/dynamic_wallpaper/

| **Document Ref** | **Class** | **Type** | **Version** | **Status** | **Effective Date** | **Next Review** | **Owner** | **Distribution** | **Supersedes** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `2026-001-whitepaper` | `D` | `whitepaper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | Dynamic Island Wallpaper |

---

## /whitepapers/risk/

| **Document Ref** | **Class** | **Type** | **Version** | **Status** | **Effective Date** | **Next Review** | **Owner** | **Distribution** | **Supersedes** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `2026-002-whitepaper` | `D` | `whitepaper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | Risk as a First‑Class Entity in Systems Design |

---

## /whitepapers/UPTF/

| **Document Ref** | **Class** | **Type** | **Version** | **Status** | **Effective Date** | **Next Review** | **Owner** | **Distribution** | **Supersedes** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `2026-003-whitepaper` | `D` | `whitepaper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | Universal Project Template Framework |
| `2026-004-whitepaper` | `D` | `whitepaper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | Deterministic Architecture Generation via Double‑Entry YAML Ledgers and Prolog Execution Loops |
| `2026-005-whitepaper` | `D` | `whitepaper` | 1.1 | `SUPERSEDED` | 2026-01-01 | — | — | OPEN | — | Structural Emptiness and Null‑Space Artefacts in Deterministic Project Pathways |
| `2026-006-whitepaper` | `D` | `whitepaper` | 2.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | `2026-005-whitepaper` | Structural Emptiness and Null‑Space Artefacts in Deterministic Project Pathways |

> **Note — 2026-005b resolution:** The original `2026-005b-whitepaper` reference is retired. The original document is retained as `2026-005-whitepaper` (SUPERSEDED, v1.1); the revised document is issued as `2026-006-whitepaper` (ACTIVE, v2.0) with a Supersedes back-reference. Sequential numbering is restored.

---

## Security Classification Scheme

| **Code** | **Level** | **Access Scope** | **Distribution Label** | **Review Cycle** | **Classification Authority** | **Description & Use Case** |
| --- | --- | --- | --- | --- | --- | --- |
| `D` | Public / Unrestricted | Open distribution | `OPEN` | None required | Corpus Authority | Default for public research papers, open-source specifications, and whitepapers intended for external publication or auditability. |
| `C` | Internal / Restricted | Internal teams or project contributors | `INTERNAL` | Annual | Project Lead | System specifications, internal technical roadmaps, or implementation notes containing non-public operational details but no sensitive IP. |
| `B` | Confidential / Commercial | Authorised personnel only | `RESTRICTED` | 6-month | Senior Authority | Core proprietary algorithms, stealth-project architectural specs, hardware containment design parameters, or pre-patent intellectual property. |
| `A` | Air-Gapped / Isolated | Offline / air-gapped environment only | `NO-NET` | On demand | Senior Authority | High-assurance security kernels, sovereign governance rules, or sensitive cryptographic systems forbidden from networked environments. |

---

## SC‑TPGM Header Block — Standard Template

```markdown
# **CLASSIFICATION: [D | C | B | A]**
Document Reference: `YYYY-NNN-type`
Version: `1.0`
Status: `DRAFT | ACTIVE | SUPERSEDED | ARCHIVED | WITHDRAWN`
Effective Date: `YYYY-MM-DD`
Next Review: `YYYY-MM-DD | —`
Owner / Custodian: `[name or role]`
Classification Authority: `[name or role]`
Distribution: `OPEN | INTERNAL | RESTRICTED | NO-NET`
Supersedes: `[Document Reference] | —`

# **Document Title**
```

---

## Status Vocabulary

| **Status** | **Meaning** |
| --- | --- |
| `DRAFT` | In preparation; not yet approved or effective. |
| `ACTIVE` | Approved, effective, and current. |
| `SUPERSEDED` | Replaced by a later document; retained for auditability. |
| `ARCHIVED` | No longer applicable; retained for historical record only. |
| `WITHDRAWN` | Removed from use; content should not be relied upon. |
