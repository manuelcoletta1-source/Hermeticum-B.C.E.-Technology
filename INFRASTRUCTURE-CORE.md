# HERMETICUM B.C.E. — Infrastructure Core

Questo repository costituisce il nucleo iniziale di una infrastruttura tecnica verificabile.

Non è una demo.  
È una base operativa osservabile.

## Funzione

Fornire un ambiente in cui:

- l’integrità è verificabile
- le modifiche sono rilevabili
- la validità è matematica
- l’audit è pubblico

## Componenti

Payload verificabile  
engineering/sample-payload/payload.txt

Manifest pubblico  
engineering/manifest/manifest.json

Regola di validità  
sha256(payload) = manifest

Guida verifica  
engineering/verify/verify-in-60s.md

## Principio operativo

Se una modifica non viene rilevata → il sistema fallisce.  
Se ogni modifica viene rilevata → il sistema è coerente.

## Stato

Nucleo infrastrutturale: attivo  
Verifica pubblica: attiva  
Evoluzione: append-only  

## Direzione

Questo nucleo è progettato per evolvere in:

- infrastruttura di identità verificabile
- sistemi AI auditabili
- ambienti robotici con identità
- infrastrutture europee verificabili
