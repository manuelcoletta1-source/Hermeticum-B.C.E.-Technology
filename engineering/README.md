# Engineering Entry — Hermeticum B.C.E. Technology

Questo spazio è progettato per **ingegneri**: ispezione, verifica, test.
Nessuna fiducia richiesta. Solo **verifica locale**.

## Quick links
- [Architecture model](./architecture/system-model.md)
- [Verify in 60 seconds](./verify/verify-in-60s.md)
- [Try to break it](./attack-test/try-to-break-it.md)

## What this is
- Un “verification core” minimalista basato su hash e confronto deterministico.
- Un set di file campione per provare **PASS/BLOCK**.

## What this is not
- Non è KYC commerciale.
- Non è un database centrale.
- Non è “trust me bro”.

## Core rule
Se un contenuto non verifica → **BLOCK** (fail-closed).
