# Style Guides

## Introduction

A style guide is a documented set of design standards that define the visual language of a product, brand, or organization. It specifies colors, typography, spacing, iconography, imagery, and tone—creating a single source of truth that ensures consistency across teams, platforms, and time. Style guides answer the question: "How should this brand/product look and feel?" and empower designers to make confident, aligned decisions.

Style guides evolved from branding guidelines (logo usage, color palettes) to encompass comprehensive UI design systems. Modern style guides document not just what components look like, but when to use them, how they behave, and why decisions were made. They bridge design and development, enabling scalable, maintainable products where every screen feels like part of a unified whole.

Creating a style guide requires distilling design decisions into reusable rules and patterns. It's equal parts documentation, governance, and communication tool—ensuring that everyone from designers to developers to stakeholders speaks the same visual language. A good style guide evolves with the product while maintaining core principles and consistency.

## Learning Objectives

By mastering Style Guides, you will be able to:

- Create comprehensive style guides covering [[Colors]], [[Typography]], [[Spacing]], [[Iconography]], and [[Components]]
- Document [[Design Tokens]] for consistent, scalable design
- Organize style guides for easy navigation and adoption
- Communicate design decisions and rationale in documentation
- Transition from style guides to full [[Design-Systems]]
- Maintain and evolve style guides as products grow
- Create both [[Brand Style Guides]] and [[UI Style Guides]]

## Key Knowledge Points

### Style Guide Fundamentals

- [[Style Guide]]

  - Documented design standards
  - Visual and verbal consistency
  - Reference for designers, developers, marketers
  - **Types:**
    - [[Brand Style Guide]]: Logo, colors, tone, photography (marketing focus)
    - [[UI Style Guide]]: Components, patterns, interactions (product focus)
    - [[Editorial Style Guide]]: Voice, grammar, terminology (content focus)

- **Purpose of Style Guides:**
  - [[Consistency]] across team and time
  - [[Speed]] (decisions already made)
  - [[Scalability]] (onboard new team members)
  - [[Quality Control]] (maintain standards)
  - [[Handoff]] (designers → developers)
  - [[Brand Integrity]]

### Core Style Guide Sections

#### 1. Colors

- [[Color Palette]]

  - **Primary Colors:** Brand identity (2-3 colors)
  - **Secondary Colors:** Supporting palette
  - **Neutral Colors:** Grays, backgrounds
  - **Semantic Colors:**
    - Success (green)
    - Warning (yellow/orange)
    - Error (red)
    - Info (blue)
  - **Each color includes:**
    - Name (e.g., "Brand Blue", "Primary")
    - Hex, RGB, HSL values
    - Usage notes ("Use for CTAs")
    - [[Accessibility]] (contrast ratios with white/black)
    - Tints and shades (5-10 variants: 50, 100, 200...900)

- [[Color Usage Guidelines]]
  - When to use each color
  - Color meaning and symbolism
  - Accessibility requirements (WCAG AA/AAA)
  - Light/dark theme variations
  - See [[Color-Theory]], [[Contrast-and-Accessibility]]

#### 2. Typography

- [[Type System]]

  - **Font Families:**
    - Primary font (body text)
    - Secondary font (headlines, optional)
    - Monospace font (code)
  - **Type Scale:** H1, H2, H3, H4, H5, H6, Body, Caption, Overline
  - **For each style:**
    - Font family, weight, size
    - Line height, letter spacing
    - Color
    - Use cases ("H1 for page titles")
  - See [[Typography]], [[Type-Hierarchy]]

- [[Typography Usage]]
  - Hierarchy rules
  - Responsive scaling
  - Line length guidelines (45-75 characters)
  - Accessibility (minimum sizes)

#### 3. Spacing & Layout

- [[Spacing System]]

  - [[8-Point Grid]] (4, 8, 16, 24, 32, 40, 48, 56, 64, 80px)
  - Or T-shirt sizes (XS, S, M, L, XL, 2XL, 3XL)
  - **Usage:**
    - Component padding
    - Margins between elements
    - Section spacing
  - See [[White-Space]], [[8-Point Grid]]

- [[Grid System]]

  - Column grids (4, 8, 12 columns)
  - Gutter sizes
  - Margins
  - Breakpoints
  - See [[Grid-Systems]]

- [[Layout Principles]]
  - Alignment rules
  - Responsive behavior
  - Max-widths for content

#### 4. Iconography

- [[Icon Style]]
  - Style (outlined, filled, duotone)
  - Stroke weight
  - Corner radius
  - Grid size (24x24px, 32x32px)
  - Color usage
- [[Icon Library]]
  - Catalog of available icons
  - Naming conventions
  - Usage guidelines (when to use which icon)
  - File formats (SVG preferred)
  - Accessibility (always pair with text label or aria-label)

#### 5. Imagery & Photography

- [[Photography Style]]

  - Mood, lighting, composition
  - Subject matter (people, products, lifestyle)
  - Filters, color grading
  - Dos and don'ts (examples)

- [[Illustration Style]]

  - Visual style (flat, geometric, hand-drawn)
  - Color usage
  - When to use illustrations vs. photos

