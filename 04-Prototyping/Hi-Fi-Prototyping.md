# Hi-Fi Prototyping

## Introduction

High-fidelity (hi-fi) prototyping creates interactive, realistic representations of a product that closely resemble the final design—complete with visual polish, realistic content, and functional interactions. Unlike low-fidelity sketches or wireframes that communicate structure and concept, hi-fi prototypes demonstrate exactly how the product will look, feel, and behave. They're the bridge between design and development, allowing stakeholders to experience the product before a single line of production code is written.

Hi-fi prototypes serve multiple critical purposes: they validate design decisions with users through [[Usability-Testing]], they align stakeholders on vision and functionality, they guide developers during implementation, and they help designers refine [[Micro-Interactions]], timing, and transitions. A well-crafted hi-fi prototype answers questions that static mockups cannot: "How does this transition feel?" "Is this interaction intuitive?" "Does the timing feel right?" "Can users complete this task?"

The investment in hi-fi prototyping pays dividends by catching usability issues before development, reducing costly code changes, and ensuring everyone—designers, developers, stakeholders, users—shares a concrete understanding of what's being built. Modern design tools like [[Figma]] have made hi-fi prototyping faster and more accessible, enabling rapid iteration and realistic testing without requiring development resources.

## Learning Objectives

By mastering Hi-Fi Prototyping, you will be able to:

- Create high-fidelity, interactive prototypes using modern design tools
- Choose appropriate fidelity levels for different testing and communication goals
- Design realistic interactions including transitions, animations, and micro-interactions
- Incorporate realistic content and data into prototypes
- Conduct [[Usability-Testing]] with hi-fi prototypes
- Present prototypes effectively to stakeholders and developers
- Balance polish with iteration speed
- Hand off prototypes to development teams with clear specifications

## Key Knowledge Points

### Hi-Fi Prototype Fundamentals

- [[High-Fidelity Prototype]]

  - Interactive, realistic representation of product
  - Visual design matches final product (colors, typography, images)
  - Functional interactions (click, scroll, navigate)
  - Realistic content (not Lorem Ipsum)
  - **Purpose:**
    - Validate design with users
    - Communicate vision to stakeholders
    - Guide development implementation
    - Test interactions and flows

- **When to Create Hi-Fi Prototypes:**

  - After [[Wireframing]] and concept validation
  - Before development begins
  - When testing complex interactions
  - For stakeholder presentations and approvals
  - For developer handoff

- **Hi-Fi vs Low-Fi:**
  - Low-fi: Quick, rough, explores concepts, tests structure
  - Hi-fi: Polished, realistic, tests usability, validates final design
  - Both have value at different stages

### Fidelity Spectrum

**Visual Fidelity:**

- **Low:** Grayscale, placeholder content, simple shapes
- **Medium:** Some color, basic styling, representative content
- **High:** Final colors, typography, images, branded elements

**Functional Fidelity:**

- **Low:** Click to next screen
- **Medium:** Basic navigation, some interactions
- **High:** Full interactions, transitions, animations, form validation, conditional logic

**Content Fidelity:**

- **Low:** Lorem ipsum, FPO (for placement only) images
- **Medium:** Representative content (close to real)
- **High:** Actual or realistic content, real data patterns

**Choose Fidelity Based On:**

- Stage of design (early = lower, late = higher)
- Testing goals (concept vs usability)
- Audience (internal team vs executive stakeholders)
- Time and resources available

### Creating Hi-Fi Prototypes

#### Step 1: Design Screens (Mockups)

- Create all screens/states needed for prototype
- Apply final visual design:

  - [[Color Palette]] from [[Style-Guides]]
  - [[Typography]] system
  - [[UI-Components]] library
  - [[Images]], icons, illustrations
  - [[White-Space]] and layout refinement

- Include all states:
  - [[Default State]]
  - [[Hover State]]
  - [[Active/Pressed State]]
  - [[Focus State]]
  - [[Disabled State]]
  - [[Error State]]
  - [[Loading State]]
  - [[Empty State]]
  - [[Success State]]

#### Step 2: Link Screens (Interactions)

- Create clickable hotspots
- Define transitions between screens
- Types of connections:
  - [[Navigation]]: Menus, buttons, tabs
  - [[Forms]]: Input interactions, validation
  - [[Overlays]]: Modals, dropdowns, tooltips
  - [[Gestures]]: Swipe, pinch, drag (mobile)

#### Step 3: Add Interactivity

