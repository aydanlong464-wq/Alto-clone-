# Aero Surf

An endless 2.5D surfing game in vivid Frutiger Aero blues and greens. Everything is real 3D (three.js) seen from a side-scrolling perspective camera. A shaded ocean rolls away to glossy islands under a rainbow, with big bubbles drifting through the sky. The front of the ocean is cut open like an aquarium, so you see a whole reef under the waves: dolphins, clownfish, tangs, angelfish, a shimmering school that swims alongside you, pufferfish that puff up, glowing jellyfish, sea turtles, coral, crabs and starfish on a glowing seabed.

The surfer is a glossy jelly figure in the style of an old Messenger buddy icon: round arms and legs, a floating head, a big soft highlight and a dark glassy outline. It comes in 10 skins.

## Play

Open `index.html` in a modern browser with WebGL. It loads three.js from the jsDelivr CDN, so it needs an internet connection.

To play it from a link, turn on GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / root**. The game then runs at `https://<your-username>.github.io/<repo-name>/`.

## How to play

| Input | Action |
| --- | --- |
| Hold anywhere (or Space / arrows) | Push down. On the water this builds speed going downhill; in the air you dive. |
| Let go | Going uphill, letting go launches you off the crest |
| K / **Skin** button | Change skin |
| N / **Night mode** button | Switch between day and night |
| P / Esc | Pause |
| M | Mute |
| R | Turn a custom model 90° |

It plays like Dune: one touch, and the surfer points along its flight path. Unlike Dune, the waves roll toward you, so the hills keep moving under you mid-flight.

- **The waves are huge.** Swells grow as you go, and monster waves come in sets.
- **Diving turns height into speed.** Just above the water, your path swoops onto the wave and keeps its momentum, so a well-timed dive onto a downslope sends you flying down it.
- **Perfect!** Come down with your path matching a downslope for a speed boost. Three in a row starts **Fever**: double points, more speed and a rainbow shimmer.
- **Up the face!** Meeting an oncoming wave face, you ride up it and can launch again. You keep most of your speed.
- **Wipeout!** Slamming steeply into a wave face ends the run, and the margin for error tightens the further you get.
- **Bubbles.** Strings of glossy soap bubbles ride along the waves' back slopes. Surf through them to pop them: each pop plays a rising note and gives a little speed. Get every bubble in a string for a **Bubble chain!** bonus and a bigger boost. Fly over them and you miss them.
- **The whitewater.** A wall of breaking foam rolls in behind you and speeds up over time. Keep your speed up and it falls back; botch a few landings and it catches you. The WHITEWATER meter shows how close it is.
- **Night mode** swaps in four night zones (Moonlit Lagoon, Bioluminescence, Aurora Night, Midnight Neon) with stars, a moon, aurora bands, glowing plankton and wake, glowing jellyfish and lit windows on the towers. Your choice is remembered.
- There is no timer. Surf as far as you can. The zones change every 600 m: Crystal Lagoon, Emerald Bay, Deep Blue, Lime Rain and Aqua Aurora.

### Full screen on a phone

Turn on GitHub Pages (below), open the game's link in Safari or Chrome, and use **Add to Home Screen**. Launched from the home screen it runs full screen in landscape, with no browser or app bars. In desktop browsers there is also a **Full screen** button.

## How it works

The water is one wave function shared by the GPU shaders and the physics, so the board rides exactly what you see. Swells are steep-faced hills rolling toward you, with small chop on top. You launch when a crest curves away faster than gravity can pull you down. Holding raises your gravity, so you stick to the water and dive faster. Whether a landing is smooth, a splash or a wipeout depends on how your flight path lines up with the wave slope and how hard you hit.

A custom surfer can be swapped in; see [`models/README.md`](models/README.md).

## Other versions

- `surf-timed.html`: the previous 2.5D version with the sunset timer and smaller waves.
- `surf2d.html`: the flat side-on (orthographic) version of this game.
- `surf3d.html`: the earlier 3D-camera surf version with backflips, rocks and buoys.

- `runner.html`: the 2D Aero downhill runner.
- `noir.html`: the original dark, high-contrast 2D runner.
