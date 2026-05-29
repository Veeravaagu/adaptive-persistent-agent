# APA Calibration Examples

Dormant reference. Load only when a fix is non-obvious or two principles appear to conflict.
Each example shows the offending content, the principle it violates, and the shortest durable fix.

---

## 1. Signal density — cutting baseline behavior

**Before**
> Always write clear, well-organized responses. Use correct grammar. Double-check your work for errors before responding. Be helpful and accurate.

**Violation:** Restates baseline model behavior (Principle 1). Every line is something the model already does reliably.

**After**
> *(deleted)*

**Why:** Nothing here is a high-signal deviation from default behavior. Keeping it dilutes the signal of the instructions that do matter.

---

## 2. Abstraction over enumeration — collapsing a case list

**Before**
> If the user asks for a summary, keep it under 200 words. If they ask for a report, use headers. If they ask for an email, use a greeting. If they ask for notes, use bullets. If they ask for a memo, ...

**Violation:** Scenario explosion (Principle 2). The list will never be complete and grows with every new format.

**After**
> Match output structure to the genre the user named; default to the most scannable form that genre implies.

**Why:** One heuristic generalizes to formats not yet enumerated.

---

## 3. Reasoning over imitation — capturing *why*, not *what*

**Before**
> Last time the user preferred "Q3 revenue rose 12%" over "Revenue experienced a notable increase." Use the first style.

**Violation:** Memorizes a surface output (Principle 3). Brittle — applies only to this one sentence.

**After**
> User prefers concrete figures over qualitative hedging in metrics reporting.

**Why:** Stores the decision criterion, which transfers to any future metric.

---

## 4. Memory hygiene — classify before persisting

**Before** (appended to memory verbatim)
> The user said the deadline for the Acme deck was Friday.

**Violation:** Unclassified one-off (Principle 4). A specific deadline doesn't generalize and will be stale next week.

**After**
> *(not persisted)* — one-off. If a pattern emerges (user consistently wants Friday delivery), persist that pattern instead.

**Why:** One-offs only persist when they reveal a reusable rule.

---

## 5. Layer separation — moving examples out of instructions

**Before** (inside `SKILL.md`)
> ... [40 lines of full input/output transcripts demonstrating tone] ...

**Violation:** Example archive bleeding into the instruction layer (Principle 11 + layer separation). Bloats the always-loaded kernel.

**After**
> Instruction layer: "Match the calibrated tone; see `examples.md` for edge cases."
> Transcripts moved to `examples.md`, loaded only when tone is ambiguous.

**Why:** Keeps the instruction kernel compact and the examples dormant until needed.

---

## 6. Evolution readiness — supersede instead of append

**Before**
> Rule (Jan): Use formal tone.
> Rule (Mar): Actually, use casual tone for internal docs.
> Rule (May): Casual everywhere now.

**Violation:** Append-only accumulation (Principle 10). Contradictory rules coexist; the reader must guess which wins.

**After**
> Use casual tone (supersedes earlier formal-tone guidance).

**Why:** Outdated knowledge is rewritten, not stacked. Memory stays inspectable.

---

## Conflict resolution note

When **signal density** (cut it) conflicts with **examples support calibration** (keep an example): keep the example only if removing it measurably increases correction cost on a recurring edge case. Otherwise cut. Default toward compression.
