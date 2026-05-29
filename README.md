# Adaptive Persistent Agent

Adaptive Persistent Agent (APA) is a design framework for building agent systems that improve over time without collapsing under messy memory, bloated instructions, or endless edge-case rules.

It gives you a way to design, audit, and maintain persistent agent behavior by separating stable instructions, reusable memory, calibration examples, and reflection loops.

## Why APA Exists

Most long-running agent systems decay for the same reasons:

- Instructions become a dumping ground for every correction.
- Memory grows append-only instead of being compressed.
- Examples start replacing reasoning.
- One-off user feedback gets treated like permanent truth.
- Context gets loaded by default instead of retrieved when needed.

APA is meant to prevent that decay. It favors compact principles, reusable heuristics, and deliberate memory hygiene over giant prompt files and brittle playbooks.

## What It Helps With

Use APA when you are designing or reviewing:

- Persistent-memory agents
- Prompt and instruction systems
- Agent skills or reusable workflows
- Automation pipelines
- Delegation systems
- Reflection and learning loops
- Memory pruning or compression strategies

## The Four-Layer Model

APA separates agent knowledge into four layers:

| Layer | Purpose |
|---|---|
| Instruction | Compact principles, constraints, and reasoning boundaries |
| Memory | Reusable heuristics, preferences, and calibration patterns |
| Examples | Dormant reference cases for ambiguity and edge grounding |
| Reflection | Session learning, compression decisions, and update history |

The instruction layer should stay small. The memory layer should carry reusable knowledge. Examples should calibrate, not dominate. Reflection should decide what gets kept, compressed, rewritten, or discarded.

## Audit Mode

Use audit mode when a system already exists.

APA scores the system across seven signals:

- Signal density
- Abstraction over enumeration
- Reasoning over imitation
- Memory hygiene
- Retrieval discipline
- Layer separation
- Evolution readiness

The output should identify the highest-cost design problems first, especially instruction bloat, duplicated memory, unclassified one-offs, and append-only growth.

## Build Mode

Use build mode when creating a new system.

Start with a compact instruction kernel, then add memory, examples, and reflection only when they have a clear role. APA pushes against upfront overconfiguration and favors learning through use.

## Repository Structure

```text
.
|-- SKILL.md
`-- references
    |-- apa-philosophy.md
    `-- examples.md
```

- `SKILL.md` contains the active APA operating instructions and audit scorecard.
- `references/apa-philosophy.md` contains the full design philosophy.
- `references/examples.md` contains calibration examples for ambiguous cases.

## How To Use

Load or adapt `SKILL.md` in any agent, prompt, workflow, or automation environment that supports reusable instructions.

Example requests:

```text
Audit this agent architecture using APA.
```

```text
Design a persistent memory structure for this workflow.
```

```text
Review this instruction file for bloat and layer violations.
```

```text
Help me decide what should become persistent memory versus reflection-only notes.
```

## Design Principles

APA is built around a few core rules:

- Do not encode baseline model behavior.
- Prefer abstractions over exhaustive case lists.
- Store decision heuristics instead of surface patterns.
- Classify knowledge as invariant, contextual, or one-off before persisting it.
- Retrieve deeper context only when it is actually needed.
- Rewrite, merge, supersede, and prune memory over time.



