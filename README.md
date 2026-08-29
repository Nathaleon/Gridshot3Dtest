# 🎯 Gridshot 3D Trainer

A browser-based, single-file 3D aim trainer inspired by Aim Lab's Gridshot — built entirely with **Three.js** and the **Web Audio API**, no build step, no dependencies to install. Open the HTML file and start clicking.

Look around with real mouse-look (Pointer Lock), move through a fully enclosed arena, and shoot procedurally generated targets or humanoid dummies with a choice of hand-modeled weapons — all tuned through an in-game pause menu.

---

## ✨ Features

### Target Modes
- **Circle Mode** — classic gridshot spheres, size and spawn area fully adjustable.
- **Dummy Mode** — humanoid practice dummies with a simple health system:
  - **3 hits** to the body (torso / arms / legs) to down a dummy
  - **1 hit** to the head for an instant kill
  - Upload your own image to use as the dummy's face
  - Live health pips floating above each dummy's head

### Spawn Area Control
Every axis is defined by a **center** and a **radius**, so you can dial in exactly where targets appear:
- Width (left/right), Height (up/down, circles only), Range (depth)
- Set radius to `0` to lock targets to one exact spot (e.g. pin every target at head height)

### Moving Targets
- Toggle wandering movement on any combination of X / Y / Z axes
- Movement is randomized — short hops, long drifts, or full stops — with a brief pause between direction changes
- Adjustable movement speed

### Weapons
Three selectable, fully procedural (no external model files) viewmodels:
- **M1 Garand** — two-tone wood stock, tapered barrel, gas tube, iron sights, sling swivels
- **Pistol** — slide, frame, exposed barrel tip, hammer
- **Carbine** — modern M4-style build with flash hider, carry rail, and collapsible stock

Each weapon has idle bob and a recoil kick on every shot. Hide the weapon entirely if you'd rather train without a visible viewmodel.

### Audio
- Synthesized mechanical **"clank"** on every shot fired
- Distinct **hit-confirmation chime** when a shot lands — a brighter, layered tone for headshots
- 100% generated with the Web Audio API — no audio files required

### Arena
- Fully enclosed room (floor, ceiling, four walls) with panel textures, corner pillars, accent lighting strips, and lit ceiling panels
- **Dark** and **Light** theme options
- A glowing ring + light beam always marks your spawn point so you never lose track of "home"

### Movement
- **WASD** free movement, clamped to stay inside the arena
- **Jump** and **Crouch** with real gravity and smooth height transitions
- **Back to Start Point** button (or press `R`) to instantly return to spawn
- A "lock movement" toggle for players who just want to train flicks without walking around

### Stats
- Live Hits / Misses / Accuracy tracked in the HUD and pause menu
- One-click counter reset

---

## 🎮 Controls

| Action | Input |
|---|---|
| Look around | Mouse |
| Shoot | Left Click |
| Move | `W` `A` `S` `D` |
| Jump | `Space` |
| Crouch (hold) | `C` or `Ctrl` |
| Return to spawn | `R` |
| Pause / open settings | `Esc` |

All settings — sensitivity, target mode, spawn area, movement, weapon, arena theme, etc. — are only editable from the **pause menu**, so nothing can be changed accidentally mid-run.

---

## 🚀 Getting Started

No installation, no build tools, no server required.

1. Download `gridshot3d.html`
2. Open it in any modern desktop browser (Chrome, Edge, or Firefox recommended)
3. Click **Start / Resume** to lock your mouse and begin training

> Requires an internet connection on first load, since Three.js is pulled from a CDN (`cdnjs.cloudflare.com`).

---

## 🛠️ Tech Stack

- **[Three.js](https://threejs.org/)** (r128) — 3D rendering, scene graph, raycasting
- **Web Audio API** — all sound effects are synthesized in real time, no audio assets
- **Pointer Lock API** — mouse-look and raw input
- **Vanilla HTML / CSS / JavaScript** — a single self-contained file, no framework, no bundler

---

## 📋 Settings Overview

| Category | Options |
|---|---|
| Aim | Sensitivity, targets at once, circle size |
| Spawn Area | Width / height / range center & radius |
| Dummy | Face image upload |
| Target Movement | Enable, axis selection (X/Y/Z), speed |
| Movement | Allow WASD/jump/crouch, back to start |
| Weapon | M1 Garand / Pistol / Carbine, hide weapon |
| Arena | Dark / Light theme |

---

## 🗺️ Possible Future Additions

- Timed sessions and scoring runs (30s / 60s challenges)
- Leaderboard / personal best tracking
- Additional target patterns (flick, tracking, switch drills)
- More weapon models and skins

---

## 📄 License

Free to use, modify, and share. Attribution appreciated but not required.
