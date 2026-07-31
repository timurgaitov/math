# 0002 — Reciprocals get below any ε

Unit: [01 — Logic and the language of proof](../units/01-logic-and-proof/plan.md)
Status: **solved** (session [0001](../sessions/0001-2026-07-31.md))

## Problem

Prove: for every ε > 0 there exists n ∈ ℕ such that 1/n < ε.

## Student's proof (final version)

> Let ε > 0 be arbitrary. Let n = floor(1/ε) + 1. n is a natural number
> because ε > 0 and by the floor definition. By the floor definition
> floor(x) + 1 > x. So 1/n = 1/(floor(1/ε) + 1) < 1/(1/ε) = ε
> [since floor(1/ε) + 1 > 1/ε > 0, so taking reciprocals flips the
> inequality — clause added at filing].

Alternative accepted style ("it suffices"): reduce the goal to n > 1/ε
via the reciprocal flip, then take n = floor(1/ε) + 1, or simply cite the
Archimedean property (ℕ is unbounded in ℝ) — an existence claim needs a
guaranteed witness, not a formula.

## What the exercise surfaced (for later recall)

- First attempt at arbitrary ε reasoned via decimal expansions
  ("0.00...1"), which silently assumes ε is a terminating decimal.
  Fix: solve the target inequality for n.
- An intermediate chain used 1/(floor(1/ε)+1) < 1/(1/ε + 1), which
  requires floor(1/ε) > 1/ε — false direction for floor.
- Draft prose manipulated the goal ("flip the initial inequality") as if
  already established; fixed by learning the claim-then-derive and
  "it suffices to show" idioms.

See [notes/existence-proofs.md](../notes/existence-proofs.md).
