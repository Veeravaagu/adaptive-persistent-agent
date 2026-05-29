---
name: adaptive-persistent-agent
description: "Applies Adaptive Persistent Agent (APA) design principles to any system, workflow, skill, or automation being built or reviewed. Trigger whenever the user is creating a new skill, building a workflow, designing an agent system, structuring automation pipelines, or wants to evaluate whether an existing system follows good design. Also trigger when the user mentions memory layers, instruction bloat, agent memory, skill architecture, persistent memory, delegation systems, or says 'APA', 'adaptive agent', 'audit my workflow', 'audit my skill', 'is this well designed', or any variation of reviewing or building systems that learn and improve over time. This skill should activate alongside other skill-building or workflow-design activities — not just when explicitly named."
---

# Adaptive Persistent Agent Design

Apply the APA principles from `references/apa-philosophy.md` to whatever system, skill, or workflow is in context.

There are two modes. **Audit mode** reviews an existing system. **Build mode** structures a new one. Pick based on whether the artifact already exists.

## Audit Procedure

Run these steps in order. Do not skip to recommendations before inventorying.

1. **Inventory the layers.** Map the system's files/sections onto the four layers (instruction, memory, examples, reflection). Flag anything that can't be placed — unplaceable content is usually bloat or a layer violation.
2. **Score each criterion** (see scorecard below) as 🟢 solid / 🟡 weak / 🔴 violated, with a one-line reason citing the specific offending content.
3. **Find the highest-cost violation first.** Bloat and append-only growth compound over time, so rank fixes by long-term cost, not ease.
4. **Propose the shortest durable fix** for each 🔴 and 🟡 — rewrite or compress rather than add.
5. **Re-check for regressions.** Confirm fixes didn't push content into the wrong layer or duplicate existing memory.

For calibration on what each fix looks like in practice, see `references/examples.md` (load only when a fix is non-obvious).

### Scorecard

Score every system against these seven signals:

| Signal | 🟢 looks like | 🔴 looks like |
|---|---|---|
| Signal density | Every line earns its place | Restates baseline model behavior |
| Abstraction over enumeration | Reusable heuristics | Exhaustive case lists / nested trees |
| Reasoning over imitation | Models *why* | Memorizes outputs |
| Memory hygiene | Classified invariant/contextual/one-off | Unclassified accumulation |
| Retrieval discipline | Loads context conditionally | Loads everything by default |
| Layer separation | Distinct layers | Examples/logs mixed into instructions |
| Evolution readiness | Supersedes & prunes | Append-only |

### Output Format

Deliver findings as: (1) a filled scorecard, (2) findings ordered by long-term cost — each naming the offending content, the principle, and the fix, (3) a one-line verdict on delegation-readiness. Lead with the single change that matters most.

## Build Mode

When structuring a new system, scaffold the four layers as distinct artifacts and keep the instruction layer minimal:

- **Instruction** (`SKILL.md` / `CLAUDE.md` / `AGENTS.md`) — philosophy, constraints, reasoning boundaries. Stays compact.
- **Memory** (`heuristics.md`, `anti_patterns.md`, …) — distilled reusable knowledge. The primary reasoning layer.
- **Examples** (`examples.md`) — dormant; loaded only under retrieval conditions.
- **Reflection** (`reflection.md` / session log) — compressed lessons and memory-update decisions.

Start empty except for the instruction kernel. Let memory and examples accrue through use, not upfront configuration.

## Layer Architecture

When designing or evaluating a system's structure, apply this hierarchy:

| Layer | Purpose | Should contain | Should NOT contain |
|---|---|---|---|
| Instruction | Define philosophy and behavior | Abstractions, principles, constraints | Transcripts, edge cases, repetitive rules |
| Memory | Reusable distilled knowledge | Heuristics, calibration patterns, decision rules | Generic advice, isolated corrections |
| Examples | Calibration only | Ambiguity resolution, edge grounding | Primary reasoning, output templates |
| Reflection | Session learning | Compressed lessons, memory update decisions | Raw session logs |

## Compression Rules

Before persisting any knowledge, apply:
- Is this reusable across contexts, or isolated to one event?
- Can this be expressed more abstractly without losing the decision signal?
- Does this duplicate something already stored?
- Is this invariant, contextual, or one-off? (One-offs do not persist unless they reveal a broader pattern.)

Store the shortest durable abstraction possible.

## Reflection Workflow

After meaningful correction or revision in any system:
1. Compare original output, corrected output, and feedback
2. Infer what reasoning or calibration changed
3. Classify: invariant / contextual / one-off
4. Assign confidence: low / medium / high
5. Decide: no update / reflection-only / persistent memory update / rewrite-prune
6. Store the shortest durable abstraction

## Reference

For full principle definitions, retrieval rules, and architecture rationale:
→ `references/apa-philosophy.md`

Load this when: principles conflict, ambiguity is high, or a decision requires deeper justification than the criteria above provide.
