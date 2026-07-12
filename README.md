# 🎙 Studio Buletin — CEITI

Consolă de emisie web pentru buletinul informativ de la pauza mare, creată pentru **Echipa de Producție Multimedia** a CEITI.

## Cum funcționează

Fluxul unei zile de buletin, pe butoane:

1. **Piesa de deschidere** — pornește cu fade-in și merge în loop până sunt gata speakerii
2. **Jingle Buletin** — un click: piesa scade lin și intră jingle-ul știut de elevi
3. **ON AIR** — banner live cât timp vorbesc speakerii
4. **Piesa de încheiere** — a doua piesă a zilei, apoi fade out final

## Surse de muzică (fără backend)

- **Spotify** — site-ul devine dispozitiv Spotify prin Web Playback SDK: cauți piesa direct în pagină și se redă integral, cu fade-uri. Necesită cont Premium + un Client ID din [Spotify Dashboard](https://developer.spotify.com/dashboard) (instrucțiunile pas cu pas sunt în panoul ⚙ Setări din site).
- **Bibliotecă locală** — tragi fișiere MP3/WAV/M4A în pagină; rămân salvate în browser (IndexedDB), cu căutare.

## Utilizare

Deschide site-ul printr-un server local:

```bash
python3 -m http.server 8765
```

apoi intră pe **http://127.0.0.1:8765** (adresa `127.0.0.1` e obligatorie pentru conectarea Spotify pe local; pe hosting HTTPS, ex. GitHub Pages, nu există restricții).

### Scurtături de tastatură

| Tastă | Acțiune |
|-------|---------|
| `Space` | Pasul următor din flux |
| `F` | Fade out lent |
| `Esc` | Stop tot |

## Paleta & tipografie

Navy `#1a293a` · Roșu `#df163c` · Teal `#20a4a2` — **Roboto Slab** (titluri) + **Open Sans** (text), identitatea vizuală CEITI.
