# **CLASSIFICATION: D**
Document Reference: `2026-001-manual-D`
Version: `1.0`
Status: `ACTIVE`
Effective Date: `2026-08-01`
Next Review: `2027-08-01`
Owner / Custodian: Corpus Authority
Classification Authority: Corpus Authority
Distribution: `OPEN`
Supersedes: `—`

# **Records Management Manual (RMM‑01)**

---

# **Records Management Manual (RMM‑01)**  
**Aligned with ISO 15489‑1:2016**  
**Sovereign Research Lab — Governance Corpus**

---

## **1. Purpose**
The Records Management Manual establishes the **principles, structures, controls, and operational procedures** governing the creation, capture, classification, storage, access, retention, and disposal of records within the Sovereign Research Lab.  
It operationalises the Governance Policy and ensures compliance with **ISO 15489‑1:2016**, embedding records integrity into the lab’s governed cognition and prototyping ecosystems.

---

## **2. Scope**
This manual applies to:
- All documents listed in the **Asset Registry**  
- All research artefacts, prototypes, models, and governance materials  
- All personnel, contributors, and autonomous agents  
- All classification levels (`D`, `C`, `B`, `A`)  
- All systems participating in record creation, including digital twins, operator‑algebraic engines, and deterministic project frameworks

---

## **3. Records Management Principles (ISO 15489‑1:2016)**

### **3.1 Authenticity**
Records must be created and captured in a manner that ensures their origin, context, and authorship are verifiable.

**Operationalisation:**  
- SC‑TPGM header block mandatory for all documents  
- Immutable commit logs for code and architectural artefacts  
- Provenance metadata embedded at creation

### **3.2 Reliability**
Records must accurately represent the activities, decisions, or facts they document.

**Operationalisation:**  
- ADR‑based decision capture (e.g., ADR‑010)  
- Mandatory architectural decision records for all major design shifts  
- Structured templates for specifications, standards, and notices

### **3.3 Integrity**
Records must be complete, unaltered, and protected against unauthorized modification.

**Operationalisation:**  
- Versioning Governance Standard (SV‑GOV)  
- Write‑once storage for governance artefacts  
- Integrity checksums and periodic verification cycles

### **3.4 Usability**
Records must remain accessible, interpretable, and usable over time.

**Operationalisation:**  
- Unified Corpus Meta‑Standard (U‑CMS)  
- Metadata schemas harmonised across all document types  
- Long‑term readability formats (Markdown, YAML, PDF/A for external releases)

---

## **4. Governance Roles**

### **4.1 Corpus Authority**
Responsible for:
- Approving documents  
- Maintaining the Asset Registry  
- Ensuring ISO 15489 compliance  
- Issuing standards, specifications, and notices

### **4.2 Governance Custodian**
Responsible for:
- Lifecycle management  
- Classification enforcement  
- Metadata quality  
- Audit preparation

### **4.3 Project Stewards**
Responsible for:
- Domain‑specific compliance  
- Ensuring correct use of templates  
- Maintaining project‑level records integrity

### **4.4 Information Security Lead**
Responsible for:
- Access control  
- Secure storage  
- Air‑gapped environment governance (`A` class)

---

## **5. Records Creation & Capture**

### **5.1 Mandatory Capture Events**
Records must be created at:
- Project initiation, revision, and closure  
- Architectural decision points  
- Model training, evaluation, and deployment  
- Governance rule changes  
- Risk assessments and controlled descent analyses  
- Publication events (papers, whitepapers, standards)

### **5.2 Required Metadata**
All records must include:
- SC‑TPGM header block  
- Document Reference (canonical)  
- Version number  
- Status  
- Effective date  
- Next review date  
- Owner / Custodian  
- Classification Authority  
- Distribution label  
- Supersedes reference (if applicable)

### **5.3 Document Types**
- `meta_spec` — corpus‑wide meta‑standards  
- `spec` — technical standards  
- `adr` — architectural decision records  
- `notice` — governance notices  
- `paper` — research papers  
- `whitepaper` — conceptual or technical whitepapers  
- `manual` — governance manuals (this document)

---

## **6. Classification & Access Control**

