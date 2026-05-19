---
name: Pinpoint
description: Free online tool to get exact pixel coordinates and percentage positions from any image
colors:
  neutral-bg: "#0d0d0f"
  surface-bg: "#141417"
  hover-bg: "#1e1e21"
  border-subtle: "#2a2a2d"
  border-strong: "#e8e6e3"
  text-primary: "#e8e6e3"
  text-muted: "#8b8a88"
  accent: "#e8e6e3"
  accent-hover: "#c8c4be"
  sidebar-bg: "#0d0d0f"
  sidebar-text: "#e8e6e3"
  sidebar-muted: "#8b8a88"
  sidebar-faint: "#6b6a68"
  sidebar-border: "#2a2a2d"
  sidebar-hover: "#1e1e21"
typography:
  body:
    fontFamily: "'SF Mono', 'Segoe UI Mono', 'Roboto Mono', Menlo, monospace"
    fontSize: "13px"
    lineHeight: 1.5
  label:
    fontFamily: "'SF Mono', 'Segoe UI Mono', 'Roboto Mono', Menlo, monospace"
    fontSize: "12px"
    fontWeight: 600
    letterSpacing: "1px"
    textTransform: "uppercase"
  value:
    fontFamily: "'SF Mono', 'Segoe UI Mono', 'Roboto Mono', Menlo, monospace"
    fontSize: "13px"
    fontWeight: 500
  copy-feedback:
    fontFamily: "'SF Mono', 'Segoe UI Mono', 'Roboto Mono', Menlo, monospace"
    fontSize: "10px"
    fontWeight: 600
rounded:
  default: "4px"
  copy-feedback: "2px"
spacing:
  gutter: "24px"
  section-gap: "32px"
  inner-y: "8px"
  inner-x: "6px"
  button-y: "12px"
  button-x: "24px"
  input-y: "12px"
  drop-zone-y: "64px"
  drop-zone-x: "24px"
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "#ffffff"
    rounded: "0"
    padding: "12px 24px"
  button-primary-hover:
    backgroundColor: "#ffffff"
    textColor: "{colors.accent}"
    rounded: "0"
  reset-button:
    backgroundColor: "transparent"
    textColor: "{colors.text-primary}"
    rounded: "0"
    border: "1px solid {colors.border-subtle}"
  reset-button-hover:
    backgroundColor: "{colors.accent}"
    textColor: "#ffffff"
  url-input:
    backgroundColor: "transparent"
    textColor: "{colors.text-primary}"
    rounded: "0"
    padding: "12px"
  drop-zone:
    backgroundColor: "{colors.surface-bg}"
    rounded: "4px"
    border: "1px solid {colors.border-subtle}"
  info-row:
    padding: "8px 6px"
    rounded: "2px"
  marker:
    border: "1px solid {colors.accent}"
    rounded: "50%"
---

# Design System: Pinpoint

## 1. Overview

**Creative North Star: "The Drafting Table"**

Pinpoint is a single-purpose measurement tool: drop an image, click a point, read the coordinates. The interface treats every pixel as measurable data. Like a modern drafting table under controlled light, the tool is fully dark — the chrome recedes so the subject (the image) commands attention.

This system explicitly rejects over-designed tool aesthetics: no gradients, no glassmorphism, no dashboards, no decorative illustration.

**Key Characteristics:**
- Full dark theme — the interface recedes, the image commands
- Monospace throughout — every character is a measured unit
- Light-on-dark typography with warm off-white text
- Split-surface: dark chrome + light marker (white crosshair)
- Click-to-copy direct manipulation

## 2. Colors

A restrained dark palette. The interface is a dark room — the chrome is `#0d0d0f`, the image is the only illuminated surface.

### Neutral
- **BG Main** (`#0d0d0f`): Full-screen background. Very dark, subtle cool undertone. The room the image sits in.
- **Surface** (`#141417`): Drop zone, input groups. Slightly lighter than BG to sit forward.
- **Hover** (`#1e1e21`): Interactive hover and focus states. Just enough lift from the background.
- **Border Subtle** (`#2a2a2d`): Dividers, input strokes, section rules. Low-contrast on dark.

### Text
- **Text Primary** (`#e8e6e3`): Primary text and data values. Warm off-white for readability without blue-light glare.
- **Text Muted** (`#8b8a88`): Labels, secondary info, empty-state placeholders.

### Accent
- **Accent** (`#e8e6e3`): Interactive actions, focus rings. Light = active, dark = rest. The accent lightens on hover (`#c8c4be`).

### Sidebar
- **Sidebar BG** (`#0d0d0f`): Matches main BG — the sidebar and canvas are continuous dark surface, separated only by the border rule.
- **Sidebar Text** (`#e8e6e3`): Matches `--text-main`.
- **Sidebar Muted** (`#8b8a88`): Matches `--text-muted`.
- **Sidebar Faint** (`#6b6a68`): The quietest text — section labels, subtle metadata, branding.
- **Sidebar Border** (`#2a2a2d`): Matches `--border-subtle`.
- **Sidebar Hover** (`#1e1e21`): Matches `--bg-hover`.

## 3. Typography

**Mono Font:** `'SF Mono', 'Segoe UI Mono', 'Roboto Mono', Menlo, monospace`

