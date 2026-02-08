# Try to break the system

This repository exposes a minimal deterministic verification model.

You are invited to test its robustness.

## Test 1 — Modify payload
Open:
engineering/sample-payload/payload.txt

Change one character.

Compute sha256 again.

Expected result:
hash no longer matches manifest → BLOCK

## Test 2 — Attempt silent modification
Modify payload without updating manifest.

Expected result:
verification fails.

## Test 3 — Attempt manifest forgery
Change manifest sha256.

Meaning:
you created a new state.
In a real anchored system this leaves trace and requires new verification state.

## Core rule
If mismatch is not detected → system is broken.
If mismatch is detected → system is coherent.

## Purpose
This repository demonstrates deterministic verification without authority trust.
