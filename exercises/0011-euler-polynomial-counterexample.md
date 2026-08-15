# 0011 — Euler's polynomial is not always prime

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md)
Status: **solved** (session [0006](../sessions/0006-2026-08-15.md))

## Problem

Prove or disprove: for every integer n ≥ 0, the number n² + n + 41 is
prime.

## Solution (student's, session 0006)

The claim is false. To disprove ∀n P(n) is to prove its negation, and
¬∀n P(n) ≡ ∃n ¬P(n) (`\neg\forall n\, P(n) \equiv \exists n\,\neg P(n)`,
De Morgan for quantifiers — the domain n ≥ 0 travels along unchanged):

> ∃n ≥ 0 such that n² + n + 41 is not prime.

Witness: n = 41. Verification:

41² + 41 + 41 = 41 · (41 + 1 + 1) = 41 · 43,

and 41 is a divisor strictly between 1 and 41 · 43, which is exactly
what "not prime" demands. ∎

(n = 40 also works: 40² + 40 + 41 = 40 · 41 + 41 = 41².)

## The lesson in the polynomial

This is Euler's famous prime-generating polynomial: for **every** n
from 0 to 39, n² + n + 41 really is prime — forty straight
confirmations, and the claim is still false. In proof-by-cases terms:
checking n = 0, …, 39 is a case proof whose split has **no
exhaustiveness license** over the infinite domain, so it proves only a
smaller theorem about {0, …, 39}.

The quantifier asymmetry, stated once:

- **∀**: proving takes an argument for arbitrary n; refuting takes one
  verified witness.
- **∃**: one verified witness proves it; refuting takes an
  arbitrary-n argument.

See [notes/disproof.md](../notes/disproof.md).
