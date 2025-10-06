# Affordances

## Introduction

Affordances are the perceived and actual properties of objects that determine how they can be used. In design, an affordance is a visual clue that signals an element's functionality—buttons look pressable, links look clickable, sliders look draggable. The term, coined by psychologist James J. Gibson and popularized in design by Don Norman, describes the relationship between an object's properties and a user's ability to interact with it.

Good affordances make interfaces intuitive and self-explanatory. Users shouldn't need instructions to know that a raised button can be clicked or that underlined text is a link. When affordances are clear, interfaces feel natural; when they're absent or misleading (a button that looks like text, text that looks like a button), users become confused and frustrated. This concept is central to creating [[Usability]] and reducing [[Cognitive Load]].

In digital interfaces, we rely heavily on [[Signifiers]]—visual indicators that communicate affordances. Since digital interfaces lack physical properties (you can't feel a screen button's texture), designers must use visual design—shadows, borders, colors, cursor changes—to signal interactivity. Mastering affordances means understanding both perception psychology and established interface conventions.

## Learning Objectives

By mastering Affordances, you will be able to:

- Understand the difference between [[Affordances]], [[Signifiers]], and [[Perceived Affordances]]
- Design UI elements with clear [[Visual Affordances]] that signal interactivity
- Apply [[Interaction Feedback]] to confirm actions and system state
- Recognize and fix [[False Affordances]] (looks interactive but isn't) and [[Hidden Affordances]] (is interactive but doesn't look it)
- Use [[Conventions]] and [[Mental Models]] to create intuitive interactions
- Apply affordance principles across [[Buttons]], [[Links]], [[Inputs]], and [[Interactive Elements]]
- Balance aesthetic goals with affordance clarity

## Key Knowledge Points

### Affordance Fundamentals

- [[Affordances]]
  - Relationship between object and user
  - What actions are possible
  - Can be:
    - **Physical:** Shape, size, weight (physical objects)
    - **Perceptual:** How properties are perceived
    - **Cognitive:** Learned associations
- [[Perceived Affordances]]

  - What users _think_ they can do
  - More important than actual affordances in UI design
  - Gap between actual and perceived = usability problem

- [[Signifiers]]
  - Communicate where actions should take place
  - Signal of affordances
  - Examples:
    - Push/Pull signs on doors (door affordance unclear)
    - Underline on links (signifies clickability)
    - Button shadows (signify pressability)
  - Don Norman: "Affordances exist, signifiers are what we add"

### Types of Affordances in UI

- [[Visual Affordances]]

  - Visual clues about interactivity
  - Color, shape, size, position, styling
  - Examples:
    - Blue, underlined text = [[Link]]
    - Raised button with shadow = [[Clickable]]
    - Cursor change (pointer) = [[Interactable]]
    - Outlined box = [[Input Field]]
    - Handle icon = [[Draggable]]

- [[Hidden Affordances]]

  - Interactive but not visually obvious
  - **Problems:**
    - Low discoverability
    - Users miss features
  - **Examples:**
    - [[Swipe Actions]] (hidden until swiped)
    - [[Right-Click Menus]]
    - [[Keyboard Shortcuts]]
    - [[Gesture Controls]]
  - **Solutions:**
    - [[Onboarding]] hints
    - Subtle visual cues
    - Progressive disclosure

- [[False Affordances]]
  - Looks interactive but isn't
  - **Problems:**
    - User frustration
    - Broken expectations
  - **Examples:**
    - Underlined text that's not a link
    - Button-styled labels
    - Clickable-looking disabled elements
  - **Solutions:**
    - Remove signifiers from non-interactive elements
    - Use [[Disabled State]] styling clearly

### Affordance Principles by Element

- [[Button Affordances]]

  - **Signifiers of clickability:**
    - Rectangular shape with rounded corners
    - Solid fill (primary) or border (secondary)
    - Button-like padding
    - Shadow/elevation
    - Color contrast
    - Cursor change (pointer)
  - **States reinforce affordance:**
    - [[Hover State]]: Color change, elevation
    - [[Active State]]: Pressed inward effect
    - [[Disabled State]]: Muted, no hover
  - **Anti-patterns:**
    - Flat, borderless buttons (low affordance)
    - Buttons that look like labels

- [[Link Affordances]]

  - **Signifiers of clickability:**
    - Blue color (convention)
    - Underline (strongest signifier)
    - Cursor change (pointer)
    - Different color from body text
  - **States:**
    - [[Hover]]: Underline appears, color change
    - [[Visited]]: Purple (convention)
  - **Trend:** Modern design removes underlines
    - Trade-off: Cleaner but less discoverable
    - Solution: Underline on hover, clear color contrast

- [[Input Field Affordances]]

  - **Signifiers of editability:**
    - Outlined box or underline
    - White/light background (writable space)
    - Blinking cursor when focused
    - [[Placeholder Text]]
    - [[Label]] nearby
  - **States:**
    - [[Focus]]: Border color change, glow
    - [[Filled]]: Contains text
    - [[Error]]: Red border, error message
    - [[Disabled]]: Grayed out, no cursor

