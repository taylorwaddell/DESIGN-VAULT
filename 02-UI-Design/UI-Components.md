# UI Components

## Introduction

UI components are the reusable building blocks of interfaces—buttons, inputs, cards, modals, navigation bars—that users interact with to accomplish tasks. Understanding common UI components, their patterns, best practices, and appropriate usage is foundational to designing intuitive, familiar interfaces. Components aren't arbitrary; they're evolved solutions to recurring interaction problems, refined through years of design practice and user testing.

Mastering UI components means knowing not just what they look like, but when to use them, how they behave, and what users expect from them. Each component has established patterns (e.g., buttons should look clickable, inputs should show focus states) that, when followed, create predictable, learnable interfaces. Breaking these patterns without good reason creates confusion and friction.

In modern design systems, components are systematically defined with states, variants, and usage guidelines. Understanding components deeply enables you to build [[Component-Libraries]], contribute to [[Design-Systems]], and communicate effectively with developers who think in component terms.

## Learning Objectives

By mastering UI Components, you will be able to:

- Identify and design core UI components ([[Buttons]], [[Inputs]], [[Cards]], [[Modals]], [[Navigation]])
- Understand appropriate use cases for each component type
- Design all necessary [[Component States]] (default, hover, focus, disabled, error, loading)
- Apply [[Accessibility]] best practices to components (ARIA, keyboard navigation, labels)
- Choose between component variations (e.g., dropdown vs. autocomplete vs. radio buttons)
- Document component behavior and usage in [[Style-Guides]]
- Build components that match platform conventions ([[iOS HIG]], [[Material Design]])

## Key Knowledge Points

### Core Components

- [[Buttons]]

  - **Types:**
    - [[Primary Button]] (main action, filled)
    - [[Secondary Button]] (secondary actions, outlined/ghost)
    - [[Tertiary Button]] (subtle actions, text-only)
    - [[Icon Button]] (icon only, compact)
    - [[Floating Action Button]] (FAB, prominent mobile action)
  - **States:** Default, Hover, Focus, Active/Pressed, Disabled, Loading
  - **Best Practices:**
    - Clear, action-oriented labels ("Save", "Continue", not "Submit")
    - Adequate padding (min 44x44px touch target on mobile)
    - Primary button per screen (focus action)
    - Disabled state visually distinct

- [[Input Fields]]

  - **Types:**
    - [[Text Input]] (single line)
    - [[Text Area]] (multi-line)
    - [[Number Input]]
    - [[Email Input]]
    - [[Password Input]] (masked, show/hide toggle)
    - [[Search Input]]
    - [[Date Picker]]
    - [[Time Picker]]
  - **Anatomy:**
    - [[Label]] (what input is for)
    - [[Placeholder]] (example or hint, not required info)
    - [[Helper Text]] (additional guidance)
    - [[Error Message]] (what went wrong, how to fix)
    - [[Character Counter]]
  - **States:** Empty, Filled, Focus, Error, Disabled, Read-only
  - **Best Practices:**
    - Always label inputs
    - Clear error messages with solutions
    - Inline validation when helpful
    - Appropriate input types (keyboard optimization on mobile)

- [[Checkboxes]]

  - **Purpose:** Multiple selections
  - **States:** Unchecked, Checked, Indeterminate (partial), Disabled
  - **Anatomy:** Checkbox + label (entire area clickable)
  - **Best Practices:**
    - Use for independent options (pizza toppings)
    - Min 44x44px touch target
    - Label clearly states what checking means

- [[Radio Buttons]]

  - **Purpose:** Single selection from multiple options
  - **States:** Unselected, Selected, Disabled
  - **Best Practices:**
    - Use when all options should be visible
    - 2-7 options ideal (more → dropdown)
    - One pre-selected by default

- [[Toggle Switches]]

  - **Purpose:** On/off, binary choice
  - **States:** Off, On, Disabled
  - **Best Practices:**
    - Immediate effect (no "save" button)
    - Clear label indicating what's being toggled
    - Different from checkbox (checkbox = selection, toggle = state)

- [[Dropdowns]] / [[Select Menus]]
  - **Purpose:** Choose one from many options
  - **States:** Default, Open, Focused, Disabled, Error
  - **Best Practices:**
    - Use when 8+ options
    - Descriptive placeholder or label
    - Searchable for long lists
    - Consider [[Autocomplete]] for better UX

### Navigation Components

- [[Navigation Bar]] / [[Nav Menu]]

  - **Types:**
    - [[Top Nav]] (horizontal, desktop)
    - [[Hamburger Menu]] (hidden, mobile)
    - [[Tab Bar]] (bottom, mobile apps)
    - [[Sidebar Navigation]] (vertical, dashboard)
  - **Elements:** Logo, nav links, search, account/profile
  - **States:** Active page indicator, hover states

