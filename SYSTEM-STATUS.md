# Stato del sistema — HERMETICUM B.C.E.

Questo repository non è solo un progetto software.

È un ambiente tecnico pubblico verificabile.

## Principio

Un sistema è valido solo se verificabile in modo indipendente.

Se una modifica non viene rilevata → il sistema è rotto.  
Se ogni modifica viene rilevata → il sistema è coerente.

## Ambiente di prova attivo

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

## Stato attuale

Ambiente: attivo  
Verifica: pubblica  
Audit: aperto  
Osservazione: continua

## Significato

Questo repository è un sistema osservabile nel tempo.  
Non richiede fiducia.  
Richiede verifica.
