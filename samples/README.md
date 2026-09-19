# Mythical Warrior — Engine Samples

Three self-contained, single-file demos of a mythical warrior character, one per rendering engine. Each is built entirely from vector/primitive shapes (no external art assets), loads its engine from a CDN, and needs no build step — just open the HTML file or serve the folder statically.

| Folder | Engine | Theme | Controls |
|---|---|---|---|
| `phaser-mythical-warrior/` | [Phaser 3](https://phaser.io/) | Ember/shadow warrior, 2D side-view | Arrow keys to move/jump, Space to attack |
| `pixijs-mythical-warrior/` | [PixiJS 7](https://pixijs.com/) | Frost warrior, 2D top-down aim | Mouse to aim, click to swing sword |
| `threejs-mythical-warrior/` | [Three.js](https://threejs.org/) | Molten guardian, 3D low-poly | Drag to orbit, scroll to zoom, click the warrior to attack |

## Running locally

No build tools required. From this directory:

```bash
python3 -m http.server 8000
```

Then open, e.g., `http://localhost:8000/phaser-mythical-warrior/`.

## What each sample demonstrates

- **Rigging with primitives**: each warrior is a container/group hierarchy (torso → head/arms/legs, arm → sword) so parts can be individually posed and tweened, the same idea a bone-based rig would use.
- **Idle animation**: breathing (scale pulse), cape sway (regenerated polygon / displaced vertices per frame), and a pulsing glow (ember core, sword aura, or eyes).
- **Interaction**: movement and an attack swing driven by keyboard, mouse aim, or raycasting, depending on what's idiomatic for the engine.
