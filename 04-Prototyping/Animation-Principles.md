# Animation Principles

## Introduction

Animation in user interfaces is more than decorative motion—it's a powerful communication tool that guides users, provides feedback, reveals relationships, and adds personality to digital experiences. When applied thoughtfully, animation clarifies interface changes, directs attention to important elements, shows cause-and-effect relationships, and makes interactions feel natural and responsive. Animation transforms static designs into dynamic, living experiences that feel intuitive and engaging.

The principles of UI animation draw from traditional animation (Disney's 12 principles), physics (natural motion), and cognitive psychology (how humans perceive movement). Understanding these foundations enables designers to create animations that feel right—neither too fast nor too slow, neither too subtle nor too jarring. The best UI animations are often invisible: users don't consciously notice them, but they feel the interface responding smoothly to their actions, guiding them naturally through tasks.

Mastering animation principles means knowing when to animate (and when not to), understanding timing and easing curves, respecting accessibility needs, and balancing delight with performance. Poor animation can frustrate users, cause motion sickness, or slow down interactions. Excellent animation reduces cognitive load, provides instant feedback, and creates memorable experiences that differentiate products. Animation is a fundamental skill for modern UI/UX designers.

## Learning Objectives

By mastering Animation Principles, you will be able to:

- Apply fundamental animation principles (timing, easing, staging) to UI design
- Choose appropriate animation durations and easing curves for different interactions
- Create animations that communicate purpose and guide user attention
- Design accessible animations that respect user motion preferences
- Balance performance considerations with visual richness
- Use animation to establish visual hierarchy and relationships
- Implement animation principles using modern design tools
- Critique and refine animations based on user feedback and best practices

## Key Knowledge Points

### Why Animation Matters

**Communication:**

- **Feedback:** Confirm actions (button pressed, item saved)
- **System Status:** Show what's happening (loading, processing)
- **Relationships:** Show how elements relate (parent-child, cause-effect)
- **Guidance:** Direct attention ("look here next")

**User Experience:**

- **Reduces cognitive load:** Smooth transitions easier to process than sudden changes
- **Maintains context:** Where elements come from and go to
- **Provides continuity:** Connects before and after states
- **Adds personality:** Brand expression through motion

**When NOT to Animate:**

- When it slows down user tasks
- When it causes motion sickness (provide alternatives)
- When it's purely decorative with no purpose
- When performance suffers

See [[Micro-Interactions]] for specific animation patterns.

### Disney's 12 Principles (Applied to UI)

Originally for character animation, adapted for UI:

**1. Squash and Stretch:**

- Objects deform when in motion
- UI: Buttons squash when pressed, modals stretch when opening
- Maintains volume (looks natural)
- Use subtly in UI (not extreme)

**2. Anticipation:**

- Preparation before main action
- UI: Button scales down slightly before bouncing up
- Helps users predict what's about to happen
- Example: Pull-to-refresh (pull down before releasing to refresh)

**3. Staging:**

- Direct attention to what's important
- UI: Animate one element at a time (sequential)
- Don't animate everything simultaneously
- Example: Form fields validate one by one, not all at once

**4. Straight Ahead vs Pose-to-Pose:**

- Straight ahead: Animate every frame (fluid, spontaneous)
- Pose-to-pose: Define key states, interpolate between (controlled)
- UI typically uses pose-to-pose (start state → end state)

**5. Follow Through and Overlapping Action:**

- Different parts stop at different times
- UI: Modal opens, then content fades in (overlapping)
- Creates more natural, layered motion
- Example: Menu slides in, then items fade in sequentially

**6. Slow In and Slow Out (Easing):**

- Objects accelerate and decelerate gradually
- UI: Ease-in, ease-out, ease-in-out curves
- Most important principle for UI animation
- See Easing section below

**7. Arc:**

- Natural motion follows curved paths
- UI: Elements move along arcs, not straight lines
- Makes motion feel more organic
- Example: Menu icon morphing to X follows slight arc

**8. Secondary Action:**

- Supporting action emphasizes main action
- UI: Button click triggers both color change (main) and shadow reduction (secondary)
- Adds richness without distraction

**9. Timing:**

- Speed of action defines meaning
- UI: Fast = light/responsive, slow = heavy/important
- Critical for UI (see Duration section)

**10. Exaggeration:**

- Emphasize important moments
- UI: Use sparingly (overshoot slightly on important actions)
- Adds personality and clarity

**11. Solid Drawing:**

- Understanding form and structure
- UI: Maintain visual hierarchy even during animation
- Elements don't disappear or become confusing mid-animation

**12. Appeal:**

- Create engaging, charismatic design
- UI: Personality through motion (bouncy, smooth, playful, professional)
- Aligns with brand

### Timing & Duration

**Duration Guidelines:**

- **<100ms:** Instant (cursor changes, hover hints)

  - Barely perceptible
  - Use for: Minor feedback

- **100-200ms:** Very fast (button feedback, toggles)

  - Quick response
  - Use for: Immediate actions, micro-interactions

- **200-300ms:** Standard (most UI transitions)

  - Sweet spot for UI
  - Use for: Modals, dropdowns, navigation

- **300-500ms:** Moderate (complex animations)

  - Noticeable but not slow
  - Use for: Multi-element animations, page transitions

- **500ms+:** Slow (use sparingly)
  - Feels sluggish for UI
  - Use for: Loading animations, special moments

**Speed Perception:**

- **Fast animations:** Light, responsive, energetic
- **Slow animations:** Heavy, important, dramatic
- Match speed to meaning

**Context Matters:**

- **Enter animations:** Can be slightly slower (200-300ms)
  - User initiated, expected
- **Exit animations:** Should be faster (150-200ms)
  - User wants to move on
- **Micro-interactions:** Very fast (100-200ms)
  - Immediate feedback

### Easing (Timing Functions)

Easing controls acceleration/deceleration during animation.

**Ease-Out (Most Common for UI):**

- Starts fast, slows at end
- Formula: Fast → Slow
- **Use for:**
  - Elements entering screen
  - Buttons responding to clicks
  - Modals opening
- **Why:** Feels responsive (immediate start) and settles gently (no abrupt stop)
- CSS: `ease-out`, `cubic-bezier(0, 0, 0.2, 1)`

**Ease-In:**

- Starts slow, speeds up at end
- Formula: Slow → Fast
- **Use for:**
  - Elements exiting screen
  - Disappearing elements
- **Why:** Draws less attention to exit
- CSS: `ease-in`, `cubic-bezier(0.4, 0, 1, 1)`

**Ease-In-Out:**

- Starts slow, fast in middle, slow at end
- Formula: Slow → Fast → Slow
- **Use for:**
  - Elements that move across screen
  - Looping animations
  - Symmetrical movements
- CSS: `ease-in-out`, `cubic-bezier(0.4, 0, 0.2, 1)`

**Linear:**

- Constant speed throughout
- Formula: Same speed
- **Use for:**
  - Loading spinners
  - Progress bars (determinate)
  - Mechanical movements
- **Why:** Predictable, measurable progress
- Feels robotic for most UI (avoid for entrances/exits)
- CSS: `linear`, `cubic-bezier(0, 0, 1, 1)`

**Custom Curves:**

- Define your own acceleration curve
- CSS: `cubic-bezier(x1, y1, x2, y2)`
- Tools: cubic-bezier.com, easings.net
- **Material Design Standard:** `cubic-bezier(0.4, 0, 0.2, 1)`

**Spring/Bounce:**

- Overshoots target, bounces back
- Playful, energetic
- Use for: Delightful moments, brand personality
- Common in iOS animations
- Libraries: Framer Motion (React), react-spring

**Easing Best Practices:**

- **Consistent:** Use same easing for similar actions
- **Natural:** Ease-out feels most natural for UI
- **Fast:** Don't slow users down with slow easing
- **Test:** Try different curves, see what feels right

### Choreography (Sequencing)

How multiple elements animate together.

**Sequential (Staggered):**

- Elements animate one after another
- Small delay between each (50-100ms)
- **Use for:**
  - List items appearing
  - Menu items sliding in
  - Form fields validating
- **Why:** Easier to follow, directs attention
- Creates rhythm

**Simultaneous:**

- All elements animate at once
- Can be overwhelming if too many
- **Use for:**
  - Related elements (icon + text)
  - Background + foreground (different speeds)

**Directional:**

- Animation follows direction of action
- **Example:**
  - Swipe left → items slide left
  - Scroll down → content enters from bottom
- Creates intuitive cause-and-effect

**Hierarchy-Based:**

- Primary elements animate first
- Secondary elements follow
- Guides attention to most important content

**Parent-Child Relationships:**

- Parent animates, children follow
- Example: Accordion expands (parent), content fades in (children)

### Motion & Physics

**Natural Motion:**

- Objects have weight and momentum
- No instant starts/stops (unless intentional)
- Easing creates natural feel

**Velocity & Acceleration:**

- Larger distances = faster movement (same duration)
- Maintains perceived speed

**Mass & Weight:**

- Heavier objects: Slower, more momentum
- Light objects: Quick, snappy
- Example: Large modal opens slower than small tooltip

**Friction & Air Resistance:**

- Elements slow down gradually
- Bounce and settle
- Spring physics

**Overshoot/Undershoot:**

- Element goes past target, returns
- Adds playfulness and energy
- Use subtly (10-20% overshoot)

### Animation Patterns

**Page Transitions:**

- [[Fade]]: Simplest, content fades out/in
- [[Slide]]: New page slides in from direction
- [[Push]]: New page pushes old page out
- [[Zoom]]: Content zooms in/out
- **Best practice:** Match to navigation direction (forward = right to left)

**Modal/Overlay:**

- [[Fade In]]: Modal appears, backdrop darkens
- [[Scale Up]]: Modal scales from small to full size
- [[Slide Up]]: Modal slides from bottom (mobile common)
- **Exit:** Faster than entrance (150ms vs 250ms)

**Loading:**

- [[Spinner]]: Indeterminate (unknown duration)
- [[Progress Bar]]: Determinate (known percentage)
- [[Skeleton Screen]]: Placeholder shapes with shimmer
- Appear after 300-500ms delay (don't flash for fast loads)

**Notification:**

- [[Slide In]]: From top or side
- [[Fade In]]: Appears in place
- [[Auto-dismiss]]: After 3-5 seconds
- [[Slide Out]]: Exit animation

**State Change:**

- [[Toggle]]: Switch slides, color changes
- [[Checkbox]]: Checkmark draws in
- [[Button]]: Scale down (pressed), scale up (hover)

See [[Micro-Interactions]] for detailed patterns.

### Accessibility

**Motion Sensitivity:**

- Some users experience motion sickness, dizziness, nausea from animations
- Vestibular disorders, ADHD, autism
- **Solution:** Respect `prefers-reduced-motion`

**Prefers-Reduced-Motion:**

- CSS media query: `@media (prefers-reduced-motion: reduce)`
- User sets preference in OS settings
- **When enabled:**
  - Remove non-essential animations
  - Reduce motion (fade instead of slide)
  - Instant transitions for decorative animations
  - Keep essential feedback (loading, success)

**Best Practices:**

- Make animations optional
- Provide static alternatives
- Don't rely on animation alone to communicate
- Test with reduced motion enabled

**Screen Readers:**

- Animations often invisible to screen readers
- Provide text alternatives
- Announce state changes
- Example: "Modal opened," "Item added to cart"

See [[Accessibility]] and [[WCAG-Guidelines]].

### Performance

**60 FPS Goal:**

- Smooth animation = 60 frames per second
- Each frame has 16.67ms to render
- Janky animation < 60fps (stutters)

**What to Animate:**

- **Cheap (GPU accelerated):**
  - `transform`: `translate`, `scale`, `rotate`
  - `opacity`
- **Expensive (triggers layout/paint):**
  - `width`, `height`
  - `margin`, `padding`
  - `top`, `left`, `right`, `bottom`
  - `color`, `background-color`

**Optimization:**

- Use `transform` instead of position properties
- Use `opacity` instead of `visibility`
- Animate fewer elements
- Reduce animation complexity
- Use `will-change` (CSS) sparingly

**Testing:**

- Chrome DevTools: Performance tab
- Record animation, analyze FPS
- Check for dropped frames

### Tools for Animation

**Design/Prototyping:**

- [[Figma]] - Smart Animate (simple)
- [[Principle]] - Timeline-based (micro-interactions)
- [[Framer]] - Code-based, spring physics
- [[ProtoPie]] - Advanced no-code
- [[After Effects]] - Complex animations (export with Lottie)

**Code Libraries:**

- [[Framer Motion]] (React) - Declarative, spring animations
- [[GSAP]] (JavaScript) - Powerful, timeline control
- [[Anime.js]] - Lightweight
- [[React Spring]] - Physics-based animations
- [[Lottie]] - After Effects animations in code

**Easing Tools:**

- cubic-bezier.com - Visual easing curve editor
- easings.net - Easing function reference
- Ceaser - CSS easing animation tool

### Best Practices

**Do:**

- ✅ Animate with purpose (feedback, guidance)
- ✅ Keep animations fast (<300ms for most UI)
- ✅ Use ease-out for most UI animations
- ✅ Respect reduced motion preferences
- ✅ Test on actual devices (performance)
- ✅ Maintain visual hierarchy during animation
- ✅ Be consistent (similar actions = similar animations)

**Don't:**

- ❌ Animate everything (overwhelming)
- ❌ Use slow animations (frustrating)
- ❌ Ignore accessibility (motion sensitivity)
- ❌ Animate without purpose (decoration only)
- ❌ Use heavy animations (performance issues)
- ❌ Rely on animation alone (provide text feedback too)

### Animation System

Create consistency with an animation system:

**Duration Tokens:**

```
--duration-instant: 100ms
--duration-fast: 200ms
--duration-normal: 300ms
--duration-slow: 500ms
```

**Easing Tokens:**

```
--ease-in: cubic-bezier(0.4, 0, 1, 1)
--ease-out: cubic-bezier(0, 0, 0.2, 1)
--ease-in-out: cubic-bezier(0.4, 0, 0.2, 1)
```

**Document:**

- When to use each duration
- When to use each easing
- Common patterns (modals, notifications, buttons)
- See [[Design-Systems]]

## Related Topics

- [[Micro-Interactions]]
- [[Figma-Prototyping]]
- [[Hi-Fi-Prototyping]]
- [[Interaction-Principles]]
- [[Accessibility]]
- [[Design-Systems]]
- [[WCAG-Guidelines]]

## Tools & Resources

**Design Tools:**

- [[Figma]] - Smart Animate
- [[Principle]] - Micro-interaction focus
- [[Framer]] - Code + design
- [[After Effects]] + [[Lottie]] - Complex animations

**Code Libraries:**

- [[Framer Motion]] - React
- [[GSAP]] - JavaScript
- [[Anime.js]] - Lightweight
- [[React Spring]] - Physics-based

**Learning Resources:**

- cubic-bezier.com - Easing editor
- easings.net - Easing reference
- Material Design: Motion guidelines
- Apple HIG: Animation section

**Books:**

- "Designing Interface Animation" by Val Head
- "Animation at Work" by Rachel Nabors
- "The Web in Motion" by Val Head
- Disney Animation: The Illusion of Life

## Practice Exercises

1. **Easing Comparison:** Create a simple square animation (move from left to right). Duplicate with 4 different easing curves: linear, ease-in, ease-out, ease-in-out. Same duration (300ms). Compare how each feels. Which is most natural for UI?

2. **Modal Animation:** Design a modal with entrance and exit animations. Entrance: Scale from 0.8 to 1, fade in backdrop, duration 250ms, ease-out. Exit: Scale to 0.8, fade out, duration 150ms, ease-in. Why is exit faster?

3. **Staggered List:** Create a list of 5 items. Animate them appearing sequentially (staggered) with 50ms delay between each. Each item: Fade in + slide up slightly. Total duration: ~400ms. Observe the rhythm.

4. **Button States:** Design button with 3 animated states: Hover (scale 1.05, ease-out, 150ms), Press (scale 0.95, ease-in, 100ms), Disabled (opacity 0.5, instant). Prototype all transitions. Test the feel.

5. **Physics Exploration:** Create a bouncing ball animation. Use spring physics (Framer Motion or similar). Adjust spring stiffness and damping. Observe how it affects the feel. When would you use bouncy vs smooth?

6. **Reduced Motion:** Take an animation-heavy prototype (modal + notifications + button states). Create a "reduced motion" version. What do you keep? What do you remove? What do you simplify?

## Further Reading

- "Designing Interface Animation" by Val Head (comprehensive guide)
- "Animation at Work" by Rachel Nabors
- "The Web in Motion" by Val Head
- "The Illusion of Life: Disney Animation" (classic, foundational)
- Material Design: Motion Design Guidelines
- Apple Human Interface Guidelines: Animation
- Nielsen Norman Group: Animation in UX
- Val Head's blog: valhead.com
- UI Animation Newsletter: uianimationnewsletter.com
