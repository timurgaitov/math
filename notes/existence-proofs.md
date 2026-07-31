# Proving ∀ and ∃ statements; proof exposition

Written after session [0001](../sessions/0001-2026-07-31.md).

## What each quantifier obligates

- Proving **∀x: ...** in prose: "let x be arbitrary" — whatever is then
  established holds for all x. A proof for one specific value (ε = 0.003)
  proves only that instance, not the ∀.
- Proving **∃x: ...**: exhibit a witness and verify it works. Two valid
  witness styles:
  - **Constructive formula**: e.g. n = floor(1/ε) + 1 — concrete,
    checkable.
  - **Cited existence**: "by the Archimedean property choose n > 1/ε" —
    an ∃ needs a guarantee, not a formula.
- Refuting is proving the negation — see
  [negating-statements.md](negating-statements.md).

## Discovery runs backwards; proofs verify forwards

Scratch work starts from the goal and solves it (want 1/n < ε; flip to
n > 1/ε; reach for floor). The written proof is a **verification**, not a
diary — it may open with an unmotivated witness ("rabbit out of the hat")
and that is fully legitimate.

Two honest expositions:

- **Rabbit first**: define the witness, claim it works, derive the goal
  through a forward-justified chain. The goal appears only at the *end*
  of the chain.
- **Reduce first**: "it suffices to show X" (meaning: X ⟹ goal, so only
  X is owed), then prove X forward. This matches the discovery order, so
  the witness arrives already motivated.

What is *not* fine: operating on the goal as if it were available
("flip the initial inequality, so we get..."). The reader cannot tell
assumption from aim.

## Bookkeeping rules that bit during session 1

- Every object is introduced before it is mentioned; "defined" may happen
  mid-proof, at the moment the need is visible, but never after use.
- Multiplying an inequality or taking reciprocals needs **positivity**,
  not just "nonzero" — negative factors flip the direction.
- Floor's defining property: floor(r) ≤ r < floor(r) + 1. In particular
  floor(r) + 1 > r, and floor(r) is *not* ≥ r.
