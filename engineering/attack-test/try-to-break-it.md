# Try to break it

This repo exposes a minimal deterministic verification model.

## Attack 1 — Modify payload
Change ONE character in `engineering/sample-payload/payload.txt`.

Expected:
- sha256 changes
- manifest mismatch
- BLOCK

## Attack 2 — “Silent edit”
Try to make a change without changing the manifest.

Expected:
- mismatch detected
- BLOCK

## Attack 3 — Manifest edit
Change the manifest sha256 to match the tampered payload.

Meaning:
- you created a new state
- in a real anchored system this must be append-only and auditable

## Core rule
If mismatch is not detected → system is broken.
If mismatch is detected → system is coherent.
