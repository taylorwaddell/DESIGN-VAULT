# Figma Prototyping

## Introduction

Figma's prototyping features transform static designs into interactive, clickable experiences without writing code. By connecting frames, defining interactions, and configuring transitions, designers can simulate realistic product behavior—from simple navigation flows to complex animations with Smart Animate. Figma prototyping bridges the gap between design and development, enabling [[Usability-Testing]], stakeholder presentations, and developer handoff all within a single collaborative tool.

Figma's prototyping capabilities have evolved to include sophisticated features: [[Smart Animate]] for automatic transitions between matching layers, [[Variables]] for dynamic content and state management, [[Conditional Logic]] for branching flows, and advanced interaction triggers beyond simple clicks. These tools enable designers to create prototypes that feel remarkably close to production, testing not just structure but timing, feel, and microinteractions before development begins.

Mastering Figma prototyping means understanding both the technical features (how to connect frames, configure transitions) and the strategic decisions (which flows to prototype, what fidelity is appropriate, how to organize for testing). A well-structured Figma prototype is more than connected screens—it's a testable, shareable artifact that drives alignment and validates design decisions across the entire product team.

## Learning Objectives

By mastering Figma Prototyping, you will be able to:

- Create interactive prototypes by connecting frames with interaction triggers
- Apply appropriate transition types (Instant, Dissolve, Slide, Smart Animate)
- Use Smart Animate to create smooth, automatic animations
- Implement [[Overlays]] for modals, dropdowns, and tooltips
- Configure advanced interactions including hover, drag, and keyboard triggers
- Use [[Variables]] to create dynamic, stateful prototypes
- Apply [[Conditional Logic]] for branching user flows
- Organize prototypes for testing and presentation
- Share and present prototypes effectively

## Key Knowledge Points

### Figma Prototyping Basics

**Prototype Tab:**

- Switch from Design tab to Prototype tab (right panel)
- This is where all interaction setup happens

**Connecting Frames:**

1. Select layer or frame
2. Click connection point (appears as blue circle)
3. Drag to target frame
4. Configure interaction settings

**Interaction Settings:**

- **Trigger:** What initiates the interaction
- **Action:** What happens
- **Destination:** Where to go
- **Animation:** How to transition
- **Easing & Duration:** Timing of animation

### Interaction Triggers

**Click Triggers:**

- [[On Click]]

  - Most common trigger
  - User taps/clicks element
  - Use for: Buttons, links, cards, navigation

- [[On Tap]] (Mobile)
  - Same as On Click for mobile context
  - Shows in mobile preview

**Hover Triggers:**

- [[While Hovering]]

  - Triggered when cursor hovers over element
  - Desktop only (no hover on mobile)
  - Use for: Button hover states, tooltips, menus
  - Returns to original state when hover ends

- [[While Pressing]]
  - Triggered during active press/hold
  - Use for: Button pressed states
  - Returns to original when released

**Keyboard Triggers:**

- [[Key / Gamepad]]
  - Triggered by specific keyboard keys
  - Use for: Keyboard navigation, shortcuts, game controls
  - Examples: Arrow keys, Enter, Escape, Spacebar

**Advanced Triggers:**