- [[Transitions]]: How screens connect

  - Instant
  - Dissolve/fade
  - Slide (left, right, up, down)
  - Push
  - Smart Animate (Figma's morphing animation)

- [[Animation Timing]]:

  - Easing curves (ease-in, ease-out, ease-in-out)
  - Duration (100-300ms for most UI animations)
  - See [[Animation-Principles]]

- [[Micro-Interactions]]:
  - Button hover effects
  - Loading indicators
  - Success confirmations
  - See [[Micro-Interactions]]

#### Step 4: Add Logic (Advanced)

- [[Conditional Logic]]:

  - Show/hide elements based on interactions
  - Branching flows (if user clicks A, show X; if B, show Y)

- [[Variables]] (Figma):

  - Store state (logged in, cart count, user name)
  - Create dynamic prototypes

- [[Form Validation]]:

  - Show error states on invalid input
  - Enable/disable submit button

- [[Data Population]]:
  - Realistic content in lists, cards
  - Multiple variants for testing

#### Step 5: Test & Refine

- Test prototype yourself first
- Walk through all [[User-Flows]]
- Check for broken links, missing states
- Conduct [[Usability-Testing]] with users
- Iterate based on findings

### Tools for Hi-Fi Prototyping

**Primary Tools:**

- [[Figma]]

  - Industry standard
  - Collaborative, cloud-based
  - Smart Animate for smooth transitions
  - Variables and conditional logic
  - Component variants for states
  - See [[Figma-Prototyping]]

- [[Adobe XD]]

  - Similar to Figma
  - Auto-animate feature
  - Voice prototyping
  - Less popular than Figma now

- [[Framer]]

  - Code-based (React)
  - Most powerful interactions
  - Steeper learning curve
  - Best for complex, custom interactions

- [[Principle]] (Mac only)

  - Animation-focused
  - Timeline-based
  - Great for micro-interactions

- [[ProtoPie]]
  - Advanced interactions without code
  - Sensors (tilt, sound)
  - Good for mobile prototypes

**Specialized Tools:**

- [[InVision]]

  - Click-through prototypes
  - Commenting and collaboration
  - Less common now (Figma dominates)

- [[Origami Studio]] (Facebook)
  - Patch-based (visual programming)
  - Advanced interactions

### Prototyping Best Practices

**Start with Key Flows:**

- Don't prototype everything
- Focus on:
  - Critical [[User-Flows]] (sign-up, checkout)
  - Novel interactions (new patterns)
  - Complex features (need validation)

**Use Realistic Content:**

- Avoid Lorem Ipsum
- Use actual copy or realistic examples
- Include realistic data patterns:
  - Long names, short names
  - Empty states, full states
  - Edge cases (999+ notifications)

**Component-Based Approach:**

- Build with [[Components-and-Variants]]
- Reusable, consistent
- Easy to update globally
- States as variants (hover, active, disabled)

**Plan for Mobile:**

- Include scroll behavior
- Touch targets (minimum 44x44px)
- Gestures (swipe, pinch)
- Responsive layouts

**Performance Matters:**

- Keep file size reasonable
- Optimize images
- Limit simultaneous animations
- Test on actual devices (not just desktop preview)

**Document Interactions:**

- Annotate non-obvious behaviors
- Note animation timings
- Explain conditional logic
- Developer handoff requires specifications

### Prototyping Patterns

**Navigation Prototypes:**

- Menu interactions (hamburger open/close)
- Tab switching
- Breadcrumb navigation
- Back button behavior
- Deep linking (jump to specific screen)

**Form Prototypes:**

- Field focus states
- Inline validation (real-time feedback)
- Error messages
- Submit button states (enabled/disabled/loading)
- Multi-step progression

**Onboarding Prototypes:**

- Welcome screens with pagination
- Skip functionality
- Progress indicators
- Swipe through tutorial

**E-commerce Prototypes:**

- Product browsing and filtering
- Add to cart animation
- Cart badge update
- Checkout flow
- Payment states

**Search Prototypes:**

- Autocomplete suggestions
- Search results loading
- Filter application
- Empty state (no results)

### Testing with Hi-Fi Prototypes

**Usability Testing:**

- Give users realistic tasks
- Observe completion rates, errors, time
- Think-aloud protocol
- See [[Usability-Testing]]

**What to Test:**

- [[Findability]]: Can users find features?
- [[Completion]]: Can they finish tasks?
- [[Intuitiveness]]: Do interactions make sense?
- [[Satisfaction]]: How do users feel about it?
- [[Errors]]: Where do they get stuck?

**Prototype Limitations:**

- Not all features may work (communicate this)
- Performance may differ from production
- Some interactions may be simulated
- Set expectations with users

### Stakeholder Presentations

**Presenting Prototypes:**

- **Context First:** Explain problem and goals
- **Demo Key Flows:** Walk through main [[User-Flows]]
- **Highlight Decisions:** Explain "why" behind choices
- **Interactive:** Let stakeholders try it
- **Gather Feedback:** What questions? Concerns?

**Presentation Tips:**

- Use presentation mode (full screen)
- Practice transitions beforehand
- Have backup (video recording if live demo fails)
- Prepare for questions about edge cases
- Show both happy path and error handling

### Developer Handoff

**Specifications Needed:**

- Screen dimensions and breakpoints
- [[Spacing]] values (padding, margins)
- [[Typography]] specs (font, size, line height, weight)
- [[Colors]] (hex, RGB values)
- [[Component States]] (hover, active, disabled, etc.)
- [[Animation Timing]] (duration, easing)
- [[Interaction Logic]] (conditional behavior)
- [[Assets]] (icons, images, optimized)

**Handoff Tools:**

- [[Figma Inspect]]: Developers can extract specs
- [[Zeplin]]: Design-to-development handoff
- [[Avocode]]: Similar to Zeplin

**Handoff Best Practices:**

- Organize files clearly (pages, layers)
- Name layers descriptively
- Use consistent naming conventions
- Document non-obvious interactions
- Be available for questions
- Walk developers through prototype

### Common Challenges

**Scope Creep:**

- Prototyping everything takes too long
- Solution: Prioritize key flows, simulate rest

**Perfection Paralysis:**

- Polishing too much delays testing
- Solution: "Good enough to test" is the goal

**Technical Constraints:**

- Prototype shows something hard to build
- Solution: Involve developers early, discuss feasibility

**User Confusion:**

- Users think it's real product
- Solution: Set expectations, use sample data labels

**Maintenance:**

- Design changes require prototype updates
- Solution: Component-based design, version control

### Beyond Click-Through

**Advanced Prototyping:**

- [[Micro-Interactions]]:

  - Button ripple effects
  - Pull-to-refresh
  - Loading skeletons
  - See [[Micro-Interactions]]

- [[Scroll Behaviors]]:

  - Sticky headers
  - Parallax effects
  - Infinite scroll
  - Scroll-triggered animations

- [[Gesture-Based]]:

  - Swipe to delete
  - Pinch to zoom
  - Drag to reorder
  - Long press actions

- [[Data-Driven]]:
  - Populate with realistic data
  - Multiple content variations
  - Test with different data lengths

## Related Topics

- [[Figma-Prototyping]]
- [[Wireframing]]
- [[Mockups]]
- [[Micro-Interactions]]
- [[Animation-Principles]]
- [[Usability-Testing]]
- [[User-Flows]]
- [[Components-and-Variants]]

## Tools & Resources

**Prototyping Tools:**

- [[Figma]] - Industry standard, collaborative
- [[Framer]] - Code-based, powerful
- [[ProtoPie]] - Advanced interactions
- [[Principle]] - Animation-focused (Mac)
- [[Adobe XD]] - Adobe ecosystem

**Handoff Tools:**

- [[Figma Inspect]] - Built-in
- [[Zeplin]] - Design handoff
- [[Avocode]] - Specs and assets

**Learning Resources:**

- Figma YouTube: Prototyping tutorials
- Framer Learn: Interactive prototyping
- Design+Code: Advanced prototyping courses

**Books:**

- "Prototyping for Designers" by Kathryn McElroy
- "The Guide to Prototyping" by UXPin
- "Designing Interface Animation" by Val Head

## Practice Exercises

1. **Simple Flow Prototype:** Design and prototype a 3-step sign-up flow (email → password → confirmation). Include: form validation, button states, transitions, success screen. Test with 3 people.

2. **Navigation Prototype:** Create a mobile app prototype with tab bar navigation (4 tabs) and a modal screen. Include: tab switching, modal open/close with overlay, smooth transitions.

3. **Micro-Interaction Focus:** Design a "like" button with multiple states: default → hover → active → liked. Add animation: scale up on click, heart fill animation. Time it appropriately (200-300ms).

4. **E-commerce Checkout:** Prototype a 4-step checkout: Cart → Shipping → Payment → Confirmation. Include: progress indicator, form validation, loading states, back navigation, success animation.

5. **Responsive Prototype:** Design one screen in 3 sizes (mobile, tablet, desktop). Prototype all 3 versions. Demonstrate how layout adapts. Include breakpoint-specific interactions.

6. **Advanced Interactivity:** Use Figma variables and conditional logic to create a prototype where: clicking "Add to Cart" updates cart badge count, clicking cart shows items added. Prototype the dynamic behavior.

## Further Reading

- "Prototyping for Designers" by Kathryn McElroy
- "The Guide to Prototyping" by UXPin (free ebook)
- "Designing Interface Animation" by Val Head
- Nielsen Norman Group: Prototyping articles
- Figma Documentation: Prototyping features
- "Validating Product Ideas" by Tomer Sharon (testing prototypes)
