# Standards (outputs)

## Output minimi
- `ipr.canon.json` (canonicalizzato)
- digest `SHA-512`
- `receipt.json` (firma ED25519 su digest)
- `PACK_MANIFEST.json` (indice del pacchetto)
- `FREEZE.md` (append-only, se applicabile)

## Vincoli
- hash-only (nessun documento)
- offline verifiable
- fail-closed (mismatch ⇒ invalid)
