# STATE ZERO — Origine del sistema

Questo documento segna lo stato iniziale verificabile del sistema.

Da questo punto ogni modifica è tracciabile nel tempo.

## Data di origine

Stato zero attivato pubblicamente.  
Il repository diventa osservabile nel tempo.

## Componenti attivi

Payload verificabile  
engineering/sample-payload/payload.txt

Manifest pubblico  
engineering/manifest/manifest.json

Guida verifica  
engineering/verify/verify-in-60s.md

Ambiente di test  
engineering/attack-test/try-to-break-it.md

## Regola

sha256(payload) deve coincidere con il manifest.  
Se non coincide → BLOCCO.

## Significato

Questo è il punto di origine tecnico.  
Non richiede fiducia.  
Può essere verificato da chiunque.

## Stato

Sistema: attivo  
Verifica: pubblica  
Tempo: iniziato
