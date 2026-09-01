# Design: hosting atlantis-group.ro pe GitHub Pages

Data: 2026-09-01

## Scop

Găzduire gratuită pentru site-ul `atlantis-group.ro` (landing page unic), cu
flux simplu de lucru: editezi local → `git push` → live.

## Arhitectură

- Repo public `rmsdes18-max/atlantis-group`.
- Site static HTML/CSS, fără pas de build. Fișiere în rădăcină:
  `index.html`, `styles.css`, `assets/`.
- GitHub Pages din branch `main`, folder `/` (root).
- `CNAME` = `atlantis-group.ro` → domeniu custom + HTTPS automat (Let's Encrypt).

## DNS (la cyberfolks)

- 4 înregistrări A pe `@`: 185.199.108.153, 185.199.109.153,
  185.199.110.153, 185.199.111.153
- CNAME pe `www` → `rmsdes18-max.github.io`
- Se elimină înregistrările vechi conflictuale pe `@` și `www`.
- Propagarea DNS + emiterea certificatului pot dura câteva ore (TTL).

## Workflow

- Repo clonat în `/Users/suuo/Documents/Atlantis Group`.
- `git add / commit / push` pe `main` → deploy automat.
- Preview local: `python3 -m http.server`.
- `README.md` conține instrucțiunile.

## Livrabile

1. Repo creat + push initial.
2. GitHub Pages activat pe `main` / root.
3. Domeniu custom setat + „Enforce HTTPS" (după emiterea certificatului).
4. DNS configurat la cyberfolks.
5. `index.html` placeholder funcțional.

## Non-obiective (YAGNI)

- Fără framework / generator static (Astro, Jekyll) până nu e nevoie.
- Fără GitHub Actions.
- Fără repo privat (ar cere GitHub Pro).
