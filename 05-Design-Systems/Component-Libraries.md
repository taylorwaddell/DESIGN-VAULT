# Component Libraries

## Introduction

A component library is a collection of reusable, pre-built UI components (buttons, inputs, cards, modals, etc.) that designers and developers can use to quickly assemble interfaces. While [[Design-Systems]] encompass principles, tokens, patterns, and documentation, the component library is the tangible toolkit—the Lego blocks that teams actually use to build products. A well-crafted component library provides consistency (every button looks and behaves the same), efficiency (don't rebuild what exists), and quality (components are tested, accessible, and responsive).

Component libraries exist in two forms: design components (Figma/Sketch libraries with variants and styles) and code components (React, Vue, Angular, Web Components with props and logic). The best component libraries keep these two in sync—designers prototype with design components, developers build with code components, and both reference the same [[Design-Tokens]] and behaviors. When design and code diverge, confusion and inconsistency follow; when they align, teams move fast with confidence.

Mastering component libraries means understanding component design (variants, states, composition), API design (props, slots, events), documentation (when to use, how to use, accessibility), and maintenance (versioning, deprecation, contribution). Whether building a custom library or adopting an existing one (Material, Ant Design, Chakra), the principles remain the same: make components flexible but not overwhelming, composable but not fragmented, documented but not verbose. A great component library is infrastructure that disappears—teams use it without thinking about it.

## Learning Objectives

By mastering Component Libraries, you will be able to:

- Design comprehensive component libraries in Figma/Sketch with variants and states
- Build code component libraries with clear, flexible APIs
- Apply atomic design methodology to organize components
- Document components effectively for designers and developers
- Maintain component library consistency between design and code
- Evaluate and choose existing component libraries for projects
- Version, deprecate, and evolve components over time
- Ensure component accessibility and responsiveness

## Key Knowledge Points

### What is a Component Library?

**Definition:**
A component library is a collection of reusable UI components (buttons, inputs, cards, navigation, modals) with consistent design and behavior, available as both design assets (Figma) and code (React, etc.).

**What's Included:**

**Design Components:**

- Figma/Sketch components with variants
- All states (default, hover, active, disabled, error)
- All sizes (small, medium, large)
- Documentation (when to use, guidelines)

**Code Components:**

- Functional implementations (React, Vue, Web Components)
- Props/API for customization
- Accessibility built-in (ARIA, keyboard support)
- Tests (unit, accessibility, visual regression)
- Documentation (props, examples, usage)

**Component Library vs UI Kit:**

- **UI Kit:** Design-only (Figma library)
- **Component Library:** Design + Code (both synced)

### Why Component Libraries Matter

**Consistency:**

- Same button everywhere (visually, behaviorally)
- Predictable user experience
- Cohesive brand

**Efficiency:**

- Reuse instead of rebuild
- Designer: Drag button from library (not redraw)
- Developer: Import button component (not re-code)
- 10x faster than starting from scratch

**Quality:**

- Components are tested (accessibility, cross-browser, responsive)
- Best practices built-in
- Fewer bugs than one-off implementations

**Collaboration:**

- Shared vocabulary ("medium primary button")
- Designers and developers reference same components
- Smoother handoff

**Scalability:**

- Add new feature? Use existing components
- New team member? They use library (don't reinvent)
- New product? Start with component library

**Maintenance:**

- Update button once → All instances update
- Easier to implement rebrand or design changes
- Centralized improvements (accessibility fix applies everywhere)

### Atomic Design Methodology

Brad Frost's Atomic Design provides a hierarchy for organizing components:

**Atoms (smallest):**

- Cannot be broken down further
- Examples: Button, Input, Label, Icon, Badge, Avatar
- Basic HTML elements styled

**Molecules (simple combinations):**

- Groups of atoms functioning together
- Examples:
  - Search field: Input + Button + Icon
  - Form field: Label + Input + Error message
  - Profile: Avatar + Name label

**Organisms (complex combinations):**

- Groups of molecules and/or atoms
- Form distinct sections of interface
- Examples:
  - Navigation bar: Logo + Menu (molecules) + Search field + Profile
  - Card: Image + Header (molecule) + Body text + Footer + Action buttons
  - Form: Multiple form fields + Submit button + validation

**Templates:**

- Page-level layouts
- Wireframes with placeholder content
- Shows content structure

**Pages:**

- Specific instances of templates with real content
- What users actually see

**For Component Libraries:**

- Focus on Atoms, Molecules, Organisms
- Templates and Pages are typically product-specific (not in shared library)

**Example Hierarchy:**

- **Atom:** Button
- **Molecule:** Search field (Input + Button)
- **Organism:** Header (Logo + Navigation + Search field + User profile)

See [[Atomic Design]] for more details.

### Component Variants and States

Every component needs to account for different contexts and interactions.

**Variants:**
Different versions of the same component type.

**Button Variants:**

- **Type:** Primary, Secondary, Tertiary, Ghost, Link
- **Size:** Small, Medium, Large
- **Icon:** Icon-only, Icon-left, Icon-right
- **Full-width:** Yes/No

**States:**
Interactive states for each variant.

**Button States:**

- Default
- Hover
- Active (pressed)
- Focus (keyboard)
- Disabled
- Loading

**Other Component States:**

**Input:**

- Empty (placeholder)
- Filled
- Focus
- Error
- Disabled
- Read-only

**Checkbox:**

- Unchecked
- Checked
- Indeterminate (partially checked)
- Disabled
- Error

**Avoid State Explosion:**
Not every variant needs every state designed individually (would be 100s of combinations).

**Solution:**

- Design common combinations (primary button: all states)
- Document state rules (hover = slightly darker)
- Developers implement states programmatically

### Component API Design

How developers use your components.

**Props (React Example):**

```jsx
<Button
  variant="primary" // Type of button
  size="medium" // Size
  disabled={false} // Disabled state
  loading={false} // Loading state
  icon={<IconName />} // Optional icon
  onClick={handleClick} // Click handler
>
  Button Text
</Button>
```

**Key Principles:**

**1. Sensible Defaults:**

```jsx
// Don't require every prop
<Button>Click me</Button>
// Defaults: variant="primary", size="medium", disabled=false
```

**2. Clear, Consistent Naming:**

- ✅ `variant` (type of component)
- ✅ `size` (small, medium, large)
- ✅ `disabled` (boolean)
- ❌ `kind`, `flavor`, `style` (confusing, inconsistent)

**3. Composition Over Configuration:**

**Configuration (many props):**

```jsx
<Card
  title="Title"
  subtitle="Subtitle"
  image="/path.jpg"
  actions={[<Button />, <Button />]}
/>
```

**Pros:** Simple for common cases
**Cons:** Inflexible, limited customization

**Composition (children/slots):**

```jsx
<Card>
  <CardHeader>
    <CardTitle>Title</CardTitle>
    <CardSubtitle>Subtitle</CardSubtitle>
  </CardHeader>
  <CardImage src="/path.jpg" />
  <CardBody>Content here</CardBody>
  <CardFooter>
    <Button>Action 1</Button>
    <Button>Action 2</Button>
  </CardFooter>
</Card>
```

**Pros:** Flexible, customizable
**Cons:** More verbose

**Best Practice:** Offer both

- Common cases: Configuration (simple API)
- Complex cases: Composition (flexible)

**4. Controlled vs Uncontrolled:**

**Controlled (parent manages state):**

```jsx
<Input value={value} onChange={setValue} />
```

Component doesn't manage its own state.

**Uncontrolled (component manages state):**

```jsx
<Input defaultValue="Hello" />
```

Component has internal state.

**Best Practice:** Support both

- Controlled for forms (parent needs to validate, submit)
- Uncontrolled for simple cases (less boilerplate)

### Building Design Components

**In Figma:**

**1. Create Base Component:**

- Design button (one variant, one state)
- Make it a component (Cmd/Ctrl + Alt + K)

**2. Add Variants:**

- Component → Add variant
- Create variants:
  - Variant property: `Type` (Primary, Secondary, Tertiary)
  - Variant property: `Size` (Small, Medium, Large)
  - Variant property: `State` (Default, Hover, Disabled)

**3. Use Auto Layout:**

- Makes component responsive to content
- Padding adjusts automatically
- See [[Components-and-Variants]]

**4. Define Styles (Tokens):**

- Use color styles for fill (linked to [[Design-Tokens]])
- Use text styles for label
- Update style → All instances update

**5. Document:**

- Description in component properties
- "When to use", "Avoid for", examples

**6. Publish to Library:**

- Share with team
- Others can insert from library

**Best Practices:**

- ✅ Name clearly: "Button / Primary / Medium"
- ✅ Use Auto Layout (responsive)
- ✅ Link to styles (tokens)
- ✅ Document usage
- ✅ Keep variants manageable (not 100 combinations)

**In Sketch:**

- Similar workflow with Symbols and Overrides
- Less popular now (Figma dominates)

### Building Code Components

**Technology Choices:**

**React:**

- Most popular
- Component-based, hooks for state
- Libraries: Chakra UI, Radix UI, Headless UI

**Vue:**

- Similar to React
- Libraries: Vuetify, Element Plus

**Angular:**

- Full framework
- Libraries: Angular Material

**Web Components:**

- Browser-native, framework-agnostic
- Use anywhere (React, Vue, plain HTML)
- Libraries: Lit, Stencil

**Svelte:**

- Compile-time framework
- Growing in popularity

**Example: Button Component (React):**

```jsx
// Button.jsx
import React from "react";
import "./Button.css";

export const Button = ({
  children,
  variant = "primary",
  size = "medium",
  disabled = false,
  loading = false,
  icon = null,
  onClick,
  ...props
}) => {
  const classNames = [
    "button",
    `button--${variant}`,
    `button--${size}`,
    loading && "button--loading",
  ]
    .filter(Boolean)
    .join(" ");

  return (
    <button
      className={classNames}
      disabled={disabled || loading}
      onClick={onClick}
      aria-busy={loading}
      {...props}
    >
      {icon && <span className="button__icon">{icon}</span>}
      <span className="button__label">{children}</span>
      {loading && <span className="button__spinner" />}
    </button>
  );
};
```

**Styles (using tokens):**

```css
/* Button.css */
.button {
  display: inline-flex;
  align-items: center;
  gap: var(--spacing-sm);
  padding: var(--spacing-sm) var(--spacing-md);
  font-size: var(--font-size-base);
  font-weight: var(--font-weight-medium);
  border-radius: var(--border-radius-md);
  border: none;
  cursor: pointer;
  transition: all var(--duration-fast) var(--easing-ease-out);
}

.button--primary {
  background-color: var(--color-primary);
  color: var(--color-white);
}

.button--primary:hover:not(:disabled) {
  background-color: var(--color-primary-hover);
}

.button--secondary {
  background-color: var(--color-secondary);
  color: var(--color-white);
}

.button--small {
  padding: var(--spacing-xs) var(--spacing-sm);
  font-size: var(--font-size-sm);
}

.button--large {
  padding: var(--spacing-md) var(--spacing-lg);
  font-size: var(--font-size-lg);
}

.button:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}

.button:focus-visible {
  outline: 2px solid var(--color-focus);
  outline-offset: 2px;
}
```

**Usage:**

```jsx
import { Button } from "./components/Button";

function App() {
  return (
    <div>
      <Button>Default Button</Button>
      <Button variant="secondary">Secondary</Button>
      <Button size="large">Large Button</Button>
      <Button disabled>Disabled</Button>
      <Button loading>Loading...</Button>
    </div>
  );
}
```

### Component Documentation

Every component needs comprehensive documentation.

**What to Document:**

**1. Overview:**

- What is this component?
- When to use it
- When NOT to use it

**Example:**

```markdown
# Button

Buttons trigger actions or navigate users.

## When to use

- Primary actions (submit form, save, confirm)
- Navigation (next step, go to page)

## When NOT to use

- Links to external pages (use Link component)
- Non-interactive elements
```

**2. Anatomy:**

- Visual breakdown of parts
- Labels for each part

**Example:**

```
[Icon] Label [Loading Spinner]
  ↑      ↑           ↑
Optional Required Optional
```

**3. Variants:**

- All available variants with visual examples
- When to use each

**Example:**

```markdown
## Variants

### Primary

Use for primary actions (submit, save, confirm)
[Visual example]

### Secondary

Use for secondary actions (cancel, back)
[Visual example]

### Tertiary

Use for low-priority actions (more options, view details)
[Visual example]
```

**4. Props/API:**

- All available props
- Type, default value, description

**Example:**

```markdown
## Props

| Prop     | Type                                   | Default   | Description           |
| -------- | -------------------------------------- | --------- | --------------------- |
| variant  | 'primary' \| 'secondary' \| 'tertiary' | 'primary' | Button style          |
| size     | 'small' \| 'medium' \| 'large'         | 'medium'  | Button size           |
| disabled | boolean                                | false     | Disables button       |
| loading  | boolean                                | false     | Shows loading spinner |
| icon     | ReactNode                              | null      | Optional icon         |
| onClick  | function                               | -         | Click handler         |
```

**5. Code Examples:**

- Common use cases with code
- Copy-paste ready

**Example:**

```jsx
// Basic usage
<Button>Click me</Button>

// With variant
<Button variant="secondary">Cancel</Button>

// With icon
<Button icon={<IconSave />}>Save</Button>

// Loading state
<Button loading>Submitting...</Button>
```

**6. Accessibility:**

- Keyboard support (Tab, Enter, Space)
- ARIA attributes
- Screen reader behavior
- Focus management

**Example:**

```markdown
## Accessibility

- Keyboard: Tab to focus, Enter/Space to activate
- Screen reader: Announces label and state
- Focus: Visible focus ring (2px outline)
- Disabled: Not focusable, announced as disabled
```

**7. Do's and Don'ts:**

- Visual examples of correct and incorrect usage
- Common mistakes

**Example:**

```markdown
## Do's and Don'ts

✅ **Do:**

- Use primary button for main action
- Use clear, action-oriented labels ("Save", "Submit")
- Limit to 1-2 primary buttons per view

❌ **Don't:**

- Don't use multiple primary buttons for different actions
- Don't use vague labels ("Click here", "OK")
- Don't disable without explanation (show error message)
```

**8. Design Files:**

- Link to Figma component
- Downloadable assets (if applicable)

### Component Library Tools

**Design:**

- **Figma:** Component libraries with variants
- **Sketch:** Symbols and libraries (less common)
- **Adobe XD:** Components and states

**Code:**

**React:**

- **Storybook:** Interactive component explorer (most popular)
- **Docz:** Documentation + live playground
- **React Styleguidist:** Component documentation generator

**Vue:**

- **Storybook:** Works with Vue
- **Vuese:** Vue component documentation

**Angular:**

- **Storybook:** Works with Angular
- **Compodoc:** Angular documentation tool

**Web Components:**

- **Storybook:** Works with Web Components
- **Custom Elements Manifest:** Standard for documenting Web Components

**Framework-Agnostic:**

- **Storybook:** Supports React, Vue, Angular, Web Components, Svelte, etc. (most versatile)

### Storybook Deep Dive

**What is Storybook:**

- Interactive component library/documentation
- Develop components in isolation
- Test different states and props
- Living documentation

**Installation:**

```bash
npx sb init
```

**Example Story:**

```jsx
// Button.stories.jsx
import { Button } from "./Button";

export default {
  title: "Components/Button",
  component: Button,
  argTypes: {
    variant: {
      control: "select",
      options: ["primary", "secondary", "tertiary"],
    },
    size: {
      control: "select",
      options: ["small", "medium", "large"],
    },
  },
};

// Default story
export const Primary = {
  args: {
    children: "Button",
    variant: "primary",
  },
};

export const Secondary = {
  args: {
    children: "Button",
    variant: "secondary",
  },
};

export const Small = {
  args: {
    children: "Small Button",
    size: "small",
  },
};

export const WithIcon = {
  args: {
    children: "Save",
    icon: <IconSave />,
  },
};

export const Loading = {
  args: {
    children: "Loading...",
    loading: true,
  },
};
```

**Features:**

- **Controls:** Interactive prop editors
- **Actions:** Log events (onClick, onChange)
- **Docs:** Auto-generated documentation
- **Accessibility addon:** Test accessibility
- **Viewport addon:** Test responsive design

**Deploy Storybook:**

- Static site
- Host on Netlify, Vercel, GitHub Pages
- Share with team, stakeholders

### Popular Component Libraries

**Learn from the best:**

**Material UI (React):**

- Google's Material Design
- Comprehensive (50+ components)
- Highly customizable (theming)
- mui.com

**Ant Design (React, Vue, Angular):**

- Enterprise-focused
- 60+ components
- Strong design language
- ant.design

**Chakra UI (React):**

- Accessible, composable
- Simple, clean design
- Great DX (developer experience)
- chakra-ui.com

**Radix UI (React):**

- Unstyled, accessible primitives
- You add styling
- Excellent accessibility
- radix-ui.com

**Headless UI (React, Vue):**

- Unstyled components by Tailwind CSS team
- Fully accessible
- Pair with Tailwind
- headlessui.com

**Shadcn UI (React):**

- Copy-paste components (not installed)
- Built on Radix + Tailwind
- You own the code
- ui.shadcn.com

**Bootstrap:**

- Oldest, most widely used
- HTML/CSS/JS (framework-agnostic)
- getbootstrap.com

**Mantine (React):**

- 100+ hooks, 120+ components
- Dark mode, customizable
- mantine.dev

**Study these for:**

- Component API design
- Documentation style
- Variant structure
- Accessibility implementation

### Keeping Design and Code in Sync

**Challenge:** Design components (Figma) and code components (React) drift apart.

**Solutions:**

**1. Single Source of Truth:**

- Design tokens in JSON
- Both Figma and code reference same tokens
- See [[Design-Tokens]]

**2. Design-to-Code Tools:**

- **Figma Dev Mode:** Inspect designs, copy code
- **Figma Variables:** Map to CSS variables
- **Anima:** Figma → React code (automated)
- **Caveats:** Generated code often needs cleanup

**3. Regular Audits:**

- Quarterly: Compare Figma library with code library
- Are variants aligned?
- Are styles (colors, spacing) same?
- Fix discrepancies

**4. Shared Documentation:**

- Document component once (Storybook)
- Embed Figma designs in Storybook
- Designers and developers see same doc

**5. Process:**

- Design in Figma first (design review)
- Build in code (matches design exactly)
- Update documentation
- Release both (Figma publish + npm publish)

### Versioning and Deprecation

**Semantic Versioning:**

- **Major (1.0 → 2.0):** Breaking changes (API changed, removed)
- **Minor (1.0 → 1.1):** New components, new features (backward compatible)
- **Patch (1.0.0 → 1.0.1):** Bug fixes

**Deprecation Process:**

1. Announce: "Button `type` prop deprecated, use `variant`"
2. Add deprecation warning (console.warn in code)
3. Provide migration guide
4. Give time (6 months, 1 year)
5. Remove in next major version

**Changelog:**
Document every release.

**Example:**

```markdown
## v2.0.0

### Breaking

- Button: Renamed `type` prop to `variant`
- Card: Removed `shadow` prop (use `elevation` instead)

### Migration Guide

- Replace `<Button type="primary">` with `<Button variant="primary">`
- Replace `<Card shadow="md">` with `<Card elevation={2}>`

### Added

- New DatePicker component
- Button: New `loading` state

### Fixed

- Input: Fixed focus ring on Safari
- Modal: Fixed scroll lock on iOS
```

### Testing Component Libraries

**Types of Tests:**

**1. Unit Tests:**

- Does component render?
- Do props work correctly?
- Do interactions fire events?

**Tools:** Jest, React Testing Library, Vitest

**Example:**

```jsx
test("Button renders with text", () => {
  render(<Button>Click me</Button>);
  expect(screen.getByText("Click me")).toBeInTheDocument();
});

test("Button calls onClick when clicked", () => {
  const handleClick = jest.fn();
  render(<Button onClick={handleClick}>Click</Button>);
  fireEvent.click(screen.getByText("Click"));
  expect(handleClick).toHaveBeenCalledTimes(1);
});
```

**2. Accessibility Tests:**

- Automated: axe, jest-axe
- Manual: Keyboard navigation, screen reader

**Example:**

```jsx
test("Button is accessible", async () => {
  const { container } = render(<Button>Click me</Button>);
  const results = await axe(container);
  expect(results).toHaveNoViolations();
});
```

**3. Visual Regression Tests:**

- Take screenshots of components
- Compare with baseline
- Detect unintended visual changes

**Tools:** Chromatic (Storybook), Percy, BackstopJS

**4. Integration Tests:**

- Test components working together
- User workflows

**Tools:** Cypress, Playwright

**Best Practice:**

- 100% unit test coverage for logic
- Accessibility tests for all interactive components
- Visual regression for key components
- Smoke tests (does it render without crashing)

### Best Practices

**Do:**

- ✅ Start small (10-15 core components)
- ✅ Design all states and variants
- ✅ Use composition (build complex from simple)
- ✅ Document thoroughly (usage, accessibility, examples)
- ✅ Build accessibility in from start
- ✅ Test (unit, accessibility, visual)
- ✅ Version clearly (semver, changelog)
- ✅ Keep design and code in sync
- ✅ Provide migration guides for breaking changes

**Don't:**

- ❌ Build everything at once (overwhelming)
- ❌ Create too many variants (simplify)
- ❌ Build in isolation (get feedback from users)
- ❌ Forget accessibility (WCAG 2.1 AA minimum)
- ❌ Let documentation lag (document as you build)
- ❌ Make breaking changes without notice
- ❌ Have design and code out of sync

## Related Topics

- [[Design-Systems]]
- [[Design-Tokens]]
- [[Components-and-Variants]]
- [[Atomic Design]]
- [[Accessibility]]
- [[Design-System-Documentation]]
- [[Usability-Testing]]

## Tools & Resources

**Design:**

- Figma (figma.com)
- Sketch (sketch.com)

**Code/Documentation:**

- Storybook (storybook.js.org)
- Docz (docz.site)
- React Styleguidist (react-styleguidist.js.org)

**Testing:**

- Jest (jestjs.io)
- React Testing Library (testing-library.com)
- Chromatic (chromatic.com) - Visual regression
- axe DevTools (deque.com) - Accessibility

**Component Libraries (Study):**

- Material UI (mui.com)
- Chakra UI (chakra-ui.com)
- Radix UI (radix-ui.com)
- Ant Design (ant.design)
- Shadcn UI (ui.shadcn.com)

**Learning:**

- Component Gallery (component.gallery)
- Storybook Showcase (storybook.js.org/showcase)

## Practice Exercises

1. **Inventory Existing Product:** Choose a website (e.g., Airbnb, Stripe). Screenshot all unique components you can find. Categorize using Atomic Design (atoms, molecules, organisms). How many button variants? How many input types? Create a spreadsheet.

2. **Design Button Component:** In Figma, create a complete Button component:

   - 3 variants (Primary, Secondary, Tertiary)
   - 3 sizes (Small, Medium, Large)
   - 5 states (Default, Hover, Active, Focus, Disabled)
   - Use Auto Layout and styles (linked to tokens)
   - Document: When to use, accessibility notes

3. **Build Button Component:** In React, build the button from Exercise 2:

   - Support props: variant, size, disabled, loading, icon, onClick
   - Use CSS with design tokens (CSS variables)
   - Accessible (semantic HTML, ARIA, focus styles)
   - Write 5 unit tests (renders, props work, onClick fires, accessibility)

4. **Document Component:** Write complete documentation for your Button:

   - Overview, when to use/avoid
   - Anatomy diagram
   - Props table (name, type, default, description)
   - 5 code examples (basic, with icon, loading, disabled, sizes)
   - Accessibility section
   - Do's and Don'ts (with visual examples)

5. **Storybook Setup:** Install Storybook in a React project. Create stories for Button:

   - Default story (interactive controls for all props)
   - 5 variant stories (Primary, Secondary, Loading, With Icon, Disabled)
   - Add documentation (MDX)
   - Run Storybook, test interactivity

6. **Component Audit:** Choose a popular component library (Material UI, Chakra). Analyze their Button component:
   - What variants do they offer?
   - What props are available?
   - How is it documented?
   - What's excellent? What's confusing?
     Write 1-page analysis with screenshots.

## Further Reading

- **"Atomic Design" by Brad Frost** (free online, atomicdesign.bradfrost.com)
- **"Design Systems" by Alla Kholmatova** (chapters on components)
- Storybook Documentation (storybook.js.org/docs)
- **"Building Design Systems" by Sarrah Vesselov & Taurie Davis**
- Component Gallery (component.gallery) - examples across systems
- **"Design Systems Handbook"** (designsystemshandbook.com)
- Brad Frost's blog (bradfrost.com) - component patterns
- Nathan Curtis on Medium (medium.com/@nathanacurtis) - component design articles
- Radix UI Documentation (radix-ui.com) - excellent component API design
- Chakra UI Documentation (chakra-ui.com) - great composition patterns
