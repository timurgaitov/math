# The even/odd dichotomy

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md).
Related: [proof-by-cases.md](proof-by-cases.md),
[proof-by-contradiction.md](proof-by-contradiction.md),
[reading-definitions.md](reading-definitions.md).

## Definitions

- n is **even** iff n = 2k for some integer k (session 0002).
- n is **odd** iff n is *not* even — pinned in session 0005, after
  noticing "odd" had been used all course without a definition.
  The familiar 2k + 1 form is then a *theorem* (below), not the
  definition.

## Theorem (dichotomy)

> Every integer n is 2k or 2k + 1 for some integer k.

Consequences: "even or odd" case splits are exhaustive, and
odd ⇒ 2k + 1 form (not even rules out 2k, leaving 2k + 1).
The exclusivity half — no integer has both forms — is
[exercise 0010](../exercises/0010-no-integer-both-even-and-odd.md),
still open.

## Proof (session 0005, built live)

**Case n ≥ 0.** Let S = { n − 2k : k ∈ ℤ, n − 2k ≥ 0 }
(`S = \{\, n - 2k : k \in \mathbb{Z},\ n - 2k \ge 0 \,\}`).

1. S is nonempty: k = 0 puts n itself in S. (First attempt claimed
   0 ∈ S — false for odd n; the witness must work for *every* n.)
2. S has a least element r: if 0 ∈ S it is least outright (nothing
   nonnegative is smaller); otherwise S consists of positive integers
   and **well-ordering** applies. (The scope patch matters:
   well-ordering as stated covers positive integers, and S can
   contain 0.)
3. r < 2, by contradiction: if r ≥ 2 then u = r − 2 = n − 2(k + 1)
   has the membership form, and u ≥ 0 from r ≥ 2 — so u ∈ S and
   u < r, contradicting leastness.
4. 0 ≤ r < 2 forces r ∈ {0, 1}: r > 0 gives r ≥ 1 by the **gap
   axiom** (below); r between 1 and 2 is excluded by the shifted gap
   (subtract 1 to land an integer in (0, 1)).
5. Translate: r = n − 2k, so n = 2k (r = 0) or n = 2k + 1 (r = 1). ∎

**Case n < 0**, by *borrowing the proven half*: −n > 0, so
−n = 2k or 2k + 1; solving, n = 2(−k) or n = 2(−k − 1) + 1. Two lines
instead of a second descent — "reduce to the case already proven",
the same instinct behind WLOG.

## The gap axiom, and what "bedrock" means

> **Gap axiom.** There is no integer m with 0 < m < 1.

Every proof chain bottoms out somewhere; this course's ground floor for
the integers is: arithmetic closure (+, −, ×), order behavior,
well-ordering, and this one gap. All other gaps are one-step theorems:
an integer in (n, n + 1) minus n would be an integer in (0, 1).

In a foundations course the gap fact is itself a theorem: ℕ is built
from the Peano axioms, and induction proves "every natural number is 0
or ≥ 1". The axiom doing the work there is *induction* — well-ordering
in different clothes (Unit 2's last topic). Technique first, foundations
later, is the deliberate order: foundations *are* proofs, and proving
them takes the very skills being trained here.

## Related exercises

- [0008 — n² + n is even](../exercises/0008-parity-of-n-squared-plus-n.md)
  (dichotomy licenses the case split)
- [0009 — odd sum, exactly one odd](../exercises/0009-odd-sum-exactly-one-odd.md)
- [0010 — exclusivity](../exercises/0010-no-integer-both-even-and-odd.md)
  (open)
