# Design Tokens

## Introduction

Design tokens are the smallest, indivisible pieces of a design system—the atomic design decisions represented as data. They capture foundational choices like colors (`#0066CC`), spacing values (`16px`), typography properties (`font-size: 14px`), and animation durations (`200ms`) in a platform-agnostic format that can transform into any platform's code (CSS, iOS, Android, React Native). Instead of hard-coding `color: #0066CC` throughout your codebase, you reference `color: $primary-blue`, and when your brand color changes, you update one token and it propagates everywhere.

The power of design tokens is consistency at scale: they're the single source of truth that ensures your blue is the same blue on web, iOS, Android, and any future platform. They enable systematic design changes—rebrand your entire product by updating token values, implement dark mode by swapping token sets, or ensure accessibility by defining color tokens with sufficient contrast. Tokens also bridge the gap between design and development: designers define tokens in design tools (Figma styles), developers consume them as code (CSS variables, JavaScript constants), and both reference the same named values.

Mastering design tokens means understanding their taxonomy (color, spacing, typography, etc.), naming conventions (clear, semantic, scalable), transformation pipelines (from JSON to platform-specific code), and integration with design tools and build processes. Tokens are infrastructure—foundational, often invisible, but essential for maintaining design consistency and enabling efficient collaboration across teams and platforms.

## Learning Objectives

By mastering Design Tokens, you will be able to:

- Understand the purpose and value of design tokens in design systems
- Create comprehensive token taxonomies (color, spacing, typography, etc.)
- Apply effective naming conventions that scale
- Distinguish between global tokens, alias tokens, and component-specific tokens
- Transform tokens from platform-agnostic formats to platform-specific code
- Implement tokens in design tools (Figma) and code (CSS Variables, Sass, JavaScript)
- Manage token versioning and updates
- Use tools like Style Dictionary to automate token transformation

## Key Knowledge Points

### What are Design Tokens?

**Definition:**
Design tokens are named entities that store visual design attributes. They're design decisions (color, spacing, typography) represented as data (JSON, YAML) that can be transformed into platform-specific formats (CSS, iOS, Android).

**Simple Example:**
Instead of:

```css
.button {
  background-color: #0066cc; /* Hard-coded */
  padding: 16px; /* Hard-coded */
}
```

With tokens:

```css
.button {
  background-color: var(--color-primary); /* Token */
  padding: var(--spacing-medium); /* Token */
}
```

**Token Definition:**

```json
{
  "color": {
    "primary": "#0066CC"
  },
  "spacing": {
    "medium": "16px"
  }
}
```

**Why This Matters:**

- Update `--color-primary` once → Changes everywhere
- Consistent values across platforms
- Semantic naming (describes purpose, not value)

### Why Design Tokens Matter

**Single Source of Truth:**

- One place defines all design decisions
- Designers and developers reference same values
- No drift between design and code

**Consistency:**

