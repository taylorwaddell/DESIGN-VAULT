# Design System Documentation

## Introduction

A design system without documentation is like a library without a catalog—components exist, but no one knows how to find or use them. Design system documentation is the guide that empowers designers, developers, product managers, and stakeholders to understand, implement, and contribute to the system. Great documentation does more than list components; it teaches principles, explains when and why to use elements, provides code examples, addresses accessibility, and evolves as the system grows.

The challenge of design system documentation is serving multiple audiences with different needs: designers need usage guidelines and Figma files, developers need code examples and APIs, product managers need to understand capabilities, and executives need to see business value. Documentation must be comprehensive yet scannable, authoritative yet approachable, up-to-date yet stable. When done well, documentation reduces support burden (teams self-serve), increases adoption (easy to understand and implement), and maintains consistency (clear guidance prevents misuse).

Mastering design system documentation means understanding information architecture (how to organize), writing clearly for different audiences, choosing the right tools (static sites, Storybook, wikis), and establishing processes for keeping docs current. It's not a one-time deliverable but a living resource that requires ongoing maintenance, feedback loops, and governance. Documentation is how your design system scales beyond its creators—it's the teacher when you're not in the room.

## Learning Objectives

By mastering Design System Documentation, you will be able to:

- Structure comprehensive documentation for diverse audiences
- Write clear, actionable guidance for components and patterns
- Choose and implement appropriate documentation tools
- Create effective code examples and usage guidelines
- Document accessibility requirements and best practices
- Establish processes for keeping documentation up-to-date
- Design information architecture that scales
- Measure and improve documentation effectiveness

## Key Knowledge Points

### Why Documentation Matters

**Without Documentation:**

- ❌ Teams don't know what's available
- ❌ Inconsistent usage (everyone interprets differently)
- ❌ Frequent support requests ("How do I...?")
- ❌ Low adoption (too hard to figure out)
- ❌ Reinvention (easier to build from scratch than find existing)
- ❌ Accessibility overlooked (not documented, not implemented)

**With Good Documentation:**

- ✅ Self-service (teams find answers without asking)
- ✅ Consistent implementation (clear guidance)
- ✅ Faster adoption (easy to understand, easy to use)
- ✅ Reduced support burden (fewer questions)
- ✅ Better quality (accessibility, best practices documented)
- ✅ Onboarding (new team members learn quickly)
- ✅ Scalability (system scales beyond core team)

**Business Value:**

- Faster time to market (teams move faster)
- Lower training costs (self-service learning)
- Higher consistency (better user experience)
- Lower maintenance costs (fewer support requests)

### Documentation Audiences

Different users need different information.

**1. Designers:**

- **Need:** Visual examples, usage guidelines, when to use, Figma files
- **Questions:** "What component should I use for X?", "What does this look like?", "Where's the Figma file?"
- **Format:** Visual examples, do's/don'ts, Figma links

**2. Developers:**

- **Need:** Code examples, API reference, implementation details, accessibility requirements
- **Questions:** "How do I implement this?", "What props does it accept?", "How do I handle this interaction?"
- **Format:** Code snippets, prop tables, technical specs

**3. Product Managers:**

- **Need:** Capabilities overview, use cases, what's available
- **Questions:** "Can the system support this feature?", "What components exist?", "What's the timeline for X?"
- **Format:** High-level overviews, component gallery

**4. Content Designers/UX Writers:**

- **Need:** Voice and tone, microcopy guidelines, content patterns
- **Questions:** "What should the button say?", "How do we write error messages?", "What's our tone?"
- **Format:** Writing guidelines, examples, [[UX-Writing]]

**5. Contributors:**

- **Need:** How to propose, design, and build new components
- **Questions:** "How do I contribute?", "What's the review process?", "Where do I start?"
- **Format:** Contribution guidelines, process documentation

**6. Stakeholders/Executives:**

- **Need:** Business value, adoption metrics, roadmap
- **Questions:** "What's the ROI?", "How widely adopted?", "What's next?"
- **Format:** Dashboards, case studies, roadmap

