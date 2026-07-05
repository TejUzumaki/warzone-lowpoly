# 🪖 WARZONE: LOW POLY TACTICAL

> A fast-paced, browser-based, low-poly 3D Battle Royale and Wave Survival game built entirely with Three.js and vanilla JavaScript. No game engines, no external assets—just pure WebGL power and raw code.

![Game Status](https://img.shields.io/badge/Status-Live-brightgreen)
![Version](https://img.shields.io/badge/Version-5.1-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📖 Table of Contents
1. [About the Project](#about-the-project)
2. [Key Features](#key-features)
3. [How to Play](#how-to-play)
4. [Technical Stack](#technical-stack)
5. [World Generation & AI](#world-generation--ai)
6. [Deployment](#deployment)

---

## 🏔️ About the Project
**WARZONE: LOW POLY TACTICAL** was developed as a proof-of-concept to prove that AAA-style mobile/browser FPS mechanics can be achieved without heavy game engines like Unity or Unreal. It features a fully interactive 3D environment, dynamic AI, physics-based movement, and a highly optimized rendering pipeline that runs smoothly at 60FPS on both desktop and mobile browsers.

## ✨ Key Features

### Gameplay
* **Two Game Modes:** Battle Royale (25 players, shrinking safe zone) and Wave Survival (endless enemy waves).
* **Staging Area & Skydive:** Players spawn on a floating lobby platform and drop into the battlefield.
* **5 Unique Weapons:** Pistol, SMG, Assault Rifle, Shotgun, and Sniper—each with distinct damage, recoil, spread, and reload mechanics.
* **Loot System:** Glowing weapon crates scattered across the map with contextual UI prompts for swapping weapons.
* **Dynamic Combat:** Bullet tracers, dynamic muzzle flash lighting, damage numbers, and headshot multipliers.

### AI Mechanics
* **Two-Faction System:** Bots are divided into two factions. They dynamically fight each other but will retaliate against the player if provoked or if the player gets too close.
* **Zone Awareness:** Bots take damage outside the safe zone and will dynamically pathfind back inside the circle.

### Mobile & UI
* **Dynamic Fire Button:** The fire button acts as a mini-joystick, allowing players to drag and aim while shooting simultaneously.
* **Proximity Audio:** Enemy gunfire volume scales dynamically based on distance.
* **Layout Editor:** A built-in system allowing players to drag, resize, and save their custom HUD layouts to `localStorage`.
* **Immersive UI:** Square minimap with directional arrows, enemy stealth (only visible on map if firing), compass, and low-ammo warnings.
* **Fullscreen & PWA Ready:** Custom fullscreen toggle and CSS overrides to prevent accidental mobile browser gestures (pull-to-refresh).

---

## 🎮 How to Play

### Desktop Controls
* **Move:** `W` `A` `S` `D`
* **Look:** Mouse
* **Fire:** Left Mouse Button
* **ADS (Aim):** Right Mouse Button
* **Sprint:** `Shift` (Hold)
* **Jump:** `Space`
* **Crouch:** `C`
* **Reload:** `R`
* **Switch Weapons:** `1` `2` `3` `4` `5`

### Mobile Controls
* **Move:** Left-side Joystick
* **Look:** Drag right side of screen
* **Fire & Aim:** Fire Button (Drag to aim)
* **ADS:** Scope Button
* **Sprint:** Run Button (Toggle)
* **Jump/Crouch/Reload:** Custom Action Buttons
* **Customize:** Go to Settings ⚙️ on the main menu to drag and resize buttons!

---

## 🛠 Technical Stack
* **Rendering:** [Three.js](https://threejs.org/) (r160)
* **Audio:** Web Audio API (Synthesized gunfire, footsteps, and UI sounds)
* **Logic:** Vanilla JavaScript (ES6 Modules)
* **Styling:** CSS3 (Flexbox, CSS Variables, Backdrop Filters)
* **Hosting:** Vercel / GitHub Pages compatible

---

## 🌍 World Generation & AI
The map is 100% procedurally generated on load. 
* **Terrain:** Uses a custom noise function to generate rolling hills, flat spawn areas, and deep trenches.
* **Vegetation & Rocks:** Dynamically clusters low-poly boulders, rock arches, pine trees, and fallen logs with dynamic collision bounding boxes.
* **AI Pathfinding:** Bots use distance-based target selection. If a bot is shot, it enters a "retaliate" state for 5 seconds. Otherwise, they prioritize opposing faction targets within a 60-unit radius, and wander dynamically when no targets are present.

---

## 🚀 Deployment

To run this game locally or deploy it yourself:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/TejUzumaki/warzone-lowpoly.git
   cd warzone-lowpoly
   ```
2. **Serve the directory:**
   Because the game uses ES6 modules, you must serve it over a local web server.
   ```bash
   npx serve .
   # or
   python -m http.server 8000
   ```
3. **Deploy to Vercel/Netlify:**
   Simply connect your GitHub repository to Vercel. No build step is required. The `index.html` is the only file you need.

---

<div align="center">
  <h3>Built with passion, code, and a lot of WebGL magic.</h3>
</div>
