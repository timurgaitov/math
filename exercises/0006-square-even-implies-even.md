# 0006 — If n² is even then n is even

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md)
Status: **solved** (session [0003](../sessions/0003-2026-08-01.md))

## Problem

Prove: for all n ∈ ℤ, if n² is even, then n is even.

## Why direct proof fails (worked through first, on purpose)

Direct setup hands you n² = 2m and demands a witness for n. Algebra with
+ and · only builds upward (from n to n²); nothing extracts n from 2m.
Mid-attempt, the equation n² = 4k² appeared — licensed by no line above it;
it presupposes n = 2k, the goal. Third appearance of the goal-in-given-pile
habit; caught by tracing which line licenses each equation.

## Student's proof (final version, by contrapositive)

Contrapositive: ∀n ∈ ℤ: n odd ⇒ n² odd. Proving it proves the original
(truth-table equivalence, verified in session).

> Let n ∈ ℤ be arbitrary.
> Since n is odd, choose k ∈ ℤ with n = 2k + 1.
> Then n² = (2k + 1)(2k + 1) = 4k² + 4k + 1 = 2(2k² + 2k) + 1.
> Exhibit l = 2k² + 2k; l ∈ ℤ as a product and sum of integers.
> So n² = 2l + 1, hence n² is odd by definition.

Then n odd ⇒ n² odd is equivalent to n² even ⇒ n even as its
contrapositive, so the original claim holds. ∎

## What the exercise surfaced (for later recall)

- Negating "n is even" literally gives ∀k ∈ ℤ: n ≠ 2k — a fence, no witness,
  nothing to compute with. The parity fact (every integer is even or odd,
  never both; taken as given until division with remainder) converts it to
  the ∃-fact "n is odd", which feeds the choose idiom again.
- The tell for contrapositive: assuming P gave material about the composite
  object (n²) with an obligation on the simple one (n); assuming ¬Q gives
  material on the simple object and an uphill computation.

See [notes/contrapositive.md](../notes/contrapositive.md).
