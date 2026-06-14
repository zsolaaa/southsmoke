---
name: Smoked & Charred
colors:
  surface: '#121414'
  surface-dim: '#121414'
  surface-bright: '#38393a'
  surface-container-lowest: '#0c0f0f'
  surface-container-low: '#1a1c1c'
  surface-container: '#1e2020'
  surface-container-high: '#282a2b'
  surface-container-highest: '#333535'
  on-surface: '#e2e2e2'
  on-surface-variant: '#e6beb2'
  inverse-surface: '#e2e2e2'
  inverse-on-surface: '#2f3131'
  outline: '#ad897e'
  outline-variant: '#5c4037'
  surface-tint: '#ffb59e'
  primary: '#ffb59e'
  on-primary: '#5e1700'
  primary-container: '#ff571a'
  on-primary-container: '#521300'
  inverse-primary: '#ae3200'
  secondary: '#ffb4a8'
  on-secondary: '#690000'
  secondary-container: '#e60000'
  on-secondary-container: '#fff6f5'
  tertiary: '#c9c6c5'
  on-tertiary: '#313030'
  tertiary-container: '#929090'
  on-tertiary-container: '#2a2a29'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#ffdbd0'
  primary-fixed-dim: '#ffb59e'
  on-primary-fixed: '#3a0b00'
  on-primary-fixed-variant: '#852400'
  secondary-fixed: '#ffdad4'
  secondary-fixed-dim: '#ffb4a8'
  on-secondary-fixed: '#410000'
  on-secondary-fixed-variant: '#930100'
  tertiary-fixed: '#e5e2e1'
  tertiary-fixed-dim: '#c9c6c5'
  on-tertiary-fixed: '#1c1b1b'
  on-tertiary-fixed-variant: '#474646'
  background: '#121414'
  on-background: '#e2e2e2'
  surface-variant: '#333535'
typography:
  display-lg:
    fontFamily: Anton
    fontSize: 72px
    fontWeight: '400'
    lineHeight: '1.1'
    letterSpacing: 0.02em
  headline-lg:
    fontFamily: Anton
    fontSize: 48px
    fontWeight: '400'
    lineHeight: '1.2'
  headline-lg-mobile:
    fontFamily: Anton
    fontSize: 36px
    fontWeight: '400'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Anton
    fontSize: 32px
    fontWeight: '400'
    lineHeight: '1.2'
  body-lg:
    fontFamily: Montserrat
    fontSize: 18px
    fontWeight: '600'
    lineHeight: '1.6'
  body-md:
    fontFamily: Montserrat
    fontSize: 16px
    fontWeight: '500'
    lineHeight: '1.5'
  label-lg:
    fontFamily: Montserrat
    fontSize: 14px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: 0.1em
spacing:
  unit: 8px
  gutter: 24px
  margin: 32px
  container-max: 1280px
---

## Brand & Style
The design system embodies the raw, visceral energy of live-fire cooking. It is built for a brand that celebrates the grit of the smokehouse—rugged, heavy, and unapologetically bold. The target audience is the BBQ enthusiast who values tradition, heat, and high-quality craft.

The visual style is **High-Contrast / Bold** with elements of **Tactile** design. It rejects minimalism in favor of "visual weight," using heavy borders, glowing "ember" effects, and a layered approach that suggests heat and depth. The UI should feel like a cast-iron skillet: durable, blackened by fire, and glowing with potential.

## Colors
The palette is dominated by the "Charcoal" (#0a0a0a) background, providing a deep, infinite canvas for high-heat accents. 

- **Ember Orange (#ff4d00):** The primary action color, representing the hottest part of the coal. Used for primary buttons and critical paths.
- **Glowing Red (#e60000):** The secondary accent, used for alerts, spicy indicators, or secondary highlights.
- **Smoke White (#f5f5f5):** The primary text color, ensuring high legibility against the dark background while avoiding the sterile feel of pure white.
- **Ash Gray (#4a4a4a):** Used for borders and secondary text to provide subtle structure without breaking the dark aesthetic.

## Typography
Typography is the primary driver of the "heavy" aesthetic. 

**Anton** is used for all headlines and display text. It must always be set in uppercase with slight tracking to enhance its monolithic, architectural feel. 

**Montserrat** provides the balance for body copy. Use Medium (500) and SemiBold (600) weights as the default to maintain the "rugged" look even in long-form text. Avoid weights below 500 to ensure the text doesn't feel thin or fragile against the heavy background.

## Layout & Spacing
The layout follows a **Fixed Grid** model on desktop and a fluid model on mobile. 

- **Desktop:** 12-column grid with wide 24px gutters. Use large margins (32px+) to give the heavy elements room to breathe.
- **Mobile:** 4-column grid with 16px gutters and 20px margins.
- **Spacing Rhythm:** Use a strict 8px base unit. For high-impact areas, use "Chunky Spacing"—larger gaps (64px+) between major sections to emphasize the scale of the content.

## Elevation & Depth
In this dark, rugged environment, depth is created through "heat" rather than traditional shadows.

- **Internal Glows:** Instead of drop shadows, active elements use inner glows and outer "bloom" effects (0px 0px 15px primary_color_hex) to look like they are radiating heat.
- **Textured Layers:** Use low-opacity grain or noise overlays on containers to mimic the texture of cast iron or charred wood.
- **Hard Borders:** Use thick, 2px borders for containers. Active states switch from an Ash Gray border to an Ember Orange border with an outer glow.

## Shapes
The design system utilizes **Sharp (0)** corners. Every element—buttons, input fields, cards, and images—should have hard, 90-degree angles to reinforce the rugged, industrial, and "meaty" nature of the brand. Avoid all rounded corners.

## Components
- **Buttons:** Primary buttons feature a vertical gradient from Ember Orange to Glowing Red. Text is black and uppercase. On hover, apply a "bloom" glow effect.
- **Chips/Tags:** Use a dark charcoal background with a 1px solid border. Use Montserrat Bold in uppercase for the label.
- **Cards:** Heavy 2px solid Ash Gray borders. No shadows. Backgrounds can use a subtle "smoke" texture or a very dark gray gradient.
- **Input Fields:** Dark backgrounds with a bottom-only 2px border that turns into a glowing Ember Orange line when focused.
- **Lists:** Separated by horizontal 2px lines with a rough, distressed appearance where possible.
- **Specialty Component (The "Sizzle" Meter):** A custom progress bar or rating component using a gradient from cold gray to glowing orange/red to represent heat or spice levels.

## OKLCH Token Map
```
--color-bg:      oklch(12% 0.008 30);   /* #121414 */
--color-surface: oklch(17% 0.010 28);   /* #1e2020 */
--color-ember:   oklch(60% 0.20 34);    /* #ff4d00 */
--color-coal:    oklch(45% 0.22 22);    /* #e60000 */
--color-ash:     oklch(78% 0.005 32);   /* #e2e2e2 */
--color-smoke:   oklch(52% 0.008 30);   /* #4a4a4a */
```

## Absolute Bans
- Bal oldali vastag akcentus-csík (`border-left` > 1px mint dekoráció)
- Gradiens szöveg (`background-clip: text`)
- Glassmorphism dekorációként
- Egyforma kártya-grid
- Modal kapcsolatfelvételhez — inline form az első opció
- Lekerekített sarkok (`border-radius > 0`)
- Fine dining esztétika (pasztell, könnyű betűk, bő fehér tér)