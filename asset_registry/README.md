`2026-0002-D-read-002.md`  

---

**CLASSIFICATION**: D  

**Document Reference**: `2026-0002-D-read-002`  
# Unified Asset Registry
### Governance  

**Version**: 0.1       

William Murray  
Research Architect  
14 August 2026  

**Status**: Draft     

**Scope**: The `/asset_registry/` directory contains the authoritative ledgers and classification governance standards for the entire organization. It serves as the single source of truth for tracking active engineering projects, technical specifications, academic research, governance notices, and security clearance schemas.  

**Primary Model / Scheme**: tmp & spec. 

---

## **1. Overview**



---

## **2. Directory Contents**

| **Filename** | **Document Ref** | **Description & Scope** |
| :--- | :--- | :--- |
| `README.md` | `2026-008-readme-D` | Directory index, usage rules, and schema validation guidelines (*this file*). |
| `2026-001-registry-D.md` | `2026-001-registry-D` | **Master Document Asset Registry:** Catalog of all specifications, ADRs, notices, manuals, papers, and whitepapers. |
| `2026-002-registry-D.md` | `2026-002-registry-D` | **Master Project Registry:** Operational ledger tracking software builds, core engines, hardware racks, and project stage lifecycles. |

---

## **3. Key Principles & Usage**

1. **Strict Immutability & Auditability:** Every entry in `2026-001-registry-D` and `2026-002-registry-D` must maintain full traceability back to an actual file, specification, or code repository root.
2. **Naming & Suffixed Identifiers:** All documents recorded in the registries follow the SC-TPGM identifier standard (`YYYY-NNN-type-CLASS.md`).
3. **Classification Integrity:** Entries inherit security rules (`A`, `B`, `C`, or `D`) based on their designated classification. Items marked `A` (Air-Gapped) or `B` (Confidential) must not expose sensitive operational metadata in public-facing registry exports.

---

## **4. Updating the Registries**

* **Adding a New Document:** Append a new entry to the corresponding folder section in `2026-001-registry-D.md`.
* **Initiating a New Project:** Assign the next available `PRJ-YYYY-NNN` identifier in `2026-002-registry-D.md` and link its primary governing specification (`2026-XXX-spec-[D|C|B|A]`).
* **Version Bumps:** Update `2026-001-registry-D.md` or `2026-002-registry-D.md` headers whenever structural schema or project milestones are modified.
