# Verify in 60 seconds (Local)

Obiettivo: verificare un payload con confronto deterministico.

## Step 1 — Scarica il repository
Opzione A: GitHub “Code → Download ZIP”
Opzione B: git clone (se usi git)

## Step 2 — Calcola sha256 del payload
Payload:
engineering/sample-payload/payload.txt

Su Linux/macOS:
- sha256sum engineering/sample-payload/payload.txt

Su Windows (PowerShell):
- Get-FileHash engineering/sample-payload/payload.txt -Algorithm SHA256

## Step 3 — Confronta con manifest
Manifest:
engineering/manifest/manifest.json

Regola:
sha256(payload) MUST equal manifest.payload.sha256

## Step 4 — Esito
- Se combacia → PASS
- Se non combacia → BLOCK (fail-closed)

## Test rapido (tamper test)
Modifica una lettera nel payload.
Ricalcola sha256.
Deve risultare diverso e quindi esito = BLOCK.
