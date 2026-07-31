# **CLASSIFICATION: D**

Document Reference: `2026-005-whitepaper`

# **Structural Emptiness and Null‑Space Artefacts in Deterministic Project Manifolds**

### Technical Standard v1.0

### Conceptual Analysis & Hybrid Engine Architecture Specification

---

#### William Murray

#### 30 July 2026

---

**Status:** Stable

**Scope:** Specifies the refactoring of UPTF architecture generators into pointer-driven dereferencing machines combining Prolog symbolic governance with native C++20 materialisation layers. Establishes the formal model for representing structural emptiness, semantic null-space markers (`null.md`), and deterministic directory manifolds.

**Primary Model / Scheme:** U‑CMS‑PTR‑1 (Pointer Machine Dereferencing & Null-Space Manifold Model)

---

Here's a draft revised opening that replaces Sections 1 and 2:

---

## 1. Overview

The UPTF architecture generator was initially implemented as a deterministic Prolog ledger engine: consuming a double-entry YAML ledger, selecting pending artefacts, generating files, and updating state. The design was correct and governance-aligned, but the ledger entries were being treated as checklist items rather than what they structurally are — symbolic references.

Each entry in `build_plan.md` contains:

- a pointer to a filesystem path
- a pointer to a template rule
- a pointer to a state bit

This means the architecture generator is not a rule-driven checklist. It is a **pointer-driven dereferencing machine**. The ledger is a pointer registry. The engine is a dereferencer. The `architecture/` directory is the materialised heap.

Recognising this has two consequences. First, it clarifies what Prolog is actually doing: symbolic governance — ledger interpretation, constraint enforcement, structural validation. Second, it identifies what Prolog should not be doing: pointer dereferencing, atomic writes, and OS-level materialisation. That belongs in a native layer.

This whitepaper formalises that two-layer model and specifies the hybrid Prolog/C++20 architecture engine that follows from it.

---

Here's the full revised document flow from Section 2 onwards, tightened for public consumption:

---

## 2. The Two-Layer Architecture Model

The correct architecture is a two-layer system.

**Layer 1 — Symbolic Governance (Prolog)**
- Ledger parsing and interpretation
- Structural validation
- Governance rule enforcement
- Determination of next artefact
- Production of the symbolic pointer registry

**Layer 2 — Native Materialisation (C++20)**
- Pointer dereferencing
- Template resolution
- Atomic file writes
- Directory creation
- State bit updates
- Deterministic execution

This mirrors standard compiler design: a symbolic front-end handling rules and constraints, and a pointer-driven back-end handling memory and code generation.

---

## 3. Why Prolog and C++20

Prolog excels at symbolic reasoning. It is the correct tool for interpreting the ledger, enforcing UPTF governance rules, and producing the pointer registry. It outputs entries of the form:

```prolog
ptr("architecture/system/context.md", "context_template_v1", pending).
```

C++20 is the correct tool for everything that follows. It provides:

- `std::filesystem` for safe path dereferencing
- `std::string_view` for zero-copy symbolic references
- `std::unique_ptr` for safe ownership semantics
- `std::unordered_map` for template registries
- RAII for deterministic cleanup

Neither layer replaces the other. Prolog governs; C++20 materialises.

---

## 4. C++20 Implementation Model

The pointer-driven model maps onto five concrete components:

**4.1 SymbolicPointer Structs**
Each ledger entry becomes a C++ struct containing a path pointer, a template pointer, and a state pointer.

**4.2 Template Dereferencer**
A class mapping template keys to canonical templates, resolving symbolic pointers and materialising artefacts deterministically.

**4.3 Execution Cursor**
A program counter traversing the pointer registry, skipping completed entries, and persisting state across crashes.

**4.4 Materialisation Kernel**
Performs atomic writes, creates directories, expands templates, and guarantees byte-identical output.

**4.5 Governance Integration**
Enforces UPTF structural invariants, avoids destructive writes, maintains auditability, and preserves ledger integrity.

---

## 5. Forward Plan

1. Formalise the pointer registry schema
2. Implement the Prolog symbolic layer
3. Implement the C++20 dereferencing engine
4. Define canonical templates
5. Integrate atomic materialisation
6. Validate against UPTF v2.1
7. Document the hybrid architecture model

---

## 6. Conclusion

The UPTF architecture generator is a pointer machine. Prolog provides symbolic governance; C++20 provides the materialisation substrate. Together they form a hybrid engine that is deterministic, auditable, pointer-correct, and UPTF-compliant.

---

