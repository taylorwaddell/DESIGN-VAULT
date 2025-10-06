# Responsive Design

## Introduction

Responsive design is the practice of creating interfaces that adapt gracefully to different screen sizes, devices, and user contexts. From smartphones to tablets to desktop monitors to TVs, users access digital products on an ever-expanding array of devices. Responsive design ensures that content remains accessible, readable, and usable regardless of viewport size. Rather than creating separate experiences for mobile and desktop, responsive design uses flexible layouts, fluid grids, and media queries to transform a single codebase into experiences optimized for any device.

The philosophy of responsive design goes beyond simply "making things fit"—it's about understanding user needs in different contexts. Mobile users often want quick access to key information, while desktop users may want comprehensive data and advanced features. Responsive design requires thinking about content hierarchy (what's essential?), interaction patterns (touch vs mouse), and performance (slower mobile networks). Done well, responsive design feels intentional on every device—not like a desktop experience squeezed into a small screen.

Mastering responsive design means understanding breakpoints (when layouts change), fluid typography (text that scales), flexible layouts (grids that adapt), touch targets (appropriate sizing for fingers), and testing strategies (devices, browsers, network conditions). It requires collaboration between designers and developers, with designers thinking in systems (not fixed-width mockups) and developers implementing adaptive layouts. Responsive design is not a feature—it's a foundational requirement for modern digital products.

## Learning Objectives

By mastering Responsive Design, you will be able to:

- Apply mobile-first design methodology effectively
- Design fluid layouts that adapt across breakpoints
- Implement flexible typography systems
- Optimize touch targets for mobile interactions
- Use CSS Grid and Flexbox for responsive layouts
- Test designs across devices and viewports
- Balance content and features across screen sizes
- Apply progressive enhancement principles

## Key Knowledge Points

### Why Responsive Design Matters

**Device Diversity:**

- Smartphones: 375px - 430px wide
- Tablets: 768px - 1024px wide
- Laptops: 1280px - 1440px wide
- Desktops: 1920px+ wide
- Foldable devices, watches, TVs, car displays...

**User Expectations:**

- 85% of adults expect mobile site to be as good or better than desktop
- Users switch devices mid-task (start on mobile, finish on desktop)
- Poor mobile experience = bounce, lost trust

**Business Impact:**

- Google mobile-first indexing (mobile version determines search ranking)
- Conversion rates: Good mobile experience = higher conversions
- Cost: One responsive codebase vs separate mobile/desktop apps (cheaper to maintain)

**Accessibility:**

- Users with low vision zoom in (responsive layouts accommodate)
- Responsive design principles overlap with accessibility (flexible text sizing, clear hierarchy)

### Mobile-First Approach

**Traditional (Desktop-First):**

1. Design for desktop (1440px wide)
2. Try to fit design into mobile (squeeze, hide, compromise)
3. Result: Mobile feels like an afterthought

**Mobile-First:**

1. Design for mobile first (375px wide)
2. Prioritize essential content (limited space forces focus)
3. Progressively enhance for larger screens (add features, detail, layout complexity)
4. Result: Mobile is intentional, desktop feels spacious

**Why Mobile-First Wins:**

- **Forces prioritization:** Limited mobile space forces you to identify what's truly important
- **Content-first:** Focus on content hierarchy, not decoration
- **Performance:** Start lean (mobile), add complexity (desktop) = faster mobile
- **Easier to expand:** Adding features/space is easier than removing/hiding
- **Accessibility:** Mobile-first often leads to clearer, simpler designs (benefits everyone)

**In Practice:**

**Mobile-First CSS:**

```css
/* Base styles (mobile) */
.container {
  padding: 16px;
  font-size: 16px;
}

/* Tablet and up (768px+) */
@media (min-width: 768px) {
  .container {
    padding: 24px;
    font-size: 18px;
  }
}

/* Desktop and up (1024px+) */
@media (min-width: 1024px) {
  .container {
    padding: 32px;
    max-width: 1200px;
    margin: 0 auto;
  }
}
```

