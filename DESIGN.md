---
name: UniTask
colors:
  surface: '#13131b'
  surface-dim: '#13131b'
  surface-bright: '#393841'
  surface-container-lowest: '#0d0d15'
  surface-container-low: '#1b1b23'
  surface-container: '#1f1f27'
  surface-container-high: '#292932'
  surface-container-highest: '#34343d'
  on-surface: '#e4e1ed'
  on-surface-variant: '#c7c5d7'
  inverse-surface: '#e4e1ed'
  inverse-on-surface: '#303038'
  outline: '#908fa0'
  outline-variant: '#464554'
  surface-tint: '#c0c1ff'
  primary: '#c0c1ff'
  on-primary: '#1000a9'
  primary-container: '#494bd6'
  on-primary-container: '#d6d5ff'
  inverse-primary: '#494bd6'
  secondary: '#40e0cb'
  on-secondary: '#003731'
  secondary-container: '#00c3af'
  on-secondary-container: '#004a42'
  tertiary: '#cdbdff'
  on-tertiary: '#370096'
  tertiary-container: '#6833ea'
  on-tertiary-container: '#ded2ff'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#e1e0ff'
  primary-fixed-dim: '#c0c1ff'
  on-primary-fixed: '#06006c'
  on-primary-fixed-variant: '#2f2ebe'
  secondary-fixed: '#62fae4'
  secondary-fixed-dim: '#3cddc8'
  on-secondary-fixed: '#00201c'
  on-secondary-fixed-variant: '#005047'
  tertiary-fixed: '#e8deff'
  tertiary-fixed-dim: '#cdbdff'
  on-tertiary-fixed: '#20005f'
  on-tertiary-fixed-variant: '#4f00d0'
  background: '#13131b'
  on-background: '#e4e1ed'
  surface-variant: '#34343d'
typography:
  display-lg:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.3'
  title-sm:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: '1.4'
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1'
    letterSpacing: 0.05em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 4px
  xs: 0.5rem
  sm: 1rem
  md: 1.5rem
  lg: 2rem
  xl: 3rem
  container-padding: 1.25rem
  gutter: 1rem
---

## Brand & Style

This design system is engineered for high-achieving academics who require a focused, premium environment to manage complex schedules. The brand personality is sophisticated, futuristic, and calm, evoking the feeling of a high-end digital sanctuary. 

The visual style is **Glassmorphism**, utilized to create a sense of depth and hierarchy within a dark, immersive space. By layering translucent surfaces over vibrant, blurred "blobs" of color, the design system achieves a sense of weightlessness. The interface prioritizes clarity and focus, using light as a primary navigator through subtle glows and precise borders.

## Colors

The palette is anchored by a deep, monochromatic background (#13131b) that minimizes eye strain during late-night study sessions. The primary accent is a dynamic gradient transitioning from Indigo to Teal, symbolizing the flow from deep focus to creative clarity. 

Glass surfaces use a very low opacity white fill to maintain "dark mode" integrity while providing enough contrast to define shape. Accent colors for status indicators (e.g., "Submitted Late") should use high-saturation reds or ambers, but remain constrained to small, semantic elements to avoid breaking the ethereal aesthetic.

## Typography

This design system utilizes **Inter** for its exceptional legibility and neutral, modern character. For Hebrew (RTL), ensure that the font weights are balanced to match the Latin counterparts. 

- **Headlines:** Use tight letter spacing and heavier weights to create a strong visual anchor.
- **Body Text:** Increased line height (1.6) is used to maintain readability on dark backgrounds.
- **RTL Support:** All typography styles must support right-to-left alignment automatically, ensuring text containers mirror correctly for Hebrew users without losing the sophisticated hierarchy.

## Layout & Spacing

The layout philosophy follows a **Fluid Grid** model, allowing task lists and cards to expand gracefully across mobile and tablet devices. A 4px baseline grid ensures vertical rhythm.

Large, blurred background "blobs" are positioned at varying depths (z-index) to provide a non-linear sense of space. These blobs should move slightly or change scale based on the view to maintain a living, organic feel. Content containers utilize generous internal padding (1.5rem) to ensure the glassmorphisn effects have enough "breathing room" to be visible behind the text.

## Elevation & Depth

Elevation in this design system is conveyed through **Glassmorphism** and backdrop filters rather than traditional shadows. 

1. **Base Layer:** The solid #13131b background with animated color blobs.
2. **Glass Layer:** Translucent surfaces with `backdrop-blur: 12px`. Each layer adds a 0.4 opacity white tint.
3. **Stroke Definition:** Every elevated element must have a 1px "inner" border using `rgba(255, 255, 255, 0.12)` on the top and left, and a slightly darker tint on the bottom and right to simulate light hitting a glass edge.
4. **Active State:** When an item is selected or active, it uses the primary gradient instead of the glass effect to pull it to the highest visual plane.

## Shapes

The shape language is consistently **Rounded**, using a 0.5rem (8px) base radius. Larger containers, such as task cards and modals, should use `rounded-xl` (1.5rem) to emphasize the soft, premium feel of the glass panels. Buttons and input fields use the base `rounded-lg` (1rem) for a friendly yet structured appearance.

## Components

- **Buttons:** Primary buttons use the Indigo-to-Teal gradient with white text. Secondary buttons are "ghost glass" (transparent background with a glass border).
- **Cards:** Task cards feature a 12px backdrop blur and a 0.4 opacity background. Status indicators (dots) are placed in the top-right (LTR) or top-left (RTL).
- **Inputs:** Input fields are dark glass panels with subtle 1px borders. On focus, the border transitions to a Teal solid stroke with a soft outer glow.
- **Chips/Labels:** Used for categories and due dates. These should be semi-opaque fills of the accent colors (Indigo/Teal) with reduced font sizes.
- **Lists:** Course folders use an accordion-style glass panel that expands to reveal a nested list of tasks.
- **RTL Mirroring:** All icons within components (e.g., chevron-right, folder icons) must flip horizontally when the interface is set to Hebrew.