**Documentation Strategy:**

- Create shared content (component overview)
- Provide role-specific deep dives (designer guidelines, developer API)
- Use tabs or sections to separate concerns

### Documentation Structure

**High-Level Hierarchy:**

```
Home/Introduction
├── Getting Started
│   ├── For Designers
│   ├── For Developers
│   └── For Contributors
├── Foundation
│   ├── Design Principles
│   ├── Accessibility
│   ├── Color (Tokens)
│   ├── Typography (Tokens)
│   ├── Spacing (Tokens)
│   ├── Iconography
│   └── Motion/Animation
├── Components
│   ├── Atoms (Button, Input, Icon, Badge, etc.)
│   ├── Molecules (Search, Form Field, etc.)
│   └── Organisms (Navigation, Card, Modal, etc.)
├── Patterns
│   ├── Forms
│   ├── Navigation
│   ├── Data Display
│   ├── Feedback (Errors, Success)
│   └── Empty States
├── Content/Voice & Tone
│   ├── Writing Principles
│   ├── Microcopy Guidelines
│   └── Terminology
├── Resources
│   ├── Design Files (Figma, Sketch)
│   ├── Code Repos (GitHub)
│   ├── Downloads (Icons, logos)
│   └── Tools & Plugins
└── About
    ├── Contribution Guidelines
    ├── Changelog
    ├── Roadmap
    ├── Support/Contact
    └── Team
```

### Component Documentation Template

For each component, document the following:

**1. Overview:**

- Brief description (1-2 sentences)
- When to use
- When NOT to use (avoid misuse)

**Example:**

```markdown
# Button

Buttons trigger actions or navigate users to another page or screen.

## When to use

- Triggering actions (submit form, save, delete)
- Primary and secondary calls-to-action
- Interactive elements that do something on click

## When NOT to use

- Navigation to external pages (use Link instead)
- Non-interactive elements (use text, not a button)
- Inline text links (use Link component)
```

**2. Anatomy:**

- Visual diagram labeling component parts
- Explain each part's purpose

**Example:**

```markdown
## Anatomy

[Icon] Label [Loading Spinner]
↑ ↑ ↑
Optional Required Optional

1. **Icon (optional):** Visual indicator of action (e.g., save icon)
2. **Label (required):** Clear, action-oriented text
3. **Loading spinner (optional):** Shown when action is processing
```

**3. Variants:**

- All available variants with visual examples
- When to use each variant

**Example:**

```markdown
## Variants

### Primary

Use for the main action on a page. Limit to 1-2 primary buttons per view.

[Visual example]

**Use for:** Submit, Save, Confirm, Next

### Secondary

Use for secondary actions that are important but not primary.

[Visual example]

**Use for:** Cancel, Back, Alternative actions

### Tertiary

Use for less important actions.

[Visual example]

**Use for:** View details, Learn more, Tertiary options
```

**4. Sizes:**

- Small, Medium, Large (visual examples)
- When to use each size

**5. States:**

- All interactive states (default, hover, active, focus, disabled, loading, error)
- Visual examples for each

**6. Behavior:**

- How component responds to interaction
- Animation, transitions
- Loading states
- Error handling

**Example:**

```markdown
## Behavior

- **Hover:** Background darkens slightly (200ms transition)
- **Active/Pressed:** Background darkens further, slight scale down
- **Focus:** Visible focus ring (2px offset, primary color)
- **Disabled:** 50% opacity, cursor not-allowed, not focusable
- **Loading:** Label replaced by spinner, button disabled during load
```

**7. Accessibility:**

- Keyboard support (Tab, Enter, Space, Arrow keys)
- Screen reader announcements
- ARIA attributes
- Focus management
- Color contrast (WCAG requirements)

**Example:**