- [[Mouse Enter / Leave]]

  - Enter: Cursor enters bounding box
  - Leave: Cursor exits bounding box
  - Stays in new state (doesn't auto-revert)

- [[Mouse Down / Up]]

  - Down: Mouse button pressed
  - Up: Mouse button released
  - More granular than While Pressing

- [[After Delay]]

  - Triggered automatically after time delay
  - Use for: Auto-advance slides, loading transitions, tooltips
  - Set delay duration (milliseconds)

- [[Drag]]
  - Triggered when element is dragged
  - Use for: Sliders, carousels, reorderable lists
  - Configure drag constraints (horizontal, vertical, both)

### Actions & Destinations

**Navigation Actions:**

- [[Navigate to]]

  - Go to another frame
  - Most common action
  - Replaces current screen

- [[Back]]

  - Return to previous frame
  - Creates navigation history
  - Like browser back button

- [[Close Overlay]]
  - Dismisses currently open overlay
  - Use for: Modal close buttons, overlay backgrounds

**Overlay Actions:**

- [[Open Overlay]]
  - Shows frame as overlay (modal, dropdown, tooltip)
  - Original screen stays underneath
  - **Position:**
    - Center
    - Top/Bottom/Left/Right
    - Manual (specify X, Y coordinates)
    - Relative to element (appears near trigger)
  - **Background:**
    - Solid color with opacity (for modal backdrop)
    - None (for tooltips)
  - **Close on click outside:** Enabled/disabled

**Scroll Actions:**

- [[Scroll to]]

  - Jump to specific section of scrollable frame
  - Smooth scroll animation
  - Use for: Anchor links, "back to top"

- [[Swap with]] (Variants)
  - Swap current component with another variant
  - Use for: Component state changes (default → hover → active)
  - See [[Components-and-Variants]]

**URL Actions:**

- [[Open Link]]
  - Open external URL
  - Use for: External links, documentation, resources

### Transition Types

**Instant:**

- No animation, immediate change
- Fastest
- Use when: Animation not needed, very fast actions

**Dissolve:**

- Fade out → Fade in
- Duration: 100-300ms typical
- Use for: Content changes, smooth transitions

**Move In/Out:**

- New screen slides in from direction
- Old screen stays or moves out
- Directions: Left, Right, Up, Down
- Use for: Navigation (forward = left, back = right on mobile)

**Slide In/Out:**

- Similar to Move but old screen also moves
- Creates connected feeling
- Use for: Drawer navigation, sequential screens

**Push:**

- New screen pushes old screen out
- Both move together
- Use for: Horizontal navigation, swipe actions

**Smart Animate:**

- Figma automatically animates matching layers
- Smooth morphing between states
- **Requirements:**
  - Layers have same name in both frames
  - Frame names can differ
- **Animates:**
  - Position, size, rotation
  - Opacity
  - Fill color
  - Stroke
  - Effects (shadows, blur)
- **Use for:**
  - Micro-interactions (button states)
  - Morphing shapes
  - Smooth transitions
  - Complex animations without manual keyframing

### Smart Animate in Depth

**How Smart Animate Works:**

1. Compares source and destination frames
2. Finds layers with matching names
3. Calculates differences (position, size, properties)
4. Automatically animates those differences

**Best Practices:**

- Use consistent layer names
- Organize layers similarly in both frames
- Test duration and easing
- Combine with dissolve for appearing/disappearing elements

**Smart Animate Examples:**

- **Button Hover:**

  - Frame 1: Button default (gray, small)
  - Frame 2: Button hover (blue, slightly larger)
  - Same layer name: "Button"
  - Smart Animate transitions color and size

- **Card Expansion:**

  - Frame 1: Card small
  - Frame 2: Card expanded (larger, more content)
  - Smart Animate smoothly scales and repositions

- **Menu Open:**
  - Frame 1: Menu closed (hamburger icon)
  - Frame 2: Menu open (X icon, menu visible)
  - Smart Animate morphs icon and slides in menu

### Animation Easing & Duration

**Easing Types:**

- [[Ease Out]] (default)

  - Starts fast, slows at end
  - Most natural for UI
  - Use for: Most transitions

- [[Ease In]]

  - Starts slow, speeds up
  - Use for: Exits, disappearing elements

- [[Ease In and Out]]

  - Starts slow, fast middle, slow end
  - Use for: Looping animations, smooth back-and-forth

- [[Linear]]
  - Constant speed
  - Use for: Progress bars, loading indicators

**Duration Guidelines:**

- **100ms:** Very fast, barely noticeable (subtle feedback)
- **200-300ms:** Standard UI transitions (most common)
- **400-500ms:** Slower, more noticeable (complex animations)
- **600ms+:** Slow, use sparingly (may feel sluggish)

**Performance:**

- Shorter = faster, less CPU
- Longer = smoother but heavier
- See [[Animation-Principles]]

### Overlays

**Creating Overlays:**

- Action: Open Overlay (not Navigate to)
- Destination: Frame to show as overlay

**Overlay Settings:**

- **Position:**

  - Center (modals)
  - Top (notifications)
  - Bottom (bottom sheets)
  - Manual (specify coordinates)

- **Background:**

  - Solid color + opacity (dim background)
  - None (transparent, for tooltips)

- **Behavior:**
  - Close when clicking outside (modals)
  - Keep open (complex overlays)

**Closing Overlays:**

- Add Close Overlay action to buttons/areas
- Click outside if enabled
- Back button can close

**Stacking Overlays:**

- Can open overlay on top of overlay
- Manage complexity carefully

**Use Cases:**

- Modals (confirmations, forms)
- Dropdowns (menus, filters)
- Tooltips (hover explanations)
- Bottom sheets (mobile actions)
- Image lightboxes

### Scroll Behavior

**Scrollable Frames:**

- Set frame to allow vertical/horizontal overflow
- Design → Clip content (off) OR Overflow behavior
- Content extends beyond frame bounds

**Fixed Elements:**

- Keep header/footer fixed while content scrolls
- Select layer → Prototype tab → Fix position when scrolling

**Scroll To Interactions:**

- Link to section within scrollable frame
- Smooth scroll animation

**Sticky Headers:**

- Use fixed position for headers
- Content scrolls underneath

### Variables & Dynamic Prototypes

**Figma Variables** (advanced feature):

- Store and reuse values
- Create dynamic, stateful prototypes

**Variable Types:**

- **Boolean:** True/false (toggle states)
- **Number:** Quantities (cart count, progress)
- **String:** Text (user name, status)
- **Color:** Color values (theme switching)

**Using Variables:**

- Create variable collection
- Assign variables to properties (text content, opacity, color)
- Update variables via interactions (Set Variable action)

**Example Use Cases:**

- **Cart Count:** Increment variable when adding items
- **Login State:** Boolean variable (logged in/out)
- **Theme Toggle:** Color variables for light/dark mode
- **Form Validation:** Boolean for form completeness

### Conditional Logic

**Conditional Actions:**

- "If X, then do Y"
- Based on variable values
- Branching flows

**Example:**

- If cart count > 0, enable checkout button
- If logged in, show dashboard; else show login
- If form valid, enable submit button

**Setting Up Conditionals:**

- Prototype tab → Advanced settings
- If/Else conditions
- Reference variables

### Component Interactions

**Interactive Components:**

- Add interactions directly to components
- Reusable interactions
- All instances inherit behavior

**Variant Swapping:**

- Switch between component variants
- Action: Change to (specific variant)
- Use for: Button states, toggles, tabs

**Example:**

- Button component with variants: Default, Hover, Active
- On Click: Change to Active variant
- Smart Animate between variants

### Prototype Organization

**Multiple Flows:**

- Use multiple starting points
- Each represents a different flow/scenario
- Name clearly: "Onboarding Flow," "Checkout Flow"

**Flow Starting Points:**

- Mark frames as flow starting points
- Creates organized structure
- Easy to share specific flows

**Annotations:**

- Add text notes for testers/developers
- Explain non-obvious interactions
- Document edge cases

**Presentation View:**

- Preview prototype full-screen
- Present to stakeholders
- Navigate flows easily

### Sharing & Presenting

**Prototype Link:**

- Share → Copy link
- Options:
  - Anyone with link
  - Invite specific people
  - Password protection

**Prototype Settings:**

- Starting frame
- Device (mobile, tablet, desktop)
- Background color
- Show hotspots (blue outlines)
- Show prototype settings panel

**Presentation Mode:**

- Full-screen prototype
- Hide Figma UI
- Professional presentations

**Embed Prototypes:**

- Embed in websites, Notion, Confluence
- Interactive iframe

**Developer Handoff:**

- Prototype shows interactions
- Inspect mode provides specs
- See [[Hi-Fi-Prototyping]] (Developer Handoff)

### Testing with Figma Prototypes

**Usability Testing:**

- Share prototype link with users
- Give tasks to complete
- Observe remotely (screen share) or in person
- See [[Usability-Testing]]

**Testing Tips:**

- Set clear starting point
- Communicate what's clickable (or enable hotspot hints)
- Explain it's a prototype (limited functionality)
- Prepare for unexpected clicks (add "Coming Soon" overlays)

**Collecting Feedback:**

- Use Figma comments
- Screen recording tools (Loom, QuickTime)
- Notes during observation

### Advanced Techniques

**Drag Interactions:**

- Trigger: Drag
- Configure constraints (horizontal, vertical, both)
- Use for: Sliders, carousels, drag-to-reorder

**Keyboard Navigation:**

- Trigger: Key
- Map keys (Arrow keys, Enter, Esc)
- Accessible navigation

**Auto-Advance:**

- Trigger: After Delay
- Use for: Carousels, tutorials, splash screens

**Nested Prototypes:**

- Instances of components with prototypes
- Reusable interactive elements

## Related Topics

- [[Hi-Fi-Prototyping]]
- [[Figma-Basics]]
- [[Components-and-Variants]]
- [[Auto-Layout]]
- [[Micro-Interactions]]
- [[Animation-Principles]]
- [[Usability-Testing]]
- [[User-Flows]]

## Tools & Resources

**Figma Resources:**

- Figma Help Center: Prototyping documentation
- Figma YouTube: Prototyping tutorials
- Figma Community: Prototype templates and examples

**Prototyping Templates:**

- Search Figma Community for "prototype template"
- iPhone/Android templates with interactions
- Common UI pattern prototypes

**Learning Platforms:**

- Figma Learn: Official courses
- Skillshare: Figma prototyping courses
- YouTube: Figma prototyping tutorials

## Practice Exercises

1. **Basic Navigation:** Create 3 frames (Home, About, Contact). Add navigation buttons. Connect with "Navigate to" action. Use Slide transition. Test the flow.

2. **Hover States:** Design a button with 3 states: Default, Hover, Active. Use While Hovering and While Pressing triggers with Smart Animate. Time transitions at 200ms.

3. **Modal Overlay:** Create a button that opens a modal overlay (centered, with backdrop). Add close button (X) and "Close on click outside." Test opening and closing.

4. **Smart Animate Morphing:** Design a card in two states: collapsed and expanded. Name matching layers identically. Connect with Smart Animate. Watch card smoothly expand.

5. **Variable Cart Counter:** Create "Add to Cart" button and cart icon with badge. Use Number variable for cart count. Increment variable on click. Display variable value in badge.

6. **Multi-Flow Prototype:** Create a complete mobile app prototype with: Onboarding (3 screens), Main app (tab navigation - 4 tabs), Settings (overlay). Mark flow starting points. Test all paths.

## Further Reading

- Figma Official Documentation: Prototyping
- "Figma Prototyping Best Practices" (Figma blog)
- Design+Code: Figma Prototyping course
- YouTube: "Figma Advanced Prototyping" tutorials
- Figma Community files: Study prototype examples
- "The Guide to Prototyping" by UXPin (principles apply to Figma)
