---
name: Playful Learning
colors:
  surface: '#fbf8ff'
  surface-dim: '#d3d8ff'
  surface-bright: '#fbf8ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f4f2ff'
  surface-container: '#ececff'
  surface-container-high: '#e5e6ff'
  surface-container-highest: '#dee1ff'
  on-surface: '#001159'
  on-surface-variant: '#414754'
  inverse-surface: '#00218d'
  inverse-on-surface: '#f0efff'
  outline: '#727785'
  outline-variant: '#c2c6d6'
  surface-tint: '#005ac2'
  primary: '#0058bd'
  on-primary: '#ffffff'
  primary-container: '#1470e8'
  on-primary-container: '#fefcff'
  inverse-primary: '#adc6ff'
  secondary: '#7a5900'
  on-secondary: '#ffffff'
  secondary-container: '#fcbc05'
  on-secondary-container: '#6b4e00'
  tertiary: '#1f6a00'
  on-tertiary: '#ffffff'
  tertiary-container: '#298600'
  on-tertiary-container: '#f8ffee'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#d8e2ff'
  primary-fixed-dim: '#adc6ff'
  on-primary-fixed: '#001a41'
  on-primary-fixed-variant: '#004494'
  secondary-fixed: '#ffdea2'
  secondary-fixed-dim: '#fcbc05'
  on-secondary-fixed: '#261900'
  on-secondary-fixed-variant: '#5c4200'
  tertiary-fixed: '#84fe58'
  tertiary-fixed-dim: '#69e03e'
  on-tertiary-fixed: '#052100'
  on-tertiary-fixed-variant: '#165200'
  background: '#fbf8ff'
  on-background: '#001159'
  surface-variant: '#dee1ff'
typography:
  display-lg:
    fontFamily: Quicksand
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: Quicksand
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
  headline-md:
    fontFamily: Quicksand
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
  headline-sm:
    fontFamily: Quicksand
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  body-lg:
    fontFamily: Quicksand
    fontSize: 20px
    fontWeight: '500'
    lineHeight: 30px
  body-md:
    fontFamily: Quicksand
    fontSize: 18px
    fontWeight: '500'
    lineHeight: 28px
  label-caps:
    fontFamily: Lexend
    fontSize: 14px
    fontWeight: '700'
    lineHeight: 20px
    letterSpacing: 0.05em
rounded:
  sm: 0.5rem
  DEFAULT: 1rem
  md: 1.5rem
  lg: 2rem
  xl: 3rem
  full: 9999px
spacing:
  base: 8px
  xs: 4px
  sm: 12px
  md: 24px
  lg: 48px
  xl: 64px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 80px
---

## Brand & Style

The design system is engineered for an immersive, joyful, and educational experience tailored specifically for children. The brand personality is exuberant, encouraging, and safe. It aims to evoke a sense of wonder and accomplishment, turning every interaction into a small celebration.

The visual style is **Tactile and Playful**, blending modern card-based layouts with high-contrast elements and soft, "squishy" physical metaphors. By using depth, vibrant primary colors, and friendly geometry, the interface feels less like a tool and more like a digital toy box. Every element is oversized and approachable, ensuring that the UI reduces cognitive load and invites exploration.

## Colors

This design system utilizes a high-energy palette of primary and secondary colors to define clear functional zones. 

- **Primary Blue:** Used for core navigation and "active" learning states.
- **Secondary Yellow:** Reserved for rewards, highlights, and "Eureka" moments.
- **Tertiary Green:** Signifies progress, success, and "Go" actions.
- **Vibrant Orange/Red:** Used sparingly for critical alerts or to draw attention to specific errors in a non-threatening way.

The background should remain a very soft, warm off-white or a faint pastel tint of the primary blue to keep the focus on the vibrant interactive components. Text contrast must remain high (Deep Navy instead of pure Black) to ensure readability for early readers.

## Typography

The typography in the design system is centered around **Quicksand** for its rounded terminals and friendly, open counters. This choice mirrors the handwriting found in early childhood education materials. 

**Lexend** is introduced for labels and functional UI elements to maximize readability, as it was specifically designed to reduce visual stress. 

- **Scale:** Type sizes are intentionally larger than standard applications to accommodate developing motor skills and lower reading speeds.
- **Hierarchy:** Use "Display" sizes for game titles and success screens. Headlines should be used for instructions, while Body-lg is the default for any reading content.
- **Color:** Avoid light grey text. Use the deep neutral or primary blue shades for all text to maintain accessibility.

## Layout & Spacing

The layout philosophy uses a **Fixed Grid** model to ensure that interactive cards and game elements remain consistent and predictable.

- **Desktop:** A 12-column grid with a max-width of 1200px. Large margins (80px) focus the child's attention on the center-stage content.
- **Mobile/Tablet:** A 4 or 8-column grid with generous 24px gutters to prevent accidental taps on neighboring elements.
- **Spacing Rhythm:** We use an 8px base unit, but most component spacing should favor the `md` (24px) or `lg` (48px) units to create "breathable" layouts that don't feel cluttered. 

Content is organized into large "Activity Cards" that stack vertically on mobile and form a balanced masonry or grid layout on larger screens.

## Elevation & Depth

Depth in this design system is conveyed through **Tactile Layering**. We avoid realistic skeuomorphism in favor of a "Soft-Physical" look:

1.  **Chunky Shadows:** Interactive elements use a 0-blur or low-blur shadow with a slight vertical offset (4px to 8px). This creates a "lifted" effect, making buttons look like physical blocks.
2.  **State-Based Depth:** When a button is pressed, the shadow offset reduces to 0px or 1px, and the element moves downward, simulating a physical click.
3.  **Tonal Stacking:** Backgrounds use very light tints of a color, while interactive containers use pure white or saturated colors with thick, playful borders (3px-4px).
4.  **Soft Blurs:** Background blurs are used only for modal overlays to keep the focus strictly on the foreground task.

## Shapes

The shape language is dominated by **maximum roundedness**. There are no sharp corners in this design system. 

- **Components:** Standard buttons and chips utilize the `pill` (level 3) shape. 
- **Cards:** Large containers use `rounded-xl` (3rem) to maintain a soft, friendly perimeter.
- **Borders:** Many interactive elements feature a "Keyline" border—a 3px to 4px solid stroke in a darker shade of the element's fill color—adding to the illustrated, cartoon-like quality.

## Components

### Buttons
Buttons are the primary interaction point. They must be "chunky" (minimum height of 64px). They feature a solid bottom shadow that matches the border color. On hover, they might grow slightly (1.05x scale), and on click, they physically "depress."

### Activity Cards
Cards are white with a thick 4px colored border. They should include a "Header Icon" area where a playful illustration introduces the card's content.

### Inputs & Selection
Checkboxes and Radio buttons are oversized (32px x 32px) and use a "Stamp" metaphor. When selected, they fill with a vibrant color and trigger a small bounce animation.

### Progress Bars
Progress bars should be thick and utilize a "liquid" fill effect. As the bar fills, it should change color from Primary Blue to Tertiary Green to signal completion.

### Feedback Toasts
Toasts appear as "Speech Bubbles" from a mascot or character, using the same rounded card style but with a small directional arrow (caret) to indicate the speaker.