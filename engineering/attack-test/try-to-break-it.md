# Try to break it (Attack-driven inspection)

Questa sezione esiste per un motivo:
un sistema serio deve poter essere attaccato, ispezionato e verificato.

## Attack 1 — Change 1 byte in payload
Azione:
- modifica 1 carattere in engineering/sample-payload/payload.txt

Atteso:
- sha256 cambia
- manifest non combacia
- esito = BLOCK

## Attack 2 — Forge the manifest
Azione:
- cambia manifest.payload.sha256 per farlo combaciare col payload manomesso

Atteso (in un sistema completo):
- il manifest deve essere versionato/ancorato
- ogni cambio lascia traccia e richiede nuovo stato pubblico

Qui (demo):
- stai simulando il motivo per cui il manifest, nel mondo reale, va ancorato e tracciato.

## Attack 3 — “Trust me” injection
Azione:
- prova a inserire una frase tipo “è valido perché lo dico io”

Atteso:
- non esiste alcun canale di validità che bypassi il confronto hash.

## Attack 4 — Confusion / ambiguity
Azione:
- prova a rendere la regola “interpretativa”

Atteso:
- la regola resta: mismatch → BLOCK
- nessun “quasi valido”.

## Conclusione
Se puoi far passare un contenuto non coerente senza lasciare traccia:
hai trovato un bug di governance.
Altrimenti:
il modello è robusto per ciò che dichiara.