Notice: Start with mobile styles, add complexity with `min-width` media queries (not `max-width`).

### Breakpoints

**What Are Breakpoints?**
Points where layout changes to accommodate different screen sizes.

**Common Breakpoints:**

- **Mobile:** 320px - 767px
- **Tablet:** 768px - 1023px
- **Desktop:** 1024px - 1439px
- **Large Desktop:** 1440px+

**Tailwind CSS Breakpoints (popular):**

- `sm`: 640px
- `md`: 768px
- `lg`: 1024px
- `xl`: 1280px
- `2xl`: 1536px

**Bootstrap Breakpoints:**

- `xs`: <576px
- `sm`: 576px
- `md`: 768px
- `lg`: 992px
- `xl`: 1200px
- `xxl`: 1400px

**Should You Use Standard Breakpoints?**

- **Pros:** Consistent, well-tested, documented
- **Cons:** May not fit your content

**Content-Based Breakpoints:**
Don't just use standard breakpoints—adjust when YOUR content breaks.

**Process:**

1. Design mobile layout
2. Resize browser wider
3. When layout looks broken/awkward, add breakpoint
4. Adjust layout at that point
5. Repeat until desktop

**Example:**
Your navigation menu fits 4 items on mobile. At 500px width, you could fit 6 items. That's your breakpoint (even if not "standard").

**Best Practice:**

- Start with standard breakpoints (768px, 1024px)
- Adjust based on your content
- Document your breakpoints in [[Design-Tokens]]

### Fluid Layouts

**Fixed Layout (Bad):**

```css
.container {
  width: 1200px; /* Always 1200px, breaks on mobile */
}
```

**Fluid Layout (Good):**

```css
.container {
  width: 100%; /* Fills available space */
  max-width: 1200px; /* Doesn't exceed 1200px */
  padding: 0 16px; /* Breathing room on edges */
}
```

**Fluid Grid:**
Use percentages or flexible units (fr in CSS Grid, flex in Flexbox).

**Example: 3-Column Layout**

**Fixed (breaks on mobile):**

```css
.column {
  width: 400px; /* Fixed width */
}
```

**Fluid:**

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 equal columns */
  gap: 16px;
}

/* On mobile: stack vertically */
@media (max-width: 767px) {
  .grid {
    grid-template-columns: 1fr; /* 1 column */
  }
}
```

**CSS Grid for Responsive Layouts:**

```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 24px;
}
```

**What This Does:**

- `auto-fit`: As many columns as fit
- `minmax(300px, 1fr)`: Each column minimum 300px, expand to fill
- Result: 1 column on mobile (can't fit 2x 300px), 2-3 columns on tablet, 3-4 on desktop
- **No media queries needed!**

**Flexbox for Responsive Layouts:**

```css
.flex-container {
  display: flex;
  flex-wrap: wrap; /* Items wrap to next line if not enough space */
  gap: 16px;
}

.flex-item {
  flex: 1 1 300px; /* Grow, shrink, base 300px */
}
```

Items wrap to new rows as viewport shrinks.

### Flexible Typography

**Fixed Font Size (Problematic):**

```css
h1 {
  font-size: 48px; /* Always 48px, too big on mobile */
}
```

**Responsive Font Sizes:**

**1. Media Queries:**

```css
h1 {
  font-size: 32px; /* Mobile */
}

@media (min-width: 768px) {
  h1 {
    font-size: 48px; /* Tablet+ */
  }
}