- [[Breadcrumbs]]

  - **Purpose:** Show location in hierarchy
  - **Best Practices:**
    - Home > Category > Subcategory > Current Page
    - Last item (current page) not clickable
    - Use sparingly (don't clutter)

- [[Tabs]]

  - **Purpose:** Switch between related views without navigation
  - **Types:** Horizontal tabs, vertical tabs, pill tabs
  - **States:** Active, Inactive, Disabled
  - **Best Practices:**
    - 3-7 tabs ideal
    - Clear active indicator
    - Labels concise

- [[Pagination]]
  - **Purpose:** Navigate multi-page content
  - **Types:**
    - Page numbers (1 2 3 ... 10)
    - Previous/Next
    - Load more button
    - Infinite scroll
  - **Best Practices:**
    - Show current page clearly
    - First/last page options
    - Total page count

### Content Components

- [[Cards]]

  - **Purpose:** Grouped, contained content unit
  - **Anatomy:** Image, title, description, action(s)
  - **Best Practices:**
    - Entire card often clickable
    - Consistent sizing in grids
    - Elevation/shadow for depth
    - Related: [[Card Layout]]

- [[Lists]]

  - **Types:**
    - [[Simple List]]
    - [[List with Avatars]]
    - [[Two-Line List]]
    - [[Three-Line List]]
  - **Best Practices:**
    - Consistent item height or clear rhythm
    - Dividers or spacing between items
    - Hover/selection states
    - Actions (swipe, long-press)

- [[Tables]]
  - **Purpose:** Display structured data
  - **Elements:** Header row, data rows, sortable columns, actions
  - **Best Practices:**
    - Left-align text, right-align numbers
    - Zebra striping or hover highlights
    - Sortable columns indicated
    - Responsive (cards on mobile)

### Feedback & Overlay Components

- [[Modals]] / [[Dialogs]]

  - **Purpose:** Focused task, important message
  - **Anatomy:** Backdrop, container, title, content, actions
  - **Types:**
    - [[Alert Dialog]] (confirm/cancel)
    - [[Form Modal]] (input required)
    - [[Fullscreen Modal]]
  - **Best Practices:**
    - Close on backdrop click or ESC key
    - Trap focus (keyboard navigation contained)
    - Clear primary action
    - Use sparingly (interrupts flow)

- [[Toast Notifications]] / [[Snackbars]]

  - **Purpose:** Temporary, non-intrusive feedback
  - **Position:** Bottom or top of screen
  - **Duration:** 3-5 seconds auto-dismiss
  - **Best Practices:**
    - Success, error, info, warning variants
    - Action optional (e.g., "Undo")
    - Don't cover critical content

- [[Tooltips]]

  - **Purpose:** Supplemental info on hover/focus
  - **Best Practices:**
    - Brief (1-2 sentences)
    - Appear on hover/focus, dismiss on mouse out
    - Don't rely on for critical info (mobile has no hover)
    - Arrow pointing to element

- [[Loading Indicators]]

  - **Types:**
    - [[Spinner]] (indeterminate wait)
    - [[Progress Bar]] (determinate percentage)
    - [[Skeleton Screen]] (content placeholder)
  - **Best Practices:**
    - Show for actions > 1 second
    - Skeleton screens feel fastest
    - Provide context ("Loading...")

- [[Badges]]

  - **Purpose:** Notification count, status indicator
  - **Best Practices:**
    - Small, typically circular
    - High contrast (red for notifications)
    - Positioned consistently (top-right of icon)

- [[Chips]] / [[Tags]]
  - **Purpose:** Compact info, filters, selections
  - **Types:** Input chip (removable), filter chip (toggleable), choice chip
  - **Best Practices:**
    - Rounded corners, compact padding
    - Clear remove action (X icon)
    - Related: [[Pill Buttons]]

### Form Components

- [[Form Layouts]]
  - [[Single-Column Form]] (best for mobile, faster completion)
  - [[Multi-Column Form]] (desktop, related fields grouped)
- [[Field Validation]]

  - [[Inline Validation]] (immediate feedback as user types)
  - [[On-Submit Validation]]
  - Clear [[Error Messages]] with solutions
  - [[Success Indicators]] (checkmark)

- [[Required Fields]]
  - Mark with asterisk (\*) or "Required" label
  - Or mark optional fields instead

## Related Topics

- [[Components-and-Variants]]
- [[UI-Patterns]]
- [[Usability-Heuristics]]
- [[Accessibility]]
- [[Design-Systems]]
- [[Style-Guides]]
- [[Affordances]]
- [[Micro-Interactions]]

## Tools & Resources

- Material Design Components
- Apple HIG: UI Elements
- Figma Community: Component libraries
- Pattern libraries: UI Patterns, Mobbin
- "Designing Interfaces" by Jenifer Tidwell

## Practice Exercises

1. **Component Audit:** Audit 5 popular apps. Document which components they use, variants, and patterns. Create visual reference sheet.

2. **Component Library:** Build a complete component library: Buttons (4 types × 5 states), Inputs (6 types × 4 states), Navigation (3 types), Cards (3 variants).

3. **State Design:** Choose 5 components and design all possible states with annotations explaining when each appears.

4. **Accessibility Check:** Review your components for ARIA labels, keyboard navigation, focus indicators, color contrast. Fix issues.

5. **Component Documentation:** Document 10 components with: usage guidelines, anatomy diagram, states, dos/don'ts, code snippets.

## Further Reading

- "Designing Interfaces" by Jenifer Tidwell
- Material Design: Components documentation
- Apple HIG: Components
- "Refactoring UI" (component design tactics)
- Nielsen Norman Group: UI component articles
