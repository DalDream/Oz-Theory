---
name: Division 1 OS
colors:
  surface: '#051424'
  surface-dim: '#051424'
  surface-bright: '#2c3a4c'
  surface-container-lowest: '#010f1f'
  surface-container-low: '#0d1c2d'
  surface-container: '#122131'
  surface-container-high: '#1c2b3c'
  surface-container-highest: '#273647'
  on-surface: '#d4e4fa'
  on-surface-variant: '#bbc9cd'
  inverse-surface: '#d4e4fa'
  inverse-on-surface: '#233143'
  outline: '#859397'
  outline-variant: '#3c494c'
  surface-tint: '#2fd9f4'
  primary: '#8aebff'
  on-primary: '#00363e'
  primary-container: '#22d3ee'
  on-primary-container: '#005763'
  inverse-primary: '#006877'
  secondary: '#adc6ff'
  on-secondary: '#002e6a'
  secondary-container: '#0566d9'
  on-secondary-container: '#e6ecff'
  tertiary: '#d6dcf5'
  on-tertiary: '#2a3043'
  tertiary-container: '#bac0d8'
  on-tertiary-container: '#484e62'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#a2eeff'
  primary-fixed-dim: '#2fd9f4'
  on-primary-fixed: '#001f25'
  on-primary-fixed-variant: '#004e5a'
  secondary-fixed: '#d8e2ff'
  secondary-fixed-dim: '#adc6ff'
  on-secondary-fixed: '#001a42'
  on-secondary-fixed-variant: '#004395'
  tertiary-fixed: '#dce1fb'
  tertiary-fixed-dim: '#c0c6de'
  on-tertiary-fixed: '#151b2d'
  on-tertiary-fixed-variant: '#40465a'
  background: '#051424'
  on-background: '#d4e4fa'
  surface-variant: '#273647'
  interface-bg: '#000000'
  panel-bg: '#020617'
  status-clear: '#22d3ee'
  status-clouded: '#fbbf24'
  status-danger: '#ef4444'
  terminal-text: '#e2e8f0'
typography:
  display-lg:
    fontFamily: JetBrains Mono
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  headline-md:
    fontFamily: JetBrains Mono
    fontSize: 20px
    fontWeight: '600'
    lineHeight: '1.4'
    letterSpacing: 0.05em
  body-base:
    fontFamily: Hanken Grotesk
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  body-sm:
    fontFamily: Hanken Grotesk
    fontSize: 14px
    fontWeight: '400'
    lineHeight: '1.5'
  label-data:
    fontFamily: Space Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.2'
    letterSpacing: 0.1em
  label-terminal:
    fontFamily: Space Mono
    fontSize: 13px
    fontWeight: '400'
    lineHeight: '1.4'
spacing:
  unit: 4px
  gutter: 16px
  margin-mobile: 20px
  margin-desktop: 40px
  panel-gap: 12px
---

## Brand & Style

The design system is an institutional, high-stakes tactical interface designed for the Public Safety Bureau. It rejects "user-friendly" softness in favor of **Clinical Militarism** and **Functional Authoritarianism**. The brand personality is cold, precise, and high-fidelity, evoking the sensation of operating a lethal tool within a surveillance state.

The aesthetic follows a **Modern Futuristic** movement with **Terminal-Style** influences. It prioritizes data density and situational awareness over decorative whitespace. Visual tension is maintained through sharp geometries, glowing data-viz accents, and a "HUD" (Heads-Up Display) feel that suggests every interaction is being logged by a higher authority.

**Key Visual Principles:**
- **The Obsidian Canvas:** A nearly-black environment where light is used strictly for data signaling, not decoration.
- **The Glowing Edge:** Thin, luminous borders (Cyan/Blue) represent "active" status and digital encryption.
- **Atmospheric Noise:** Subtle scanline overlays and low-opacity grid backgrounds to ground the UI in a hardware-specific reality.
- **Zero-Curve Discipline:** Minimal use of rounded corners to maintain a rigid, official, and professional tone.

## Colors

The palette is optimized for low-light, high-contrast environments. The background is a "Pure Black" to maximize the luminosity of the cyan and blue data elements.

