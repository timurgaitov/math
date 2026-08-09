# 0007 — √2 is irrational

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md)
Status: **solved** (session [0004](../sessions/0004-2026-08-05.md))

## Problem

Prove: √2 ∉ ℚ (`\sqrt{2} \notin \mathbb{Q}`) — there are no n, m ∈ ℤ,
m ≠ 0, with √2 = n/m.

## Why the old skeletons jam (worked through first, on purpose)

The statement is a bare negation ¬S with S = "√2 ∈ ℚ" — no ∀x: P ⇒ Q at
top level, so contrapositive has nothing to flip (flipping the *definition*
of ℚ only hands the definition back — the contrapositive of an ⇔ is the
same ⇔). Unpacked, ¬S says ∀n, m ∈ ℤ, m ≠ 0: n ≠ m√2 — a direct setup
with an **empty given pile**: two arbitrary integers, an obligation, and
nothing to choose from. This wall is what motivates contradiction: assume
S itself and the pile fills instantly.

## Student's proof (by contradiction, infinite descent)

> Goal: √2 ∉ ℚ.
> 1. Assume the opposite: √2 ∈ ℚ.
> 2. By definition of ℚ (written without division), choose n, m ∈ ℤ,
>    m ≠ 0, such that m√2 = n.
> 3. Square both sides: 2m² = n².
> 4. n² equals twice the integer m², so n² is even by definition.
> 5. By [exercise 0006](0006-square-even-implies-even.md) (n² even ⇒
>    n even), n is even.
> 6. Since n is even, choose k ∈ ℤ with n = 2k.
> 7. Substitute: 2m² = 4k², so m² = 2k².
> 8. So m² is even, and by 0006 again, m is even.
> 9. Since m is even, choose t ∈ ℤ with m = 2t.
> 10. Substitute into line 2: √2·(2t) = 2k, so √2·t = k — the equation of
>     line 2 again, with the smaller pair (k, t). And t ≠ 0, since
>     m = 2t and m ≠ 0.
> 11. Steps 3–10 now apply verbatim to (k, t), and so on forever, halving
>     the (never-zero) denominator each round.
> 12. Track |m|: after i rounds the denominator is |m|/2ⁱ, and every term
>     must be a positive integer.
> 13. Eventually 2ⁱ > |m|, so 0 < |m|/2ⁱ < 1 — but there is no integer
>     strictly between 0 and 1. Contradiction.
> 14. Valid steps preserve truth, so a false conclusion means the pile
>     holds a falsehood; everything in the pile except the assumption is
>     previously established; therefore the assumption is the liar:
>     √2 ∉ ℚ. ∎

This is the **infinite descent** version. The textbook packaging below
(session [0005](../sessions/0005-2026-08-09.md)) is the same engine
pre-paid: well-ordering spent up front to strengthen the choose, so the
dividing-by-2 move runs once and crashes immediately, instead of forever.

## Lowest-terms packaging (session 0005)

The textbook opening "write √2 = a/b in lowest terms" is a
**strengthened choose**, unpacked live as:

1. Assume √2 ∈ ℚ; representations with positive a, b exist (flip both
   signs if needed). Form A = { a ∈ ℤ⁺ : √2 = a/b for some b ∈ ℤ⁺ } —
   nonempty under the assumption, so **well-ordering** hands a least
   numerator a, and its b comes along uniquely.
2. Least numerator ⇒ lowest terms, one step: a common divisor k > 1
   would give √2 = (a/k)/(b/k) with a/k < a in A — contradiction.
   (The k > 1 strictness is what makes a/k smaller.)

Then the proof, fully licensed:

> a² = 2b² ⇒ a² even ⇒ a even ([0006](0006-square-even-implies-even.md))
> ⇒ a = 2c ⇒ 4c² = 2b² ⇒ b² = 2c² ⇒ b even (0006 again)
> ⇒ 2 divides both a and b — but gcd(a, b) = 1 is in the pile. ∎

Notes from the live run:

- First assembly tried 2 = a²/b², gcd(a, b) = 1 ⇒ b = 1 — which leans
  on gcd(a, b) = 1 ⇒ gcd(a², b²) = 1, true but **unlicensed** (a real
  theorem, not bedrock). Rerouted through 0006 on prompt.
- The crash pair here is R ∧ ¬R with ¬R coming *from the pile itself*
  (gcd = 1), where the descent version crashed against a known truth —
  the two sources of ¬R, one proof each.

## What the exercise surfaced (for later recall)

- Opening line matters: first draft said "assume the statement is true"
  right after announcing the goal ¬S — literally assuming the goal. Fixed
  to "assume the opposite". The contradiction skeleton must *say* what is
  assumed and in what relation to the goal.
- Sign hole: the descent first tracked t with 0 < t/2ⁱ, but the pile only
  gives m ≠ 0 — m = −6 breaks it. Patched by tracking |t| (`|t|`,
  LaTeX `\lvert t \rvert`); the ≠ 0 part is licensed by m = 2t ∧ m ≠ 0
  ⇒ t ≠ 0, re-firing at every level of the descent.
- Mid-derivation an unlicensed "2t = k" appeared; asked which line
  licenses it, student re-derived and landed on the licensed 2t² = k².
  The licensing reflex works but still needs the prompt.
- Bedrock fact made explicit: no strictly decreasing sequence of positive
  integers is infinite (equivalent to the well-ordering principle); the
  final crash lands on "no integer strictly between 0 and 1".

See [notes/proof-by-contradiction.md](../notes/proof-by-contradiction.md).
