# Proof Pack — Stato verificabile

Questo repository espone un set minimo verificabile nel tempo.

Può essere scaricato, archiviato e confrontato in futuro.

## Contenuto del proof pack

Payload verificabile  
engineering/sample-payload/payload.txt

Manifest pubblico  
engineering/manifest/manifest.json

Guida verifica  
engineering/verify/verify-in-60s.md

Test di modifica  
engineering/attack-test/try-to-break-it.md

## Regola

sha256(payload) deve coincidere con il manifest.  
Se non coincide → BLOCCO.

## Uso

Puoi:
- scaricare l’intero repository
- archiviare questo stato
- verificare tra anni la coerenza

## Scopo

Non dimostrare oggi.  
Dimostrare nel tempo.

Se tra anni il sistema sarà ancora coerente,
questo proof pack ne sarà la prova.
