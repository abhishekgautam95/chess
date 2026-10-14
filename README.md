# ♟️ Wizard's Chess 3D — Gothic Altar

A fully playable, single-file 3D Wizard's Chess web application rendered in an atmospheric gothic cathedral setting. Built with **Three.js**, **Tailwind CSS**, and **Material Design 3**, featuring procedural textures, synthetic Web Audio combat sounds, dynamic shattering particle physics, an integrated AI opponent, and live tactical commentary powered by **Gemini AI**.

---

## 🔮 Highlights & Features

### 🏰 1. Gothic Cathedral Environment
* **Architectural Elements:** Ribbed vaulted columns, stone buttresses, an elevated sacrificial altar pedestal, and a stained-glass rose window casting atmospheric colored god-rays.
* **Atmosphere:** Dynamic shadow mapping, warm flickering torchlight sconces, deep exponential scene fog, and floating golden arcane ember motes.
* **Zero External 3D Assets:** All geometry and textures (Carrara marble veining and volcanic purple-cracked obsidian) are procedurally generated in memory using the HTML5 Canvas API and Three.js primitives.

### ⚔️ 2. Wizard's Combat & Particle Physics
* **Custom Piece Archetypes:** 32 stylized 3D chess pieces (Sentinels, War Steeds, Bastions, Scepters, and Sovereigns) accented with gold leaf (White) or dark glowing runic inlay (Black).
* **Parabolic Levitation Arc:** Moving pieces elevate and float toward destination squares using cubic easing curves.
* **Violent Shatter Physics:** Capturing an enemy piece violently pulverizes it into 36 tumbling geometric stone fragments with floor bouncing, camera shake, and impact decay.

### 🔊 3. Synthetic Web Audio Engine
* **No External Audio Files:** 100% synthesized in-browser audio via the Web Audio API.
* **Effects:**
  * Harmonic chimes on piece selection.
  * Resonant whoosh and deep stone clunk on landing.
  * Multi-frequency noise buffer burst combined with a sub-bass thump on piece destruction.

### 🧠 4. Chess Engine & Opponent AI
* **Full 8×8 Grid Rules Implementation:**
  * Pawn standard steps, initial double-moves, diagonal captures, and auto-promotion to Queen upon reaching the back rank.
  * Knight jumps, Rook horizontals/verticals, Bishop diagonals, Queen omnidirectional sliding, and King single-step moves.
  * King capture victory state and win banner modal.
* **Chronomancy (Undo):** Fully reversible turn stack tracking piece movements and resurrected captured meshes.
* **Heuristic AI Engine:** Built-in Black opponent evaluating moves via material weighting and capture priority.

### 🧙‍♂️ 5. The Archmage's Oracle (Gemini Integration)
* **Live Tactical Commentary (`gemini-3-flash-preview`):** Generates concise, immersive gothic reactions to captures, sacrifices, and tactical blunders.
* **Spoken Arcane Decrees (`gemini-2.5-flash-preview-tts`):** Synthesizes live prophecies and victory decrees into direct browser-playable voice audio via custom PCM16-to-WAV conversion.
* **Interactive Divination Drawer:** On-demand consulting to divine best moves, evaluate cosmic balance, or unleash obsidian incantations.

---

## 🛠️ Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **Three.js (r128)** | 3D scene rendering, lighting, camera animation, and procedural geometry |
| **Three.js OrbitControls** | Pan, orbit, and pinch-to-zoom camera controls |
| **Tailwind CSS** | Material 3 translucent glassmorphism surfaces and responsive UI |
| **Web Audio API** | Procedural sound generation (chimes, stone hits, explosive shatter) |
| **Google Fonts** | *Cinzel* (gothic display headings) & *Roboto* (Material body font) |
| **Material Symbols** | Modern icon set for all single-level navigation elements |
| **Gemini API** | Generative text commentary and speech synthesis (TTS) |

---

## 🚀 Getting Started

### Prerequisites
* Any modern web browser supporting WebGL and the Web Audio API (Chrome, Edge, Firefox, Safari, Brave).
* No Node.js build process, bundlers, or local server installations are strictly required; it runs directly as a standalone static HTML document.

### Quick Launch
1. Save the application source as `index.html`.
2. Double-click `index.html` to open it in your browser.
3. Drag with the primary mouse button to orbit the cathedral; scroll/pinch to zoom.

### Optional: Enabling the Archmage Gemini Oracle
To enable live AI commentary and voice synthesis:
1. Obtain an API key from [Google AI Studio](https://aistudio.google.com/).
2. Open `index.html` in an editor.
3. Locate the `GeminiArchmageService` class near line 340:
   ```javascript
   class GeminiArchmageService {
     constructor() {
       this.apiKey = "YOUR_GEMINI_API_KEY_HERE";
       // ...
     }
   }
   ```
4. Save the file and refresh your browser.

---

## 🎮 How to Play

### Controls & Interactions
* **Select Piece:** Left-click / tap on any of your pieces (Marble for White, Obsidian for Black).
* **View Valid Moves:** Valid targets illuminate with green glyph rings (movement) or crimson rings (combat captures).
* **Execute Move:** Click on an illuminated destination ring.
* **Orbit Camera:** Click and drag anywhere in the cathedral space.
* **Zoom:** Mouse scroll wheel or two-finger pinch.

### Top App Bar Controls
* **🤖 AI Mode:** Toggles between *2-Player Pass & Play* and *Solo vs Obsidian AI*.
* **✨ Oracle:** Opens the Archmage's divination dialog for strategy and analysis.
* **🎙️ Voice:** Toggles Gemini spoken audio decrees on or off.
* **🎥 Camera:** Switches between cinematic 3D perspective and top-down tactical altar view.
* **🔊 Audio:** Mutes or unmutes synthesized sound effects.
* **↩️ Undo:** Reverses the prior turn and restores destroyed pieces.
* **🔄 Reset:** Clears the board and starts a fresh match.

---

## 📁 File Structure

```
.
├── index.html       # Self-contained application: Three.js engine, procedural
│                    # shaders/textures, sound synth, chess rules, UI, and Gemini bridge.
└── README.md        # Comprehensive documentation and setup guide.
```

---

## 📜 License

Distributed under the MIT License. Free for personal, educational, and creative modification.