@media (min-width: 1024px) {
  h1 {
    font-size: 64px; /* Desktop+ */
  }
}
```

**2. Viewport Units:**

```css
h1 {
  font-size: 8vw; /* 8% of viewport width */
}
```

**Pros:** Scales smoothly
**Cons:** Can get too small or too large

**3. Clamp (Best):**

```css
h1 {
  font-size: clamp(32px, 5vw, 64px);
  /* Min 32px, preferred 5vw, max 64px */
}
```

**What This Does:**

- Small screens: 32px (minimum)
- Medium screens: 5vw (scales with viewport)
- Large screens: 64px (maximum, doesn't get absurdly large)

**Fluid Typography Scale:**

Use [[Design-Tokens]] with clamp:

```css
:root {
  --font-size-xs: clamp(0.75rem, 0.7rem + 0.25vw, 0.875rem);
  --font-size-sm: clamp(0.875rem, 0.8rem + 0.375vw, 1rem);
  --font-size-base: clamp(1rem, 0.9rem + 0.5vw, 1.125rem);
  --font-size-lg: clamp(1.125rem, 1rem + 0.625vw, 1.25rem);
  --font-size-xl: clamp(1.25rem, 1.1rem + 0.75vw, 1.5rem);
  --font-size-2xl: clamp(1.5rem, 1.3rem + 1vw, 2rem);
  --font-size-3xl: clamp(2rem, 1.7rem + 1.5vw, 3rem);
}
```

**Tools:**

- Utopia (utopia.fyi) - Fluid typography calculator
- Type Scale (typescale.com) - Generate scales

**Line Length:**
Optimal: 50-75 characters per line.

**Responsive:**

```css
.content {
  max-width: 65ch; /* Max 65 characters wide */
}
```

`ch` unit = width of "0" character in current font.

### Responsive Images

**Problem:** Large images on mobile waste bandwidth, slow load.

**Solutions:**

**1. Max-Width:**

```css
img {
  max-width: 100%; /* Never exceed container */
  height: auto; /* Maintain aspect ratio */
}
```

**2. Responsive Images (HTML):**

```html
<img
  src="small.jpg"
  srcset="small.jpg 480w, medium.jpg 768w, large.jpg 1200w"
  sizes="(max-width: 768px) 100vw, 50vw"
  alt="Description"
/>
```

**What This Does:**

- Browser chooses appropriate image based on screen size
- Mobile: loads small.jpg (faster)
- Desktop: loads large.jpg (sharper)

**3. Picture Element (Art Direction):**

```html
<picture>
  <source media="(max-width: 768px)" srcset="mobile-crop.jpg" />
  <source media="(min-width: 769px)" srcset="desktop-wide.jpg" />
  <img src="desktop-wide.jpg" alt="Description" />
</picture>
```

Use when mobile needs different crop (not just smaller version).

**4. Modern Formats:**

```html
<picture>
  <source srcset="image.avif" type="image/avif" />
  <source srcset="image.webp" type="image/webp" />
  <img src="image.jpg" alt="Description" />
</picture>
```

AVIF/WebP = smaller files (faster), fallback to JPG.

**5. Lazy Loading:**

```html
<img src="image.jpg" loading="lazy" alt="Description" />
```

Image loads only when scrolled near (saves bandwidth).

### Touch Targets and Mobile Interactions

**Touch Target Size:**

- **Minimum:** 44x44px (Apple HIG, WCAG 2.1)
- **Recommended:** 48x48px (Material Design)
- **Why:** Fingers are less precise than mouse cursors

**Spacing Between Targets:**

- **Minimum:** 8px gap between interactive elements
- Prevents accidental taps

**Example:**

```css
.button {
  min-width: 48px;
  min-height: 48px;
  padding: 12px 24px;
}

