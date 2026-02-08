# Verify in 60 seconds (Local)

Obiettivo: verificare un payload con confronto deterministico.

## Step 1 — Download
- GitHub: Code → Download ZIP
oppure
- git clone (se usi git)

## Step 2 — Compute sha256
Payload:
engineering/sample-payload/payload.txt

Linux/macOS:
sha256sum engineering/sample-payload/payload.txt

Windows PowerShell:
Get-FileHash engineering/sample-payload/payload.txt -Algorithm SHA256

## Step 3 — Compare with manifest
Manifest:
engineering/manifest/manifest.json

Regola:
sha256(payload) MUST equal manifest.payload.sha256

## Step 4 — Result
- match → PASS
- mismatch → BLOCK (fail-closed)

## Tamper test
Modifica 1 carattere nel payload e ricalcola sha256.
Deve risultare diverso.
Se il manifest non cambia: esito deve essere BLOCK.
