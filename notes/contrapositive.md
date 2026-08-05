# Contrapositive

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md).
Related: [direct-proof.md](direct-proof.md),
[negating-statements.md](negating-statements.md),
[proof-by-contradiction.md](proof-by-contradiction.md),
[logic-identities.md](logic-identities.md).

## The rule

¬Q ⇒ ¬P (`\neg Q \Rightarrow \neg P`) is *the same statement* as P ⇒ Q —
proving one proves the other.

Verified by truth table (filled in by hand, session 0003): the columns for
P ⇒ Q and ¬Q ⇒ ¬P agree in all four rows. The only row where either can
fail is P true, Q false — both implications forbid exactly that one
situation.

The quantifier stays put: the contrapositive of ∀n: P(n) ⇒ Q(n) is
∀n: ¬Q(n) ⇒ ¬P(n). The flip happens inside the ∀, not to it.

## When it lights up

Look at where each version puts the raw material. Direct proof hands you P;
contrapositive hands you ¬Q. If P gives awkward material (facts about a
composite object like n²) while the obligation sits on the simple object
(n), the computation runs downhill — and algebra with + and · only builds
upward. If ¬Q gives material on the simple object, the contrapositive turns
the proof uphill.

Classic case, worked in [exercise 0006](../exercises/0006-square-even-implies-even.md):
"n² even ⇒ n even" is stuck directly; "n odd ⇒ n² odd" is a routine direct
proof.

## Negation may need a positive form

Negating an ∃-definition yields a ∀-fact: "n not even" is literally
∀k ∈ ℤ: n ≠ 2k — a fence with no witness, nothing to choose. Trade it for
an ∃-fact via the parity fact:

> Every integer is even or odd, never both, where
> n is odd ⇔ ∃k ∈ ℤ: n = 2k + 1.

(The dichotomy is a theorem — it follows from division with remainder,
to be met properly later; taken as given for now.)

General lesson: negations produce ∀-fences; definitions like "odd" restore
∃-material the choose idiom can feed on.

## Related exercises

- [0006 — if n² is even then n is even](../exercises/0006-square-even-implies-even.md)