- [[Draggable Affordances]]

  - **Signifiers:**
    - [[Drag Handle]] icon (⋮⋮ or ☰)
    - Cursor change (grab hand)
    - Slight movement on hover
  - **Feedback:**
    - [[Ghost Element]] while dragging
    - Drop zones highlighted
    - Snap-to-grid behavior

- [[Scrollable Affordances]]
  - **Signifiers:**
    - [[Scrollbar]] (traditional)
    - [[Fade Effect]] at edges (content continues)
    - [[Overflow Indicators]] (shadows, gradients)
    - Content cut off at edge
  - **Problems with hidden scrollbars:**
    - Users may not realize content scrolls
    - Solution: Fade indicators, peek content

### Interaction Feedback

- [[Hover Feedback]]

  - **Purpose:** Show element is interactive
  - **Methods:**
    - Color change
    - Underline appears
    - Elevation increase
    - Cursor change
    - Tooltip appears
  - **Limitation:** No hover on touch devices

- [[Focus Feedback]]

  - **Purpose:** Show keyboard focus (accessibility critical)
  - **Methods:**
    - Blue outline (default)
    - Glow effect
    - Border color change
  - **Never remove:** `outline: none` without replacement
  - See [[Keyboard-Navigation]], [[Accessibility]]

- [[Active / Pressed Feedback]]

  - **Purpose:** Confirm user action registered
  - **Methods:**
    - Button pressed inward (shadow change)
    - Color darkening
    - Scale slightly down
  - **Timing:** Immediate (<100ms)

- [[Loading Feedback]]
  - **Purpose:** System is processing
  - **Methods:**
    - [[Spinner]] replaces button text
    - [[Progress Bar]]
    - [[Skeleton Screen]]
    - Button disabled with loading state
  - See [[Visibility of System Status]]

### Conventions & Mental Models

- [[Interface Conventions]]

  - Learned expectations about how UI works
  - **Examples:**
    - Logo in top-left links to homepage
    - Search in top-right
    - Save icon = floppy disk (historical artifact)
    - Red = error/stop, Green = success/go
    - X = close
  - **When to follow:** Always, unless strong reason
  - **When to break:** Innovation must outweigh learning curve

- [[Platform Conventions]]

  - iOS, Android, Windows have different conventions
  - **Examples:**
    - iOS: Back button top-left
    - Android: Back button bottom (hardware or on-screen)
    - iOS: Tab bar bottom
    - Android: Bottom nav or top tabs
  - Follow [[Apple HIG]], [[Material Design]] for consistency

- [[Mental Models]]
  - User's internal understanding of how system works
  - **Design implication:** Match mental models or teach new ones explicitly
  - **Example:** File/folder metaphor (even though it's not how computers store files)

### Reducing Ambiguity

- [[Clear Affordances Checklist]]

  - Is it obvious what this element does?
  - Does it look different from non-interactive elements?
  - Does it provide feedback on interaction?
  - Does it match user expectations?
  - Would a new user understand without instructions?

- [[Testing Affordances]]
  - [[Five-Second Test]]: Can users identify interactive elements in 5 seconds?
  - [[First-Click Test]]: Where do users try to click first?
  - [[Usability-Testing]]: Observe where users struggle

## Related Topics

- [[Usability-Heuristics]] (Recognition Rather Than Recall)
- [[UI-Components]]
- [[Micro-Interactions]]
- [[Feedback and Response]]
- [[Accessibility]]
- [[Mental Models]]
- [[Design-Principles]]
- [[Visual Hierarchy]]

## Tools & Resources

- "The Design of Everyday Things" by Don Norman (foundational)
- Nielsen Norman Group: Affordances articles
- [[Figma]] for designing and testing affordances
- [[Maze]] for first-click testing

## Practice Exercises

1. **Affordance Audit:** Analyze 5 interfaces. Identify elements with strong affordances, weak affordances, false affordances, hidden affordances. Document with screenshots.

2. **Before/After:** Take a design with poor affordances. Redesign to make all interactive elements obvious. Compare click-through rates if possible.

3. **State Design:** Design a button with all states (default, hover, focus, active, disabled, loading). Ensure each state clearly communicates its meaning.

4. **Convention Challenge:** Identify 10 UI conventions users expect. Design variations that break conventions. Test with users to measure impact.

5. **Hidden Affordance Solutions:** Find 5 interfaces with hidden affordances (swipe actions, gestures, etc.). Propose visual solutions to make them more discoverable.

6. **First-Click Test:** Create a new interface. Test with 5 users: "Where would you click to [perform task]?" Document misclicks, improve affordances, retest.

## Further Reading

- "The Design of Everyday Things" by Don Norman
- "Designing with the Mind in Mind" by Jeff Johnson
- Nielsen Norman Group: Affordances in UX
- "About Face" by Alan Cooper (interaction design)
- Don Norman: Signifiers, Not Affordances (article clarification)
