# 0012 — not every prime is odd

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md)
Status: **solved** (session [0006](../sessions/0006-2026-08-15.md))

## Problem

Disprove: for every integer n, if n is prime then n is odd.

## Solution (student's, session 0006)

The statement to prove is the negation. Pushing ¬ through the ∀ and
then through the implication with ¬(P ⇒ Q) ≡ P ∧ ¬Q
(`\neg(P \Rightarrow Q) \equiv P \land \neg Q`):

> ∃n such that n is prime **and** n is not odd.

So a counterexample to an implication must make the hypothesis *true*
and the conclusion *false* — a non-prime even number would disprove
nothing.

Witness: n = 2. Two conjuncts to verify.

**2 is not odd.** Witness k = 1 gives 2 = 2k, so 2 is even. Since
odd := not even, "2 is not odd" literally reads "2 is not not even",
which double negation collapses to "2 is even" — already verified.
No theorem needed.

**2 is prime.** Definition (repaired live — see below): n is prime iff
n > 1 and every integer k ≥ 1 with k | n satisfies k = 1 or k = n.
Then 2 > 1, and the positive divisors split into cases:

- k = 1: 2 = 2 · 1 ✓ (allowed by the disjunct k = 1)
- k = 2: 2 = 1 · 2 ✓ (allowed by k = n)
- k > 2: if 2 = k · m, then m ≥ 1 forces km ≥ k > 2 and m ≤ 0 forces
  km ≤ 0 — both clash with km = 2. So no such divisor (the same
  trap-the-multiplier argument as [0010](0010-no-integer-both-even-and-odd.md),
  no division used).

Exhaustiveness of {1, 2, > 2} over k ≥ 1 quietly uses a **shifted gap**
(no integer strictly between 1 and 2) — a theorem-cousin of the gap
axiom. ∎

## Two potholes hit on the way

- **The definition of prime needs positive divisors.** The first
  attempt quantified over all k ∈ ℤ; then k = −1 divides 2
  (2 = (−1)·(−2)) yet equals neither 1 nor 2, and the definition
  wrongly disqualifies 2. Restricting to k ≥ 1 is the repair.
- **Definitions decide what's free and what costs a theorem.** With
  odd := not even, "even ⇒ not odd" is free (double negation). Had odd
  been *defined* as "has the form 2k + 1", the same step would cost the
  at-most-one theorem ([0010](0010-no-integer-both-even-and-odd.md)) —
  whose real content is exactly what makes the two readings of "odd"
  interchangeable.

See [notes/disproof.md](../notes/disproof.md).
