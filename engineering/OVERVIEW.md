# Engineering Overview

This repository provides a deterministic, audit-first verification proof.

## What you can verify
- Payload: engineering/sample-payload/payload.txt
- Manifest: engineering/manifest/manifest.json
- Rule: mismatch → BLOCK (fail-closed)

## Minimal model
1) payload
2) sha256
3) manifest declares expected sha256
4) independent verification
5) fail-closed

## Why it matters
- No authority required for technical validity
- Verification cost is low; forgery cost is high
- Tampering is detectable by design

## Entry points
- Verify: engineering/verify/verify-in-60s.md
- Attack test: engineering/attack-test/try-to-break-it.md
- Architecture: engineering/architecture/system-model.md
