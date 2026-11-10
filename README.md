# Cube Lab

A Rubik's Cube lab that runs entirely in the browser: simulator, solver, scrambler, pattern lab, painting, tutorials, a speedcube timer, and bot races, including live races with a real cube through your camera.

- Cubes: 2×2, 3×3, 4×4, 5×5, plus Pyraminx, Skewb, Megaminx, Square-1 and a Circle 3×3 mod
- Solver with step-by-step playback (2×2 and 3×3 search; other puzzles replay your move history)
- Scrambler, saved patterns, TXT export/import, painting mode, tutorials (Beginner, CFOP, Roux)
- Play tab: bot races, time attack, par, daily puzzle, skills, Cube Points and diamonds
- Live real-cube races with camera tracking and optional video recording
- Installable as an app (PWA) and works offline after the first visit

Everything is in one `index.html` with no build step and no dependencies. Progress is saved in your browser's local storage.

## Publish on GitHub Pages

1. Create a new public repository on GitHub (for example `cube-lab`).
2. Choose **Add file → Upload files** and drop in every file from this folder:
   `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `icon.svg`, `README.md`, `LICENSE`.
   Then **Commit changes**.
3. Open **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, then **Save**.
4. After a minute, your app is live at `https://YOUR-USERNAME.github.io/cube-lab/`.

GitHub Pages serves over HTTPS, which the camera features and the install prompt require.

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000. Opening `index.html` directly from disk works for most features, but the camera, install prompt and offline mode need `http://localhost` or HTTPS.

## Updating

Replace `index.html` in the repository. If visitors still see the old version, change `VERSION` in `sw.js` (for example to `cube-lab-v2`) and commit it as well.

## License

MIT. See `LICENSE`.