- **Primary (Cyan #22d3ee):** Used for "Active" states, holographic borders, and successful mission status (SECURED). It represents the "Clear" Hue.
- **Secondary (Clinical Blue #3b82f6):** Used for official directives, secondary data points, and standard structural elements.
- **Functional Accents:**
    - **Amber/Yellow (#fbbf24):** Indicates "Slightly Clouded" status or "DEFERRED" missions.
    - **Crimson (#ef4444):** Reserved for "Operation Caution," High Crime Coefficients, and critical system warnings.
- **Neutrals:** Shades of deep navy provide depth for nested panels, while muted slate grays are used for non-essential monospaced meta-data.

## Typography

The typography system relies on a "Hybrid Technical" approach. 

1. **JetBrains Mono (Headlines):** Used for all primary navigation and screen headers. Large-scale headings should be uppercase to mimic official Bureau documentation.
2. **Hanken Grotesk (Body):** Used for mission descriptions and Akane’s dialogue. Its clean, sharp sans-serif nature ensures high readability for long-form investigation reports while remaining modern.
3. **Space Mono (Data/Labels):** Used for status scores, timestamps, and "Terminal" input fields. The monospaced nature reinforces the feeling of a system-generated log.

**Text Styles:**
- All labels and headers should favor **Uppercase** styling with slightly increased letter spacing (tracking) to mimic radar or CRT displays.
- Use **Cyan** for monospaced data fields to differentiate system-active text from narrative text.

## Layout & Spacing

This design system utilizes a **Fixed Grid within a Fluid Container**. The interface should feel like a multi-panel dashboard where information is "slotted" into specific sectors.

- **Grid Model:** 12-column grid for desktop; 4-column grid for mobile.
- **Rhythm:** A 4px baseline grid governs all internal padding.
- **Sectioning:** Use explicit "Dividers" rather than whitespace to separate content. In this system, whitespace is seen as "wasted bandwidth."
- **Mobile Reflow:** On mobile, mission cards stack vertically, but the "Status Bar" (Hue/Stability) remains pinned to the top as a persistent HUD element.
- **Borders:** Panels should be defined by 1px solid borders in deep navy (#020617) or cyan (#22d3ee) for active focus.

## Elevation & Depth

Depth is conveyed through **Tonal Layering** and **Luminous Outlines** rather than traditional shadows.

- **Base Layer:** Pure Black (#000000).
- **Surface Layer:** Deep Navy (#020617) with a subtle 10% opacity cyan "glow" on the top border.
- **Interactive Layer:** Elements that are interactive (buttons, cards) use a 1px Cyan border with a 0 0 8px Cyan outer glow to simulate a holographic projection.
- **Scanning Textures:** A global overlay of 2px height horizontal scanlines at 3% opacity creates the feel of a CRT monitor.
- **Backdrop Blurs:** When modals appear, they should use a heavy backdrop blur (12px) with a 40% opacity black tint, maintaining the focus on the "Terminal" without losing the environmental context.

## Shapes

The shape language is strictly **Geometric and Sharp (0px roundedness)**. 

- **Primary Shapes:** Rectangles with hard 90-degree angles.
- **The "Angled Corner" Motif:** To add a futuristic "Bureau" feel, certain container corners (top-left or bottom-right) can be clipped at a 45-degree angle (8px-12px chamfer) to signify "official" tactical windows.
- **Dividers:** Horizontal rules should be thin (1px) and punctuated with small squares at the ends to indicate "End of Data Stream."

## Components

### Buttons & Inputs
- **Primary Tactical Button:** Solid Cyan background with black uppercase JetBrains Mono text. No rounded corners. Hover state: 1px Cyan border with transparent background and Cyan text.
- **Terminal Input:** Transparent background, 1px Cyan border on bottom only. Leading prompt character `>` in mono font.
- **Mission Cards:** Deep navy background, 1px Blue border. The header of the card should be a solid Blue bar with White text. Status (LOCK-ON) should be a high-contrast tag in the top right.

### Status Indicators
- **Hue Meter:** A horizontal segmented bar (10 segments). Fill segments based on Hue status (Cyan for clear, Yellow for clouded, Red for caution).
- **Stability Score:** Large, centered JetBrains Mono number with a "Scanning" animation overlay.

### Secure Channel (Chat)
- **Kogami (User):** Left-aligned, bordered boxes with a "User ID" label at the top.
- **Akane (AI):** Right-aligned, slightly tinted Blue background to distinguish "Official Inspector" directives.
- **Timestamp:** Every message must be prefixed with a monospaced ISO-8601 timestamp in 10px text.

### Investigation Reports
- **Format:** Structured like a legal document. Use monospaced font for the "Analysis" headers and Hanken Grotesk for the "Assessment" paragraphs. Use 1px dotted lines to separate report sections.
