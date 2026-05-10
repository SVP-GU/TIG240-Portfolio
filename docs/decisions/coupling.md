# Coupling

> **Status:** Decided by the class in Session 1.
> **TODO:** Replace this placeholder with the agreed list of shared files and their owners.

## Why this is a deliberate decision

Each shared file in the repo is a place where multiple groups will need to coordinate — to merge, resolve conflicts, and discuss. That is **not a bug**: it is where the conversations happen that the site is supposed to surface (positioning, peer awareness, quality bar).

The architectural question is *which conversations are worth having*, and which should be avoided by giving each group its own file to edit.

This is Simon's near-decomposability in practice: most work should be local (per-group, no coordination), with a few well-chosen shared layers where coordination is the point.

## Default coupling (in this seed)

- `docs/challenges/<challenge>/index.md` — co-authored by the 3–4 groups in each challenge. **Conflicts expected.**
- `docs/decisions/axes-of-variation/<challenge>.md` — drafted by the track lead, edited by the cluster.
- `docs/decisions/*.md` — co-authored by the whole class.

## Decoupled by design (per-group)

- `docs/challenges/<challenge>/<park>.md` — owned by exactly one group. Should never conflict.

## Decision

docs/challenges/<challenge>/index.md — Skrivs gemensat av de grupper som ingår i samma challenge. Konflikter förväntas

docs/decisions/axes-of-variation/<challenge>.md — Draftas av koordiantorer och justeras av samtliga medlemmar på varje challenge

docs/decisions/*.md — Hela klassen ansvarar för innehållet. Koordinationer comittar.

docs/challenges/<challenge>/<park>.md — Ägs av exakt en grupp. Borde aldrig leda till konflikt.

## Conflict-resolution norm

Allt arbete ska göras i separata branches.
Pull requests ska granskas innan de mergas in i main.
Track lead ansvarar för att lösa konflikter i delade filer.
Rebase ska användas före merge när det är möjligt.