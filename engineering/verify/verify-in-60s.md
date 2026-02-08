# Verify in 60 seconds (deterministic)

This repo contains a minimal, engineer-facing proof:
**hash-only verification + fail-closed rule**.

## Files
- Payload: `engineering/sample-payload/payload.txt`
- Manifest: `engineering/manifest/manifest.json`

Manifest declares the expected sha256:

`563dec5f69b0a0c81714af2055f04b8b4870653e8a273254d35b19adf4755756`

## Verify (any OS)

### Option A — Linux / macOS
Compute:
`sha256sum engineering/sample-payload/payload.txt`

### Option B — Windows PowerShell
Compute:
`Get-FileHash engineering/sample-payload/payload.txt -Algorithm SHA256`

## Rule (fail-closed)
- If computed sha256 == manifest sha256 → **PASS**
- Else → **BLOCK**

## Tamper test
Change **one character** in `payload.txt` and recompute.
The sha256 must change. If manifest is unchanged, result must be **BLOCK**.
