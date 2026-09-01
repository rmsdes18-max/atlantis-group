# atlantis-group

Site static pentru **atlantis-group.ro**, găzduit gratuit pe GitHub Pages.

## Cum lucrezi la site

1. Editează fișierele: `index.html`, `styles.css`, imagini în `assets/`.
2. Previzualizare locală:
   ```bash
   python3 -m http.server 8000
   ```
   apoi deschide http://localhost:8000
3. Publică modificările:
   ```bash
   git add -A
   git commit -m "descriere schimbare"
   git push
   ```
4. În ~1 minut modificările sunt live pe https://atlantis-group.ro

## Cum funcționează hosting-ul

- GitHub Pages servește branch-ul `main`, folderul rădăcină.
- Fișierul `CNAME` leagă domeniul custom `atlantis-group.ro`.
- HTTPS este gestionat automat de GitHub (certificat Let's Encrypt).
- DNS-ul domeniului este la cyberfolks (înregistrări A către GitHub + CNAME pe `www`).

## Nu șterge

- `CNAME` — pierderea lui deconfigurează domeniul.