**Character:** Monospace throughout. Every character occupies the same horizontal measure, which makes coordinate values visually align and tabulate naturally. The font choice is technical, not decorative.

### Hierarchy
- **Body** (400, 13px, 1.5): The default measure for all text. Labels, values, instructions, metadata.
- **Label** (600, 12px, 1.5, 1px letter-spacing, uppercase): Section headers and column labels. The uppercase + letter-spacing pattern creates a clear taxonomy without adding visual weight.
- **Value** (500, 13px, tabular-nums): Raw coordinate values and data points. `font-variant-numeric: tabular-nums` ensures digit alignment across values.
- **Copy Feedback** (600, 10px): Inline confirmation after copy action. Smallest type, highest weight.

## 4. Elevation

**The Flat Rule.** All surfaces are coplanar. No shadows, no z-depth, no elevation. The image is the only depth cue. The sidebar rests beside the canvas, not above it. This is a measurement tool; simulated depth would interfere with measurement.

## 5. Components

### Buttons
- **Shape:** Sharp — zero border-radius (0). Rectangular, mechanical.
- **Primary ("Load"):** Light background (`#e8e6e3`) with dark text (`#0d0d0f`). On hover, inverts — dark bg, light text. Transition in 200ms ease-out. Uppercase 12px, 600 weight, 0.5px letter-spacing.
- **Reset ("Load New Image"):** Ghost style on dark sidebar — transparent, light text (`#e8e6e3`), subtle border (`#2a2a2d`). On hover, bg darkens to `#0d0d0f`, border becomes light.

### Input / URL Field
- **Style:** Sharp zero-radius inset stroke. Transparent background (inherits `#141417` surface). Mono 13px, light text (`#e8e6e3`). On focus, background shifts to Hover (`#1e1e21`). The Load button attaches flush-right with a 1px intervening border.

### Drop Zone
- **Shape:** Rounded (`4px` radius). Subtle dashed-rectangle border (`1px solid #2a2a2d`) on dark surface (`#141417`). On hover or drag-over, border turns accent (`#e8e6e3`) and background shifts to Hover (`#1e1e21`).
- **Padding:** `64px` top/bottom, `24px` left/right. Generous clearance around the instruction text.
- **Internal URL bar:** Full-width input + button group bounded at `400px` max, centered.

### Info Row
- **Style:** Horizontal label-value pair with dashed bottom border. `8px` vertical, `6px` horizontal padding (expanded to negative margins for hover state). On hover, background shifts to Hover Grey and the value text underlines — signaling clickability.
- **Copy feedback:** Ink pill (`#1a1c21`) with Paper (`#fcfaf7`) text appears over the row, pinned right, after a successful clipboard write. Fades in, waits 1s, fades out.

### Marker
- **Shape:** Circular ring (`22px` diameter, `1.5px` border) with centered crosshair lines. White (`#ffffff`) with a subtle outer shadow (`0 0 0 1px rgba(0,0,0,0.12)`) to stay visible on any image. Positioned via `transform: translate(-50%, -50%)` to center precisely on the click point. No fill — the image shows through.

### Sidebar
- **Structure:** Fixed `340px` right panel. Dark surface (`#0d0d0f`) with subtle border separation from the main canvas. All text is light-on-dark (`#e8e6e3`).
- **Header:** A crosshair icon (CSS-only, two intersecting lines) sits beside the "Pinpoint — Coordinate Inspector" label. This is the only visual mark in the sidebar; no logo, no image.
- **Coordinate Hero:** When an image loads, a three-row coordinate readout appears below the header showing X, Y, and percentage values. The hero acts as a live measurement display — always visible, always updated. It's separated from sections below by a thin rule.
- **Section Headers:** 10px uppercase label with a full-width hairline rule extending to the right (`::after`). Section headers are faint — the sections contain the data, the headers just organize it.
- **Info Rows:** 12px label on the left, 12px value on the right (tabular-nums). Subtle hover state fills the row background. Copy-on-click works on all rows. Highlight values get a text color bump, not a background chip.
- **Empty States:** 12px text, faint color, inline with row padding.
- **Footer:** Pushed to bottom with a top border rule. Contains the ghost reset button and brand link.

### Image Container
- **Style:** Full-flex canvas area. Dark surface (`#1e1e21`) with `4px` radius. The image sits directly in the wrapper — no shadow, no elevation, per The Flat Rule.

## 6. Do's and Don'ts

### Do:
- **Do** keep the interface dark (`#0d0d0f`) — the image is the only light source.
- **Do** use light accent (`#e8e6e3`) for buttons and interactive states.
- **Do** use monospace throughout — coordinates should tabulate.
- **Do** keep the image area free of chrome — the image is the subject.
- **Do** use direct click-to-copy on every data row.

### Don't:
- **Don't** mix light and dark surfaces — the entire chrome layer is a single dark tone.
- **Don't** use colored accents — light = active, dark = rest.
- **Don't** add dashboards, charts, or multi-panel layouts.
- **Don't** wrap the image in frames, cards, or containers with padding.
- **Don't** animate layout properties — ease only background, color, border-color, opacity.
- **Don't** use rounded buttons (radius > 0).