- [[Image Specifications]]
  - Aspect ratios
  - File formats (JPG, PNG, WebP)
  - Optimization guidelines
  - Responsive sizing

#### 6. Components

- [[Component Documentation]]

  - For each component:
    - **Visual:** What it looks like (all states)
    - **Usage:** When to use, when not to use
    - **Anatomy:** Parts and their names
    - **Behavior:** Interactions, states
    - **Code:** Markup/component name
    - **Accessibility:** ARIA labels, keyboard navigation
    - **Examples:** Real-world usage
  - See [[UI-Components]], [[Components-and-Variants]]

- [[Component Library]]
  - Buttons (primary, secondary, tertiary, ghost, icon)
  - Inputs (text, textarea, select, checkbox, radio, toggle)
  - Navigation (header, sidebar, tabs, breadcrumbs)
  - Feedback (modals, toasts, tooltips, alerts)
  - Data display (tables, cards, lists)
  - Full catalog with live examples

#### 7. Voice & Tone

- [[Voice Guidelines]]

  - Brand personality (friendly, professional, playful)
  - Vocabulary (industry terms, jargon)
  - Grammar and style (sentence length, active voice)

- [[Tone Variations]]

  - Success messages (encouraging)
  - Error messages (helpful, not blaming)
  - Empty states (motivating)
  - Onboarding (welcoming)

- [[Writing Examples]]
  - Good and bad examples
  - Templates for common messages

### Design Tokens

- [[Design Tokens]]
  - Named design decisions
  - Platform-agnostic values
  - **Examples:**
    - `color-primary: #0066CC`
    - `spacing-md: 16px`
    - `font-size-h1: 32px`
  - **Benefits:**
    - Single source of truth
    - Easy global updates
    - Translates to code (CSS variables, Sass, JSON)
  - See [[Design-Tokens]]

### Style Guide Organization

- **Common Structures:**

  1. **Foundations:** Colors, Typography, Spacing, Iconography
  2. **Components:** UI components with documentation
  3. **Patterns:** Common UI patterns and flows
  4. **Resources:** Downloads, tools, contact

- **Formats:**

  - [[Living Style Guide]]: Web-based, updated automatically (Storybook, ZeroHeight)
  - [[Static Documentation]]: PDF, Figma file (less ideal, gets outdated)
  - [[Component Playground]]: Interactive examples (best for developers)

- **Tools:**
  - [[Figma]] (design & documentation)
  - [[Zeroheight]] (style guide website from Figma)
  - [[Storybook]] (component explorer for developers)
  - [[Notion]] / [[Confluence]] (documentation)

### Style Guide Best Practices

- **Make It Accessible:**

  - Easy to find (central location)
  - Searchable
  - Organized logically
  - Up-to-date

- **Make It Actionable:**

  - Clear dos and don'ts
  - Code examples
  - Downloadable assets
  - Copy-paste values

- **Make It Collaborative:**

  - Version control (track changes)
  - Contribution guidelines (how to propose changes)
  - Feedback mechanism
  - Stakeholder buy-in

- **Make It Living:**

  - Update regularly
  - Announce changes
  - Deprecation process
  - Evolution not revolution

- **Show, Don't Just Tell:**
  - Visual examples
  - Real UI screenshots
  - Before/after comparisons
  - Interactive demos

### From Style Guide to Design System

- [[Design System]] = Style Guide + Component Library + Guidelines + Culture
- **Progression:**
  1. **Ad-hoc** (no standards)
  2. **Style Guide** (documented standards)
  3. **Component Library** (reusable code/design)
  4. **Design System** (comprehensive, governed, cultural)
- See [[Design-Systems]]

## Related Topics

- [[Design-Systems]]
- [[Design-Tokens]]
- [[Component-Libraries]]
- [[Brand Identity]]
- [[Typography]]
- [[Color-Theory]]
- [[UI-Components]]
- [[Documentation]]

## Tools & Resources

- [[Figma]] (design & documentation)
- [[Zeroheight]] (generate style guide sites from Figma)
- [[Storybook]] (component documentation for devs)
- [[Notion]] (documentation platform)
- Example style guides:
  - Material Design Guidelines
  - Apple Human Interface Guidelines
  - Shopify Polaris
  - IBM Design Language
  - Atlassian Design System

## Practice Exercises

1. **Mini Style Guide:** Create a basic style guide for a fictional product: 8 colors, 5 text styles, spacing scale, 5 components. Document in Figma.

2. **Component Documentation:** Choose 3 UI components. Document each with: states, usage, anatomy, accessibility, code example.

3. **Brand Analysis:** Find 3 brand style guides (Google "brand guidelines PDF"). Analyze structure, content, strengths, weaknesses.

4. **Audit & Document:** Audit an existing product's visual design. Extract and document: colors used, typography styles, spacing patterns. Create retroactive style guide.

5. **Living Style Guide:** Use Zeroheight or similar to create a web-based style guide from your Figma components. Include navigation, search, and live examples.

## Further Reading

- "Design Systems" by Alla Kholmatova
- "Atomic Design" by Brad Frost
- Material Design Guidelines (comprehensive example)
- Shopify Polaris (excellent documentation)
- "Building Design Systems" (Smashing Magazine articles)
- Examples: styleguides.io (collection of real style guides)
