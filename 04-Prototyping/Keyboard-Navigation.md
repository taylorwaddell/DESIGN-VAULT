# Keyboard Navigation

## Introduction

Keyboard navigation is the ability to interact with a digital interface using only keyboard input—no mouse, trackpad, or touch required. This capability is essential for many users: people who are blind or have low vision (using screen readers), people with motor disabilities (who can't use a mouse), and power users who prefer keyboard efficiency. An interface that works seamlessly with keyboard alone is more accessible, more usable, and often more efficient than one that requires constant switching between keyboard and mouse.

Effective keyboard navigation follows predictable patterns: Tab moves forward through interactive elements, Shift+Tab moves backward, Enter activates buttons and links, Space toggles checkboxes and scrolls pages, Arrow keys navigate within components like dropdowns and tabs, and Escape cancels actions and closes overlays. These conventions are learned expectations—violating them creates confusion and frustration. When keyboard navigation is thoughtfully implemented, it becomes invisible: users flow through interfaces naturally, completing tasks without friction.

Designing for keyboard navigation requires understanding focus management (where keyboard focus is, where it moves, how it's indicated visually), logical tab order (following visual hierarchy), keyboard shortcuts (accelerators for common actions), and focus traps (keeping focus within modals). It also means testing your designs by unplugging the mouse and trying to complete tasks with keyboard alone—a revealing exercise that immediately exposes usability issues invisible to mouse users.

## Learning Objectives

By mastering Keyboard Navigation, you will be able to:

- Design interfaces that are fully operable via keyboard
- Implement logical, predictable tab order
- Create visible, high-contrast focus indicators
- Manage focus in dynamic interfaces (modals, single-page apps)
- Use appropriate keyboard shortcuts and document them
- Test keyboard navigation systematically
- Fix common keyboard accessibility issues
- Understand WCAG requirements related to keyboard access

## Key Knowledge Points

### Why Keyboard Navigation Matters

**Who Relies on Keyboard:**

- **Screen reader users** (blind, low vision)

  - Navigate entirely by keyboard
  - Screen readers don't use mouse

- **Motor disabilities**

  - Can't use mouse (tremors, limited mobility, paralysis)
  - Use keyboard, switch devices, or voice control

- **Power users**

  - Keyboard faster for repetitive tasks
  - Shortcuts increase efficiency

- **Temporary limitations**
  - Broken arm, holding baby
  - Mouse broken or unavailable

**Percentage:** ~15-20% of users benefit from keyboard navigation

**Legal Requirement:**

- WCAG 2.1.1 (Level A): All functionality via keyboard
- WCAG 2.1.2 (Level A): No keyboard trap
- See [[WCAG-Guidelines]]

### Basic Keyboard Controls

**Standard Keys:**

**Tab:**

- Move to next focusable element
- Cycles through: Links, buttons, form fields, custom controls
- Most important navigation key

**Shift + Tab:**

- Move to previous focusable element
- Reverse tab order

**Enter:**

- Activate focused element
- Submit forms
- Click buttons and links

**Space:**

- Activate buttons
- Toggle checkboxes
- Scroll page down (if not focused on control)

**Arrow Keys:**

- Navigate within components:
  - Dropdowns, select menus
  - Radio button groups
  - Tabs
  - Sliders
  - Custom controls

**Escape (Esc):**

- Cancel action
- Close modal/dialog
- Clear dropdown without selection
- Exit fullscreen

**Home/End:**

- Jump to beginning/end of input field
- Jump to first/last item in list

**Page Up/Page Down:**

- Scroll page
- Navigate large lists

**Keyboard Combinations:**

- **Cmd/Ctrl + key:** Browser/OS shortcuts
- **Alt + key:** Access keys (less common now)

### Focus Management

**What is Focus:**

- Indicates which element will receive keyboard input
- Only one element has focus at a time
- Must be visible to users

**Focusable Elements (Native HTML):**

- Links (`<a href="...">`)
- Buttons (`<button>`)
- Form fields (`<input>`, `<textarea>`, `<select>`)
- Elements with `tabindex="0"` or positive tabindex

**Non-focusable (by default):**

- `<div>`, `<span>`, `<p>`, `<img>`, etc.
- Can be made focusable with `tabindex`

**tabindex Attribute:**

```html
<!-- tabindex="0": Natural tab order, focusable -->
<div tabindex="0" role="button">Click me</div>

<!-- tabindex="-1": Not in tab order, but focusable via JS -->
<div tabindex="-1" id="modal-title">Title</div>

<!-- tabindex="1+" (positive): Custom tab order (AVOID) -->
<!-- Creates unpredictable order, hard to maintain -->
```

**Best Practice:**

- Use native focusable elements when possible (`<button>` not `<div onclick>`)
- Use `tabindex="0"` for custom interactive elements
- Use `tabindex="-1"` for programmatic focus (modals)
- Avoid positive tabindex values (creates confusion)

### Focus Indicators

**Visual Focus Indicator:**

- Shows which element currently has keyboard focus
- Essential for keyboard users
- Often a border, outline, or highlight

**Default Browser Styles:**

- Browser provides default outline (often blue)
- DON'T remove without replacement (`outline: none` is bad unless you add alternative)

**WCAG Requirements:**

- **2.4.7 Focus Visible (Level AA):** Keyboard focus indicator must be visible
- **WCAG 2.2 addition (2.4.11-13):** More specific contrast and size requirements
- **Minimum contrast:** 3:1 against background
- **Minimum size:** Should clearly indicate focused element

**Design Focus Indicators:**

- **Outline:** Border around element

  - `outline: 2px solid #0066cc;`
  - Doesn't affect layout (doesn't push other elements)

- **Border:** Can use border instead

  - May affect layout (adds space)

- **Background:** Change background color

  - Often combined with border/outline

- **Shadow:** Box-shadow
  - `box-shadow: 0 0 0 3px rgba(0, 100, 200, 0.5);`

**Examples:**

```css
/* Good: Custom outline */
button:focus {
  outline: 2px solid #0066cc;
  outline-offset: 2px;
}

/* Good: Combination */
input:focus {
  border-color: #0066cc;
  box-shadow: 0 0 0 3px rgba(0, 100, 200, 0.3);
}

/* Bad: Removed without replacement */
*:focus {
  outline: none; /* ❌ Never do this */
}

/* Acceptable: Replace with custom */
button:focus {
  outline: none; /* Remove default */
  box-shadow: 0 0 0 3px #0066cc; /* Add custom ✅ */
}
```

**Accessibility Note:**
Some users have trouble seeing low-contrast indicators. High contrast (3:1 minimum) and clear differentiation are essential.

See [[Accessibility]] for more.

### Tab Order

**What is Tab Order:**

- The sequence in which elements receive focus when pressing Tab
- Should match visual order (left to right, top to bottom)
- Should be logical and predictable

**Default Tab Order:**

- Follows DOM (document) order
- Top to bottom in HTML code
- Interactive elements only (links, buttons, form fields)

**Best Practices:**

- **Visual order = Tab order:**

  - If visual layout differs from DOM order (e.g., CSS flexbox reordering), fix DOM order
  - Don't rely on `tabindex` to fix bad structure

- **Logical progression:**

  - Header → Navigation → Main content → Sidebar → Footer
  - Form fields in logical order
  - Related controls grouped

- **Skip links:**
  - "Skip to main content" link at beginning
  - Allows skipping navigation (saves time for keyboard users)
  - Often visually hidden until focused

**Testing Tab Order:**

1. Press Tab repeatedly
2. Observe focus moving through page
3. Does it follow visual order?
4. Does it skip anything important?
5. Does it focus on non-interactive elements?

**Common Issues:**

- Tab order doesn't match visual order
- Important elements not focusable
- Too many focusable elements (every word in paragraph)
- Skips sections

### Focus Trap (Modals/Dialogs)

**What is Focus Trap:**

- When modal/dialog is open, keyboard focus stays within modal
- Tab cycles through modal elements only
- Can't accidentally tab to content behind modal

**Why Needed:**

- Prevents confusion (user doesn't know they've left modal)
- Accessibility requirement (WCAG 2.1.2)
- Better UX (keeps context)

**Implementation:**

**Opening Modal:**

1. Store reference to element that opened modal (for returning focus later)
2. Move focus to modal (usually first focusable element or modal itself)
3. Trap focus within modal

**Within Modal:**

- Tab: Move to next focusable element in modal
- Shift+Tab: Move to previous
- When reaching last element, Tab wraps to first
- When at first element, Shift+Tab wraps to last

**Closing Modal:**

1. Close modal
2. Return focus to element that opened modal (or logical place)
3. Release focus trap

**Example Flow:**

1. User clicks "Open Modal" button → Focus on button
2. Modal opens → Focus moves to modal close button (or first field)
3. User tabs through modal elements (cycles within modal)
4. User presses Escape or clicks Close → Modal closes
5. Focus returns to "Open Modal" button

**Code Pattern (conceptual):**

```javascript
// Find all focusable elements in modal
const focusableElements = modal.querySelectorAll(
  'button, [href], input, select, textarea, [tabindex]:not([tabindex="-1"])'
);
const firstElement = focusableElements[0];
const lastElement = focusableElements[focusableElements.length - 1];

// Trap focus
modal.addEventListener("keydown", (e) => {
  if (e.key === "Tab") {
    if (e.shiftKey && document.activeElement === firstElement) {
      e.preventDefault();
      lastElement.focus(); // Wrap to last
    } else if (!e.shiftKey && document.activeElement === lastElement) {
      e.preventDefault();
      firstElement.focus(); // Wrap to first
    }
  }

  if (e.key === "Escape") {
    closeModal(); // Escape closes modal
  }
});

// On close, return focus
function closeModal() {
  modal.close();
  openButton.focus(); // Return focus to trigger
}
```

**Libraries:**

- focus-trap (npm package)
- React: react-focus-lock
- Handles edge cases automatically

### Keyboard Shortcuts

**Types:**

**Single-Key Shortcuts:**

- Single letter or character
- Example: ? for help, / for search (GitHub, Twitter)
- **Risk:** Can conflict with screen readers, forms
- **WCAG 2.1.4:** Must be able to turn off, remap, or only active when component focused

**Modifier Shortcuts:**

- Cmd/Ctrl + key, Alt + key
- Example: Cmd+S for save, Cmd+F for find
- Safer (less conflict)
- Platform conventions (Cmd on Mac, Ctrl on Windows)

**Access Keys:**

- Alt + key (Windows), Ctrl+Alt + key (Mac)
- Example: `<button accesskey="s">Save</button>`
- Less common now (conflicts, discoverability issues)

**Best Practices:**

- **Document shortcuts:**

  - Provide shortcut reference (? key often opens help)
  - Tooltip on hover

- **Use conventions:**

  - Cmd/Ctrl+S = Save
  - Cmd/Ctrl+Z = Undo
  - Cmd/Ctrl+F = Find
  - Esc = Cancel/Close

- **Make discoverable:**

  - Show in menus
  - Tooltips
  - Help documentation

- **Allow customization:**

  - Power users may want to remap
  - Avoid conflicts

- **Don't override browser shortcuts:**
  - Cmd/Ctrl+T, Cmd/Ctrl+W, etc. (users expect these)

**Examples:**

- Gmail: j/k for next/previous email, c for compose
- Slack: Cmd+K for quick switcher
- Figma: R for rectangle, T for text
- VS Code: Cmd+P for file search

### Component-Specific Navigation

**Dropdown Menus:**

- **Tab:** Focus on menu trigger (button)
- **Enter/Space:** Open menu
- **Arrow Down/Up:** Navigate menu items
- **Enter:** Select item, close menu
- **Esc:** Close menu without selecting

**Tabs:**

- **Tab:** Focus on tab list
- **Arrow Left/Right:** Switch between tabs
- **Tab (again):** Move to tab panel content
- Optional: **Home/End** for first/last tab

**Radio Buttons:**

- **Tab:** Focus on radio group (first checked or first item)
- **Arrow Up/Down** (or Left/Right): Select different radio
- Only one radio in group is in tab order (arrow keys navigate group)

**Checkboxes:**

- **Tab:** Focus on checkbox
- **Space:** Toggle checked/unchecked

**Sliders:**

- **Tab:** Focus on slider
- **Arrow Left/Right:** Decrease/increase value
- **Home/End:** Min/max value
- **Page Up/Down:** Larger increments (optional)

**Date Picker:**

- **Tab:** Focus on input or calendar button
- **Enter/Space:** Open calendar
- **Arrow keys:** Navigate days
- **Page Up/Down:** Previous/next month
- **Enter:** Select date
- **Esc:** Close calendar

**Modal/Dialog:**

- **Tab:** Cycle through focusable elements (trapped)
- **Esc:** Close modal, return focus

**Accordion:**

- **Tab:** Focus on accordion header
- **Enter/Space:** Toggle expanded/collapsed
- **Tab (again):** Move to next header (if collapsed) or content (if expanded)
- **Arrow Up/Down:** Move between headers (optional pattern)

### Skip Links

**What are Skip Links:**

- Links at the beginning of page
- Allow skipping repetitive content (navigation)
- Jump directly to main content

**Why Needed:**

- Keyboard users don't want to tab through entire nav every page
- Screen reader users don't want to hear nav every time
- Improves efficiency

**Implementation:**

```html
<body>
  <a href="#main-content" class="skip-link">Skip to main content</a>

  <nav>
    <!-- Navigation links -->
  </nav>

  <main id="main-content" tabindex="-1">
    <!-- Main content -->
  </main>
</body>
```

**Styling:**

```css
/* Hidden until focused */
.skip-link {
  position: absolute;
  top: -40px;
  left: 0;
  background: #000;
  color: #fff;
  padding: 8px;
  z-index: 100;
}

.skip-link:focus {
  top: 0; /* Appears when tabbed to */
}
```

**Best Practices:**

- First focusable element on page
- Visible when focused (don't hide with `display: none`)
- Can have multiple ("Skip to navigation," "Skip to search")

### Common Keyboard Issues

**Issue: Elements not focusable**

- Problem: Using `<div>` with `onclick` instead of `<button>`
- Fix: Use semantic HTML or add `tabindex="0"` and `role`

**Issue: No visible focus indicator**

- Problem: `outline: none` without replacement
- Fix: Add custom focus styles with sufficient contrast

**Issue: Illogical tab order**

- Problem: Visual order doesn't match DOM order
- Fix: Reorder HTML or fix CSS layout

**Issue: Focus not managed in SPA**

- Problem: Page changes but focus stays on old element (now hidden)
- Fix: Move focus to new content (heading or container with `tabindex="-1"`)

**Issue: Modal doesn't trap focus**

- Problem: Can tab to background content
- Fix: Implement focus trap

**Issue: Can't close modal with Esc**

- Problem: Only closeable by clicking X
- Fix: Add Esc key handler

**Issue: Dropdown doesn't work with keyboard**

- Problem: Only opens on click, can't navigate with arrows
- Fix: Implement keyboard handlers (Enter/Space to open, arrows to navigate)

### Testing Keyboard Navigation

**Manual Testing:**

1. **Unplug mouse** (or don't use it)

2. **Press Tab repeatedly:**

   - Does focus move through all interactive elements?
   - Is tab order logical (matches visual order)?
   - Are focus indicators visible?
   - Can you reach everything important?

3. **Use each interactive element:**

   - Buttons: Press Enter or Space (do they work?)
   - Links: Press Enter (do they navigate?)
   - Form fields: Type, Tab to next
   - Dropdowns: Arrow keys to navigate, Enter to select
   - Modals: Esc to close, focus trapped?

4. **Try keyboard shortcuts:**

   - Do documented shortcuts work?
   - Any conflicts?

5. **Navigate complex components:**
   - Tabs: Arrow keys to switch tabs?
   - Accordions: Enter/Space to toggle?
   - Date pickers: Calendar navigable with keyboard?

**Screen Reader Testing:**

- See [[Accessibility]] and [[Screen-Readers]]
- Many keyboard issues affect screen reader users

**Automated Testing:**

- Tools: axe DevTools, WAVE
- Catch some issues (missing tabindex, missing labels)
- Can't catch tab order or focus management issues (requires manual testing)

### Best Practices

**Do:**

- ✅ Use semantic HTML (`<button>`, `<a>`, `<input>`)
- ✅ Provide visible focus indicators (3:1 contrast minimum)
- ✅ Logical tab order (matches visual order)
- ✅ Trap focus in modals
- ✅ Return focus after interactions (modal close, item deleted)
- ✅ Support Esc key for canceling/closing
- ✅ Test with keyboard only
- ✅ Provide skip links

**Don't:**

- ❌ Remove focus outline without replacement
- ❌ Use `<div>` with `onclick` (use `<button>`)
- ❌ Rely on hover only (provide focus state too)
- ❌ Positive tabindex values (creates unpredictable order)
- ❌ Keyboard trap without escape (must be able to leave)
- ❌ Assume everyone uses a mouse

## Related Topics

- [[Accessibility]]
- [[WCAG-Guidelines]]
- [[Screen-Readers]]
- [[Interaction-Principles]]
- [[Usability-Heuristics]]
- [[Forms]]
- [[Micro-Interactions]]

## Tools & Resources

**Testing Tools:**

- Browser DevTools: Inspect focus order
- axe DevTools: Automated keyboard accessibility checks
- WAVE: Identify keyboard issues
- Keyboard Emulator: Test without physical keyboard

**Screen Readers (for testing):**

- VoiceOver (Mac): Cmd+F5
- NVDA (Windows): Free download
- JAWS (Windows): Paid

**Code Libraries:**

- focus-trap: JavaScript focus trap utility
- react-focus-lock: React focus trap
- tabbable: Find tabbable elements

**Guidelines:**

- WCAG 2.1 Success Criteria 2.1 (Keyboard Accessible)
- Apple HIG: Keyboard
- Material Design: Accessibility

**Learning:**

- WebAIM: Keyboard Accessibility
- A11y Project: Keyboard navigation
- MDN Web Docs: Keyboard-navigable JavaScript widgets

## Practice Exercises

1. **Keyboard-Only Navigation:** Navigate a complex website (e.g., Amazon, GitHub, Airbnb) using keyboard only. Unplug mouse. Can you complete a task (search, add to cart, submit form)? Document issues and what works well.

2. **Tab Order Audit:** Open a multi-section page. Press Tab repeatedly and observe focus order. Map out the actual tab order. Does it match visual hierarchy? Identify issues. Sketch an improved tab order.

3. **Focus Indicator Design:** Take a UI kit or design system. Evaluate focus indicators on all interactive elements (buttons, links, inputs). Do they meet WCAG 2.4.7 (visible, 3:1 contrast)? Redesign if needed.

4. **Modal Focus Trap:** Create or prototype a modal dialog. Test: (1) Focus moves to modal when opened, (2) Tab cycles within modal only, (3) Esc closes modal, (4) Focus returns to trigger on close. Document implementation.

5. **Dropdown Keyboard Navigation:** Design a custom dropdown menu. Define keyboard interactions: Tab to trigger, Enter/Space to open, Arrow Down/Up to navigate options, Enter to select, Esc to cancel. Prototype or document spec.

6. **Keyboard Shortcuts:** Choose an interface you use often. Identify 5 common actions. Design keyboard shortcuts for each (consider conflicts, discoverability, documentation). Create a shortcuts reference card.

## Further Reading

- **"Inclusive Components" by Heydon Pickering** (keyboard patterns for complex components)
- **"Form Design Patterns" by Adam Silver** (keyboard-accessible forms)
- WebAIM: Keyboard Accessibility (webaim.org/techniques/keyboard)
- WCAG 2.1 Guideline 2.1: Keyboard Accessible
- MDN: Keyboard-navigable JavaScript widgets
- A11y Project: Keyboard navigation checklist
- "Accessibility for Everyone" by Laura Kalbag (chapter on keyboard access)
- GOV.UK Service Manual: Keyboard accessibility
