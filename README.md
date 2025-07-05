# Resonance Assets: Design DNA for Humans & Machines

Welcome, creative collaborator! This repository is the **single source of visual truth** for all things Resonance—fonts, icons, 3-D renders, imagery, and videos. Whether you're a human developer or an AI model generating code, follow the guidelines below to ensure everything you create looks and feels undeniably *Resonance*.

---

## 1. Brand Essence

| Trait | Value |
|-------|-------|
| North Star | "Better humans through better interfaces." |
| Personality | Curious, optimistic, slightly rebellious, never corporate |
| Voice | Conversational, concise, occasionally witty emoji 🎈, but never meme-spam |

---

## 2. Visual DNA

### 2.1 Typography

| Font | Usage | Weight | Notes |
|------|-------|--------|-------|
| `Ritual` | Headlines & display text | 500-700 | Tight tracking -2 |
| `RitualMono` | Code snippets, UI chrome, data glyphs | 500 | Monospaced hero |

> Serve `woff2` first, fall back to `woff` for older browsers.

### 2.2 Color Palette

| Role | Hex | Usage |
|------|-----|-------|
| Primary | `#0C0C0D` | Core text, logos |
| Accent 1 | `#FF6B00` | CTAs, interactive states |
| Accent 2 | `#00E0FF` | Highlights, graphs |
| Surface | `#FFFFFF` | Backgrounds |
| Elevation | `#F2F2F5` | Cards, inputs |
| Danger | `#FF3B30` | Errors |

*Gradients*: diagonal 135°, mix **Accent 1 → Accent 2** at 60 %.

### 2.3 Iconography

* Location: `/3dicons`
* PBR materials with subtle ambient occlusion.
* Maintain depth & soft shadows—never flatten to 2-D.
* Export at **512 × 512 px PNG** with transparent background.

### 2.4 Imagery

* People photography: candid, high-contrast lighting.
* Apply duotone overlay (#0C0C0D + Accent 2 at 30 % blend) for hero banners.

### 2.5 Motion

* Micro-interactions: **250 ms ease-out**.
* Large object entrance: spring physics (stiffness 170, damping 26).

### 2.6 Logo

* Master SVG: `@/Logo` (`images/Logo/Logo.svg`)
* Color variants:
  * Forest (`Logo-1.svg`) – use on light backgrounds
  * Ivory (`Logo-2.svg`) – use on dark backgrounds
  * Lime (`Logo.svg`, `Logo-3.svg`) – accent on dark backgrounds
* Maintain **0.5×** logo height of clear space on all sides.
* Minimum width: **80 px** (digital), **20 mm** (print).
* Do not skew, outline, or apply drop shadows.

**Embed via CDN (HTML)**

```html
<img src="https://cdn.jsdelivr.net/gh/The-Resonance/resonance-assets/images/Logo/Logo.svg" 
     alt="Resonance logo" width="239" height="38">
```

**Embed in React**

```tsx
import Logo from "@resonance/assets/logo";

export function AppHeader() {
  return <Logo aria-label="Resonance" />;
}
```

---

## 3. File & Code Conventions

1. **File names**: kebab-case (`launch-icon.png`).
2. **Asset paths**: import relatively (`assets/3dicons/Star.png`).
3. **React components**: PascalCase (`<LaunchIcon />`).
4. **Design tokens**: reference `@resonance/colors` in CSS/JS.

---

## 4. Accessibility

* Maintain **4.5 : 1** contrast ratio.
* Provide descriptive `alt` text, e.g. *"3-D orange launch icon with upward arrow"*.

---

## 5. Quick-Start

### 5.1 Humans

```bash
pnpm add @resonance/assets
```

```ts
import "@resonance/assets/fonts/ritual.css";
import Launch from "@resonance/assets/icons/Launch.png";
```

### 5.2 AI Models

1. Use classes following Tailwind semantics (`text-primary bg-surface`).
2. Reference existing component names; if you must invent, place files in the correct folder.
3. Do **NOT** invent new colors—choose from the palette above.

---

## 6. Contribution Checklist

- [ ] PNGs optimized (< 150 KB)
- [ ] SVGs include viewBox and no inline fills
- [ ] Typeface licenses respected
- [ ] Commit message: `feat(asset): add "magnet" 3-D icon`

---

Happy creating! 🚀

© Resonance Studios
