# The algebra of logic (propositional identities)

Written after session [0004](../sessions/0004-2026-08-05.md).
Related: [negating-statements.md](negating-statements.md) (quantifier
layer), [contrapositive.md](contrapositive.md),
[proof-by-contradiction.md](proof-by-contradiction.md).

## Two ways to prove an equivalence

- **Truth table**: brute force, check every row. The ground truth.
- **Algebraic**: rewrite one formula into the other by chaining known
  identities — like transforming x² − 1 into (x − 1)(x + 1) without
  plugging in numbers. Every identity used is itself a *cached truth
  table*: verified by rows once, reused forever.

An **identity** is an equivalence true for *all* values of its letters —
the logical counterpart of (x + y)² = x² + 2xy + y². That is what makes
substitution legal: the letters are placeholders, and compound formulas
may be slotted in (A := ¬P is fine), exactly as x may stand for (a − b).

## The toolkit (each verified by hand, sessions 0001–0004)

- **The implication identity**: P ⇒ Q ≡ ¬P ∨ Q
  (`P \Rightarrow Q \equiv \neg P \lor Q`) — an implication is a
  disjunction in disguise: "either P fails, or Q holds". Derived in
  session 0004 from the table via (P ∧ Q) ∨ ¬P, compressed by
  distributivity.
- **De Morgan**: ¬(A ∨ B) ≡ ¬A ∧ ¬B and ¬(A ∧ B) ≡ ¬A ∨ ¬B — ¬ swaps
  ∨ ↔ ∧ and hits each side.
- **Double negation**: ¬¬A ≡ A.
- **Commutativity / distributivity** of ∨ and ∧, as in arithmetic
  (∨ distributes over ∧ and vice versa).

Worked results:

- Contrapositive equivalence, algebraically:
  ¬Q ⇒ ¬P ≡ ¬¬Q ∨ ¬P ≡ Q ∨ ¬P ≡ ¬P ∨ Q ≡ P ⇒ Q. No rows checked.
- **Negation of an implication**:
  ¬(P ⇒ Q) ≡ ¬(¬P ∨ Q) ≡ P ∧ ¬Q — an *and*, not an implication: the
  certificate that the condition held and the promise failed.

## The four forms of an implication

| name | form | equivalent to |
|---|---|---|
| original | P ⇒ Q | contrapositive |
| contrapositive | ¬Q ⇒ ¬P | original |
| converse | Q ⇒ P | inverse |
| inverse | ¬P ⇒ ¬Q | converse |

Trap met in session 0004: negating both sides of an implication in place
builds the **inverse**, not the negation — it does not flip truth (it is
the converse in disguise: ¬P ⇒ ¬Q ≡ P ∨ ¬Q ≡ Q ⇒ P). The honest
negation is P ∧ ¬Q, computed above. Corollary: the contrapositive of an
⇔ is the same ⇔ — flipping a definition can never produce a new attack.

## What it all rests on (three commitments)

1. **Bivalence** — every statement is true or false, exactly one.
2. **Connectives are defined by their tables** — the table for ∨ is not
   a theorem but the contract for the symbol; likewise ¬, ∧, ⇒.
3. **Compositionality** — a compound's truth value depends only on its
   parts' truth values, never their subject matter. This is why a
   four-row check is a *complete* proof.

(There is also a purely syntactic road — axiom schemes plus modus ponens,
no truth mentioned — certifying exactly the same formulas, by the
completeness theorem. Deliberately not our road for now.)