```markdown
## Accessibility

### Keyboard Support

- **Tab:** Focus button
- **Enter or Space:** Activate button
- **Shift + Tab:** Focus previous element

### Screen Reader

- Announces: "Button, [Label]"
- If loading: "Button, [Label], busy"
- If disabled: "Button, [Label], dimmed" or "disabled"

### ARIA Attributes

- `role="button"` (if not using `<button>` element)
- `aria-busy="true"` when loading
- `aria-disabled="true"` when disabled
- `aria-label` if label is not text (icon-only button)

### Focus

- Visible focus indicator (2px outline, primary color, 2px offset)
- Focus order follows DOM order

### Color Contrast

- All variants meet WCAG 2.1 Level AA contrast requirements (4.5:1 minimum)
```

See [[Accessibility]], [[WCAG-Guidelines]], [[Keyboard-Navigation]]

**8. Content Guidelines:**

- Label best practices
- Microcopy guidelines
- Examples

**Example:**

```markdown
## Content Guidelines

### Button Labels

- Use action-oriented verbs (Save, Delete, Submit, Continue)
- Be specific (not "Click here" or "OK")
- Keep short (1-3 words ideal)
- Use sentence case ("Save changes" not "Save Changes")

✅ **Good:**

- "Save draft"
- "Delete account"
- "Add to cart"

❌ **Avoid:**

- "Click here"
- "OK"
- "Submit" (too generic, specify what's submitted)
```

See [[UX-Writing]]

**9. Code Examples:**

- Common use cases
- Copy-paste ready
- Multiple examples (basic, with options, complex)

**Example:**

````markdown
## Code Examples

### Basic Usage

\```jsx
<Button>Click me</Button>
\```

### With Variant and Size

\```jsx
<Button variant="secondary" size="large">
Cancel
</Button>
\```

### With Icon

\```jsx
<Button icon={<IconSave />}>
Save changes
</Button>
\```

### Loading State

\```jsx
<Button loading={isSubmitting}>
Submit
</Button>
\```

### Disabled

\```jsx
<Button disabled>
Unavailable
</Button>
\```
````

**10. Props/API Reference:**

- Table of all props
- Type, default value, description

**Example:**

```markdown
## Props

| Prop       | Type                                         | Default     | Description                            |
| ---------- | -------------------------------------------- | ----------- | -------------------------------------- |
| `variant`  | `'primary'` \| `'secondary'` \| `'tertiary'` | `'primary'` | Visual style of button                 |
| `size`     | `'small'` \| `'medium'` \| `'large'`         | `'medium'`  | Size of button                         |
| `disabled` | `boolean`                                    | `false`     | Disables button interaction            |
| `loading`  | `boolean`                                    | `false`     | Shows loading spinner, disables button |
| `icon`     | `ReactNode`                                  | `null`      | Icon to display (left side)            |
| `onClick`  | `(event: MouseEvent) => void`                | -           | Click event handler                    |
| `type`     | `'button'` \| `'submit'` \| `'reset'`        | `'button'`  | HTML button type                       |
```

**11. Do's and Don'ts:**

- Visual examples of correct and incorrect usage
- Common mistakes to avoid

**Example:**

```markdown
## Do's and Don'ts

### Do

✅ Use primary button for the main action
[Visual example]

✅ Use clear, action-oriented labels
[Visual example: Button labeled "Save changes"]

✅ Limit primary buttons (1-2 per view)
[Visual example]

### Don't

❌ Don't use multiple primary buttons for different actions
[Visual example showing confusing multiple primary buttons]

❌ Don't use vague labels
[Visual example: Button labeled "Click here"]

❌ Don't disable without explanation
[Visual example: Disabled button with no error message nearby]
```

**12. Related Components/Patterns:**

- Links to similar components
- Alternative components

**Example:**

```markdown
## Related

- **Link:** For navigation to other pages
- **IconButton:** Button with only an icon (no label)
- **Button Group:** Multiple related buttons
```

**13. Design Files:**

- Link to Figma component
- Downloadable assets

**Example:**

```markdown
## Design Files

