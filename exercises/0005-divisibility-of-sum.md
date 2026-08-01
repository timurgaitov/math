# 0005 — Divisibility of a sum

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md)
Status: **solved** (session [0003](../sessions/0003-2026-08-01.md))

## Problem

Prove: for all a, b, c ∈ ℤ, if a | b and a | c, then a | (b + c).

## Student's proof (final version)

Written skeleton-first: setup and final obligation stated before any algebra.

> Let a, b, c ∈ ℤ be arbitrary.
> Since a | b, choose m ∈ ℤ with b = ma.
> Since a | c, choose n ∈ ℤ with c = na.
> *(Obligation: exhibit k ∈ ℤ with b + c = ka.)*
> Then b + c = ma + na = (m + n)a.
> Take k = m + n; k ∈ ℤ since ℤ is closed under addition.
> So b + c = ka, hence a | (b + c) by definition.

## What the exercise surfaced (for later recall)

- First exercise done skeleton-first: assumptions unpacked and the exhibit
  obligation stated *before* computing. The discipline held — the goal never
  entered the given pile.
- Clean first attempt, closure line included unprompted.

See [notes/direct-proof.md](../notes/direct-proof.md).
