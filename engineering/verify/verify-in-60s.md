# Verify in 60 seconds (deterministic)

This repository exposes a minimal deterministic verification model.

## Payload
engineering/sample-payload/payload.txt

## Manifest
engineering/manifest/manifest.json

## Expected sha256
563dec5f69b0a0c81714af2055f04b8b4870653e8a273254d35b19adf4755756

## Verification rule
sha256(payload) MUST equal manifest sha256  
If not → BLOCK

## How to verify (any system)

Linux / macOS:
sha256sum engineering/sample-payload/payload.txt

Windows PowerShell:
Get-FileHash engineering/sample-payload/payload.txt -Algorithm SHA256

## Tamper test
Change ONE character in payload.
Recompute sha256.

Result must differ → verification must fail (BLOCK).
