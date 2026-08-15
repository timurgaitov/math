# 0010 — no integer is both even and odd

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md)
Status: **solved** (session 0006)

## Problem

Prove: no integer is both even and odd.

## Context

The [dichotomy theorem](../notes/even-odd-dichotomy.md) says every
integer has *at least one* of the forms 2k, 2k + 1. This exercise is the
other half — *at most one*. Together they make "even or odd" an
exclusive or.

Note the definition in play: odd := not even, so the claim unpacks to
"no integer with the form 2k + 1 is even" — equivalently, 2k + 1 = 2t is
impossible. It surfaced in [0009](0009-odd-sum-exactly-one-odd.md),
where the direct route wrote "2g + 1 is odd by definition" — a step this
exercise licenses.

Expected engine: the same bedrock gap fact the dichotomy proof ends on.

## Solution (student's, session 0006)

Suppose for contradiction there exist k, t ∈ ℤ with 2k + 1 = 2t. Then
1 = 2(t − k). Let m = t − k; m ∈ ℤ since ℤ is closed under subtraction.
So 2m = 1.

- If m ≤ 0, then 2m ≤ 0, forcing 1 ≤ 0 — false.
- If m ≥ 1, then 2m ≥ 2, forcing 1 ≥ 2 — false.

So 0 < m < 1: an integer strictly inside (0, 1), contradicting the gap
axiom. Hence no such k, t exist. ∎

Notes from the live run: the first draft crashed into "1 is even, which
is absurd" — but "1 is not even" is an instance of this very theorem,
not a pile fact; the crash must land on named bedrock. Second draft
reached m = 1/2 by division, which ℤ doesn't have — replaced by the
two-sided order argument above. With the
[dichotomy theorem](../notes/even-odd-dichotomy.md), even/odd is now an
exclusive-or: every integer has exactly one of the forms 2k, 2k + 1.
