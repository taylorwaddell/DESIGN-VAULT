# Auto-Layout

## Introduction

Auto-Layout is Figma's most powerful feature for creating responsive, flexible designs that adapt to content changes automatically. It transforms static frames into intelligent containers that resize, reflow, and maintain spacing rules—mimicking how CSS Flexbox works in code. Mastering Auto-Layout is the difference between rigid, brittle designs and production-ready interfaces that handle real-world content variability.

Before Auto-Layout, designers manually adjusted every element when content changed—a tedious, error-prone process. Auto-Layout automates this, enabling designs that grow with content, stack dynamically, and maintain consistent spacing without manual intervention. It's essential for building [[Components]], [[Design-Systems]], and responsive layouts that developers can implement faithfully.

Auto-Layout thinking requires a shift from pixel-perfect positioning to rules-based design. You define spacing, padding, and alignment rules; Figma handles the math. This systematic approach scales beautifully, making designs more maintainable and closer to how they'll be coded.

## Learning Objectives

By mastering Auto-Layout, you will be able to:

- Add Auto-Layout to frames and understand when to use it vs. manual positioning
- Control [[Spacing Between Items]] and [[Padding]] systematically
- Switch between [[Horizontal Layout]] and [[Vertical Layout]] layouts
- Use [[Hug Contents]] and [[Fill Container]] resize behaviors effectively
- Create responsive components that adapt to content changes
- Nest Auto-Layout frames to create complex, flexible layouts
- Apply [[Advanced Auto-Layout]] features (absolute positioning, wrapping, canvas stacking)
- Build production-ready components that match developer expectations

## Learning Objectives

By mastering Auto-Layout, you will be able to:

- Add Auto-Layout to frames and understand when to use it vs. manual positioning
- Control [[Spacing Between Items]] and [[Padding]] systematically
- Switch between [[Horizontal]] and [[Vertical]] directions
- Use [[Hug Contents]], [[Fill Container]], and [[Fixed Size]] resize behaviors
- Create responsive components that adapt to content changes
- Nest Auto-Layout frames to build complex, flexible layouts
- Apply [[Alignment and Distribution]] settings
- Build production-ready components using Auto-Layout principles

## Key Knowledge Points

### Auto-Layout Fundamentals

- [[Auto-Layout]]

  - Figma's responsive layout engine
  - Based on [[Flexbox]] concepts from CSS
  - Add to frame: Shift + A
  - Transforms frame into Auto-Layout frame
  - Purple outline indicator

- **When to Use Auto-Layout:**
  - Buttons (text + icon, adapts to label length)
  - Cards (content stacks vertically)
  - Lists (items stack with consistent spacing)
  - Navigation bars (items distribute horizontally)
  - Form fields (label, input, helper text stack)
  - Any component that needs to resize with content

### Direction

- [[Direction]]
  - [[Horizontal Layout]] (→)
    - Items flow left-to-right
    - Use for: nav bars, button groups, breadcrumbs
  - [[Vertical Layout]] (↓)
    - Items flow top-to-bottom
    - Use for: cards, forms, lists, articles
  - Toggle: Click direction icon in properties panel

### Spacing

- [[Spacing Between Items]]

  - Gap between child elements
  - Consistent spacing (e.g., 8px, 16px, 24px)
  - Related to [[8-Point Grid]]
  - Keyboard: Set in properties panel or use inspector

- [[Padding]]
  - Space between frame edges and content
  - Can be:
    - Uniform (all sides equal)
    - Horizontal + Vertical
    - Individual (top, right, bottom, left)
  - Typical values: 16px, 24px, 32px
  - Related to [[White-Space]]

### Resize Behaviors

- [[Hug Contents]]

  - Frame shrinks/grows to fit child content
  - No extra space
  - Use for: buttons, tags, badges, pills
  - Auto-width based on text length

- [[Fill Container]]

  - Child stretches to fill available space in parent
  - Use for: backgrounds, dividers, full-width elements
  - Flexible sizing

