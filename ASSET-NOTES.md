# 🎨 Asset Notes & Design Specifications

This document provides architectural details, design rules, color palettes, and SVG animation mechanics for the `@sanketchute17` GitHub profile package.

---

## 🎨 Color Palette & Design Tokens

The visual theme uses a high-contrast dark theme inspired by modern developer portfolios:

| Element | Color Hex | Usage |
| :--- | :--- | :--- |
| **Deep Navy Background** | `#070b16` | Main container background |
| **Card Surface** | `#0d1527` / `#0f192e` | Nested card backgrounds |
| **Electric Blue** | `#247bff` | Primary accent, orbits, borders, links |
| **Cyan Glow** | `#00c6ff` | Highlight tags, laser beams, status indicators |
| **Crimson Red** | `#ff354f` | Secondary accent, badges, warning signals |
| **Off-White Primary Text** | `#ffffff` / `#f8fafc` | Headings, name, primary titles |
| **Muted Secondary Text** | `#94a3b8` | Subtext, bullet descriptions, dates |

---

## 📁 Asset Directory Breakdown

### 1. `assets/hero.svg` (850 x 340 px)
- **Role**: Greeting, name reveal, role badge, location tag, and floating developer avatar.
- **Animations**:
  - `fadeIn`: Greeting badge text smooth fade-in.
  - `slideUp`: Name reveal upward motion transition.
  - `pulse`: Status indicator glowing green & red pulses.
  - `float`: Right-hand avatar card floating animation.

### 2. `assets/about-life.svg` (850 x 360 px)
- **Role**: Presents 3 core engineering pillars (AI & ML, Full-Stack Cloud, Systems & Database).
- **Facts**: Based strictly on resume capabilities (PINN, LLM tutors, Web Bluetooth, React 18, FastAPI, RESTful APIs). No personal hobbies claimed.

### 3. `assets/stack.svg` (850 x 430 px)
- **Role**: Categorized tech stack chips (Languages, Frontend, Backend, Databases/Tools) with an animated right-side orbit diagram.
- **Animations**:
  - `rotateOrbit`: Continuous 360° spin of orbiting tech nodes.
  - `nodePulse`: Pulsing glow on central core node and satellite nodes.

### 4. `assets/id-dashboard.svg` (850 x 360 px)
- **Role**: Animated developer ID card displaying verified credentials, education (RTMNU B.Tech AI 8.2 CGPA, MSBTE Diploma 80.97%), featured projects, and work experience.
- **Animations**:
  - `scanLine`: Vertical glowing blue scanner beam animating across the card.

### 5. `assets/connect.svg` (850 x 320 px)
- **Role**: Contact grid with 4 clear cards (Email, LinkedIn, Portfolio, GitHub) paired with a generic pointing developer avatar graphic on the left.
- **Animations**:
  - `pointPulse`: Glowing laser beam animation pointing to contact cards.

### 6. `assets/avatar.svg` & `assets/pointing-avatar.svg` (200 x 200 px)
- **Role**: Generic tech developer avatars featuring glowing visors, headset detail, and tech accents.

---

## ♿ Accessibility & Reduced-Motion Mechanics

All SVGs incorporate standard `@media (prefers-reduced-motion: reduce)` CSS rules:

```css
@media (prefers-reduced-motion: reduce) {
  .pulse-dot, .float-avatar, .orbit-line, .scan-line {
    animation: none !important;
    opacity: 1 !important;
  }
}
```

This ensures that users with motion sensitivity or low-power devices receive clean, fully legible static renderings.
