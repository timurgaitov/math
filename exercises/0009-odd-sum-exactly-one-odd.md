# 0009 — odd sum means exactly one odd summand

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md)
Status: **solved** (session [0005](../sessions/0005-2026-08-09.md))

## Problem

Prove: for any integers x, y — if x + y is odd, then exactly one of
x, y is odd.

## Direct route (set up first): four cases

Dichotomy applied to each of x and y licenses the split into
(even, even), (even, odd), (odd, even), (odd, odd).

- (even, even) and (odd, odd): the sum is even
  ([0003](0003-sum-of-two-evens.md) / Lemma B of
  [0008](0008-parity-of-n-squared-plus-n.md)), so the hypothesis
  "x + y odd" is *false* and the case closes by **vacuous truth** —
  an implication with a false hypothesis holds with nothing to show.
- (even, odd): x + y = 2k + 2t + 1 = 2(k + t) + 1, and the conclusion
  holds. (Caution: "2g + 1 is odd" = "2g + 1 is not even" still owes
  a license — [exercise 0010](0010-no-integer-both-even-and-odd.md).)
- (odd, even): follows from the previous case **WLOG** — see below.

## Student's improvement: contrapose first

Since odd := not even, double negation gives ¬(x + y odd) ≡ x + y even,
and ¬(exactly one of x, y odd) ≡ both odd or both even. So the
contrapositive of the claim is:

> x, y both even or both odd ⇒ x + y even

— exactly the two sum-lemmas already proven, and the case split is now
licensed by the **or in the hypothesis itself**, not by dichotomy. Two
cases instead of four, no vacuous cases, and the 2g + 1 debt never
arises. ∎

## The WLOG mechanism (worked through on the direct route)

The proven (even, odd) case is a lemma L: ∀x, y — x even ∧ y odd ⇒
(x + y odd ⇒ exactly one of x, y odd). Standing in the case x odd,
y even, instantiate L at (y, x): it hands back
"y + x odd ⇒ exactly one of y, x odd". Matching this against the goal
needs two checks: y + x = x + y (commutativity of +) and
"exactly one of y, x" ≡ "exactly one of x, y" (commutativity of the
connectives). Both hold, so the swap is licensed.
See [notes/proof-by-cases.md](../notes/proof-by-cases.md) for the
obligation in general and the failure mode.
