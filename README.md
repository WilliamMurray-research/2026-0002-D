# Foundations

A repository for original frameworks, principles, ideas, hypotheses, and informal proofs.

I am drawn to moments where a field is navigating by the wrong conceptual frame: where practitioners have inherited a framing that is imprecise, inverted, or simply unnamed. The work here attempts to replace those frames with more precise ones - to make implicit trade-offs explicit, and to give vocabulary to mechanisms that exist in practice but resist articulation.

Each piece takes something practitioners navigate by intuition and makes it explicit: a trade-off with a name, a mechanism with a structure, a pattern that recurs across domains that appear unrelated. The cross-domain applicability is the test. If a principle only holds in one place, it is an observation. If it holds in five, it is a framework.

This is a record of how I think - not a literature review, not a tutorial series, not commentary on others' work. The frameworks here are original in the sense that they were developed to fill a gap: a thing I needed a name for that did not yet have one.

---

## What lives here

**Principles** - formal statements of trade-offs or exchange relationships, with corollaries and cross-domain illustrations.
*Example: The Latency–Accuracy Exchange Principle - that time is not a cost to be minimised but a resource to be deliberately invested in pursuit of correctness.*

**Mechanism notes** - structural analyses of how something works, below the level at which it is usually discussed.

**DSL specifications** - formal grammars and design documents for domain-specific languages developed across the project portfolio.

**Emergent-structure analyses** - examinations of patterns that arise without being designed: in systems, in graphs, in computation.

**Theoretical drafts** - early-stage ideas in development, marked as such.

---

## How to read these

Each framework is meant to stand alone. The abstract states the principle. The body derives consequences and tests the principle against domains where it should apply. If the principle fails a domain, that failure is noted — a framework that only survives curated examples is not yet a framework.

Where a paper draws on established work, it cites it. Where it proposes something new, it says so.

---

## Relationship to the project portfolio

The project portfolio is where these ideas are built. This repository is where they are articulated. A framework developed while designing Project 4 (non-backtracking walks on Hashimoto matrices) may appear here as a paper on spectral structure and information propagation. The code and the prose are two registers of the same inquiry.

---

## Summaries

### The Architecture of Plausibility

This paper deconstructs the operational reality of large language models, arguing that they are fundamentally statistical "plausibility engines" optimized for linguistic coherence rather than empirical correspondence with reality. Because their training focuses on next-token prediction rather than factual grounding, they produce authoritative hallucinations and logical mimicry that place a heavy cognitive burden on human auditors. To mitigate these risks, the framework advocates for an architectural separation of concerns - anchoring volatile models to verifiable truth structures through Retrieval-Augmented Generation (RAG), programmatic execution tools, and disciplined validation boundaries.

### Cognitive Minimalism in Programming

This ideative research report proposes a framework for programming best practices based on Occam's Razor and Cognitive Load Theory to promote cognitive minimalism and epistemic restraint. The report argues that languages and practices designed to reduce cognitive burden can improve developer productivity, code maintainability, and system comprehensibility, particularly for neurodivergent individuals and in complex modular systems.

### The First Honest Machine

I argue that the fundamental challenge facing artificial intelligence is not scaling capability, but engineering "honest" systems whose internal reasoning is transparent, governed, and resilient against "drift" - the silent accumulation of unexamined errors across intermediate states. I contend that current monolithic AI models operate as inscrutable statistical engines, creating institutional fragility when deployed in high-stakes environments where output justification is essential. To solve this, I propose replacing end-to-end decoding with a governed, dual-chamber architecture that structurally separates generative synthesis from symbolic runtime governance, utilises a multi-stage proposer–validator pipeline, maintains an auditable, deterministic memory ledger, and employs documentation as an unyielding constitutional substrate. Ultimately, I conclude the future of artificial intelligence belongs not to the most powerful models, but to constitutional architectures engineered for verifiable structural integrity and trust.

### The Latency–Accuracy Exchange Principle

This paper introduces the latency–accuracy exchange principle: the idea that time is a resource deliberately invested to purchase correctness, determinism, and governance fidelity. Drawing on complexity theory, verification, distributed systems, and safety critical engineering, it argues that many systems should invert the industry’s speed first bias. The principle provides a formal lens for designing systems where correctness is paramount, demonstrating its application across databases, compilers, APIs, distributed consensus, and testing architectures.

### A Multi-Model, Syntax-Preserving, Drift-Resistant Conjecture-to-Proof Pipeline

A technical manuscript outlining a structured, operator‑directed workflow for multi‑model conjecture formation, critique, formalisation, and proof verification. Emphasises drift‑resistance, syntax preservation, falsifiability, and rigorous versioning across all phases of reasoning.

### Prototyping as an Epistemic Taxonomy in Software Systems

This paper advances a taxonomy of prototyping in software systems, distinguishing abductive, inductive, and deductive modes, and argues that deductive prototyping offers a structurally rigorous alternative to intuition‑driven exploration. By formalising conjectures into hypotheses, grounding them in mathematical, empirical, or algorithmic constraint models, and deriving mechanisms prior to implementation, deductive prototyping reduces pre‑execution uncertainty, exposes structural impossibilities early, and enables system‑wide refinements rather than local patching. The framework positions deductive prototyping as a high‑leverage epistemic method in domains where formal constraints are available, reframing prototype construction as a disciplined knowledge‑generation process rather than an exploratory artefact.

### Risk as a First-Class Entity in Systems Design: Establishing ISO 27000, ISO 31000, and ISO 42001 as the Minimum Professional Standard for Autonomous and Semi-Autonomous Systems

This whitepaper argues that risk must be treated as a first‑class entity in the design of autonomous and semi‑autonomous systems. Drawing on decades of professional experience witnessing unmanaged risk bankrupt organisations and cause real‑world harm, it establishes ISO 27000, ISO 31000, and ISO 42001 as the minimum acceptable professional standard for responsible automation. The paper outlines how modern failure modes exceed human intuition, why traditional engineering cultures fall short, and how risk‑first architecture provides the only defensible foundation for safe, governed, and accountable system design.

---

*All work here is original unless cited.*
