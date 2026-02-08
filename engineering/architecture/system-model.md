# System Model — Verification Architecture

## Goal
Produrre stati verificabili e auditabili nel tempo, senza dipendere da autorità centrali.

## Primitive
Hash crittografico:

H(m) = h

- m = payload (contenuto)
- h = fingerprint (impronta)

Proprietà operative: determinismo, resistenza a preimage, resistenza a collisioni (pratica).

## Layers

### Layer 1 — Payload
File reali (documenti/manifest/config).

### Layer 2 — Hashing
payload → sha256 → fingerprint  
Se cambia 1 byte, cambia l’hash.

### Layer 3 — Manifest
Un file che dichiara:
- quale payload è atteso
- quale hash è considerato valido

### Layer 4 — Verification (indipendente)
Un verificatore:
1) scarica payload
2) calcola sha256
3) confronta con manifest
4) PASS o BLOCK

### Layer 5 — Fail-closed
Regola: mismatch → BLOCK  
Niente interpretazione.

## Cost model
Cv = costo verifica  
Cf = costo falsificazione non rilevata

Obiettivo: Cf >> Cv

- Cv basso: calcolo locale
- Cf alto: attacco crittografico / riscrittura storica / compromissione ampia

## Output
Valido ⇢ solo se i confronti deterministici combaciano.  
Altrimenti ⇢ BLOCK.
