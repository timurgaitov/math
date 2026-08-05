# Proof by contradiction

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md).
Related: [contrapositive.md](contrapositive.md),
[logic-identities.md](logic-identities.md),
[direct-proof.md](direct-proof.md).

## The skeleton

To prove a statement T:

1. **Assume the opposite**: ¬T (`\neg T`) goes into the given pile as a
   usable fact.
2. Reason validly from the pile — every line licensed by a line above it,
   exactly as in a direct proof.
3. Arrive at an **absurdity**: a statement contradicting a known fact
   (or the pile itself).
4. Conclude T.

## Why step 4 is licensed (the "liar in the pile" argument)

Valid steps preserve truth: if everything in the pile were true, every
derived line would be true too. A false conclusion therefore means the
pile holds a falsehood. Everything in the pile except the assumption is a
previously established truth — so the assumption is the liar, and its
negation T holds.

Caution: this convicts the assumption only when it is the *sole*
unverified thing in the pile. With several unproven assumptions in play,
a contradiction only convicts *some* member — no telling which.

## Contradiction vs. contrapositive (unit checkbox)

Both proved on the same job, P ⇒ Q:

|  | contrapositive | contradiction |
|---|---|---|
| assumes | ¬Q | ¬(P ⇒ Q) ≡ P ∧ ¬Q — both conjuncts land in the pile |
| target | ¬P, a marked destination | *any* absurdity — no map |
| really is | a direct proof of the flipped implication | a march until something breaks |

- **More fuel, no map.** Contradiction hands strictly more assumptions
  (P and ¬Q vs. ¬Q alone) but names no destination; contrapositive knows
  exactly where it is going. ("Known truths" are in every pile — they are
  not the difference.)
- **Exclusive territory.** Contrapositive needs an arrow to flip.
  A bare negation like √2 ∉ ℚ has none — contradiction attacks it
  directly: assume √2 ∈ ℚ and the empty pile fills instantly.
- Terminology: the flip to ¬Q ⇒ ¬P is *contraposing*, not "inverting" —
  the inverse ¬P ⇒ ¬Q is a different (and inequivalent) statement; see
  [logic-identities.md](logic-identities.md).

## Infinite descent

The engine of [exercise 0007](../exercises/0007-sqrt2-irrational.md): the
assumption reproduces itself with strictly smaller positive-integer data,
forever — impossible, because

> **no strictly decreasing sequence of positive integers is infinite**

(each step drops by ≥ 1, so after k steps the term is ≤ a − k, eventually
below 1 — and there is no integer strictly between 0 and 1). Equivalent
to the **well-ordering principle**: every nonempty set of positive
integers has a least element.

## Related exercises

- [0007 — √2 is irrational](../exercises/0007-sqrt2-irrational.md)
