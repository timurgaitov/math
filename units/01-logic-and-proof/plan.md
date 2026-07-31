# Unit 1 — Logic and the language of proof

Part of the [curriculum](../../curriculum.md). Method: [METHOD.md](../../METHOD.md).

## Goal

Rebuild fluency in the raw material of proofs: what a mathematical statement
is, how quantifiers and implication really work, and how to negate things
correctly. By the end, the student should read a statement like
"for every ε > 0 there exists δ > 0 such that …" and know exactly what would
prove it and what would refute it.

## First session: diagnostic

Start with a short conversation to find the real starting level. Probe with
questions like:

- What is the negation of "every prime greater than 2 is odd"?
- Is "if 1 = 2, then 5 is prime" true or false, and why?
- What's the difference between "∀x ∃y: y > x" and "∃y ∀x: y > x"?

Adjust the pace based on what comes back.

## Topics

- [ ] Statements vs. non-statements; truth values
- [x] Logical connectives: and, or, not, implies, iff — implication's truth
      table and why vacuous truth makes sense (verified in diagnostic)
- [x] Quantifiers ∀ and ∃; order of quantifiers and why it matters
      (verified in diagnostic)
- [x] Negating statements mechanically (De Morgan, negating quantifiers,
      negating implication) — session 0001; retest cold before closing unit
- [ ] What counts as a proof; proving vs. refuting; the role of
      counterexamples (largely covered in session 0001 via refutation and
      the 1/n < ε proof; revisit alongside remaining proofs)
- [ ] Reading and unpacking a definition (using divisibility and evenness as
      the running examples)

## Done when

- Student can negate any quantified statement correctly without hesitation.
- Student can state, for a given claim, what a proof would need to show and
  what a counterexample would look like.
- Student has written 2–3 short proofs of trivial claims (e.g. sum of two even
  numbers is even) with correct logical structure.

## Companion reading (optional)

Book of Proof, Chapter 2 (Logic); §1.1 for set notation as it comes up.
See [curriculum.md](../../curriculum.md) for the book link and full mapping.

Notes produced by this unit go in `notes/` (e.g. `notes/implication.md`,
`notes/quantifiers.md`). Exercises in `exercises/`.
