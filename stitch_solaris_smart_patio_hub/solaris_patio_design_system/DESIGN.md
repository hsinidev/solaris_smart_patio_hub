---
name: Solaris-Patio Design System
colors:
  surface: '#fcf9f5'
  surface-dim: '#dcdad6'
  surface-bright: '#fcf9f5'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f6f3ef'
  surface-container: '#f0ede9'
  surface-container-high: '#eae8e4'
  surface-container-highest: '#e5e2de'
  on-surface: '#1c1c1a'
  on-surface-variant: '#45474d'
  inverse-surface: '#31302e'
  inverse-on-surface: '#f3f0ec'
  outline: '#75777d'
  outline-variant: '#c5c6cd'
  surface-tint: '#545e76'
  primary: '#051125'
  on-primary: '#ffffff'
  primary-container: '#1b263b'
  on-primary-container: '#828da7'
  inverse-primary: '#bbc6e2'
  secondary: '#a03f30'
  on-secondary: '#ffffff'
  secondary-container: '#fe8672'
  on-secondary-container: '#741f13'
  tertiary: '#171006'
  on-tertiary: '#ffffff'
  tertiary-container: '#2d2519'
  on-tertiary-container: '#988c7b'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#d7e2ff'
  primary-fixed-dim: '#bbc6e2'
  on-primary-fixed: '#101b30'
  on-primary-fixed-variant: '#3c475d'
  secondary-fixed: '#ffdad4'
  secondary-fixed-dim: '#ffb4a7'
  on-secondary-fixed: '#400200'
  on-secondary-fixed-variant: '#80281b'
  tertiary-fixed: '#efe0cd'
  tertiary-fixed-dim: '#d2c4b2'
  on-tertiary-fixed: '#221a0f'
  on-tertiary-fixed-variant: '#4f4538'
  background: '#fcf9f5'
  on-background: '#1c1c1a'
  surface-variant: '#e5e2de'
typography:
  display-lg:
    fontFamily: Montserrat
    fontSize: 34px
    fontWeight: '700'
    lineHeight: 42px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Montserrat
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.01em
  title-sm:
    fontFamily: Montserrat
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
  body-lg:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 26px
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  label-caps:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.08em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 8px
  xs: 4px
  sm: 12px
  md: 20px
  lg: 32px
  xl: 48px
  container-margin: 20px
  gutter: 16px
---

## Brand & Style

The design system is anchored in an **Atmospheric-Premium** aesthetic, blending the technical precision of smart home control with the emotional warmth of outdoor living. It targets a high-end audience seeking seamless integration between technology and comfort.

The UI style utilizes a **Glassmorphic-Tactile** hybrid approach. Semi-transparent "frosted" layers evoke the airiness of a patio environment, while soft, ambient shadows provide the depth needed for a premium feel. The interface feels "alive" through the use of **Glow effects** (diffuse box-shadows and inner glows) specifically reserved for active heating and lighting states, simulating the physical warmth of the hardware it controls. The experience is mobile-first, prioritizing large, ergonomic touch targets and high-readability contrast ratios.

## Colors

This design system uses a palette inspired by natural elements:
- **Navy Blue (#1B263B):** Used for primary text, deep structural elements, and night-mode states to provide a grounding, high-contrast foundation.
- **Terracotta (#C05746):** The primary action color, representing warmth and human connection. It is used for active states, primary buttons, and heating indicators.
- **Sand (#F5E6D3):** A soft background and secondary surface color that maintains a "warm-light" atmosphere without the harshness of pure white.
- **Glow Accent:** A specialized orange-gold glow is applied to heating icons and active "Comfort Zones" to provide immediate visual feedback of thermal activation.

The default mode is **Light**, but it utilizes the Sand tone as the canvas to maintain the "atmospheric" requirement.

## Typography

The typography strategy balances geometric strength with utilitarian clarity. **Montserrat** is used for headlines to provide an "architectural" and premium feel, reflecting the physical structures of smart shading. Its high x-height and bold weights ensure maximum impact on mobile screens.

**Inter** is utilized for all body copy and interface labels. Its neutral, systematic nature ensures that technical data (temperatures, percentages, timers) is instantly legible. High contrast is maintained by using Navy Blue for primary text on Sand backgrounds, ensuring accessibility in outdoor high-glare environments.

## Layout & Spacing

This design system employs a **Fluid Mobile-First Grid**. The layout relies on a 4-column system for mobile devices with 20px outer margins to prevent thumb-crowding. 

Spacing follows a strict 8px rhythmic scale. Components like control cards and sliders use "MD" (20px) padding to create a breathable, premium feel. Vertical stack spacing is generous to accommodate the "atmospheric" aesthetic, ensuring no single screen feels cluttered with data.

## Elevation & Depth

Depth is communicated through three specific layers:
1.  **The Base (Sand):** The ground-level canvas, opaque and matte.
2.  **The Glass Layer (Backdrop-blur):** Used for secondary controls and navigation bars. These elements use a `blur(12px)` effect and a `1px` semi-transparent white border to simulate polished glass.
3.  **The Active Layer (Soft Shadows):** Primary interaction cards use a multi-layered ambient shadow (`0px 10px 30px rgba(27, 38, 59, 0.08)`) to appear elevated.

Active heating elements do not use traditional shadows; they use **Outer Glows** in Terracotta to signify energy and warmth emanating from the component.

## Shapes

The design system uses a **Rounded** shape language to feel approachable and organic. 
- **Standard Cards:** 1rem (16px) corner radius.
- **Buttons & Inputs:** 0.5rem (8px) for a more structured, precise feel.
- **Control Sliders:** Use pill-shaped (full-round) ends for handles to emphasize the "sliding" physical metaphor.
Buttons never use sharp corners, ensuring the "comfort" brand pillar is visually reinforced.

## Components

### Buttons
- **Primary:** Terracotta background, Sand text, subtle elevation shadow.
- **Secondary/Glass:** Backdrop-blur with a 1px Navy Blue outline at 20% opacity.

### Control Cards
Cards house the main smart features (Shade, Heat, Light). They use the Sand background but transition to a soft Glassmorphic state when "Off" and gain a subtle Navy Blue inner-border when "On."

### Heating Glow Sliders
A bespoke slider component where the track "warms up" from Sand to Terracotta as the user drags. The handle emits a `box-shadow: 0 0 15px #C05746` when active.

### Chips & Status Indicators
Small, pill-shaped badges used for "Eco-Mode" or "Scheduled." These use Navy Blue text on a 10% opacity Navy Blue background to remain subtle but professional.

### Inputs
Text fields and selection menus use a high-contrast bottom border and a slightly darker Sand tint for the fill area, ensuring they are easily identifiable as interactive fields.