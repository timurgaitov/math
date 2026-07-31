# 0003 — Sum of two even integers is even

Unit: [01 — Logic and the language of proof](../units/01-logic-and-proof/plan.md)
Status: **solved** (session [0002](../sessions/0002-2026-07-31.md))

## Problem

Prove: the sum of two even integers is even.

Quantifier structure (exposed before proving):
∀x, y ∈ ℤ: (x even ∧ y even) → x + y even.

## Student's proof (final version)

> Let x, y be arbitrary even numbers.
> Since x is even, choose m ∈ ℤ with x = 2m.
> Since y is even, choose n ∈ ℤ with y = 2n.
> Let S = x + y. Then S = 2m + 2n = 2(m + n).
> Let k = m + n; k ∈ ℤ since m and n are.
> So there exists k with S = 2k, hence S is even by definition.

## What the exercise surfaced (for later recall)

- First draft listed "∃k: 2k = S" alongside the two given existence
  statements, as if all three were assumptions — the goal placed in the
  "given" pile. Fixed on prompting: assumptions hand you witnesses,
  the conclusion demands one, and it may appear only at the end.
- Learned the **choose** idiom: "∃m: x = 2m" is a statement, not a name;
  to compute with m one writes "choose m ∈ ℤ with x = 2m".
- Checking the witness lands in the right set (m + n ∈ ℤ) was done
  unprompted.

See [notes/reading-definitions.md](../notes/reading-definitions.md).
