# ⛩️ Anikage-group.github.io

Built using native WebGL (Three.js), modern CSS token systems, and zero external heavy video dependencies, Anikage-group.github.io renders procedurally lit 3D canvas environments alongside responsive, accessible web layouts.

---

## ✨ Key Features & Architecture

### 🎥 WebGL & Visual FX Engine
- **Procedural Lighting & Canvas Shader**: Built on `Three.js` with dynamic 2D/3D gradient noise, fbm canvas generation, and tangent-space normal map height calculations.
- **Atmospheric Effects**: Features runtime grain overlays, radial vignette shaders, and custom reactive glow emitters (e.g., dynamic flames and lantern glimmers).
- **Multi-Layer Parallax Foreground**: Layered SVG and WebP assets (temple walls, pine trees, tall grass, stone lanterns, sakura branches, shrine ruins) with natural swaying animations.

### 📱 Layout & Navigation
- **Chapter-Based Journey**: Interactive multi-section layout navigating through *The Gate* (About Us), *Pathways* (Featured Gallery), *Curriculum* (Project Index), and *Eternity* (Closing Lockup).
- **Dynamic Layout Toggles**: Configurable layout variations controlled via HTML `data-layout-*` attributes (e.g., `data-layout-hero="b"`, `data-layout-story="b"`).
- **Responsive Navigation Drawer**: Custom-built mobile overlay menu with locked scroll states and fluid transitions.
- **Progress Rail & Cursor Tracking**: Fixed visual chapter indicator rail alongside a spring-damped custom cursor dot with reactive hover scaling (`data-cursor`).

### ♿ Accessibility & Fallbacks
- **Reduced Motion Support**: Fully respects `prefers-reduced-motion: reduce` by disabling canvas loops, particle sway, and CSS transforms.
- **Non-WebGL Fallback (`no-webgl`)**: Gracefully degrades to CSS radial gradient backgrounds and high-impact wordmarks when WebGL is unavailable or disabled.

---

## 🛠️ Technology Stack

- **Core**: HTML5, CSS3 (Modern Tokens & Variables), JavaScript (ES6+)
- **Graphics Engine**: [Three.js](https://threejs.org/) (WebGL rendering, procedural textures, normal mapping)
- **Frameworks & Tooling**: [Vite](https://vitejs.dev/), [Svelte](https://svelte.dev/)
- **Media Playback**: [Artplayer](https://artplayer.js.org/)
- **Typography**: Onest, Noto Sans JP

---

## 📁 Project Structure

```text
.
├── index.html                 # Main entry point & WebGL runtime script
├── assets/
│   ├── favicon.png            # Application favicon
│   ├── logo.png               # Anikage brand identity mark
│   ├── fonts.css              # Custom font declarations (Onest, NotoJP)
│   ├── three.min.js           # Three.js core library
│   ├── ReAnime/               # Project preview captures
│   │   ├── index.png
│   │   ├── home.png
│   │   └── anime.png
│   └── foreground/            # Multi-depth parallax PNG/WebP layers
│       └── png/
│           ├── temple-wall.webp
│           ├── pine-tree.webp
│           ├── tall-grass.webp
│           ├── stone-lantern.webp
│           ├── sakura-branch.webp
│           └── shrine-ruins.webp
│
│
└── README.md                  # Project documentation
```

---

## 💻 Local Development Setup

To run this site locally without any build tool requirements:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Anikage-Group/Anikage-group.github.io
   cd Anikage-group.github.io
   ```

2. **Serve the directory:**
   Since the project utilizes ES modules and web assets, serve it via any static HTTP server:
   
   *Using Python 3:*
   ```bash
   python -m http.server 8000
   ```

   *Using Node (`serve` or `http-server`):*
   ```bash
   npx serve .
   ```

3. **Open in browser:**
   Navigate to `http://localhost:8000` (or the provided local port).

---

## 🔗 Official Links & Community

- **GitHub Organization**: [github.com/Anikage-Group](https://github.com/Anikage-Group)
- **Flagship Repository**: [Anikage-Group/AniKage](https://github.com/Anikage-Group/Anikage-group.github.io)

---

<p align="center">
  <b>The Anikage Group</b> — Crafting modern anime web experiences.
</p>
