# Disproof — a counterexample is a proof

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md).
Related: [logic-identities.md](logic-identities.md),
[proof-by-cases.md](proof-by-cases.md).

## The concept

A false claim is *disproven*, not merely doubted — and "false" is
proven with the same rigor as "true". A disproof of a claim S is a
proof of ¬S. A counterexample is not "evidence against"; it is the
core of that proof.

## The skeleton

1. **Compute the negation honestly.** Push ¬ through the quantifiers
   and connectives with the identities already in the toolbox:
   - ¬∀n P(n) ≡ ∃n ¬P(n) (`\neg\forall n\,P(n) \equiv \exists n\,\neg P(n)`)
     — De Morgan for quantifiers; the domain restriction travels along
     unchanged.
   - ¬(P ⇒ Q) ≡ P ∧ ¬Q — so a counterexample to an implication must
     make the hypothesis **true** and the conclusion **false**. An
     object that fails the hypothesis disproves nothing.
2. **Exhibit a witness.**
3. **Verify the witness.** Every property claimed of it gets a license
   — no plausible-looking unchecked witnesses. Verifying may itself
   take real work (in [0012](../exercises/0012-primes-not-all-odd.md),
   "2 is prime" needed a case analysis).

## The quantifier asymmetry

| | prove | refute |
|---|---|---|
| ∀n P(n) | argument for arbitrary n | one verified witness |
| ∃n P(n) | one verified witness | argument for arbitrary n |

Refuting one quantifier is proving the other applied to ¬P — the table
is De Morgan in disguise.

## Finite checking proves nothing about ∀

Checking finitely many instances of an infinite ∀-claim is a proof by
cases with **no exhaustiveness license** — it proves a theorem about
the checked set only. Cautionary example: Euler's polynomial
n² + n + 41 is prime for every n from 0 to 39 and composite at n = 41
([0011](../exercises/0011-euler-polynomial-counterexample.md)). Forty
confirmations, false claim.
