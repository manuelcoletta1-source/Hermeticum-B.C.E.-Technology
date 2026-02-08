# System Model — Verification Architecture (Audit-first)

## Goal
Produrre stati verificabili, auditabili e confrontabili nel tempo, senza dipendere da un’autorità centrale.

---

## Primitiva
Hash crittografico:

H(m) = h

dove:
- m = payload (contenuto)
- h = fingerprint (impronta deterministica)

Proprietà operative richieste:
- determinismo
- resistenza a preimage
- resistenza a collisioni (pratica)

---

## Layers

### Layer 1 — Payload
Il contenuto “vero” (file, manifesti, policy, documenti).

### Layer 2 — Hashing
Calcolo dell’impronta:
- payload → sha256 → fingerprint

Una variazione di 1 bit produce un fingerprint diverso.

### Layer 3 — Manifest
Un file che dichiara:
- quali payload sono validi
- quali hash devono combaciare

### Layer 4 — Verification (indipendente)
Un verificatore:
1) scarica il payload
2) calcola sha256
3) confronta con manifest
4) PASS oppure BLOCK

Nessuna API privata richiesta.

### Layer 5 — Fail-closed
Regola:
- mismatch → invalido (BLOCK)

Non esistono “quasi validi”.

---

## Dominanza ingegneristica (metrica)
Definizioni:
- Cv = costo verifica
- Cf = costo falsificazione non rilevata

Obiettivo:
Cf >> Cv

Nel modello hash-audit:
- Cv è basso (calcolo locale)
- Cf è alto (attacchi crittografici / riscrittura storica / compromissione ampia)

---

## Threat model minimo
- Tampering sul payload: rilevato via mismatch hash
- Tampering sul manifest: rilevato se ancorato/versionato e confrontato
- Social engineering: ridotto perché la verifica è deterministica

---

## Output
Uno stato è **valido** solo se i confronti deterministici combaciano.
Altrimenti: BLOCK.