### **6.1 Classification Levels**
As defined in your Security Classification Scheme:

| Level | Code | Distribution | Description |
|------|------|--------------|-------------|
| Public / Unrestricted | `D` | `OPEN` | External publications, open standards |
| Internal / Restricted | `C` | `INTERNAL` | Internal specifications, roadmaps |
| Confidential / Commercial | `B` | `RESTRICTED` | Proprietary algorithms, stealth architectures |
| Air‑Gapped / Isolated | `A` | `NO-NET` | Sovereign governance rules, cryptographic kernels |

### **6.2 Access Rules**
- Access is role‑based and classification‑dependent  
- `A` class records require physical isolation  
- All access events must be logged  
- Retrieval must occur through the Unified Asset Registry

---

## **7. Storage & Protection**

### **7.1 Storage Architecture**
- Version‑controlled repositories for code and specs  
- Immutable archives for governance artefacts  
- Encrypted storage for `B` and `A` class records  
- Air‑gapped vaults for sovereign materials

### **7.2 Security Controls**
- MFA for all restricted systems  
- Zero‑trust pathways  
- Continuous monitoring  
- Automated anomaly detection

---

## **8. Records Retrieval**

### **8.1 Retrieval Mechanisms**
- Unified Asset Registry search  
- Metadata‑driven discovery  
- Operator‑graph traversal for linked artefacts  
- Controlled gateways for restricted records

### **8.2 Retrieval Logging**
All retrieval events must be logged with:
- User identity  
- Timestamp  
- Record reference  
- Classification level  
- Retrieval method

---

## **9. Records Lifecycle Management**

### **9.1 Status Vocabulary**
As defined in your corpus:

- `DRAFT`  
- `ACTIVE`  
- `SUPERSEDED`  
- `ARCHIVED`  
- `WITHDRAWN`

### **9.2 Versioning**
Governed by SV‑GOV:
- Semantic versioning for standards  
- Incremental versioning for papers and whitepapers  
- Supersedes chain must be maintained (e.g., `2026-006-whitepaper` supersedes `2026-005-whitepaper`)

### **9.3 Retention**
Retention periods depend on:
- Classification level  
- Regulatory requirements  
- Research value  
- Governance significance

### **9.4 Disposal**
Disposal must be:
- Authorized by Governance Custodian  
- Logged  
- Verified  
- Securely executed (digital shredding, cryptographic erasure, physical destruction for `A` class)

---

## **10. Audit & Compliance**

### **10.1 Annual Audit**
Audits must assess:
- ISO 15489 compliance  
- Metadata quality  
- Integrity of governance artefacts  
- Security posture  
- Lifecycle management effectiveness

### **10.2 Continuous Compliance**
- Automated checks integrated into governed cognition stack  
- Alerts for deviations  
- Mandatory remediation workflows

---

## **11. Templates & Standards**

### **11.1 SC‑TPGM Header Block**
Mandatory for all documents.

### **11.2 TST — Technical Standard Template**
Required for all specifications.

### **11.3 ADR Template**
Required for all architectural decisions.

### **11.4 Metadata Schema**
Defined in U‑CMS; must be applied consistently.

---

## **12. Manual Review & Updates**
This manual must be reviewed:
- Annually  
- After major architectural changes  
- After significant incidents or controlled descent events

Updates must be:
- Versioned  
- Logged  
- Approved by Corpus Authority

---

## **13. Definitions**
Include ISO‑aligned definitions for:
- Record  
- Metadata  
- Provenance  
- Integrity  
- Lifecycle  
- Governance artefact  
- Sovereign record  
- Controlled descent  
- Corpus Authority  
- Custodian  
- Steward

---

## **14. Adoption**
This manual becomes effective immediately upon approval by the Corpus Authority and is binding across all lab operations.

---

If you want, I can also generate:

- **RMM‑01 Annexes**  
  - Metadata schema  
  - Classification matrix  
  - Lifecycle flow diagrams  
  - ADR catalogue  
- **A fully cross‑linked governance corpus map**  
- **A deterministic YAML ledger for document issuance** (aligned with your UPTF work)

Which annex or extension should I produce next?
