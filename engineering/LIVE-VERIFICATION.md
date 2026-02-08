# Ambiente di verifica pubblica

Questo repository è un ambiente di verifica deterministica aperto.

Chiunque può controllare in modo indipendente l’integrità del sistema.

## Set di prova attivo

Payload  
engineering/sample-payload/payload.txt

Manifest  
engineering/manifest/manifest.json

Guida verifica  
engineering/verify/verify-in-60s.md

Test di attacco  
engineering/attack-test/try-to-break-it.md

## Regola di validità

sha256(payload) deve coincidere con sha256 nel manifest.  
Se non coincide → BLOCCO (fail-closed)

## Cosa puoi fare

1. Verificare localmente l’integrità
2. Modificare il payload
3. Ricalcolare l’hash
4. Osservare il blocco del sistema

Se una modifica non viene rilevata → il sistema è rotto.  
Se ogni modifica viene rilevata → il modello è coerente.

## Stato

Ambiente: attivo  
Verifica: pubblica  
Politica: HASH-ONLY · FAIL-CLOSED · AUDIT-FIRST
