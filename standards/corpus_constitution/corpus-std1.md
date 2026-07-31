# **CLASSIFICATION: D**  
Document Reference: `2026-001-spec`  
# **SC‑TPGM – Security Classification & Title‑Page Governance Standard**  
### Technical Standard v1.0  
### Corpus Governance & Architecture Specification  
---  
#### William Murray  
#### 31 July 2026  
---  
**Status:** Stable  
**Scope:** Governs classification, title‑page structure, metadata, and security signalling for all documents in the governed corpus.  
**Primary Model / Scheme:** SC‑TPGM (Security Classification & Title‑Page Governance Model)

---

# **Scope**
This Standard governs the **title‑page structure, metadata schema, classification signalling, and security‑reinforcement rules** for **all documents within the governed corpus**, regardless of sensitivity level.

Applicability:

- All governed documents (Classes A–D)  
- All title pages  
- All metadata blocks  
- All classification markers  

Exclusions:

- Documents outside the governed corpus  
- Non‑title‑page formatting rules (covered by other standards)

This Standard inherits all corpus‑level rules defined in the **Unified Corpus Meta‑Standard (U‑CMS)**.

---

# **Primary Model / Scheme: SC‑TPGM**
The **Security Classification & Title‑Page Governance Model (SC‑TPGM)** defines the structural, semantic, and visual rules for constructing secure, consistent, and machine‑readable title pages.

It comprises five layers:

1. **Classification Layer**  
2. **Semantic Title Layer**  
3. **Metadata Layer**  
4. **Visual Hierarchy Layer**  
5. **Security Reinforcement Layer**

---

# **1. Introduction**
Title pages in governed corpora are **security signalling devices**, not decorative elements.  
They must:

- communicate sensitivity  
- enforce classification clarity  
- support machine‑interpretation  
- maintain corpus‑level consistency  
- reinforce governance authority  

This Standard defines the normative rules for constructing such pages.

---

# **2. Normative References**
This specification is self‑contained. Optional alignment:

- ISO‑style document control conventions  
- Corporate security‑classification banner practices  
- APA professional formatting (informative only)

---

# **3. Terms and Definitions**

**Strictly Confidential**  
Highest sensitivity classification requiring prominent, repeated visual signalling and explicit handling instructions.

**Semantic Line Breaks**  
Manual line breaks inserted at conceptual boundaries to improve readability of long titles or subtitles.

**High‑Level Circulation**  
Distribution to executive or strategic stakeholders requiring elevated clarity, authority, and security signalling.

**Ideative Report**  
A document type focused on conceptual, strategic, or exploratory content rather than empirical or operational data.

---

# **4. SC‑TPGM Core Framework**

## **4.1 Components**
- **Classification Layer** — Defines banners, markers, and notices.  
- **Semantic Title Layer** — Governs main title, subtitle, spacing, and conceptual segmentation.  
- **Metadata Layer** — Specifies author, affiliation, date, and report‑type placement.  
- **Visual Hierarchy Layer** — Controls spacing, margins, font sizes, and layout clarity.  
- **Security Reinforcement Layer** — Ensures repeated cues and legal notices.

---

## **4.2 Typography & Layout Metrics (Normative)**

### **Font Families (Allowed)**
- Sans-serif: Arial, Helvetica, Calibri  
- Serif: Times New Roman, Garamond  

### **Minimum Sizes**
- Classification Marker: **14pt bold uppercase**  
- Main Title: **16–18pt bold**  
- Subtitle: **14–16pt**  
- Metadata Block: **12pt**  

### **Margins**
- All sides: **1 inch / 2.54 cm**

### **Line Spacing**
- Title block: **double-spaced**  
- Metadata block: **1.15–1.5 line spacing**

### **Banner Rules**
- Top banner: **mandatory for Class A**  
- Bottom banner: **mandatory for Class A**  
- Banner height: **0.6–1.0 cm** (if rendered visually)

---

## **4.3 Semantic Line Break Examples**

Correct:
```
Architecting Advanced AI for Strategic Foresight
and Organic Discovery
```

Incorrect:
```
Architecting Advanced AI for Strategic
Foresight and Organic Discovery
```

---

## **4.4 Normative Layout Schema**

```
+------------------------------------------------------------+
| CLASSIFICATION: [A/B/C/D]                                  |
|                                                            |
| Document Reference: `YYYY-XXX-spec`                        |
| # [Primary Title] – [Document Class or Standard Name]      |
| ### Technical Standard vX.Y                                |
| ### Governance & Architecture Specification                |
|                                                            |
| [Author Name]                                              |
| [Document Date]                                            |
|                                                            |
| Status: Draft / Stable / Deprecated                        |
|                                                            |
| Scope: [Short scope line]                                  |
| Primary Model / Scheme: [Model]                            |
|                                                            |
| ---------------------------------------------------------- |
| Confidentiality Notice (Class A/B/C only)                  |
| ---------------------------------------------------------- |
| CLASSIFICATION: [A/B/C/D] (Bottom Banner for Class A only) |
+------------------------------------------------------------+
```

---

