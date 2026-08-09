# 0008 — n² + n is always even

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md)
Status: **solved** (session [0005](../sessions/0005-2026-08-09.md))

## Problem

Prove: for every integer n, n² + n is even.

## Student's proof (by cases — produced before the technique was named)

Two lemmas first:

> **Lemma A** (= [exercise 0003](0003-sum-of-two-evens.md)): even + even
> is even. Choose k, t with x = 2k, y = 2t; x + y = 2(k + t). ∎
>
> **Lemma B**: odd + odd is even. Choose k, t with x = 2k + 1,
> y = 2t + 1; x + y = 2(k + t + 1). ∎

Then the case split:

> 1. n is either even or odd — licensed by the
>    [dichotomy theorem](../notes/even-odd-dichotomy.md).
> 2. Case n even: n² = n·n is even (twice the integer k·n where n = 2k),
>    and even + even is even by Lemma A.
> 3. Case n odd: ¬(n even) ⇒ ¬(n² even) — the **contrapositive** of
>    [0006](0006-square-even-implies-even.md) (n² even ⇒ n even) — so n²
>    is odd, and odd + odd is even by Lemma B. ∎

## What the exercise surfaced

- The case split's exhaustiveness (line 1) and Lemma B's choose
  (odd ⇒ 2t + 1 form) both lean on the same theorem — every integer is
  2k or 2k + 1 — which was then proven from well-ordering plus the gap
  axiom: [notes/even-odd-dichotomy.md](../notes/even-odd-dichotomy.md).
- Line 3's middle arrow ran a lemma *in contrapositive form*; the
  license (equivalence with 0006) was produced on prompt.
- Both obligations of a cases proof made explicit:
  [notes/proof-by-cases.md](../notes/proof-by-cases.md).
