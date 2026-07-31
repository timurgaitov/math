# 0001 — Negation drills

Unit: [01 — Logic and the language of proof](../units/01-logic-and-proof/plan.md)
Status: **solved** (session [0001](../sessions/0001-2026-07-31.md))

## Problems

1. Negate: "every prime greater than 2 is odd."
2. Negate: ∀x ∃y: y > x (over ℤ), and verify the negation is false.
3. Negate, in words and symbols: "for every ε > 0 there exists n ∈ ℕ such
   that 1/n < ε." Watch what happens to the bounds "ε > 0" and "n ∈ ℕ".

## Solutions (student's)

1. ∃x: x is prime ∧ x > 2 ∧ x is not odd — "there exists a prime greater
   than 2 that is not odd."
2. ∃x ∀y: y ≤ x. False: against any candidate x, the witness y = x + 1
   defeats it.
3. ∃ε > 0 ∀n ∈ ℕ: 1/n ≥ ε. Derived by unpacking the bound:
   ¬(∀ε: ε > 0 → S(ε)) = ∃ε: ε > 0 ∧ ¬S(ε), then
   ¬(∃n ∈ ℕ: 1/n < ε) = ∀n ∈ ℕ: 1/n ≥ ε. Both bounds survive unchanged,
   swapping roles (filter ↔ demand).

## Errors made on the way (worth re-testing later)

- First negation attempt kept the ∀ and the implication and negated pieces
  inside: "if x is not prime or x ≤ 2 then it is not odd." Diagnosed via:
  a negation must talk about the *same* objects and have opposite truth
  value; refuting a universal needs one exhibit, not a new rule.
- Second attempt: "every prime > 2 is not odd" (kept ∀, negated only Q).
  Killed by the finite test case {3, 5, 8}: statement and candidate
  negation both came out false.
- Third attempt: ∃x: P(x) → ¬Q(x) (kept → under ∃). Killed by vacuous
  truth: x = 4 witnesses it trivially, so it fails to be false when the
  original is true.

See [notes/negating-statements.md](../notes/negating-statements.md).
