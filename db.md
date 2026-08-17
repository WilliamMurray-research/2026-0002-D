**From Naming Specification**  

Based on Section 11 (Registry Compliance) and the surrounding architecture defined in Specification 3.1, the central asset registry must track the following fields across two core scopes: System Counters / State and Directory & Document Metadata.
1. Global System Counters (Registry Level)
To enforce global uniqueness and sequence integrity, the registry must track high-level counters:

| Field Name | Type | Description |
|---|---|---|
| next_directory_id | CHAR(4) | Next available globally sequential 4-digit DDDD identifier (0001–9999). |
| directory_sequence_counters | MAP/JSON | Map tracking the next available 3-digit sequence number (NNN) per doc_type per directory (e.g., { "2026-0001-D": { "spec": "002", "req": "001" } }). |

2. Directory Entity Fields. 
Directories act as the authoritative security and lifecycle anchors for all contained files.

| Field Name | Type | Description |
|---|---|---|
| year | CHAR(4) | Four-digit creation year (YYYY). |
| directory_id | CHAR(4) | Unique sequential directory ID (DDDD). |
| lifecycle_code | CHAR(1) | Derived from the 1st digit of DDDD (0–9: Governance, R&D, Product, etc.). |
| classification | CHAR(1) | Inherited security level (A, B, C, or D). |
| created_at | DATE / TIMESTAMP | Date/time the directory was created in the repository. |
| export_policy | ENUM/STRING | Export visibility rule derived from classification (Omit, Redacted Stubs, Limited Metadata, or Full). |

3. Document Entity Fields. 
Tracks individual document identity, versioning, status, and supersession lineage.

| Field Name | Type | Description |
|---|---|---|
| document_reference | STRING | Full authoritative identifier (YYYY-DDDD-C-TYPE-NNN). |
| directory_id | CHAR(4) | Parent directory DDDD key (Foreign Key). |
| year | CHAR(4) | Creation year (must match parent directory). |
| classification | CHAR(1) | Inherited classification letter (A–D). |
| doc_type | VARCHAR(10) | Lowercase approved type code (e.g., spec, req, adr). |
| sequence | CHAR(3) | Stable sequence number (NNN) identifying the document family within the directory. |
| header_version | VARCHAR(10) | Semantic version from document header (e.g., 3.1). Changes independently of filename. |
| status | ENUM | Restricted vocabulary: Draft, Stable, Superseded, or Retired. |
| superseded_by | STRING (Nullable) | Explicit target reference (YYYY-DDDD-C-TYPE-NNN) when status is Superseded. |
| reclassified_from | STRING (Nullable) | Origin document reference if created via a Section 5 reclassification procedure. |
| file_path | TEXT | Relative path to the file within the repository (e.g., /docs/2026-0001-D-spec-001.md). |

4. Graph Relationship / Lineage Attributes (Memgraph Alignment)  
To support graph indexing (Section 10.3), the registry must maintain structural edge attributes:  
 * VERSION_OF Edge: Links semantic revisions of the same identity (NNN) when updating header_version without changing the filename.  
 * SUPERSEDES Edge: Links documents of different identities when a new file replaces an old file.  
 * RECLASSIFIED_FROM Edge: Tracks lineage specifically across security/lifecycle migrations (accompanied by a SUPERSEDES edge).  