- [[Fixed Size]]
  - Element maintains specific width/height
  - Doesn't respond to content or parent changes
  - Use when precise dimensions required

### Alignment & Distribution

- [[Alignment]]
  - Horizontal: Left, Center, Right
  - Vertical: Top, Center, Bottom
  - Controls how items align within Auto-Layout frame
- [[Distribution]]
  - [[Packed]]: Items grouped together
  - [[Space Between]]: Items spread with space between
  - Horizontal stacks: distribute along width
  - Vertical stacks: distribute along height

### Advanced Features

- [[Absolute Position]]

  - Remove item from Auto-Layout flow
  - Position manually (like CSS `position: absolute`)
  - Use for: overlays, badges, notifications
  - Right-click layer → "Absolute position"

- [[Canvas Stacking]]

  - Controls z-order within Auto-Layout
  - First on top vs. Last on top
  - Affects overlapping elements

- [[Text Baseline Alignment]]

  - Align text by baseline instead of bounding box
  - Better optical alignment for mixed text sizes

- [[Negative Spacing]]

  - Overlap items intentionally
  - Use for: avatars, layered effects

- [[Auto-Layout Wrapping]]
  - Items wrap to next row/column when space runs out
  - Experimental feature
  - Use for: tags, pills, responsive grids

### Nesting Auto-Layout

- [[Nested Auto-Layout]]

  - Auto-Layout frames inside Auto-Layout frames
  - Build complex layouts from simple rules
  - Example structures:
    - **Card:** Vertical parent → horizontal image row → vertical content stack
    - **Nav Bar:** Horizontal parent → logo (fixed) → nav links (packed) → actions (space between)
    - **Form:** Vertical parent → multiple field groups (each a vertical auto-layout)

- **Best Practices:**
  - Keep nesting logical and minimal
  - Name layers clearly ("Content Stack", "Button Row")
  - Use consistent spacing values throughout

### Auto-Layout + Components

- [[Auto-Layout Components]]
  - Components with Auto-Layout become truly reusable
  - Content changes, component adapts
  - Examples:
    - Button: text changes length, button resizes
    - Card: different content lengths, card grows/shrinks
    - List item: varying text, consistent spacing maintained
  - See [[Components-and-Variants]]

## Related Topics

- [[Figma-Basics]]
- [[Components-and-Variants]]
- [[Responsive-Design]]
- [[8-Point Grid]]
- [[White-Space]]
- [[UI-Components]]
- [[Design-Systems]]

## Tools & Resources

- Figma Auto-Layout Playground (official tutorial file)
- Figma YouTube: Auto-Layout tutorials
- Auto-Layout cheat sheet (Figma Community)
- [[Flexbox]] documentation (web development parallel)

## Practice Exercises

1. **Button Family:** Create 5 button variants (small, medium, large, icon-only, icon-left) using Auto-Layout. Test with different text lengths.

2. **Responsive Card:** Build a card component (image, title, description, button) using nested Auto-Layout. Resize from 280px to 400px wide and ensure it adapts gracefully.

3. **Navigation Bar:** Create a nav bar with logo (left), nav links (center), and user menu (right) using space-between distribution. Should work at 375px and 1440px widths.

4. **Form Layout:** Design a multi-field form (label, input, helper text, error state) where each field is an Auto-Layout component. Stack 5 fields with consistent spacing.

5. **List with Mixed Content:** Create a list where each item has variable content (some have images, some don't; varying text lengths). Use Auto-Layout to maintain consistent spacing.

6. **Tag/Chip System:** Build a tag component that wraps text with padding. Create a container where multiple tags wrap to multiple rows (using wrap feature).

## Further Reading

- Figma: Auto-Layout Documentation
- "Figma Auto-Layout: Complete Guide" (YouTube)
- Auto-Layout best practices (Figma Community)
- CSS Flexbox Guide (parallel learning for developers)
