# Aero Surf

A physics-based endless surfing game in 3D, styled in Frutiger Aero: glossy turquoise ocean, puffy clouds, palm-tree islands, floating bubbles, lens flare, and a shiny 3D surfer on a 3D board.

## Play

Open `index.html` in a modern browser with WebGL. It loads three.js from the jsDelivr CDN, so it needs an internet connection.

To play it from a link, turn on GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / root**. The game then runs at `https://<your-username>.github.io/<repo-name>/`.

## Controls

| Input | Action |
| --- | --- |
| Tap / Space / ↑ | Jump |
| Hold in the air | Backflip |
| P / Esc | Pause |
| M | Mute |
| R | Turn a custom model 90° |

Land with your board matching the wave or you wipe out. Jump the rocks and buoys.

## How it works

- **The ocean** is one wave function shared by the GPU shader and the physics, so the board rides exactly the water you see. Three wind-wave layers plus big rolling swells that move toward you. The shader adds sky reflections (Fresnel), sun glitter, turquoise light through raised water, foam on steep faces and crests, and a foam wake behind the board.
- **Physics.** Gravity pulls you along the wave slope. You launch when a crest falls away faster than gravity can follow, and landings project your velocity back onto the water.
- **The surfer** is built from glossy capsules with leg IK, so the knees bend as it crouches. You can swap in your own model; see [`models/README.md`](models/README.md).
- **Zones** change every 1000 m: Lagoon, Deep Blue, Sunset Gloss, Aurora (night) and Citrus.

## Other versions

- `runner.html`: the 2D Aero downhill runner.
- `noir.html`: the original dark, high-contrast 2D runner.
