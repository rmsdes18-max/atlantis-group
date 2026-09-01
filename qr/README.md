# Cod QR — atlantis-group.ro

Toate variantele encodează: **https://atlantis-group.ro**
Corecție de erori: nivel H (max) — rezistă la tipar mic și la un logo suprapus în centru.

| Fișier | Utilizare |
|--------|-----------|
| `atlantis-group-qr.svg` | Print (cărți de vizită, flyere) — negru pe fundal alb, vectorial |
| `atlantis-group-qr-transparent.svg` | Design — fără fundal, module negre |
| `atlantis-group-qr.png` | Fallback raster (2624×2624 px) |

## Reguli la tipar
- Păstrează zona liberă (quiet zone) din jur — e deja inclusă (4 module).
- Dimensiune minimă recomandată pe carte de vizită: ~2×2 cm.
- Nu schimba proporțiile (păstrează pătrat).
- Dacă vrei alt link, regenerează — nu edita fișierul manual.

## Regenerare
```bash
pip3 install --user segno
python3 -c "import segno; segno.make('https://atlantis-group.ro', error='h').save('qr/atlantis-group-qr.svg', scale=16, border=4)"
```
