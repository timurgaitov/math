# Negating quantified statements

Written after session [0001](../sessions/0001-2026-07-31.md).

## The rules

- ¬(∀x: P(x) → Q(x)) = ∃x: P(x) ∧ ¬Q(x)
- ¬(∃x: P(x) ∧ Q(x)) = ∀x: P(x) → ¬Q(x)
- Quantifier flips (∀ ↔ ∃), connective swaps (→ ↔ ∧), inner statement
  gets negated. Apply outside-in, one layer at a time, treating the inner
  part as an opaque block.

Example: ¬(∀ε > 0 ∃n ∈ ℕ: 1/n < ε) = ∃ε > 0 ∀n ∈ ℕ: 1/n ≥ ε.

## The pairing, and why it makes sense

- **∀ travels with →**: "every prime > 2 is odd" walks through all x;
  objects failing the hypothesis get a free pass (vacuous truth), a real
  demand appears only where P holds.
- **∃ travels with ∧**: a witness must fully qualify — both conjuncts,
  no free passes.
- Mismatches break: ∃ with → is nearly free to satisfy (any x failing P
  is a vacuous witness); ∀ with ∧ demands everything of everything
  ("all x are prime and odd" — never what was meant).
- The negation swap in one sentence: "not everyone passed the test" =
  "someone qualified for the test and failed it."

## Filter vs. demand

In ∀x: P → Q, the hypothesis P is a **filter**: it selects which objects
the statement talks about; failing P can never hurt the statement.
In ∃x: P ∧ Q, P is a **demand** on the witness. Same P, opposite role;
the quantifier decides which.

Bounded quantifiers are filters in shorthand: "∀ε > 0: S" unpacks to
"∀ε: ε > 0 → S". Under negation a bound **survives unchanged but changes
jobs** — filter becomes demand on the witness, or back:
¬(∀ε: ε > 0 → S) = ∃ε: ε > 0 ∧ ¬S. Dropping the bound instead changes
the statement (∀ε ∃n: 1/n < ε is false — take ε = −1).

## Smell tests for a candidate negation

- A statement and its negation have opposite truth values, always.
- The negation talks about the *same* objects, claiming the opposite
  about at least one — never about objects the original ignored.
- Refuting "∀x: P → Q" requires exactly one exhibit: an x with P and
  not-Q. If the candidate negation demands more (or different) evidence,
  it is wrong.
- Small finite worlds kill bad rules fast: "every element of {3, 5, 8}
  is odd" is false, so its negation must be true — test the candidate.
