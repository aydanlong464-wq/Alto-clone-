# Aero Surf

An endless 2.5D surfing game in vivid Frutiger Aero blues and greens. Everything is real 3D (three.js) seen from a side-scrolling perspective camera. A shaded ocean rolls away to glossy islands under a rainbow, with big bubbles drifting through the sky. The front of the ocean is cut open like an aquarium, so you see dolphins, fish, light rays and a glowing grassy seabed under the waves.

The surfer is a glossy jelly figure in the style of an old Messenger buddy icon: round arms and legs, a floating head, a big soft highlight and a dark glassy outline. It comes in 10 skins.

## Play

Open `index.html` in a modern browser with WebGL. It loads three.js from the jsDelivr CDN, so it needs an internet connection.

To play it from a link, turn on GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / root**. The game then runs at `https://<your-username>.github.io/<repo-name>/`.

## How to play

| Input | Action |
| --- | --- |
| Hold anywhere (or Space) | Push down. On the water this builds speed going downhill; in the air you dive. |
| Let go | Going uphill, letting go launches you off the crest |
| In the air: hold the **right** half (or →/D) | Dive and tip the board nose **down** |
| In the air: hold the **left** half (or ←/A) | Dive and tip the board nose **up** |
| K / **Skin** button | Change skin |
| P / Esc | Pause |
| M | Mute |
| R | Turn a custom model 90° |

- **The waves are huge.** Swells grow as you go, and monster waves come in sets.
- **Landings are judged on your board angle.** Tip the board to match the wave before you touch down. If you let go in the air, the board slowly levels to your flight path.
- **Smooth!** Land with the board flat on a downslope to keep your speed and get a boost. Three in a row starts **Fever**: double points, more speed and a rainbow shimmer.
- **Splash!** A slightly-off landing costs speed. **Wipeout!** A clearly wrong angle, nose-first or tail-first, ends the run.
- There is no timer. Surf as far as you can. The zones change every 600 m: Crystal Lagoon, Emerald Bay, Deep Blue, Lime Rain and Aqua Aurora.

## How it works

The water is one wave function shared by the GPU shaders and the physics, so the board rides exactly what you see. Swells are steep-faced hills rolling toward you, with small chop on top. You launch when a crest curves away faster than gravity can pull you down. Holding raises your gravity, so you stick to the water and dive faster. Whether a landing is smooth, a splash or a wipeout depends on how your flight path lines up with the wave slope and how hard you hit.

A custom surfer can be swapped in; see [`models/README.md`](models/README.md).

## Other versions

- `surf-timed.html`: the previous 2.5D version with the sunset timer and smaller waves.
- `surf2d.html`: the flat side-on (orthographic) version of this game.
- `surf3d.html`: the earlier 3D-camera surf version with backflips, rocks and buoys.

- `runner.html`: the 2D Aero downhill runner.
- `noir.html`: the original dark, high-contrast 2D runner.
