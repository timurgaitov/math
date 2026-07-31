# Reading and using definitions

Unit: [01 — Logic and the language of proof](../units/01-logic-and-proof/plan.md).
Related: [existence-proofs.md](existence-proofs.md),
[negating-statements.md](negating-statements.md).

## Definitions

- **Divisibility**: a | b ⇔ ∃k ∈ ℤ (`\exists k \in \mathbb{Z}`): b = ka.
- **Evenness**: n is even ⇔ ∃k ∈ ℤ: n = 2k.

Both rest only on multiplication and one quantifier. A definition should be
built from things simpler than itself — "a | b ⇔ b mod a = 0" is a true fact
but not a good definition, because mod is itself defined on top of division.

## The idea in one's own words

A definition is used in two directions, and each direction has an idiom:

- **Entrance (assumption hands you a witness).** From "x is even" you may
  write: *since x is even, choose m ∈ ℤ with x = 2m.* The bare statement
  "∃m: x = 2m" is not a name; the **choose** step is what turns existence
  into a symbol you can compute with.
- **Exit (goal demands a witness).** To prove "S is even" you must
  *exhibit* a k and check both S = 2k **and** k ∈ ℤ — the witness must
  live in the right set.

Pitfall (made once, in [0003](../exercises/0003-sum-of-two-evens.md)):
unpacking the goal's definition in the "given" pile, i.e. writing
"∃k: 2k = S" next to the assumptions. The conclusion's witness may appear
only at the end, produced, not assumed.

The definition decides, not intuition:

- 5 | 0 — yes (k = 0). Anything divides 0.
- 0 | 5 — no (k·0 = 0 ≠ 5 for every k).
- 0 | 0 — **yes** (k = 0 works; any k does). Intuition shouts "division by
  zero," but the definition contains no division. An ∃ needs one witness;
  proving all k work is true here but more than asked.

## Worked examples

Sum of two evens is even
([exercise 0003](../exercises/0003-sum-of-two-evens.md)); divisibility is
transitive ([exercise 0004](../exercises/0004-divisibility-transitive.md)).
Both follow the same skeleton: arbitrary objects → choose witnesses from
assumptions → compute → exhibit the goal's witness → check it is in ℤ.

## Related exercises

- [0003 — sum of two evens](../exercises/0003-sum-of-two-evens.md)
- [0004 — divisibility is transitive](../exercises/0004-divisibility-transitive.md)
