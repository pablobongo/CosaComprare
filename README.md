# Cosa Comprare

PWA per lista della spesa condivisa tra due dispositivi.  
Stack: HTML + CSS + Vanilla JS | Backend: Google Apps Script | DB: Google Sheets

## File principali
- `index.html` — app completa (HTML + CSS + JS in un unico file)
- `manifest.json` — configurazione PWA
- `sw.js` — service worker per cache offline
- `Code.gs` — backend Google Apps Script (deploy separato)

## WEBAPP_URL
Impostato in `index.html` nella costante `WEBAPP_URL` (riga ~578).  
Quando si redeploya `Code.gs`, aggiornare questa costante e aggiornare la cache del SW
cambiando il `CACHE_NAME` in `sw.js` (es. `cosa-comprare-v1.0.1`).

## Deploy
1. Carica tutti i file su repository GitHub pubblico
2. Settings → Pages → Branch main → Save
3. URL disponibile su `https://[username].github.io/cosa-comprare/`

## Limitazione nota v1.0.0
I prodotti "Completati" sono salvati solo in locale (non sincronizzati tra dispositivi).
