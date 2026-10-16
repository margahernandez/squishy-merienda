# Squishy Merienda

A squishy simulator where every toy is a freshly made Filipino merienda. Poke, press, squeeze, pull and smoosh a siopao, puto, leche flan, palitaw or pandesal right in your browser.

**Play it:** https://margahernandez.github.io/squishy-merienda/

## What's inside

- **Five merienda:** siopao, puto, leche flan, palitaw and pandesal, each with its own texture, setting and feel.
- **Real squish:** 3D soft-body physics in WebGL. The dough keeps its volume, dents and bulges where you press, and slowly rises back.
- **Five actions:** poke, press, squeeze, pull and smoosh.
- **Two-finger stretch:** on a phone, pick Pull and spread two fingers on a merienda to stretch it out.
- **A recipe for each one:** tweak softness, rise time and jiggle in Settings. Your tweaks are remembered on your device.
- **Its own sound:** each merienda has a synthesized sound kit, from the siopao's soft puffs to the leche flan's wet plops and the pandesal's crusty crackle.
- **Works on phones too:** the Merienda and Settings drawers move to the top and bottom on small screens, and Android phones get a little haptic buzz.

## Controls

| Key | Does |
| --- | --- |
| `1`–`5` | Poke, Press, Squeeze, Pull, Smoosh |
| `V` | Switch between top and tilted camera |
| `Space` / `Enter` | Hold the current action (when the food is focused) |
| `Esc` | Close a drawer |

## How it's built

Plain HTML, CSS and JavaScript with no build step and no libraries.

- `index.html` is the app: the title card, name, action bar and the two drawers.
- `labs/` holds one self-contained page per merienda (physics, rendering and sound). The app loads them in a frame and talks to them with `postMessage`.
- Everything is drawn with WebGL and Canvas 2D, and every sound is made live with the Web Audio API, so there are no image textures or audio files to download apart from the menu thumbnails.

## Run it locally

Any static file server works:

```sh
python3 -m http.server
```

Then open http://localhost:8000.

---

Designed and built by [Marga Hernandez](https://margahernandez.framer.ai).