.button + .button {
  margin-left: 8px; /* Space between buttons */
}
```

**Touch vs Mouse Interactions:**

**Hover:** Doesn't exist on touch (finger isn't hovering).

- Don't rely on hover for critical information
- Use hover as enhancement (desktop), not requirement

**Example:**
❌ **Bad:** Information only visible on hover (mobile users can't see)
✅ **Good:** Information always visible, hover adds visual feedback

**Gestures:**

- **Swipe:** Common (carousels, dismissing items)
- **Pinch to zoom:** Expected (images, maps)
- **Long press:** Less common (document with visual cue)

**Form Inputs:**

- Large enough to tap (48px height)
- Appropriate keyboard (email input shows @ key)

```html
<input type="email" />
<!-- Mobile keyboard includes @ -->
<input type="tel" />
<!-- Mobile keyboard shows numbers -->
<input type="number" />
<!-- Mobile keyboard shows numeric -->
```

### Navigation Patterns

**Desktop Navigation:**

- Horizontal menu bar
- Dropdowns on hover
- Lots of space

**Mobile Navigation:**

- Limited space
- Common patterns:

**1. Hamburger Menu:**

- Icon (☰) opens slide-out drawer
- Pros: Saves space
- Cons: Hidden (lower discoverability)
- Use: When many menu items

**2. Tab Bar (Bottom Navigation):**

- 3-5 icons at bottom of screen
- Pros: Always visible, easy to reach with thumb
- Cons: Limited items
- Use: Apps with 3-5 top-level sections

**3. Priority+ Navigation:**

- Show most important items, hide rest in "More"
- Pros: Balance visibility and space
- Cons: Some items hidden
- Use: When some items more important than others

**4. Full-Screen Menu:**

- Hamburger opens full-screen overlay menu
- Pros: Space for large links, imagery
- Cons: Takes over screen
- Use: When menu is important experience (e.g., restaurant site)

**Progressive Disclosure:**

- Hide complexity, reveal on demand
- Mobile: Show essential info, "See more" expands
- Desktop: Show all info (more space)

### Content Strategy for Responsive Design

**Same content across all devices? Not always.**

**Content Parity:**

- **Argument for:** Users should access same content on any device
- **Argument against:** Mobile users often want different things (faster, key info)

**Best Practice:**

- **Essential content:** Same across all devices
- **Additional content:** Available on mobile (via "Show more", tabs), but not prominent
- **Example:** Product page:
  - **Essential (all devices):** Image, price, "Add to cart", key specs
  - **Additional (desktop prominent, mobile collapsed):** Full description, reviews, related products

**Content Hierarchy:**

**Mobile:**

1. Hero image
2. Headline
3. Key benefit (1 sentence)
4. Call-to-action button
5. "Learn more" (expands to full description)

**Desktop:**

1. Hero image (larger)
2. Headline
3. Full description (visible)
4. Call-to-action button (prominent)
5. Additional sections (testimonials, features)

**Progressive Enhancement:**

- Start with core content/functionality (works on all devices, even without JS)
- Enhance for larger screens (more detail, advanced features)
- Enhance for modern browsers (animations, advanced interactions)

### Testing Responsive Designs

**Browser DevTools:**

- Chrome DevTools: Device Mode (Cmd/Ctrl + Shift + M)
- Responsive viewport, rotate, throttle network
- Test breakpoints

**Real Devices:**

- **Why:** DevTools approximate, real devices reveal:
  - Actual touch interactions
  - Performance (older devices slower)
  - Rendering differences
- **Test on:** At least 1 iPhone, 1 Android, 1 tablet

**Device Lab:**

- Collection of devices for testing
- Company device lab or services (BrowserStack, Sauce Labs)

**Network Conditions:**

- Test on slow networks (3G)
- Chrome DevTools: Network throttling
- Mobile users often on slow/spotty connections

**Orientation:**

- Test portrait and landscape
- Layouts should work in both

**Text Zoom:**

- Users with low vision zoom text (browser settings)
- Test at 200% zoom (WCAG requirement)
- Layout should accommodate (not break, not cut off)

**Checklist:**

- ✅ Text readable without zooming (minimum 16px body text)
- ✅ Touch targets minimum 48x48px, 8px spacing
- ✅ Content accessible (no horizontal scroll)
- ✅ Navigation works on mobile (hamburger, tab bar, etc.)
- ✅ Forms usable (large inputs, appropriate keyboards)
- ✅ Images responsive (don't overflow, load quickly)
- ✅ Performance acceptable (loads in <3 seconds on 3G)
- ✅ Works without JavaScript (progressive enhancement)
- ✅ Works at 200% zoom (accessibility)
- ✅ Works in portrait and landscape

### Responsive Design in Figma

**Frames:**

- Create frames for each breakpoint (Mobile, Tablet, Desktop)
- Example: iPhone 14 (390px), iPad (768px), Desktop (1440px)

**Auto Layout:**

- Essential for responsive design
- Hug contents (component sizes to content)
- Fill container (component expands to fill)
- Direction (horizontal → vertical on mobile)
- See [[Auto-Layout]]

**Constraints:**

- Pin elements to sides (left, right, top, bottom, center)
- Scale (element grows with frame)

**Variants:**

- Create component variants for different breakpoints
- Example: Button → Mobile (stacked icon/text), Desktop (inline icon/text)
- See [[Components-and-Variants]]

**Responsive Components:**

- Design components to work at multiple sizes
- Test by resizing frame

**Device Mockups:**

- Mockup assets (place designs in device frames)
- Communicate responsive design to stakeholders

**Prototyping:**

- Prototype interactions at different breakpoints
- Show hamburger menu opening, tab switching, etc.
- See [[Figma-Prototyping]]

### Design Systems and Responsive Design

**Responsive Components:**

- Every component should be responsive
- Document behavior at different sizes
- Example: Card → Mobile (stacked), Desktop (horizontal)

**Responsive Tokens:**

- Space tokens (spacing values different at mobile/desktop)

```css
:root {
  --spacing-md: 16px;
}

