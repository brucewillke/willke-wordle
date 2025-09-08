# wxrdle-lite (static)

A zero-backend Wordle-style game you can host on GitHub Pages.  
Custom dictionaries live in `/words/*.txt`.

## Customize
- Edit `config.json` for title, defaults, and daily settings.
- Put answer/allowed lists under `/words/answers-<len>.txt` and `/words/allowed-<len>.txt` (lowercase, one word per line).
- Add more lengths by adding more files (e.g., 6, 7…).

## Run locally
Open `index.html` with a local HTTP server (due to fetch of local files):
```bash
python3 -m http.server 8080
# then visit http://localhost:8080
```

## Deploy on GitHub Pages
- Push to `main`.
- Enable **Settings → Pages → Build from a branch**, or keep the provided workflow (`.github/workflows/pages.yml`).

## Notes
- This is fully static: answers live in the repo, so anyone can view the lists.
- Local stats are stored in `localStorage` (per-browser), not synced.
