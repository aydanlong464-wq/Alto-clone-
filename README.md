# Aero Surf

A 2.5D surfing game: Frutiger Aero gloss with Killer 7 colors. Everything is real 3D (three.js) seen from a side-scrolling perspective camera. The shaded ocean surface rolls away to glossy islands and blocky towers on the horizon, and the front of the ocean is cut open like an aquarium, so you see under the waves: light rays, caustics, iridescent fish, seaweed, bubbles and a 3D seabed. The surfer is a bubbly, iridescent figure with round arms and legs and a floating head.

## Play

Open `index.html` in a modern browser with WebGL. It loads three.js from the jsDelivr CDN, so it needs an internet connection.

To play it from a link, turn on GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / root**. The game then runs at `https://<your-username>.github.io/<repo-name>/`.

## How to play

| Input | Action |
| --- | --- |
| Hold (tap-and-hold / Space) | Push into the wave. Going downhill this builds speed; in the air you dive. |
| Let go | Going uphill, letting go launches you off the crest |
| P / Esc | Pause |
| M | Mute |
| R | Turn a custom model 90° |

- **Smooth!** Land matching a downslope to keep your speed and get a boost. Three in a row starts **Fever** (double points, faster, rainbow glow).
- **Splash! / Plunge!** Landing against a wave costs speed. A hard bad landing dunks you under the water until you float back up.
- **Beat the sunset.** You start with 45 seconds. Every 600 m you reach a new zone and get more time. When the clock runs out, night falls and the run ends.
- **Zones:** Vista Lagoon, Red Room, Neon Floor, Ultraviolet, Sunset Gloss, Cyber Lime.

## How it works

The water is one wave function shared by the GPU shaders and the physics, so the board rides exactly what you see. Swells are a chain of rolling hills moving toward you, with small chop on top. You launch when a crest curves away faster than gravity can pull you down, and holding raises your gravity so you stick to the water and dive faster.

A custom surfer can be swapped in; see [`models/README.md`](models/README.md).

## Other versions

- `surf2d.html`: the flat side-on (orthographic) version of this game.
- `surf3d.html`: the earlier 3D-camera surf version with backflips, rocks and buoys.

- `runner.html`: the 2D Aero downhill runner.
- `noir.html`: the original dark, high-contrast 2D runner.
