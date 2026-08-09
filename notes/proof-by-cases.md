# Proof by cases (and WLOG)

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md).
Related: [direct-proof.md](direct-proof.md),
[even-odd-dichotomy.md](even-odd-dichotomy.md),
[logic-identities.md](logic-identities.md).

## The skeleton

To prove a statement G:

1. Split the situation into cases C₁, C₂, … (`C_1, C_2, \dots`).
2. Inside each case, add Cᵢ to the given pile and prove G.
3. Conclude G outright.

## The two obligations

1. **Every case closes the goal.** No case may end on something merely
   *related* to G — each one ends on G itself.
2. **The split is exhaustive, and exhaustiveness is a claim needing its
   own license.** "n is even or odd" is not free; it is the
   [dichotomy theorem](even-odd-dichotomy.md). If some object escapes
   every case, the proof says nothing about it.

Where exhaustiveness licenses come from:

- A **theorem** — dichotomy for parity splits; splitting on x, y jointly
  applies it twice (2 × 2 = 4 cases).
- The **hypothesis itself** — if the given pile holds A ∨ B (`A \lor B`),
  the cases A and B are exhaustive by the meaning of ∨. Contraposing
  [0009](../exercises/0009-odd-sum-exactly-one-odd.md) turned a
  dichotomy-licensed 4-way split into a hypothesis-licensed 2-way one.

## Vacuous cases

A case may falsify the hypothesis of the goal instead of reaching its
conclusion: proving "x + y even" when the goal is "x + y odd ⇒ …"
closes the case by **vacuous truth** — an implication with a false
hypothesis is true (both F-rows of the ⇒ table), with nothing to show.
A legitimate close, but a hint the proof might contrapose into a shape
with no dead cases.

## WLOG — "without loss of generality"

Used when two cases are mirror images: prove one, claim the other
follows "by symmetry". The claim carries an obligation:

> **WLOG's obligation.** The transformation carrying the missing case
> into the proven one must leave the statement unchanged — and that
> invariance must be checked, not waved at.

The mechanism, precisely (from
[0009](../exercises/0009-odd-sum-exactly-one-odd.md)): the proven case
is a universally quantified lemma L; the missing case is L
*instantiated with the variables swapped*; the check is that the
swapped conclusion is syntactically the goal — there via commutativity
of + and of the connectives.

**Failure mode**: writing WLOG when the variables play asymmetric roles
(e.g. anything involving x < y or x − y). "Arbitrary variables" is not
the license — every ∀-claim has arbitrary variables. Invariance under
the specific swap is.