@media (min-width: 768px) {
  --spacing-md: 24px;
}
```

**Responsive Patterns:**

- Document common responsive patterns (navigation, forms, cards)
- Provide code examples for each breakpoint

See [[Design-Systems]], [[Component-Libraries]]

### Common Responsive Design Mistakes

**1. Not Testing on Real Devices:**

- DevTools ≠ real experience
- Always test on actual phones, tablets

**2. Tiny Text on Mobile:**

- Minimum 16px for body text (or users will zoom)

**3. Hover-Dependent Interactions:**

- Touch devices don't have hover
- Don't hide critical info behind hover

**4. Small Touch Targets:**

- Minimum 48x48px, 8px spacing
- Small targets frustrate mobile users

**5. Hidden Content on Mobile:**

- If it's important, don't hide it (or make it easy to reveal)
- Users won't find buried content

**6. Horizontal Scrolling:**

- Should never happen (except intentional carousels)
- Content should fit viewport width

**7. Fixed-Width Layouts:**

- Use fluid layouts (percentages, fr, flex)

**8. Not Considering Performance:**

- Large images, heavy JavaScript = slow on mobile

**9. Desktop-First Thinking:**

- Results in mobile feeling like afterthought
- Start mobile-first

**10. Ignoring Landscape Orientation:**

- Test portrait AND landscape

### Best Practices

**Do:**

- ✅ Design mobile-first (essential content first)
- ✅ Use fluid layouts (percentages, CSS Grid, Flexbox)
- ✅ Use flexible typography (clamp, viewport units)
- ✅ Make touch targets 48x48px minimum
- ✅ Test on real devices (not just DevTools)
- ✅ Optimize images (responsive images, modern formats, lazy loading)
- ✅ Consider performance (slow networks)
- ✅ Progressive enhancement (core content works everywhere)
- ✅ Test at 200% zoom (accessibility)
- ✅ Document responsive behavior in design system

**Don't:**

- ❌ Design only for desktop
- ❌ Use fixed widths (breaks on smaller screens)
- ❌ Rely on hover interactions (touch devices)
- ❌ Make text too small (<16px)
- ❌ Make touch targets too small (<48px)
- ❌ Hide important content on mobile
- ❌ Ignore performance (large assets)
- ❌ Forget to test in landscape
- ❌ Skip real device testing

## Related Topics

- [[Design-Systems]]
- [[Design-Tokens]]
- [[Layout-and-Composition]]
- [[Grid-Systems]]
- [[Auto-Layout]]
- [[Accessibility]]
- [[Performance]]
- [[Figma-Prototyping]]

## Tools & Resources

**Design:**

- Figma (responsive design with Auto Layout)
- Responsively App (responsively.app) - Test multiple devices at once

**Development:**

- Chrome DevTools (Device Mode)
- Firefox Responsive Design Mode
- BrowserStack (browserstack.com) - Real device testing
- Sauce Labs (saucelabs.com) - Real device testing

**Testing:**

- Responsive Design Checker (responsivedesignchecker.com)
- Am I Responsive (amiresponsive.co) - Screenshot multiple devices
- Google Mobile-Friendly Test (search.google.com/test/mobile-friendly)
- WebPageTest (webpagetest.org) - Performance testing

**Typography:**

- Utopia (utopia.fyi) - Fluid typography calculator
- Type Scale (typescale.com) - Typography scales

**Learning:**

- **"Responsive Web Design" by Ethan Marcotte** (the original book)
- **"Mobile First" by Luke Wroblewski**
- A List Apart articles on responsive design (alistapart.com)
- Brad Frost's responsive design patterns (bradfrost.com)
- MDN Responsive Design Guide (developer.mozilla.org)

## Practice Exercises

1. **Mobile-First Design:** Choose a desktop website (e.g., Airbnb homepage). Redesign it mobile-first:

   - Sketch mobile layout (320px wide)
   - Identify essential content (what must be on mobile?)
   - Design tablet layout (768px) - what do you add?
   - Design desktop layout (1440px) - what do you add?
     Present 3 layouts showing content/layout evolution.

2. **Fluid Typography System:** Create a fluid typography scale using `clamp()`:

   - 5 sizes: xs, sm, base, lg, xl
   - Each should scale smoothly from mobile (320px) to desktop (1920px)
   - Use Utopia (utopia.fyi) or calculate manually
   - Implement in CSS, test by resizing browser

3. **Responsive Component:** Design and code a responsive Card component:

   - **Mobile (< 768px):** Vertical (image top, content below), full width
   - **Tablet/Desktop (> 768px):** Horizontal (image left, content right)
   - Use CSS Grid or Flexbox
   - Implement in HTML/CSS, test at multiple breakpoints

4. **Navigation Pattern:** Design responsive navigation for a site with 6 top-level pages:

   - **Mobile:** Hamburger menu (slide-out drawer)
   - **Tablet:** Collapsed menu (show 3 items + "More")
   - **Desktop:** Full horizontal menu (all 6 items visible)
     Create mockups in Figma for all 3 breakpoints, prototype interactions.

5. **Responsive Audit:** Choose your favorite website. Audit its responsive design:

   - Test on mobile, tablet, desktop (DevTools + real device)
   - Evaluate:
     - Touch targets (size, spacing)
     - Text readability (size, line length)
     - Content hierarchy (mobile vs desktop)
     - Performance (load time on 3G)
     - Accessibility (zoom to 200%)
   - Note 5 issues, propose improvements
     Write 1-2 page report with screenshots.

6. **Breakpoint Strategy:** For a hypothetical design system:
   - Define breakpoints (mobile, tablet, desktop, large desktop)
   - Justify each breakpoint (why those sizes?)
   - Define behavior for:
     - Typography (sizes at each breakpoint)
     - Spacing (padding, margins)
     - Grid (columns at each breakpoint)
     - Container max-width
   - Document as design tokens (JSON or CSS)

## Further Reading

- **"Responsive Web Design" by Ethan Marcotte** (the foundational book)
- **"Mobile First" by Luke Wroblewski** (mobile-first philosophy)
- **"Responsible Responsive Design" by Scott Jehl** (performance-focused)
- **"Going Responsive" by Karen McGrane** (content strategy)
- A List Apart: "Responsive Web Design" (alistapart.com/article/responsive-web-design)
- Brad Frost: "Responsive Navigation Patterns" (bradfrost.com)
- MDN: Responsive Design (developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)
- Google Web Fundamentals: Responsive Design (web.dev/responsive-web-design-basics)
- **"Design for Real Life" by Eric Meyer & Sara Wachter-Boettcher** (context-aware design)
- Smashing Magazine responsive design articles (smashingmagazine.com)
