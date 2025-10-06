# Mockups

## Introduction

Mockups are high-fidelity, static representations of interfaces that incorporate final visual design—colors, typography, imagery, icons, and polished details. They bridge the gap between structural [[Wireframes]] and interactive [[Hi-Fi-Prototyping]], providing pixel-perfect representations of what the final product will look like. Mockups answer the question: "What will this actually look like to users?"

Creating mockups requires applying all [[Visual Design Fundamentals]]—[[Color-Theory]], [[Typography]], [[Layout-and-Composition]], [[Design-Principles]]—to translate wireframe structures into aesthetically refined interfaces. Mockups are where brand personality emerges, visual hierarchy is perfected, and designs become production-ready assets that developers can implement faithfully.

In professional workflows, mockups serve multiple purposes: client presentations, stakeholder approvals, developer handoff specifications, and design system documentation. They represent the "design intent" that prototypes will bring to life and developers will code.

## Learning Objectives

By mastering Mockups, you will be able to:

- Transform [[Wireframes]] into high-fidelity mockups with complete visual design
- Apply [[Style-Guides]] and [[Design-Systems]] consistently across mockups
- Create pixel-perfect layouts that meet [[Accessibility]] standards
- Design mockups for multiple [[Breakpoints]] (mobile, tablet, desktop)
- Use [[Real Content]] vs. placeholder content effectively
- Prepare mockups for [[Developer Handoff]] with proper documentation
- Create [[Design Specs]] and annotations for implementation
- Manage mockup [[Version Control]] and iterations

## Key Knowledge Points

### Mockup Fundamentals

- [[Mockups]]

  - High-fidelity visual designs
  - Static (non-interactive, see [[Hi-Fi-Prototyping]] for interactive)
  - Pixel-perfect precision
  - Final colors, typography, imagery
  - Production-ready visual assets

- **Purpose of Mockups:**
  - [[Visual Design Approval]] (stakeholders sign off)
  - [[Developer Handoff]] (implementation specifications)
  - [[Design Documentation]] (what was designed and why)
  - [[Marketing Assets]] (screenshots, app store images)
  - [[Portfolio Presentation]]

### From Wireframe to Mockup

- **Progression:**

  1. Start with approved [[Wireframes]]
  2. Apply [[Style-Guides]] (colors, typography)
  3. Add [[Visual Hierarchy]] through size, weight, color
  4. Incorporate [[Brand Elements]] (logos, icons, imagery)
  5. Refine [[Spacing]] and [[Alignment]] (pixel-perfect)
  6. Add [[States]] (default, hover, active, error, etc.)
  7. Polish [[Micro-Details]] (shadows, borders, effects)

- **What Changes from Wireframe:**
  - Gray boxes → [[Brand Colors]]
  - Placeholder text → [[Real Typography]] with [[Type-Hierarchy]]
  - Shape placeholders → [[Icons]], [[Images]], [[Illustrations]]
  - Generic layouts → [[On-Brand Design]]
  - Basic structure → [[Visual Polish]]

### Visual Design Application

- [[Color Application]]

  - Apply [[Color-Theory]] and [[Color-Harmonies]]
  - Use [[Design Tokens]] from style guide
  - Ensure [[Contrast-and-Accessibility]] (WCAG AA minimum)
  - Define [[Primary Colors]], [[Secondary Colors]], [[Accent Colors]]
  - Surface colors, text colors, border colors

- [[Typography Application]]

  - Implement [[Type Scale]]
  - Establish clear [[Type-Hierarchy]]
  - Use proper [[Line Height]], [[Letter Spacing]]
  - Ensure readability (min 16px body text)
  - Apply [[Text Styles]] consistently

- [[Imagery & Media]]

  - Use high-quality [[Images]]
  - Consistent [[Image Treatment]] (cropping, filters, overlays)
  - [[Illustrations]] aligned with brand style
  - [[Icons]] (consistent size, stroke, style)
  - [[Placeholder Images]] (Unsplash, stock photos) for demos

- [[White-Space & Spacing]]
  - Apply [[8-Point Grid]] spacing
  - Use consistent [[Padding]] and [[Margins]]
  - Create [[Breathing Room]]
  - Balance density and clarity

### Responsive Mockups

- [[Breakpoints]]

  - Mobile: 375px, 414px (iPhone)
  - Tablet: 768px, 834px (iPad)
  - Desktop: 1280px, 1440px, 1920px
  - Design key breakpoints, not every size

- [[Responsive Design Considerations]]

  - Content reflow and stacking
  - Image sizing and cropping
  - Navigation adaptations (hamburger menu on mobile)
  - Typography scaling
  - Touch target sizes (min 44x44px on mobile)

