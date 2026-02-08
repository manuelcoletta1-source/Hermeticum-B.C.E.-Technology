# Challenge — Prova a romperlo

Questo repository espone un modello di verifica deterministica (hash-only) con logica fail-closed.

Qui non ti chiediamo fiducia.
Ti chiediamo di verificare e, se vuoi, di provare a rompere.

## Obiettivo della challenge

Dimostrare una delle due cose:

1) Il sistema è incoerente (bug di governance / bug di verifica)  
oppure  
2) Il modello regge: ogni manomissione viene rilevata

## Cosa puoi attaccare (in chiaro)

- Payload: engineering/sample-payload/payload.txt
- Manifest: engineering/manifest/manifest.json
- Regola: sha256(payload) deve coincidere con il manifest
- Test guidato: engineering/attack-test/try-to-break-it.md

## Condizione di “vittoria” (severa)

Hai vinto se riesci a far accettare un contenuto modificato
senza che il mismatch venga rilevato.

In pratica:
- payload cambia
- manifest non cambia
- eppure la verifica non segnala mismatch

Se riesci, il modello è rotto.

## Condizione di “tenuta” (successo del modello)

Qualsiasi modifica anche minima:
- cambia la sha256
- produce mismatch
- attiva fail-closed (BLOCK)

## Regole di comportamento

- Solo analisi e test su questi file.
- Nessun tentativo di accesso ad account, token, credenziali, o infrastrutture esterne.
- Il punto non è “hackerare GitHub”, ma testare la coerenza del modello.

## Come segnalare un problema

Apri una Issue e descrivi:
- cosa hai modificato
- che output hai ottenuto
- perché ritieni che sia una violazione della regola deterministica
