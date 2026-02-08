# Try to break it (Attack-driven inspection)

Questa sezione è volutamente “ostile”: un sistema serio deve reggere l’ispezione.

## Attack 1 — Modify payload
Azione:
- cambia 1 carattere in engineering/sample-payload/payload.txt

Atteso:
- sha256 cambia
- manifest non combacia
- esito = BLOCK

## Attack 2 — Modify manifest to match tampered payload
Azione:
- aggiorna manifest.payload.sha256 per farlo combaciare col payload manomesso

Significato:
- hai creato un nuovo stato
- nel sistema reale, questo cambio deve essere tracciato e ancorato (append-only)

## Attack 3 — Add “trust” bypass
Azione:
- prova a inventare una regola che bypassa la verifica

Atteso:
- non esiste alcun bypass: mismatch → BLOCK

## Attack 4 — Ambiguity injection
Azione:
- prova a rendere la regola interpretativa

Atteso:
- la regola resta deterministica: match o mismatch.