- [[Mobile-First]] vs [[Desktop-First]]
  - Mobile-first: Start small, scale up
  - Desktop-first: Start large, scale down
  - Mobile-first often leads to clearer hierarchy

### Component States

- [[UI States]]

  - [[Default State]]
  - [[Hover State]]
  - [[Focus State]]
  - [[Active State]] / [[Pressed State]]
  - [[Disabled State]]
  - [[Error State]]
  - [[Loading State]]
  - [[Empty State]]
  - [[Success State]]

- **Best Practice:**
  - Design all states for interactive elements
  - Show states in mockups or separate state sheet
  - Document state behavior for developers

### Real Content vs. Placeholders

- [[Real Content]]

  - Actual copy (or close approximation)
  - Real data patterns (names, emails, numbers)
  - Exposes layout issues (long names, edge cases)
  - Better for testing and presentations

- [[Placeholder Content]]

  - Lorem Ipsum text
  - Stock photos
  - Generic labels
  - Useful for template design
  - Risky: hides real-world problems

- **Best Practice:**
  - Use real content whenever possible
  - Test with [[Edge Cases]] (very long text, no data, etc.)
  - Use [[Content-First Design]] approach

### Developer Handoff

- [[Design Specs]]

  - Measurements (padding, margins, sizes)
  - Colors (hex codes, RGB values)
  - Typography (font family, size, weight, line height)
  - Shadows and effects (blur, spread, opacity)
  - Border radii
  - Icon sizes and source files

- [[Figma Inspect Mode]]

  - Developers can inspect designs
  - Auto-generate CSS, iOS, Android code
  - Measure spacing
  - Copy style values

- [[Design Documentation]]

  - Annotations explaining interactions
  - Component usage guidelines
  - Content rules
  - Accessibility notes

- [[Asset Export]]
  - Export icons (SVG preferred)
  - Export images (@1x, @2x, @3x for mobile)
  - Provide design files (Figma links)
  - Icon fonts or sprite sheets

### Mockup Organization

- [[File Organization]]

  - Separate pages for different sections
  - Naming conventions (e.g., "Home - Desktop", "Profile - Mobile")
  - Version numbers or dates
  - Archive old versions

- [[Mockup Presentations]]
  - Create cover slides
  - Show context (device frames)
  - Include annotations
  - Before/after comparisons
  - Design rationale documentation

### Tools & Techniques

- [[Figma Mockups]]

  - Use [[Components-and-Variants]] for consistency
  - [[Auto-Layout]] for responsive flexibility
  - [[Styles]] for colors and typography
  - [[Plugins]] for content, mockups, optimization

- [[Mockup Plugins]] (Figma)
  - Unsplash (high-quality images)
  - Content Reel (realistic data)
  - Iconify (icon library)
  - Stark (accessibility checking)
  - Mockup generators (device frames)

## Related Topics

- [[Wireframing]]
- [[Hi-Fi-Prototyping]]
- [[Style-Guides]]
- [[Design-Systems]]
- [[Visual Hierarchy]]
- [[Typography]]
- [[Color-Theory]]
- [[Accessibility]]
- [[Responsive-Design]]
- [[Developer Handoff]]

## Tools & Resources

- [[Figma]] (primary tool)
- [[Sketch]] (Mac-only alternative)
- [[Adobe XD]]
- Device mockup generators (Figma Community)
- Stock photo sources: Unsplash, Pexels
- Icon libraries: Iconify, Feather Icons, Material Icons

## Practice Exercises

1. **Wireframe to Mockup:** Take 3 wireframes you created and transform them into high-fidelity mockups. Apply consistent style guide.

2. **Responsive Set:** Design the same screen at 3 breakpoints (mobile 375px, tablet 768px, desktop 1440px). Ensure visual consistency.

3. **State Sheet:** Choose one component (button or input field) and design all 7 states (default, hover, focus, active, disabled, error, loading).

4. **Real Content Test:** Design a user profile card with placeholder content. Then redesign with real, messy data (long names, no avatar, lots of bio text). Compare.

5. **Developer Handoff:** Create a mockup with complete specifications annotated: all measurements, colors, typography details. Export necessary assets.

6. **Style Guide Application:** Create a 3-page mockup set (home, list, detail) using a pre-existing style guide (Material Design or iOS HIG). Maintain strict consistency.

## Further Reading

- "Refactoring UI" by Adam Wathan & Steve Schoger (visual design tactics)
- Figma: Design and handoff best practices
- "Designing Interface Animation" by Val Head
- Material Design Guidelines (comprehensive mockup examples)
- Apple HIG (iOS design patterns)
