# Cay's Counting Party

Static toddler counting game (1 to 10). Plain HTML, CSS and JavaScript. No build step, no dependencies.

## Run it locally

    cd games/counting-party
    python3 -m http.server 8000

Then open http://localhost:8000. Opening index.html by double-click (file://) blocks the audio files, so the game falls back to the browser voice and plays no music.

## Files

- `index.html`: the whole game. Names, counted objects and fallback lines are in the EDIT ME block at the top of the script.
- `assets/img/{mom,dad,cay}_{idle,cheer}.png`: character sprites.
- `assets/audio/`: `welcome`, `num_1..10`, `tap_1..10`, `yay_1..4`, `finale`, `music` (all .mp3).
- `manifest.webmanifest`, `icon-180.png`, `icon-512.png`: Add to Home Screen support.
- `.nojekyll`: lets GitHub Pages serve the folder as-is. All paths are relative, so it works from a subfolder.

## Fallbacks

Any single asset can be missing without breaking the game: a missing character PNG uses the built-in SVG drawing, a missing voice clip is spoken by the browser voice, and missing music just means no music.

## Not included

No service worker, so it needs a connection each time it loads.