# **5. Classification Classes (Normative)**

## **5.1 Class A — Strictly Confidential**
Requires maximum visual signalling, repeated banners, and explicit legal notices.

Triggers:

- High‑level circulation  
- Strategic or highly sensitive content  
- Risk of unauthorized disclosure  

Semantic summary:  
Maximum‑sensitivity strategic documents.

---

## **5.2 Class B — Confidential**
Requires clear but non‑repeated markings; no mandatory bottom banner.

Triggers:

- Sensitive but non‑strategic content  
- Internal circulation  

Semantic summary:  
Moderate‑sensitivity internal documents.

---

## **5.3 Class C — Unclassified Sensitive**
Minimal marking; optional notices.

Triggers:

- Operational content  
- Low‑risk distribution  

Semantic summary:  
Low‑tier sensitivity.

---

## **5.4 Class D — Non‑Sensitive (Public / Open Distribution)**
Class D documents **shall still carry a classification marker**, explicitly indicating non‑sensitive status (e.g., `PUBLIC`, `OPEN`, `NON-SENSITIVE`, `UNRESTRICTED`).

Triggers:

- Public documentation  
- Open technical standards  
- Non‑sensitive architectural specifications  

Semantic summary:  
Zero‑sensitivity documents, explicitly marked.

---

# **6. Governance Requirements (Normative)**

1. **Documentation Requirement**  
   All title‑page elements shall be explicitly documented and reproducible.

2. **Justification Requirement**  
   Any deviation from SC‑TPGM shall include rationale.

3. **Placement Requirement**  
   Classification markers shall appear at the **top of the document**.  
   Class A shall also include a bottom banner.

4. **Compatibility Requirement**  
   Title‑page structure shall remain compatible with corporate/government security conventions.

5. **Corpus Integrity Requirement**  
   Title‑page rules shall remain consistent across all governed documents.

This Standard inherits corpus‑level governance rules from the U‑CMS.

---

# **7. Target Maturity Framework (Informative)**

## **7.1 Stage 1 — Pre‑Standard (v0.x)**
- Ad‑hoc formatting  
- Inconsistent signalling  
- No semantic line breaks  

Purpose: Establish baseline.

---

## **7.2 Stage 2 — Structured (v1.x)**
- Standardized banners  
- Defined metadata placement  
- Semantic title structuring  

Purpose: Achieve consistency.

---

## **7.3 Stage 3 — Governed (v2.x)**
- Full SC‑TPGM compliance  
- Integrated security reinforcement  
- Corporate alignment  

Purpose: Ensure governance.

---

## **7.4 Stage 4 — Institutional (v3.x)**
- Organization‑wide adoption  
- Automated compliance checks  
- Corpus‑level governance  

Purpose: Institutionalize the standard.

---

# **8. Tagging Requirements (Normative)**

All documents shall be tagged with identifiers matching the reference code (`YYYY-XXX-spec`) and internal metadata.

Tagging shall be consistent across:

- Document headers  
- Metadata blocks  
- Change logs  

Tagging forms part of the audit trail.

---

# **9. Pre‑Release Identifiers (Normative)**

- **alpha** — exploratory draft  
- **beta** — near‑stable draft  
- **rc** — release candidate  

Examples:

- `1.0.0-alpha`  
- `1.0.0-rc.1`

---

# **10. Integrity Rules (Normative)**

A document is **invalid** if it:

- Omits mandatory banners (Class A)  
- Misplaces title or subtitle  
- Uses non‑professional fonts  
- Omits author or date  
- Omits confidentiality notice (Class A/B/C)  
- **Omits or malforms the `CLASSIFICATION:` field**  
- **Contradicts the corpus‑versioned roadmap (U‑CMS)**  

---

# **11. Corpus Change Protocol (Normative)**

- Changes require ADR justification.  
- Boundary‑altering changes require MAJOR increments.  
- Corpus changes are versioned independently.  
- Corpus integrity must be preserved.

---

# **12. Transition State Machine (Normative)**

### Allowed Transitions
- Draft → Stable  
- Stable → Deprecated  

### Forbidden Transitions
- Deprecated → Stable without justification  
- Any transition contradicting roadmap  

### Preconditions
- Class A: Security markings validated  
- Class B: Internal circulation confirmed  
- Class C: Sensitivity assessed  
- Class D: Public/open status confirmed  

---

# **13. Compliance & Audit**

Supports:

- Decision traceability  
- Security auditability  
- Compliance alignment  
- Deterministic evolution  

All changes must be reviewable and justified.

---

# **14. Document Control**

**Document Owner:** Corpus Governance Authority  
**Change Authority:** Standards Board  
**Review Cycle:** Per MAJOR change  

---

# **v1.0 Summary of Changes**
- Initial constitutional alignment with U‑CMS  
- Added Class D  
- Added typography/layout metrics  
- Added normative layout schema  
- Added classification‑validity rule  
- Added semantic line‑break examples  

---

# **Changelog**
| Version ID | Date | Key Changes |
|-----------|------|-------------|
| 1.0 | 2026‑07‑31 | Initial governed release |

---