- Same blue everywhere (web, iOS, Android)
- Same spacing scale across all components
- No "close enough" colors (#0066CC vs #0065CB)

**Scalability:**

- Add new platform? Transform tokens
- Rebrand? Update token values, not thousands of hard-coded values
- Dark mode? Swap token sets

**Maintenance:**

- Update once, applies everywhere
- Reduce technical debt (no scattered magic numbers)
- Easier to audit and enforce standards

**Collaboration:**

- Shared vocabulary ("primary-blue" not "that blue")
- Design tools and code reference same tokens
- Clear communication between design and dev

### Types of Design Tokens

Design tokens typically cover these categories:

**1. Color Tokens:**

- **Brand Colors:**

  - `color-brand-primary`, `color-brand-secondary`
  - Company colors

- **Semantic Colors:**

  - `color-success`, `color-error`, `color-warning`, `color-info`
  - Meaning-based

- **Neutral Colors:**

  - `color-gray-100` through `color-gray-900`
  - Blacks, whites, grays

- **Text Colors:**

  - `color-text-primary`, `color-text-secondary`, `color-text-disabled`
  - Hierarchy

- **Background Colors:**

  - `color-background-primary`, `color-background-secondary`
  - Surface colors

- **Border Colors:**
  - `color-border-default`, `color-border-hover`

**2. Spacing Tokens:**

- **Scale:**

  - `spacing-xs`: 4px
  - `spacing-sm`: 8px
  - `spacing-md`: 16px
  - `spacing-lg`: 24px
  - `spacing-xl`: 32px
  - `spacing-2xl`: 48px
  - `spacing-3xl`: 64px

- **Component-Specific:**
  - `button-padding-horizontal`: 16px
  - `card-padding`: 24px

**3. Typography Tokens:**

- **Font Family:**

  - `font-family-primary`: "Inter, sans-serif"
  - `font-family-monospace`: "Fira Code, monospace"

- **Font Size:**

  - `font-size-xs`: 12px
  - `font-size-sm`: 14px
  - `font-size-base`: 16px
  - `font-size-lg`: 18px
  - `font-size-xl`: 20px
  - `font-size-2xl`: 24px
  - `font-size-3xl`: 32px

- **Font Weight:**

  - `font-weight-normal`: 400
  - `font-weight-medium`: 500
  - `font-weight-semibold`: 600
  - `font-weight-bold`: 700

- **Line Height:**

  - `line-height-tight`: 1.2
  - `line-height-normal`: 1.5
  - `line-height-relaxed`: 1.75

- **Letter Spacing:**
  - `letter-spacing-tight`: -0.02em
  - `letter-spacing-normal`: 0
  - `letter-spacing-wide`: 0.02em

**4. Sizing Tokens:**

- **Component Sizes:**

  - `size-button-sm`: 32px
  - `size-button-md`: 40px
  - `size-button-lg`: 48px

- **Icon Sizes:**

  - `size-icon-sm`: 16px
  - `size-icon-md`: 24px
  - `size-icon-lg`: 32px

- **Layout:**
  - `size-container-max-width`: 1200px
  - `size-sidebar-width`: 240px

**5. Border Tokens:**

- **Width:**

  - `border-width-thin`: 1px
  - `border-width-medium`: 2px
  - `border-width-thick`: 4px

- **Radius:**

  - `border-radius-none`: 0
  - `border-radius-sm`: 4px
  - `border-radius-md`: 8px
  - `border-radius-lg`: 16px
  - `border-radius-full`: 9999px (circle)

- **Style:**
  - `border-style-solid`, `border-style-dashed`

**6. Shadow Tokens:**

- **Elevation:**
  - `shadow-sm`: `0 1px 2px rgba(0,0,0,0.05)`
  - `shadow-md`: `0 4px 6px rgba(0,0,0,0.1)`
  - `shadow-lg`: `0 10px 15px rgba(0,0,0,0.1)`
  - `shadow-xl`: `0 20px 25px rgba(0,0,0,0.1)`

**7. Animation Tokens:**

- **Duration:**

  - `duration-instant`: 100ms
  - `duration-fast`: 200ms
  - `duration-normal`: 300ms
  - `duration-slow`: 500ms

- **Easing:**
  - `easing-ease-in`: `cubic-bezier(0.4, 0, 1, 1)`
  - `easing-ease-out`: `cubic-bezier(0, 0, 0.2, 1)`
  - `easing-ease-in-out`: `cubic-bezier(0.4, 0, 0.2, 1)`

See [[Animation-Principles]] for more on timing.

**8. Z-Index Tokens:**

- **Layers:**
  - `z-index-dropdown`: 1000
  - `z-index-sticky`: 1100
  - `z-index-modal-backdrop`: 1200
  - `z-index-modal`: 1300
  - `z-index-popover`: 1400
  - `z-index-tooltip`: 1500

### Token Hierarchy

**Global Tokens (Primitive/Base):**

- Raw values, not context-specific
- Building blocks for other tokens
- Rarely used directly in components

**Example:**

```json
{
  "color": {
    "blue": {
      "500": "#0066CC",
      "600": "#0052A3"
    }
  }
}
```

**Alias Tokens (Semantic):**

- Reference global tokens
- Add meaning/purpose
- Used in components

**Example:**

```json
{
  "color": {
    "primary": "{color.blue.500}",
    "primary-hover": "{color.blue.600}"
  }
}
```

**Component Tokens:**

- Specific to components
- Reference alias or global tokens

**Example:**

```json
{
  "button": {
    "background": "{color.primary}",
    "background-hover": "{color.primary-hover}",
    "padding-horizontal": "{spacing.md}"
  }
}
```

**Hierarchy Benefit:**

- Change `color.blue.500` → Updates `color.primary` → Updates `button.background`
- One change cascades through system

### Naming Conventions

**Good naming is critical for scalability.**

**Structure:**

```
[category]-[property]-[variant]-[state]
```

**Examples:**

- `color-text-primary`
- `color-background-secondary-hover`
- `spacing-button-horizontal`
- `font-size-heading-large`

**Principles:**

**1. Semantic, Not Descriptive:**

- ✅ `color-primary` (purpose)
- ❌ `color-blue` (visual)
- **Why:** If brand changes from blue to green, semantic name still works

**Exception:** Global tokens can be descriptive

- `color-blue-500` (global)
- `color-primary: {color.blue.500}` (alias, semantic)

**2. Consistent Patterns:**

- Use same structure across all tokens
- Predictable, easy to remember
- Examples:
  - `spacing-xs`, `spacing-sm`, `spacing-md` (size scale)
  - `color-gray-100` through `color-gray-900` (numeric scale)

**3. Hierarchy in Name:**

- Most general → Most specific
- `color-text-primary` (color, then what, then variant)
- Not `primary-text-color` (inconsistent order)

**4. Avoid Abbreviations (unless universal):**

- ✅ `background`, `horizontal`
- ❌ `bg`, `horiz` (harder to remember, less searchable)
- **Exception:** `xs`, `sm`, `md`, `lg`, `xl` (universal in design)

**5. Scale Naming:**

**T-shirt sizes:**

- `xs`, `sm`, `md`, `lg`, `xl`, `2xl`, `3xl`
- Intuitive, familiar

**Numeric:**

- `100`, `200`, `300`, ... `900`
- Common for color scales (Tailwind, Material)
- Middle is base (500 often primary)

**Avoid:**

- `small`, `smaller`, `smallest` (confusing)
- `1`, `2`, `3` (not intuitive what middle is)

### Token Formats

**JSON (Most Common):**

```json
{
  "color": {
    "primary": "#0066CC",
    "secondary": "#6C757D"
  },
  "spacing": {
    "sm": "8px",
    "md": "16px",
    "lg": "24px"
  }
}
```

**YAML:**

```yaml
color:
  primary: "#0066CC"
  secondary: "#6C757D"
spacing:
  sm: "8px"
  md: "16px"
  lg: "24px"
```

**JavaScript/TypeScript:**

```javascript
export const tokens = {
  color: {
    primary: "#0066CC",
    secondary: "#6C757D",
  },
  spacing: {
    sm: "8px",
    md: "16px",
    lg: "24px",
  },
};
```

**CSS Variables:**

```css
:root {
  --color-primary: #0066cc;
  --color-secondary: #6c757d;
  --spacing-sm: 8px;
  --spacing-md: 16px;
  --spacing-lg: 24px;
}
```

**Sass Variables:**

```scss
$color-primary: #0066cc;
$color-secondary: #6c757d;
$spacing-sm: 8px;
$spacing-md: 16px;
$spacing-lg: 24px;
```

### Token Transformation

**Problem:** Design tools and platforms use different formats.

**Solution:** Store tokens in platform-agnostic format (JSON), transform to platform-specific formats.

**Workflow:**

```
tokens.json (source of truth)
    ↓
Style Dictionary / Theo (transformation tool)
    ↓
    ├→ variables.css (web)
    ├→ Colors.swift (iOS)
    ├→ colors.xml (Android)
    └→ tokens.js (React Native)
```

**Style Dictionary (Amazon):**

- Most popular token transformation tool
- Transforms JSON → Any format
- Extensible, customizable

**Installation:**

```bash
npm install style-dictionary
```

**Config:**

```javascript
// config.json
{
  "source": ["tokens/**/*.json"],
  "platforms": {
    "css": {
      "transformGroup": "css",
      "buildPath": "build/css/",
      "files": [{
        "destination": "variables.css",
        "format": "css/variables"
      }]
    },
    "ios": {
      "transformGroup": "ios",
      "buildPath": "build/ios/",
      "files": [{
        "destination": "Colors.swift",
        "format": "ios-swift/class.swift"
      }]
    }
  }
}
```

**Run:**

```bash
style-dictionary build
```

**Output (CSS):**

```css
:root {
  --color-primary: #0066cc;
  --spacing-md: 16px;
}
```

**Output (Swift):**

```swift
class Colors {
  static let primary = UIColor(hex: "0066CC")
}
```

**Other Tools:**

- **Theo (Salesforce):** Similar to Style Dictionary
- **Diez:** Cross-platform design token framework

### Using Tokens in Design Tools

**Figma:**

**Styles = Tokens**

- Color Styles → Color tokens
- Text Styles → Typography tokens
- Effect Styles → Shadow tokens

**Creating Styles:**

1. Select element (text, shape)
2. Style properties panel → Create style
3. Name with token naming convention: `color/primary`, `spacing/md`
4. Reuse across designs

**Syncing Figma ↔ Code:**

- **Figma Tokens Plugin:** Import/export JSON tokens
- **Manual:** Export styles, manually create code tokens
- **Figma API:** Automate extraction

**Best Practice:**

- Design in Figma using styles
- Export to JSON
- Transform to code
- Keep Figma and code in sync

**Sketch:**

- Similar workflow with Shared Styles
- Less popular now (Figma dominates)

### Implementing Tokens in Code

**CSS Variables (Modern Web):**

**Define:**

```css
:root {
  --color-primary: #0066cc;
  --color-text-primary: #333;
  --spacing-md: 16px;
  --font-size-base: 16px;
}
```

**Use:**

```css
.button {
  background-color: var(--color-primary);
  padding: var(--spacing-md);
  font-size: var(--font-size-base);
}
```

**Benefits:**

- Native CSS (no preprocessor)
- Dynamic (can change at runtime)
- Cascade and inheritance

**Dark Mode with Tokens:**

```css
:root {
  --color-background: #ffffff;
  --color-text: #333333;
}

[data-theme="dark"] {
  --color-background: #1a1a1a;
  --color-text: #eeeeee;
}

body {
  background-color: var(--color-background);
  color: var(--color-text);
}
```

Toggle `data-theme="dark"` → Colors update automatically

**JavaScript/TypeScript:**

**Define:**

```typescript
export const tokens = {
  color: {
    primary: "#0066CC",
    text: {
      primary: "#333",
      secondary: "#666",
    },
  },
  spacing: {
    sm: "8px",
    md: "16px",
    lg: "24px",
  },
};
```

**Use (React):**

```jsx
import { tokens } from "./tokens";

function Button() {
  return (
    <button
      style={{
        backgroundColor: tokens.color.primary,
        padding: tokens.spacing.md,
      }}
    >
      Click me
    </button>
  );
}
```

**Use (Styled Components):**

```javascript
import styled from "styled-components";
import { tokens } from "./tokens";

const Button = styled.button`
  background-color: ${tokens.color.primary};
  padding: ${tokens.spacing.md};
`;
```

**Sass Variables:**

**Define:**

```scss
$color-primary: #0066cc;
$spacing-md: 16px;
```

**Use:**

```scss
.button {
  background-color: $color-primary;
  padding: $spacing-md;
}
```

**Note:** Sass variables are compile-time (can't change dynamically). Use CSS variables for runtime changes.

### Token Documentation

**For each token category, document:**

**1. Purpose:**

- What is this token for?
- When to use it?

**2. Values:**

- All token names and values
- Visual examples (color swatches, spacing examples)

**3. Usage:**

- Code examples
- Do's and Don'ts

**4. Related Tokens:**

- What tokens are related? (primary, primary-hover)

**Example (Color Token Docs):**

````markdown
## Primary Color

**Token:** `color-primary`
**Value:** `#0066CC`
**Usage:** Primary brand color for CTAs, links, emphasis

**Related:**

- `color-primary-hover`: `#0052A3` (hover state)
- `color-primary-active`: `#003D7A` (pressed state)

**Code:**

```css
.button {
  background-color: var(--color-primary);
}
```
````

**Do:**

- ✅ Use for primary buttons
- ✅ Use for important links

**Don't:**

- ❌ Don't use for body text (insufficient contrast)

```

### Versioning Tokens

**Semantic Versioning:**
- **Major (1.0 → 2.0):** Breaking changes (token renamed, removed)
- **Minor (1.0 → 1.1):** New tokens added (backward compatible)
- **Patch (1.0.0 → 1.0.1):** Token value updated (e.g., color adjusted)

**Changelog:**
```

## v2.0.0

### Breaking

- Renamed `color-brand` → `color-primary`
- Removed `spacing-xs` (use `spacing-sm` instead)

### Added

- `color-success-light`, `color-error-light`

### Changed

- `color-primary`: #0066CC → #0052FF (brand update)

```

**Migration Guide:**
Provide find-replace instructions for breaking changes.

### Token Governance

**Who Owns Tokens:**
- Design systems team
- Design + engineering collaboration

**How to Request New Token:**
1. Propose in GitHub issue or Slack
2. Justify need (why not use existing?)
3. Design team reviews
4. If approved, add to tokens, document, release

**Avoid Token Sprawl:**
- Too many tokens = harder to maintain
- Before adding, ask: Can existing token work?
- Consolidate similar values

**Example:**
- ❌ `spacing-15`: 15px (too specific, use `spacing-md`: 16px)
- ✅ Limited scale: xs, sm, md, lg, xl (covers 90% of cases)

### Common Mistakes

**Mistake: Too Many Tokens**
- 50 shades of gray
- Solution: Curated palette (7-10 grays max)

**Mistake: Descriptive Names at Wrong Level**
- `color-blue` used directly in components (what if brand changes?)
- Solution: `color-blue-500` (global), `color-primary` (alias), components use alias

**Mistake: Inconsistent Naming**
- `colorPrimary`, `text-color`, `COLOR_SECONDARY`
- Solution: Pick convention, enforce

**Mistake: No Documentation**
- Tokens exist but no guidance on when to use
- Solution: Document purpose, usage, examples

**Mistake: Design and Code Out of Sync**
- Figma has one blue, code has another
- Solution: Single source of truth, automated sync

### Best Practices

**Do:**
- ✅ Start with essentials (color, spacing, typography)
- ✅ Use semantic naming (purpose over appearance)
- ✅ Create hierarchy (global → alias → component)
- ✅ Document thoroughly
- ✅ Version and changelog
- ✅ Automate transformation (Style Dictionary)
- ✅ Sync design tools and code

**Don't:**
- ❌ Create token for every unique value (curate)
- ❌ Use descriptive names for component-level tokens
- ❌ Let tokens proliferate unchecked
- ❌ Forget to document
- ❌ Have multiple sources of truth

## Related Topics

- [[Design-Systems]]
- [[Component-Libraries]]
- [[Style-Guides]]
- [[Color-Theory]]
- [[Typography]]
- [[Design-System-Documentation]]
- [[Responsive-Design]]

## Tools & Resources

**Token Tools:**
- Style Dictionary (amzn.github.io/style-dictionary)
- Theo (Salesforce, github.com/salesforce-ux/theo)
- Diez (diez.org)

**Design Tools:**
- Figma Tokens Plugin (figma.com/community/plugin/843461159747178978)
- Figma (Styles = tokens)

**Examples:**
- Salesforce Lightning Design Tokens
- Shopify Polaris Tokens
- Material Design Tokens
- IBM Carbon Tokens

**Books/Articles:**
- "Tokens in Design Systems" (Nathan Curtis, Medium)
- "Design Tokens for Dummies" (Louis Chenais)
- Design Systems Handbook (designsystemshandbook.com)

## Practice Exercises

1. **Create Token System:** Define a complete token set for a hypothetical project:
   - Color: Primary, secondary, neutrals (7 grays), semantic (success, error, warning)
   - Spacing: 6-value scale (4px - 64px)
   - Typography: Font sizes (7 sizes), weights (3-4), line heights
   - Shadows: 4 elevation levels
   Format as JSON.

2. **Naming Exercise:** Given these values, create appropriate token names:
   - `#0066CC` (brand blue)
   - `#FFFFFF` (white background)
   - `16px` (standard padding)
   - `700` (bold font weight)
   - `0 4px 6px rgba(0,0,0,0.1)` (card shadow)

3. **Token Hierarchy:** Take 3 colors: `#0066CC`, `#0052A3`, `#003D7A`. Create:
   - Global tokens (blue-500, blue-600, blue-700)
   - Alias tokens (primary, primary-hover, primary-active)
   - Component token (button-background)
   Show references using `{token.path}` syntax.

4. **Style Dictionary Setup:** Install Style Dictionary. Create `tokens.json` with 5 color tokens and 3 spacing tokens. Configure Style Dictionary to output CSS variables and JavaScript. Run build. Verify outputs.

5. **Figma Styles:** In Figma, create a mini design system:
   - 5 Color Styles (named with token convention: `color/primary`, etc.)
   - 3 Text Styles (`text/heading`, `text/body`, `text/caption`)
   - 2 Effect Styles (shadows: `shadow/sm`, `shadow/md`)
   Use these styles to design a simple card component.

6. **Dark Mode Tokens:** Create two token sets (light and dark mode) for:
   - Background color (primary, secondary)
   - Text color (primary, secondary)
   - Border color
   Show how same semantic token name maps to different values per theme.

## Further Reading

- **"Tokens in Design Systems" by Nathan Curtis** (Medium article series)
- **"Design Tokens for Dummies" by Louis Chenais**
- Style Dictionary Documentation (amzn.github.io/style-dictionary)
- **"Design Systems" by Alla Kholmatova** (chapter on tokens)
- **"Expressive Design Systems" by Yesenia Perez-Cruz** (tokens and theming)
- Salesforce UX: Design Tokens documentation
- Shopify Polaris: Design Tokens
- Material Design: Design tokens (m3.material.io)
- Figma: Variables documentation (tokens in Figma)

```
