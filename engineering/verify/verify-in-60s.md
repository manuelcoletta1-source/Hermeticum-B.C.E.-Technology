# Verify in 60 seconds (deterministic)

## What to verify
- Payload: `engineering/sample-payload/payload.txt`
- Manifest: `engineering/manifest/manifest.json`

## Rule (fail-closed)
Computed sha256(payload) must match manifest sha256.
Mismatch → BLOCK.

## How to compute sha256 (examples)
- Linux/macOS: `sha256sum engineering/sample-payload/payload.txt`
- Windows PowerShell: `Get-FileHash engineering/sample-payload/payload.txt -Algorithm SHA256`

## Tamper test
Change one character in payload, recompute sha256:
- sha256 must change
- if manifest unchanged → BLOCK
