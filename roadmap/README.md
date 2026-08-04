# Governance Framework — Complete Register Set

---

## Register Index

| **Register** | **Path** | **Purpose** |
| --- | --- | --- |
| [Asset Registry](#asset-registry) | `/governance/registers/assets/` | All corpus documents across all directories |
| [Policy Register](#policy-register) | `/governance/registers/policies/` | Policies governing the corpus and its operations |
| [Standard Register](#standard-register) | `/governance/registers/standards/` | Standards and specifications |
| [Procedure Register](#procedure-register) | `/governance/registers/procedures/` | Operational procedures and work instructions |
| [Template Register](#template-register) | `/governance/registers/templates/` | Governed document templates |
| [Decision Register](#decision-register) | `/governance/registers/decisions/` | Architectural and governance decisions (ADRs) |
| [Risk Register](#risk-register) | `/governance/registers/risks/` | Identified risks and mitigations |
| [Access Control Register](#access-control-register) | `/governance/registers/access/` | Role-to-classification authorisations |
| [Audit Log](#audit-log) | `/governance/registers/audit/` | Chain of custody and change events |
| [Retention Schedule](#retention-schedule) | `/governance/registers/retention/` | Retention and disposal rules by document type |

---

## Asset Registry

> Full schema defined in `asset_registry.md`. Master flat index below.

| **Document Ref** | **Class** | **Type** | **Version** | **Status** | **Effective Date** | **Next Review** | **Owner** | **Distribution** | **Supersedes** | **Path** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `2026-001-meta_spec` | `D` | `meta_spec` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | `/governance/documents/` | Unified Corpus Meta‑Standard (U‑CMS) |
| `2026-002-spec` | `D` | `spec` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | `/governance/documents/` | SC‑TPGM — Security Classification & Title‑Page Governance Standard |
| `2026-003-spec` | `D` | `spec` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | `/governance/documents/` | TST — Technical Standard Template |
| `2026-004-spec` | `D` | `spec` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | `/governance/documents/` | SV‑GOV — Versioning Governance Standard |
| `2026-005-adr` | `D` | `adr` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | `/governance/documents/` | ADR‑010 — Suffix Schema Formalization |
| `2026-006-notice` | `D` | `notice` | 1.0 | `ACTIVE` | 2026-01-01 | — | Corpus Authority | OPEN | — | `/governance/documents/` | Contributions Disabled — Corpus Governance Notice |
| `2025-001-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2025-01-01 | — | — | OPEN | — | `/papers/` | Cognitive Minimalism in Programming |
| `2026-001-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | `/papers/` | The Architecture of Plausibility |
| `2026-002-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | `/papers/` | A Multi-Model, Syntax-Preserving Pipeline |
| `2026-003-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | `/papers/` | The First Honest Machine |
| `2026-004-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | `/papers/` | The Latency–Accuracy Exchange Principle |
| `2026-005-paper` | `D` | `paper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | `/papers/` | Prototyping as an Epistemic Taxonomy |
| `2026-001-whitepaper` | `D` | `whitepaper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | `/whitepapers/dynamic_wallpaper/` | Dynamic Island Wallpaper |
| `2026-002-whitepaper` | `D` | `whitepaper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | `/whitepapers/risk/` | Risk as a First‑Class Entity in Systems Design |
| `2026-003-whitepaper` | `D` | `whitepaper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | `/whitepapers/UPTF/` | Universal Project Template Framework |
| `2026-004-whitepaper` | `D` | `whitepaper` | 1.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | — | `/whitepapers/UPTF/` | Deterministic Architecture Generation via Double‑Entry YAML Ledgers |
| `2026-005-whitepaper` | `D` | `whitepaper` | 1.1 | `SUPERSEDED` | 2026-01-01 | — | — | OPEN | — | `/whitepapers/UPTF/` | Structural Emptiness and Null‑Space Artefacts |
| `2026-006-whitepaper` | `D` | `whitepaper` | 2.0 | `ACTIVE` | 2026-01-01 | — | — | OPEN | `2026-005-whitepaper` | `/whitepapers/UPTF/` | Structural Emptiness and Null‑Space Artefacts |

---

## Policy Register

> Policies define **what must be done** and **why**. They carry mandatory language and require approval by the Classification Authority.

### Schema

| **Policy Ref** | **Class** | **Version** | **Status** | **Effective Date** | **Next Review** | **Owner** | **Distribution** | **Supersedes** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `2026-001-policy` | `D` | — | `DRAFT` | — | — | — | — | — | *(to be defined)* |

### Recommended initial policies

| **Suggested Ref** | **Title** |
| --- | --- |
| `2026-001-policy` | Document Lifecycle Policy |
| `2026-002-policy` | Classification & Handling Policy |
| `2026-003-policy` | Numbering Authority Policy |
| `2026-004-policy` | Retention & Disposal Policy |
| `2026-005-policy` | Access Control Policy |
| `2026-006-policy` | Audit & Integrity Policy |

---

## Standard Register

> Standards define **how something must be built or structured**. Already partially populated via `/governance/documents/` — cross-referenced here.

| **Standard Ref** | **Class** | **Version** | **Status** | **Effective Date** | **Next Review** | **Owner** | **Distribution** | **Supersedes** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `2026-002-spec` | `D` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | SC‑TPGM — Security Classification & Title‑Page Governance Standard |
| `2026-003-spec` | `D` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | TST — Technical Standard Template |
| `2026-004-spec` | `D` | 1.0 | `ACTIVE` | 2026-01-01 | 2027-01-01 | Corpus Authority | OPEN | — | SV‑GOV — Versioning Governance Standard |

---

## Procedure Register

> Procedures define **step-by-step operational instructions** for enacting policies and standards.

| **Procedure Ref** | **Class** | **Version** | **Status** | **Effective Date** | **Next Review** | **Owner** | **Distribution** | **Implements** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| *(none registered)* | — | — | — | — | — | — | — | — | — |

### Recommended initial procedures

| **Suggested Ref** | **Title** | **Implements** |
| --- | --- | --- |
| `2026-001-procedure` | Document Registration Procedure | `2026-003-policy` |
| `2026-002-procedure` | Classification Assignment Procedure | `2026-002-policy` |
| `2026-003-procedure` | Change Control Procedure | `2026-001-policy` |
| `2026-004-procedure` | Document Review & Approval Procedure | `2026-001-policy` |
| `2026-005-procedure` | Disposal & Archival Procedure | `2026-004-policy` |

> **Note:** The `Implements` column cross-references the Policy Ref that the procedure operationalises, creating a traceable policy-to-procedure hierarchy.

---

## Template Register

> Governed templates are assets and must be registered. Templates live in `/governance/templates/`.

| **Template Ref** | **Class** | **Version** | **Status** | **Effective Date** | **Next Review** | **Owner** | **Distribution** | **Applies To** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| *(none registered)* | — | — | — | — | — | — | — | — | — |

### Recommended initial templates

| **Suggested Ref** | **Title** | **Applies To** |
| --- | --- | --- |
| `2026-001-template` | Standard Document Header Template | All types |
| `2026-002-template` | Paper Template | `paper` |
| `2026-003-template` | Whitepaper Template | `whitepaper` |
| `2026-004-template` | Policy Template | `policy` |
| `2026-005-template` | Procedure Template | `procedure` |
| `2026-006-template` | ADR Template | `adr` |

---

## Decision Register

> Architectural and governance decisions. Cross-referenced from the asset registry where suffix is `adr`.

| **Decision Ref** | **Class** | **Version** | **Status** | **Effective Date** | **Decided By** | **Distribution** | **Supersedes** | **Canonical Title** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `2026-005-adr` | `D` | 1.0 | `ACTIVE` | 2026-01-01 | Corpus Authority | OPEN | — | ADR‑010 — Suffix Schema Formalization |

---

## Risk Register

> Identifies risks to corpus integrity, governance continuity, or document security.

| **Risk Ref** | **Class** | **Risk Title** | **Category** | **Likelihood** | **Impact** | **Rating** | **Mitigation** | **Owner** | **Status** | **Last Reviewed** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `2026-001-risk` | `D` | Reference number collision | Governance | Medium | High | High | Implement Numbering Authority Policy (`2026-003-policy`) | Corpus Authority | `OPEN` | — |
| `2026-002-risk` | `D` | No audit trail for document changes | Governance | High | High | Critical | Define and implement Audit Log format | Corpus Authority | `OPEN` | — |
| `2026-003-risk` | `D` | Uncontrolled status drift (DRAFT never moves to ACTIVE) | Lifecycle | Medium | Medium | Medium | Enforce Document Review & Approval Procedure | Corpus Authority | `OPEN` | — |
| `2026-004-risk` | `D` | Corpus grows beyond manual registry management | Scalability | High | Medium | High | Implement machine-readable manifest (YAML/JSON) | Corpus Authority | `OPEN` | — |

### Risk Rating Matrix

| | **Low Impact** | **Medium Impact** | **High Impact** |
| --- | --- | --- | --- |
| **High Likelihood** | Medium | High | Critical |
| **Medium Likelihood** | Low | Medium | High |
| **Low Likelihood** | Low | Low | Medium |

---

## Access Control Register

> Maps classification tiers to authorised roles or individuals. Required for tiers `B` and `A` to be enforceable.

| **Access Ref** | **Classification Tier** | **Role / Principal** | **Granted By** | **Effective Date** | **Expiry / Review** | **Notes** |
| --- | --- | --- | --- | --- | --- | --- |
| `2026-001-access` | `D` | Public | Corpus Authority | 2026-01-01 | — | Open distribution; no restriction |
| `2026-002-access` | `C` | *(to be defined)* | — | — | Annual | Internal contributors only |
| `2026-003-access` | `B` | *(to be defined)* | — | — | 6-month | Authorised personnel only |
| `2026-004-access` | `A` | *(to be defined)* | — | — | On demand | Air-gapped access only |

---

## Audit Log

> Immutable record of all create, update, status-change, classification-change, and disposal events across the corpus.

### Schema

| **Event Ref** | **Timestamp** | **Document Ref** | **Event Type** | **From State** | **To State** | **Actor** | **Notes** |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `2026-001-event` | 2026-01-01T00:00:00Z | `2026-001-meta_spec` | `CREATE` | — | `ACTIVE` | Corpus Authority | Initial registration |

### Event Types

| **Type** | **Meaning** |
| --- | --- |
| `CREATE` | Document registered for the first time |
| `REVISE` | Version incremented; content changed |
| `STATUS_CHANGE` | Status field updated (e.g. DRAFT → ACTIVE) |
| `CLASSIFY` | Classification tier assigned or changed |
| `SUPERSEDE` | Document marked SUPERSEDED; successor registered |
| `ARCHIVE` | Document moved to ARCHIVED state |
| `WITHDRAW` | Document withdrawn |
| `DISPOSE` | Document permanently removed per retention schedule |
| `ACCESS_GRANT` | Access authorisation added |
| `ACCESS_REVOKE` | Access authorisation removed |

---

## Retention Schedule

> Defines how long each document type is retained in each status before disposal is permissible.

| **Document Type** | **ACTIVE Retention** | **SUPERSEDED Retention** | **ARCHIVED Retention** | **Disposal Method** | **Authority** |
| --- | --- | --- | --- | --- | --- |
| `meta_spec` | Indefinite | Indefinite | Indefinite | Never dispose | Corpus Authority |
| `spec` | Indefinite | 7 years | 7 years | Secure deletion | Corpus Authority |
| `policy` | Indefinite | 7 years | 7 years | Secure deletion | Corpus Authority |
| `procedure` | Indefinite | 3 years | 3 years | Secure deletion | Corpus Authority |
| `adr` | Indefinite | Indefinite | Indefinite | Never dispose | Corpus Authority |
| `paper` | Indefinite | Indefinite | Indefinite | Never dispose | Corpus Authority |
| `whitepaper` | Indefinite | 5 years | 5 years | Secure deletion | Corpus Authority |
| `template` | Indefinite | 3 years | 3 years | Secure deletion | Corpus Authority |
| `notice` | Until superseded | 1 year | 1 year | Secure deletion | Corpus Authority |
| `risk` | Until closed | 3 years after close | 3 years | Secure deletion | Corpus Authority |

> **Note:** "Secure deletion" means overwrite or cryptographic erasure appropriate to the classification tier of the document at time of disposal.

---

## Status Vocabulary (Corpus-Wide)

| **Status** | **Meaning** |
| --- | --- |
| `DRAFT` | In preparation; not yet approved or effective |
| `ACTIVE` | Approved, effective, and current |
| `SUPERSEDED` | Replaced by a later document; retained for auditability |
| `ARCHIVED` | No longer applicable; retained for historical record only |
| `WITHDRAWN` | Removed from use; content must not be relied upon |
| `OPEN` | Risk or action item not yet resolved *(Risk Register only)* |
| `CLOSED` | Risk or action item resolved *(Risk Register only)* |
| `ACCEPTED` | Risk accepted without mitigation *(Risk Register only)* |
