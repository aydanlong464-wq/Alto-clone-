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

It plays like Tiny Wings and Dune. Holding makes you heavy: you rush down the slopes, dive in the air, and slow down if you hold going up. Letting go as you crest launches you. The swells are long, smooth, rolling hills that drift toward you slowly, so you can read them and find a rhythm.

- **Landings are real physics.** The part of your speed along the slope is kept, and the part slamming into it is lost. Come down parallel to a downslope for a **Perfect** (a small boost); three in a row starts **Fever**. A bad angle bleeds speed. Slamming nose-first into a slope at speed is a **wipeout**.
- **The hills grow.** They get longer and taller the further you go.
- **Bounce bubbles.** Rows of big clear rainbow soap bubbles float above the waves, like the bubbles in Tiny Wings 2. Come down on one and it pops and bounces you back up, a little slower than you came in. They're spread out, so chaining bounces without touching the water (**Bounce ×2, ×3…**) takes well-timed dives, and each one in a chain scores more. Some bubbles hold gold coins that pay out when they pop. Hitting one from below or the side just pops it.
- **Speed boosts.** Glowing chevrons (») ride on the waves. Grab one for an instant speed kick plus a couple of seconds of extra push. Like Tiny Wings' speed coins, a boost right before a wave face can send you somewhere you don't want to go.
- **The whitewater** is the sunset from Tiny Wings. A wall of breaking foam rolls in behind you and keeps speeding up, so it catches everyone eventually; the better your landings, the longer you stay ahead. The WHITEWATER meter shows how close it is.
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