- [Figma Component →](https://figma.com/file/...)
- [Sketch Symbol →](https://sketch.com/...)
```

**14. Changelog:**

- Version history for this component
- What changed, when

**Example:**

```markdown
## Changelog

### v2.1.0 (2024-03-15)

- Added `loading` prop and state

### v2.0.0 (2024-01-10)

- **Breaking:** Renamed `type` prop to `variant`
- Added `tertiary` variant

### v1.2.0 (2023-11-05)

- Added `size` prop (small, medium, large)
```

### Foundation Documentation

**Design Principles:**

- Core principles guiding design decisions
- Examples of principles in action
- See [[Design-Principles]]

**Design Tokens:**

- Color palette (all tokens, values, usage)
- Typography scale
- Spacing scale
- Shadows, borders, animation values
- How to use tokens in design and code
- See [[Design-Tokens]]

**Accessibility:**

- Commitment to accessibility (WCAG Level AA)
- General guidelines (color contrast, keyboard, screen readers)
- Testing procedures
- See [[Accessibility]], [[WCAG-Guidelines]]

**Voice & Tone:**

- Writing principles
- How to write for your product
- Microcopy guidelines
- See [[UX-Writing]]

**Iconography:**

- Icon library (all icons)
- Usage guidelines (size, color, accessibility)
- How to request new icons

**Motion/Animation:**

- Animation principles (when, why, how)
- Timing values (duration tokens)
- Easing curves
- Examples
- See [[Animation-Principles]]

### Pattern Documentation

Patterns are higher-level than components—they're solutions to common problems.

**For Each Pattern:**

**1. Overview:**

- What is this pattern?
- What problem does it solve?

**2. When to Use:**

- Use cases
- Examples

**3. Anatomy:**

- What components are involved?
- Layout structure

**4. Variants:**

- Different versions of the pattern

**5. Behavior:**

- How it works (step-by-step)
- Interactions

**6. Accessibility:**

- Keyboard navigation
- Screen reader behavior
- Focus management

**7. Examples:**

- Visual examples
- Code examples (if applicable)

**8. Best Practices:**

- Do's and don'ts

**Example Pattern: Form Validation**

```markdown
# Form Validation

Pattern for providing feedback on form input errors.

## When to Use

- Multi-field forms
- Required fields
- Fields with format requirements (email, phone, password)

## Anatomy

- Input field
- Label (indicates required with asterisk if needed)
- Helper text (optional, explains format)
- Error message (shown on validation failure)
- Error icon (visual indicator)

## Behavior

### Inline Validation (Recommended)

1. User types in field
2. On blur (leaving field), validate
3. If invalid, show error message below field
4. Field border turns red, error icon appears
5. When user corrects, error clears immediately

### On-Submit Validation

1. User fills form
2. Clicks submit
3. If errors, show error messages for all invalid fields
4. Focus first error field
5. User corrects and resubmits

## Accessibility

- Error messages: `aria-describedby` links to error text
- Invalid fields: `aria-invalid="true"`
- Required fields: `aria-required="true"` or `required` attribute
- Error summary: At top of form (if multiple errors)
- Screen reader announces errors when they appear (live region)

## Best Practices

✅ **Do:**

- Validate on blur, not on every keystroke (less frustrating)
- Show errors inline (near field)
- Be specific ("Email must include @" not "Invalid")
- Disable submit button if form invalid

❌ **Don't:**

- Don't show errors before user interacts with field
- Don't use generic messages ("Error")
- Don't rely on color alone (use icon + text)
```

### Getting Started Guides

**For Designers:**

```markdown
# Getting Started: Designers

## 1. Install Figma

If you don't have Figma, sign up at figma.com

## 2. Get Access to Design System Library

Request access in #design-systems Slack channel

## 3. Enable Library in Figma

1. Open any Figma file
2. Click Assets panel (left sidebar)
3. Click library icon (book)
4. Enable "DesignCo Design System"

## 4. Insert Components

1. Open Assets panel
2. Search for component (e.g., "Button")
3. Drag onto canvas
4. Customize using properties panel (variants, text)

## 5. Use Styles (Tokens)

- Color: Select element, click fill, choose from color styles
- Typography: Select text, click text dropdown, choose text style
- Effects: Select element, click effects, choose effect style

## 6. Learn Components

Browse this documentation to understand when and how to use each component

## 7. Stay Updated

- Watch #design-systems-updates channel
- Review changelog for new components and updates
```

**For Developers:**

````markdown
# Getting Started: Developers

## 1. Install Package

\```bash
npm install @designco/design-system
\```

## 2. Import Styles (CSS)

\```javascript
// In your app entry file (e.g., App.js, index.js)
import '@designco/design-system/dist/styles.css';
\```

## 3. Import Components

\```javascript
import { Button, Input, Card } from '@designco/design-system';

function App() {
return (
<div>
<Button variant="primary">Click me</Button>
<Input label="Name" />
</div>
);
}
\```

## 4. Use Design Tokens (CSS Variables)

\```css
.custom-component {
background-color: var(--color-primary);
padding: var(--spacing-md);
border-radius: var(--border-radius-md);
}
\```

## 5. Explore Components

- Browse component documentation for props, examples, and usage
- Check Storybook for interactive demos: [storybook.designco.com](https://storybook.designco.com)

## 6. TypeScript Support

Package includes TypeScript types. Import types as needed:
\```typescript
import { ButtonProps } from '@designco/design-system';
\```

## 7. Stay Updated

- Watch GitHub repo for releases
- Subscribe to #design-systems-updates Slack channel
- Review changelog for breaking changes
````

### Contribution Guidelines

Document how to contribute to the design system.

**Include:**

**1. When to Contribute:**

- New component needed across multiple products
- Enhancement to existing component
- Bug fix

**2. When NOT to Contribute:**

- One-off, product-specific component
- Experimental, not validated yet
- Duplicates existing component

**3. Contribution Process:**

```markdown
## Contribution Process

### 1. Propose

- Open GitHub issue or post in #design-systems Slack
- Describe: What component? Why needed? Use cases?
- Design systems team reviews (1 week)

### 2. Design

- If approved, create designs in Figma
- Include all variants, states
- Share in Figma for review
- Design team reviews, provides feedback

### 3. Build

- Once design approved, build component
- Match design exactly
- Include accessibility (ARIA, keyboard, focus)
- Write unit tests (>80% coverage)
- Write accessibility tests (jest-axe)

### 4. Document

- Write component documentation (use template)
- Include: Overview, anatomy, variants, props, examples, accessibility, do's/don'ts
- Create Storybook stories

### 5. Review

- Open pull request
- Code review by design systems team
- Design review (matches Figma?)
- Accessibility review

### 6. Merge & Release

- Once approved, merge to main
- Included in next release (minor or major)
- Announced in changelog and Slack

### 7. Evangelize

- Share in demo or show-and-tell
- Update products to use new component
```

**4. Standards:**

- Code style (linting, formatting)
- Accessibility requirements (WCAG 2.1 Level AA)
- Testing requirements (unit, accessibility)
- Documentation requirements (complete template)

**5. Resources:**

- Component documentation template
- Code sandbox/starter
- Figma starter file
- Contact for questions

### Tools for Documentation

**1. Static Site Generators:**

**Docusaurus (Recommended):**

- React-based, fast
- Markdown files
- Versioning built-in
- Search built-in
- Customizable
- Used by: Relay, Jest, Prettier
- docusaurus.io

**VuePress:**

- Vue-based
- Markdown files
- Simple, fast
- vuepress.vuejs.org

**Gatsby:**

- React-based, flexible
- More complex setup
- Good for custom designs
- gatsbyjs.com

**Eleventy (11ty):**

- Simple, fast, flexible
- Markdown, multiple templating languages
- 11ty.dev

**2. Storybook:**

- Interactive component explorer
- Code playground
- Docs addon (auto-generated docs from components)
- Best for component library documentation (not general design system docs)
- Often used alongside static site (Docusaurus for principles/patterns, Storybook for components)
- storybook.js.org

**3. Notion / Confluence:**

- Wikis, easy to edit
- Good for internal docs
- Not great for versioning or code examples
- Hard to make public

**4. Zeroheight:**

- Design system-specific documentation platform
- Integrates with Figma
- Beautiful, polished
- Paid service
- zeroheight.com

**5. Custom Solutions:**

- Build your own with Next.js, Remix, etc.
- Total control, more work

**Recommendation:**

- **Docusaurus (general design system docs)** + **Storybook (component playground)** = comprehensive documentation

### Writing Style

**Be Clear:**

- Short sentences
- Simple words (avoid jargon)
- Active voice ("Use Button for..." not "Button should be used for...")

**Be Specific:**

- ❌ "Use this component for actions"
- ✅ "Use Button to trigger actions like submitting a form or saving a draft"

**Be Concise:**

- Remove fluff
- Get to the point
- Use bullet points and lists (easier to scan)

**Show, Don't Just Tell:**

- Include visual examples
- Include code examples
- Use do's and don'ts with visuals

**Be Actionable:**

- Tell users what to do, not just what exists
- "To add a button, import the Button component and..."

**Be Accessible:**

- Use headings (H1, H2, H3) for hierarchy
- Use descriptive link text ("View Button component" not "Click here")
- Provide alt text for images

### Keeping Documentation Up-to-Date

**Challenge:** Documentation drifts out of sync with code.

**Solutions:**

**1. Document as You Build:**

- Don't build first, document later
- Write docs as part of component development (required for merge)

**2. Automate Where Possible:**

- **Prop tables:** Generate from TypeScript types (Storybook Docs addon does this)
- **Code examples:** Embed live code (CodeSandbox, StackBlitz)
- **Changelog:** Auto-generate from git commits or pull requests

**3. Review Process:**

- Pull requests must include documentation updates
- Design review includes checking docs

**4. Ownership:**

- Each component has an owner (responsible for docs)
- Design systems team reviews periodically

**5. Deprecation Warnings:**

- Mark outdated docs clearly ("This component is deprecated, use X instead")

**6. Version Documentation:**

- Document each major version separately
- Users can switch versions (Docusaurus supports this)

**7. Feedback Loop:**

- "Was this helpful?" on each page
- Link to "Report an issue" (GitHub issue template)
- Monitor questions in Slack (indicates missing docs)

### Measuring Documentation Effectiveness

**Metrics:**

**Quantitative:**

- **Page views:** Most/least visited pages
- **Search queries:** What are users searching for? (gaps in docs?)
- **Support requests:** Decreasing? (docs working) Increasing? (docs not working)
- **Time on page:** Too short = not helpful? Too long = too confusing?
- **GitHub issues:** Bugs? Requests? Questions? (should be in docs)

**Qualitative:**

- **User feedback:** "Was this helpful?" surveys
- **User interviews:** Ask designers/developers about docs
- **Contribution rate:** More contributions = easier to contribute (docs clear)

**Health Check:**

- Quarterly: Review analytics, identify top 10 issues
- Annual: Full documentation audit (what's missing? outdated? confusing?)

### Best Practices

**Do:**

- ✅ Write for your audience (designers, developers, PMs)
- ✅ Show visual examples (images, videos, live demos)
- ✅ Provide copy-paste code examples
- ✅ Document accessibility thoroughly
- ✅ Keep docs and code in sync (document as you build)
- ✅ Make docs searchable (search bar)
- ✅ Version documentation (if breaking changes)
- ✅ Provide "Getting Started" guides
- ✅ Use consistent structure (template for components)
- ✅ Gather feedback (improve based on user needs)

**Don't:**

- ❌ Build components then document later (docs will lag)
- ❌ Assume users know context (explain clearly)
- ❌ Use jargon without defining it
- ❌ Create docs and never update
- ❌ Write only for developers (designers need docs too)
- ❌ Skip accessibility documentation (critical)
- ❌ Make docs hard to find (prominent link, good SEO)

## Related Topics

- [[Design-Systems]]
- [[Component-Libraries]]
- [[Design-Tokens]]
- [[Accessibility]]
- [[UX-Writing]]
- [[Style-Guides]]

## Tools & Resources

**Documentation Tools:**

- Docusaurus (docusaurus.io)
- Storybook (storybook.js.org)
- Zeroheight (zeroheight.com)
- VuePress (vuepress.vuejs.org)

**Examples (Study These):**

- Material Design (material.io) - Comprehensive
- Carbon Design System (carbondesignsystem.com) - Excellent structure
- Polaris (polaris.shopify.com) - Great guidelines
- Lightning (lightningdesignsystem.com) - Clear examples
- Atlassian Design System (atlassian.design) - Strong content guidance
- Primer (primer.style) - GitHub's design system
- Spectrum (spectrum.adobe.com) - Adobe's design system

**Writing Resources:**

- **"Docs for Developers" by Jared Bhatti et al.** (technical writing)
- Microsoft Writing Style Guide (accessible writing)
- Hemingway Editor (hemingwayapp.com) - Readability

**Learning:**

- Design Systems Handbook (designsystemshandbook.com)
- Nathan Curtis articles (medium.com/@nathanacurtis)

## Practice Exercises

1. **Analyze Existing Docs:** Choose a design system (Material, Carbon, Polaris). Spend 30 minutes exploring documentation. Evaluate:

   - How is it organized (IA)?
   - How clear are component docs?
   - What's excellent?
   - What's confusing or missing?
     Write 1-page analysis with recommendations.

2. **Document a Component:** Choose a component you've designed or built (Button, Input, Card). Write complete documentation using the template:

   - Overview, when to use/avoid
   - Anatomy
   - Variants (with visual examples)
   - States
   - Behavior
   - Accessibility (keyboard, screen reader, ARIA)
   - Content guidelines
   - Code examples (3-5)
   - Props table
   - Do's and don'ts (with visuals)
   - Related components

3. **Write Getting Started Guide:** For a hypothetical design system, write a "Getting Started for Developers" guide:

   - Installation (npm install)
   - Basic setup (import styles)
   - First component (code example)
   - Using tokens (code example)
   - Where to learn more (links)
     Keep under 500 words, clear and actionable.

4. **Create Contribution Guidelines:** Write contribution guidelines for a design system:

   - When to contribute (criteria)
   - Contribution process (propose → design → build → review → release)
   - Standards (code quality, accessibility, testing, documentation)
   - Resources (templates, contacts)
     1-2 pages.

5. **Documentation IA:** Design information architecture for a design system documentation site:

   - List all top-level sections (Getting Started, Foundation, Components, Patterns, etc.)
   - List sub-sections for each
   - Consider: Multiple audiences (designers, developers, PMs), discoverability, scalability
     Create a sitemap (visual or outline).

6. **Audit Documentation:** Find 3 pieces of your current documentation (or a public design system). For each:
   - Is it clear? (Can someone follow it without help?)
   - Is it complete? (All necessary information?)
   - Is it actionable? (Tells user what to do?)
   - Is it accessible? (Headings, alt text, clear language?)
     Note improvements needed for each.

## Further Reading

- **"Docs for Developers" by Jared Bhatti et al.** (technical documentation)
- **"Design Systems" by Alla Kholmatova** (chapter on documentation)
- Docusaurus Documentation (docusaurus.io/docs)
- **"Documentation System" by Brad Frost** (article)
- Nathan Curtis on Medium (articles on design system documentation)
- **"Writing Design System Documentation" by Amy Hupe** (articles)
- Microsoft Writing Style Guide (microsoft.com/en-us/style-guide)
- **"Design Systems Handbook"** (free, designsystemshandbook.com)
- Good documentation examples: Material, Carbon, Polaris, Lightning, Primer
