# Retro Tetris: Fable vs Astra

Four complete, single-file falling-block games. Same rules family, four visual languages — a colour-pencil sheet photographed on 16mm, a paper arcade cabinet with film grain, a sketchbook film edition, and a crayon sheet on a pencil grid.

No build step. No server. Open a file, or play them on GitHub Pages.

## Play

| Game | File | GitHub Pages |
| --- | --- | --- |
| **Graphite Blocks** (Fable) | [`Tetris-Fable.html`](Tetris-Fable.html) | [Play](https://miaai-lab.github.io/Retro-Tetris-Fable-vs-Astra/Tetris-Fable.html) |
| **Paper Tetris** (Astra) | [`Tetris-Astra.html`](Tetris-Astra.html) | [Play](https://miaai-lab.github.io/Retro-Tetris-Fable-vs-Astra/Tetris-Astra.html) |
| **Sketchbook Film** (GLM-5.3-Flash) | [`Tetris-GLM5-3-Flash-EXL3.html`](Tetris-GLM5-3-Flash-EXL3.html) | [Play](https://miaai-lab.github.io/Retro-Tetris-Fable-vs-Astra/Tetris-GLM5-3-Flash-EXL3.html) |
| **Pencil Tetris** (Qwen3.8-Flash) | [`Tetris-Qwen3.8-Flash.html`](Tetris-Qwen3.8-Flash.html) | [Play](https://miaai-lab.github.io/Retro-Tetris-Fable-vs-Astra/Tetris-Qwen3.8-Flash.html) |
| Landing | [`index.html`](index.html) | [https://miaai-lab.github.io/Retro-Tetris-Fable-vs-Astra/](https://miaai-lab.github.io/Retro-Tetris-Fable-vs-Astra/) |

Locally:

```bash
# any static server, or just open the HTML in a browser
python3 -m http.server 8080
# then visit http://localhost:8080/
```

Audio unlocks on the first click or keypress (browser autoplay rules).

## The versions

### Graphite Blocks — `Tetris-Fable.html`

Drawn in colour pencil on 5mm graph paper and shot on 16mm stock. Tiles, grain, music, and SFX are all generated at runtime — no image or audio assets.

- 10×20 well, 7-bag randomizer, SRS with wall kicks (including 180°)
- Hold, next queue, lock delay, DAS / ARR, ghost piece
- Soft drop, hard drop, T-spin-aware scoring
- Touch: swipe to move, tap to rotate, swipe down to drop
- High score in `localStorage`

### Paper Tetris — `Tetris-Astra.html`

A paper-and-ink arcade layout with rolling film grain, on-screen buttons, and generated sound and music. Fully offline once the file is loaded.

- Hold, next piece, score / lines / level
- Keyboard plus on-screen / touch controls
- Mute for SFX and music independently

### Sketchbook Film — `Tetris-GLM5-3-Flash-EXL3.html`

Hand-inked paper well, rolling film grain, and generated tiles. Music is a Korobeiniki chiptune loop (off by default). Built with GLM-5.3-Flash.

- 10×20 well, 7-bag randomizer, wall kicks, hold, next, ghost piece
- Soft drop, hard drop, DAS / ARR, high score in `localStorage`
- Independent mute for SFX and music (on-screen buttons or keys)

### Pencil Tetris — `Tetris-Qwen3.8-Flash.html`

Drawn in crayon on a wobbly pencil grid over aged graph paper, with the scoring hand-lettered. Tiles, paper grain and the Korobeiniki tune are generated at runtime — no image or audio files ride along. Built with Qwen3.8-Flash.

- 10×20 well, 7-bag randomizer, wall kicks, next queue
- Soft drop, hard drop, DAS / ARR auto-repeat, on-screen buttons for touch
- Scoring 100/300/500/800 per line times level, level up every 10 lines
- Music is optional and off by default: M or the music button, remembered between visits
- Sound stays silent while the game is paused, over, or hidden

## Controls

### Graphite Blocks (Fable)

| Action | Keys |
| --- | --- |
| Move | ← → |
| Soft drop | ↓ |
| Hard drop | Space |
| Rotate clockwise | ↑ or X |
| Rotate counter-clockwise | Z |
| Rotate 180° | A |
| Hold | C |
| Pause | P |
| Restart | R |
| Cycle film grain | G |
| Mute effects | M |
| Mute music | N |

Click or tap the title / game-over screen to start.

### Paper Tetris (Astra)

| Action | Keys |
| --- | --- |
| Move | ← → |
| Soft drop | ↓ |
| Hard drop | Space |
| Rotate clockwise | ↑ or X |
| Rotate counter-clockwise | Z |
| Hold | C or Shift |
| Pause | P or Esc |
| Restart | R |
| Start / resume | Enter |

On-screen buttons cover the same actions on a phone.

### Sketchbook Film (GLM-5.3-Flash)

| Action | Keys |
| --- | --- |
| Move | ← → |
| Soft drop | ↓ |
| Hard drop | Space |
| Rotate clockwise | ↑ or X |
| Rotate counter-clockwise | Z |
| Hold | C |
| Pause | P |
| Restart | R |
| Mute effects | M |
| Mute music | N |

Click or tap the playfield to start. On-screen buttons toggle music and sound.

### Pencil Tetris (Qwen3.8-Flash)

| Action | Keys |
| --- | --- |
| Move | ← → |
| Soft drop | ↓ |
| Hard drop | Space |
| Rotate clockwise | ↑ or X |
| Rotate counter-clockwise | Z |
| Pause | P or Esc |
| Start / restart | Enter |
| Music on / off | M |

On-screen buttons cover the same actions, including music. Click or tap the board to start.

## Repository layout

```
.
├── index.html                         # GitHub Pages landing (links all games)
├── Tetris-Fable.html                  # Graphite Blocks
├── Tetris-Astra.html                  # Paper Tetris — Offline Edition
├── Tetris-GLM5-3-Flash-EXL3.html      # Sketchbook Film Edition
├── Tetris-Qwen3.8-Flash.html          # Pencil Tetris
├── LICENSE                            # GNU Affero General Public License v3.0
└── README.md
```

Each game is a self-contained HTML document (markup, CSS, and JavaScript in one file).

## License

Copyright (C) 2026 MiaAI Lab

This program is free software: you can redistribute it and/or modify it under the terms of the [GNU Affero General Public License](LICENSE) as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

See [`LICENSE`](LICENSE) for the full terms. If you run a modified version on a network (including GitHub Pages or any other public host), AGPL-3.0 requires that you offer the corresponding source to users who interact with it.
