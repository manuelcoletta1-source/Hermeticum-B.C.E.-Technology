# Deterministic Proof — v1 (LOCKED)

This folder exposes a minimal deterministic verification proof.

## Proof set (v1)
- Payload: `engineering/sample-payload/payload.txt`
- Manifest: `engineering/manifest/manifest.json`
- Verify guide: `engineering/verify/verify-in-60s.md`
- Attack test: `engineering/attack-test/try-to-break-it.md`

## Expected behavior
Rule:
sha256(payload) MUST equal manifest sha256  
If mismatch → BLOCK (fail-closed)

## What you can test
1) Verify payload sha256 matches the manifest
2) Modify ONE character in payload and recompute
3) Observe mismatch and fail-closed behavior (BLOCK)

## Why this is engineering-grade
- independent verification (no authority trust)
- tamper-evidence by design
- low verification cost / high forgery cost
- append-only evolution via repo history

## Status
v1 proof set: ACTIVE  
verification: deterministic  
policy: HASH-ONLY | FAIL-CLOSED | AUDIT-FIRST | UE-FIRST
