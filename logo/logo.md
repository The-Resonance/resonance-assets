# Resonance Logo Embed Guide

The Resonance logo lives in this repository so you can reference it directly from any front-end without copying files around.

---

## 1. CDN Embed (HTML)

```html
<img src="https://cdn.jsdelivr.net/gh/The-Resonance/resonance-assets/images/Logo/Logo.svg" 
     alt="Resonance logo" width="239" height="38">
```

This points at the master lime-on-dark variant. Swap the filename with `Logo-1.svg` (forest) or `Logo-2.svg` (ivory) if you need a different treatment.

---

## 2. React Component

```bash
pnpm add @resonance/assets
```

```tsx
import Logo from "@resonance/assets/logo";

export function Header() {
  return (
    <header className="flex items-center gap-4">
      <Logo aria-label="Resonance" />
      <h1 className="text-xl font-ritual">Resonance</h1>
    </header>
  );
}
```

---

## 3. CSS Background

```css
.logo {
  background-image: url("https://cdn.jsdelivr.net/gh/The-Resonance/resonance-assets/images/Logo/Logo.svg");
  width: 239px;
  height: 38px;
  background-size: contain;
  background-repeat: no-repeat;
}
```

---

## 4. Usage Rules

1. Maintain **0.5×** logo height of clear space on all sides.
2. Minimum digital width: **80 px**.
3. Never recolor outside the approved variants or apply distortion effects.

---

> Need another file format or size? Open an issue or ping the Resonance design team.

© Resonance Studios 