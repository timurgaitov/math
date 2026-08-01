# Direct proof

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md).
Related: [reading-definitions.md](reading-definitions.md),
[contrapositive.md](contrapositive.md).

## The logical skeleton

To prove ∀x ∈ S (`\forall x \in S`): P(x) ⇒ Q(x) (`\Rightarrow`):

1. Let x ∈ S be arbitrary.
2. Assume P(x).
3. Derive Q(x).
4. Conclude: since x was arbitrary, the claim holds for all x ∈ S.

That is all direct proof is, logically. Two rules the skeleton enforces:

- **Arbitrary means arbitrary.** The proof may use nothing about x beyond
  membership in S and what P grants. Any extra fact ("say x = 6", a silent
  x > 0) forfeits the ∀.
- **Q is a target, never a fact.** The goal sits on the far side as the
  thing to reach; it may not enter the pile of usable facts. Reflex worth
  building: every equation written must be licensed by a numbered line
  above it.

## The working skeleton

Step 3 is a black box; in practice, with definitions built on ∃
(`\exists`) — even, divisible — it opens into:

- 3a. **Unpack** each assumption by its definition — the **choose** idiom:
  each ∃-fact hands over a witness with a name.
- 3b. **Compute** with the witnesses.
- 3c. **Deliver** the goal by its definition — the **exhibit** idiom:
  produce the goal's witness and verify it, including membership (k ∈ ℤ,
  by closure of ℤ under + and ·).

Choose/exhibit are not part of direct proof itself; they are what happens
when direct proof meets ∃-shaped definitions. Both idioms:
[reading-definitions.md](reading-definitions.md).

## Skeleton-first discipline

Write the setup and the final obligation *before* any algebra: arbitrary
objects, assumptions unpacked, and precisely what exhibit will demand at
the end. At that point the proof is "set up" — anyone reading knows exactly
what remains. Done this way in [exercise 0005](../exercises/0005-divisibility-of-sum.md).

## Related exercises

- [0005 — divisibility of a sum](../exercises/0005-divisibility-of-sum.md)
- Earlier proofs with the same (then-unnamed) skeleton:
  [0003](../exercises/0003-sum-of-two-evens.md),
  [0004](../exercises/0004-divisibility-transitive.md)
