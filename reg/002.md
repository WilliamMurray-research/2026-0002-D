`2026-0002-D-reg-002.md`  

---

**CLASSIFICATION**: D  

**Document Reference**: `2026-0002-D-reg-002`  
# Project Registry  
### Governance  

**Version**: 0.1        

William Murray  
Research Architect  
15 August 2026  

**Status**: Draft     

**Scope**: This registry serves as the authoritative ledger for all software systems, research implementations, and hardware infrastructure projects within the organization. While `2026-001-registry-D` tracks static document assets, specifications, and published papers, `2026-002-registry-D` governs the active operational lifecycle, technical stack parameters, deployment target milestones, and governing specification mappings for engineering initiatives.   

**Primary Model / Scheme**: tmp & spec

  

---

## **1. Overview & Operational Scope**



---

## **2. Active Projects Ledger**

| **Project Code** | **Class** | **Phase / Stage** | **Completion** | **Target Deployment** | **Lead / Custodian** | **Primary Tech Stack** | **Governing Spec Ref** | **Repository / Path** | **Canonical Name & Objective** |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `PRJ-2026-001` | `D` | `DEV` | `~30%` | `2026-Q4` | William Murray | Python / PyTorch / HuggingFace | `2026-001-project-D` | `/projects/aus_rewrite_t5/` | **AusRewrite-T5** — Australian English Legal & Statutory Rewriting Engine |
| `PRJ-2026-002` | `B` | `DISCOVERY` | `~15%` | `2027-Q1` | William Murray | Prolog / LISP / Rust / Zig / Erlang / Julia | `2026-007-spec-D` | `/projects/manifold_core/` | **Manifold Research Core** — Multi-Language Interoperable Deterministic Reasoning Engine |
| `PRJ-2026-003` | `B` | `PROCURING` | `~10%` | `2027-Q1` | William Murray | Hardware / Custom Thermal Isolation | `2026-008-spec-B` | `/infrastructure/rack_blackwell_01/` | **High-Density Inference Rack** — 20kW Air-Gapped Blackwell Server & Liquid Heat Exchange System |

---

## **3. Project Lifecycle & Phase Definitions**

| **Phase Code** | **Definition & Operational Exit Criteria** |
| :--- | :--- |
| `CONCEPT` | Pre-engineering state; feasibility evaluation, domain mapping, and initial whitepaper generation. |
| `DISCOVERY` | Architectural prototyping, formal verification logic modeling, and dependency/interoperability testing. |
| `DEV` | Active code construction, pipeline assembly, and unit testing under standard versioning rules. |
| `PROCURING` | Physical hardware sourcing, custom enclosure fabrication, or infrastructure site preparation. |
| `STAGING` | Integration testing, local air-gapped evaluation, and pre-deployment validation loops. |
| `PROD` | Commercial release, live operational deployment, or continuous background inference execution. |
| `MAINTENANCE` | System complete and stable; receiving critical updates and periodic governance audits only. |
| `DEPRECATED` | Scheduled for sunset or replacement by a successor project code. |

---

## **4. Project Classification & Security Rules**

Projects inherit the security restrictions of their assigned Classification Code. All project repositories, hardware setups, and data stores must adhere to the corresponding distribution boundaries:


```

+-------------------------------------------------------------------------------+
|  CLASS A: AIR-GAPPED / ISOLATED                                               |
|  - Strictly offline / local air-gapped compute environments.                   |
|  - Zero network transport layer; local model execution only.                  |
+-------------------------------------------------------------------------------+
|
v
+-------------------------------------------------------------------------------+
|  CLASS B: CONFIDENTIAL / COMMERCIAL                                           |
|  - Stealth initiatives, core IP, proprietary algorithms, containment designs. |
|  - Restricted access; pre-commercial intellectual property.                  |
+-------------------------------------------------------------------------------+
|
v
+-------------------------------------------------------------------------------+
|  CLASS C: INTERNAL / RESTRICTED                                               |
|  - Operational tooling, internal CI pipelines, and non-public frameworks.     |
|  - Shared across internal contributors; no public exposure.                   |
+-------------------------------------------------------------------------------+
|
v
+-------------------------------------------------------------------------------+
|  CLASS D: PUBLIC / UNRESTRICTED                                               |
|  - Open-source tools, public specifications, published research models.       |
|  - Unrestricted distribution and public auditability.                          |
+-------------------------------------------------------------------------------+

```

---

## **5. Maintenance & Audit Protocols**

1. **Update Cadence:** The Project Registry must be updated upon any milestone change, stage transition, or significant adjustment to completion percentage.
2. **Review Cycle:** Annual audit by the Classification Authority or upon the initiation of any new `PRJ-YYYY-NNN` identifier.
3. **Traceability:** Every commercial or production project must link directly to a valid governing specification in `/governance/` or a dedicated specification document within its project directory.

```
