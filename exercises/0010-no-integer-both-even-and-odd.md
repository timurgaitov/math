# 0010 — no integer is both even and odd

Unit: [02 — Proof techniques](../units/02-proof-techniques/plan.md)
Status: **open**

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
