# Adaptive Persistent Agent Design — Full Philosophy

Source document. Load when principles conflict, ambiguity is high, or deeper justification is needed.

---

## Core Design Principles

### 1. Do not encode baseline model capabilities

Only encode information the base model would not reliably infer or perform on its own.

Do not store:
- Generic best practices
- Obvious formatting behavior
- Universal quality standards
- Basic correctness expectations
- Common-sense operational behavior

Store:
- User-specific heuristics
- Workflow-specific decision rules
- Recurring calibration patterns
- Domain-specific reasoning tendencies
- Persistent behavioral preferences

Persistent memory should contain high-signal deviations from baseline behavior.

---

### 2. Prefer abstractions over exhaustive branching

Avoid:
- Giant playbooks
- Endless edge-case handling
- Scenario explosion
- Deeply nested procedural trees
- Bloated instruction layers

Prefer:
- Compressed abstractions
- Behavioral principles
- Reusable heuristics
- Adaptive reasoning
- Minimal operational kernels

The system should generalize instead of enumerating every possible situation.

---

### 3. Model decision-making processes instead of outputs

Do not optimize for:
- Memorizing outputs
- Reproducing surface patterns
- Copying prior examples mechanically

Instead:
- Infer why outputs were preferred
- Model the reasoning process behind decisions
- Learn evaluation criteria
- Capture reusable heuristics

The goal is calibrated reasoning, not imitation.

---

### 4. Separate invariant, contextual, and one-off knowledge

All learned information should be classified before entering persistent memory.

**Invariant** — Stable across contexts.
**Contextual** — Useful only under certain conditions.
**One-off** — Do not persist unless it reveals a broader reusable principle.

This prevents overgeneralization, memory pollution, brittle systems, and conflicting memory accumulation.

---

### 5. Learn through iteration and reflection

Do not rely on:
- Exhaustive upfront configuration
- Giant onboarding questionnaires
- Static preference inventories

Prefer:
- Iterative correction
- Reflection loops
- Progressive calibration
- Real-world usage feedback

Adaptive systems should improve through interaction over time.

---

### 6. Compression is mandatory

Persistent memory systems decay without active compression.

The system must continuously:
- Compress
- Merge
- Rewrite
- Supersede
- Prune

Avoid append-only memory growth. Long-term scalability depends on preserving signal density.

---

### 7. Retrieval should be conditional

Do not retrieve all context by default.

Retrieve additional context only when:
- Ambiguity is high
- Confidence is low
- Principles conflict
- Nuance materially affects outcomes
- Stakes justify additional context

Additional context should be activated selectively.

---

### 8. Store semantic heuristics instead of surface patterns

Avoid:
- Rigid output preferences
- Isolated examples without reasoning
- Brittle pattern memorization

Prefer:
- Decision heuristics
- Abstraction layers
- Contextual reasoning boundaries
- Durable behavioral patterns

The system should understand why changes matter.

---

### 9. Avoid instruction bloat

Large instruction systems degrade over time.

Prefer:
- Compact instruction kernels
- High signal-to-noise ratio
- Compressed operational guidance
- Dense abstractions

Persistent instruction layers should remain intentionally small.

---

### 10. Memory must evolve

Persistent systems must support:
- Supersession
- Reinterpretation
- Pruning
- Rewriting outdated knowledge

Do not preserve obsolete or contradictory memory indefinitely. Memory should evolve with changing workflows and preferences.

---

### 11. Examples support calibration, not primary reasoning

Examples should:
- Resolve ambiguity
- Calibrate nuance
- Improve difficult edge cases

Examples should NOT:
- Dominate reasoning
- Replace abstractions
- Become the primary intelligence layer

Abstract reasoning should remain primary.

---

### 12. Optimize for low-friction delegation

The objective is not perfect replication.

The objective is:
- Reliable delegation
- Progressively calibrated outputs
- Reduced correction cost
- Increasing trust over time

The system succeeds when outputs become consistently usable with minimal iteration.

---

## Recommended System Architecture

### Layer 1 — Persistent Instruction Layer
Examples: AGENTS.md, CLAUDE.md, SKILL.md

Purpose: define philosophy, operational behavior, memory discipline, reasoning boundaries.

Should contain: abstractions, principles, operational constraints.
Should NOT contain: large transcripts, excessive examples, repetitive instructions, edge-case enumerations.

This layer should remain compact.

---

### Layer 2 — Distilled Memory Layer
Examples: principles.md, heuristics.md, anti_patterns.md, transformation_patterns.md

Purpose: store reusable abstractions and calibrated behavioral knowledge to support long-term adaptation.

This is the primary reasoning layer.

---

### Layer 3 — Example Archive Layer

Purpose: calibration, ambiguity resolution, edge-case grounding.

Examples should remain dormant unless retrieval conditions are triggered.

---

### Layer 4 — Reflection Layer

Purpose: session-by-session learning. Compare outputs against corrections, infer reasoning changes, compress lessons, decide whether persistent memory updates are warranted.

Reflection drives long-term adaptation.

---

## Retrieval Rules

Retrieve deeper context only when:
- Ambiguity is high
- Confidence is low
- Principles conflict
- Nuance materially affects outcomes
- Stakes justify additional context

Otherwise: rely on distilled abstractions first.

---

## Operational Goal

Build adaptive systems that:
- Improve through use
- Compress intelligently
- Remain inspectable
- Avoid context bloat
- Generalize behavior
- Support reliable delegation
- Prioritize reasoning over memorization
- Scale across workflows and domains
