# Statements vs. open sentences

Unit: [01 — Logic and the language of proof](../units/01-logic-and-proof/plan.md).
Related: [negating-statements.md](negating-statements.md).

## Definition

A **statement** is a sentence that is definitely true or definitely false —
even if nobody currently knows which. An **open sentence** contains a free
variable, so its truth depends on the variable's value; it becomes a
statement once every variable is bound (by a quantifier) or fixed.

## The idea in one's own words

- "x + 1 = 3" — open sentence: x is free. Being an equation is not the
  problem; "∀x ∈ ℤ (`\forall`): x + 1 = 3" contains the same equation and
  *is* a statement (a false one, witness x = 0).
- "Every even number > 2 is the sum of two primes" — statement. Nobody
  knows its truth value (Goldbach), but it has one.
- Questions and commands are not statements.
- Vague sentences ("n! grows very fast") are not statements: no threshold,
  no truth value. Much of what definitions do is turn vague claims into
  statements — e.g. "∀n ≥ 4: n! > 2ⁿ" is a precise (true) neighbor of the
  vague one.

## Worked example

Session [0002](../sessions/0002-2026-07-31.md) five-way check: the two
errors worth remembering were calling "x + 1 = 3" a non-statement *for the
wrong reason* ("it's an equation" — the real reason is the free variable)
and calling the vague "grows very fast" a checkable statement.

## Related exercises

- Quick five-item check in session [0002](../sessions/0002-2026-07-31.md);
  no separate exercise file.
