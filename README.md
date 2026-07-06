# WARZONE: LOW POLY TACTICAL (v6.0)

A fast-paced, browser-based, 3D Battle Royale and Wave Survival game built entirely with Three.js and Vanilla JavaScript. No external assets, no game engines—everything from the 3D models to the sound effects is procedurally generated in code.

![Three.js](https://img.shields.io/badge/Three.js-r160-black) ![JavaScript](https://img.shields.io/badge/Vanilla-JS-yellow) ![Platform](https://img.shields.io/badge/Platform-Browser/WebGL-blue)

## 🎮 Game Modes

*   **Battle Royale:** Drop into a massive map with 24 AI bots. The dynamic safe zone shrinks over time. Scavenge for weapons, manage your inventory, and be the last one standing.
*   **Wave Survival:** Endure escalating waves of enemy AI. Eliminate them to earn health and ammo boosts. How long can you survive?

## ✨ Key Features (v6.0 Overhaul)

*   **3D Panorama Main Menu:** A fully rendered dynamic 3D lobby scene featuring your character, opposing bots, sandbags, and floating weapons. The camera orbits smoothly to showcase the scene.
*   **Military-Grade UI:** A strict charcoal and white aesthetic. No bright colors or cheap emojis.
*   **Inline SVG Icon System:** All HUD and gameplay buttons use crisp, scalable vector graphics for a clean, AAA-game feel.
*   **Smart Touch Controls:** 
    *   Dynamic Fire Button: Press to shoot, drag to aim simultaneously.
    *   ADS Sensitivity Scaling: Look sensitivity halves when aiming down sights for precision.
*   **Tactical Minimap:** Dark military-green background with distinct Red/Blue faction triangles for enemies and a White directional triangle for the player.
*   **Layout Editor:** Fully customizable HUD. Drag, resize, and save your button placements to `localStorage`.
*   **Procedural Audio:** All gunshots, footsteps, and UI clicks are synthesized in real-time using the Web Audio API.

## 🌍 World Generation

*   **Procedural Terrain:** Rolling hills, flat spawn areas, and deep trenches generated via math noise.
*   **Environmental Clutter:** Massive dodecahedron mountain ranges, rock arches, pine forests, fallen logs, and loot crates.
*   **Invisible Boundaries:** Walls extend deep downward to prevent graphical glitches at the map edges.

## 🤖 Enemy AI

*   **Two-Faction System:** Red and Blue bots prioritize fighting each other.
*   **Player Interaction:** Bots will ignore the player unless provoked, if the player gets too close, or if no enemy bots are nearby.
*   **Zone Awareness:** AI takes damage outside the safe zone and will dynamically pathfind back to the center.

## 🛠️ Tech Stack

*   **Rendering:** Three.js (r160)
*   **Audio:** Web Audio API
*   **Architecture:** Single-file `index.html` (HTML/CSS/JS combined)
*   **Hosting:** Vercel / GitHub

## 🚀 Deployment

To deploy the game locally or push an update to Vercel:

1. Clone the repository:
   ```bash
   git clone https://github.com/TejUzumaki/warzone-lowpoly.git
   cd warzone-lowpoly
   ```
2. To deploy to Vercel:
   ```bash
   vercel --prod --yes
   ```

## 📋 Controls

*   **Move:** WASD / Left Joystick
*   **Look:** Mouse / Right Screen Drag
*   **Fire:** Left Click / Fire Button (Drag to aim)
*   **Sprint:** Shift / Run Button (Toggle)
*   **ADS:** Right Click / Scope Button
*   **Jump:** Space / Jump Button
*   **Switch Weapon:** 1-5 / Swap Button
*   **Loot:** Walk near glowing crates

---
*Developed by TejUzumaki.*
