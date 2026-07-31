# 0004 — Divisibility is transitive

Unit: [01 — Logic and the language of proof](../units/01-logic-and-proof/plan.md)
Status: **solved** (session [0002](../sessions/0002-2026-07-31.md))

## Problem

Prove: for integers a, b, c, if a | b and b | c, then a | c.

## Student's proof (final version)

> Let a, b, c be arbitrary integers with a | b and b | c.
> Since a | b, choose m ∈ ℤ with b = ma.
> Since b | c, choose n ∈ ℤ with c = nb.
> Then c = nb = n(ma) = (nm)a.
> Let k = nm; k ∈ ℤ.
> So there exists k with c = ka, hence a | c by definition.

## What the exercise surfaced (for later recall)

- Clean first attempt; the choose/exhibit skeleton from
  [0003](0003-sum-of-two-evens.md) transferred without prompting.
- Minor style point: keep parentheses visible (c = n(ma) = (nm)a) so the
  associativity step is explicit when algebra gets less trivial.

See [notes/reading-definitions.md](../notes/reading-definitions.md).
