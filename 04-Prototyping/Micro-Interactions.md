# Micro-Interactions

## Introduction

Micro-interactions are the small, contained moments of functionality that accomplish a single task—often with delightful animation or feedback. They're the subtle animations when you "like" a post, the gentle vibration when toggling a setting, the satisfying checkmark when completing a task, or the bouncy notification badge that draws your eye. Though tiny in scope, micro-interactions are crucial to user experience: they provide feedback, communicate status, guide attention, prevent errors, and add personality to interfaces.

Every interaction in a digital product—from clicking a button to dragging a slider to pulling down to refresh—can be enhanced by thoughtful micro-interaction design. These moments turn functional requirements into engaging experiences. A button doesn't just change color on click; it depresses slightly, creates a subtle shadow, maybe ripples outward. A form doesn't just validate silently; it shakes gently for errors, shows a green checkmark for success, provides immediate, clear feedback that guides the user forward without friction.

The best micro-interactions are invisible by design—users don't consciously notice them, but they'd feel their absence. They reduce cognitive load by providing instant feedback, they reinforce mental models by behaving predictably, and they inject moments of joy into routine tasks. Mastering micro-interactions means understanding animation principles, interaction feedback, timing, and knowing when subtlety serves users better than spectacle.

## Learning Objectives

By mastering Micro-Interactions, you will be able to:

- Identify opportunities for micro-interactions in user interfaces
- Design feedback mechanisms that communicate state and action outcomes
- Apply animation principles to create smooth, purposeful motion
- Implement micro-interactions using modern design and prototyping tools
- Balance personality with usability in interactive moments
- Optimize timing and easing for natural-feeling interactions
- Design accessible micro-interactions that don't exclude users
- Test and refine micro-interactions based on user feedback

## Key Knowledge Points

### Micro-Interaction Structure

Dan Saffer's framework (from "Microinteractions" book):

**1. Trigger:**

- Initiates the micro-interaction
- **User-initiated:** Button click, toggle switch, swipe
- **System-initiated:** Notification arrives, process completes, error occurs

**2. Rules:**

- What happens during the interaction
- Logic and conditions
- Example: "When toggle is tapped, switch state from off to on"

**3. Feedback:**

- How the system communicates what's happening
- Visual, auditory, haptic
- Example: Toggle animates from left to right, color changes gray → blue

**4. Loops & Modes:**

- What happens over time or in different states
- Repeat behaviors, time-based changes
- Example: Loading spinner loops until process completes

### Common Micro-Interaction Types

**Button Interactions:**

- [[Button Hover]]

  - Color change (subtle shift)
  - Scale up slightly (1.05x)
  - Shadow increase (elevation)
  - Cursor change (pointer)
  - Duration: 150-200ms
  - Easing: Ease-out

- [[Button Press/Active]]

  - Scale down (0.95x) - feels "pressed"
  - Color darker or more saturated
  - Shadow decrease (depresses)
  - Duration: 100ms
  - Easing: Ease-in

- [[Button Disabled]]
  - Reduced opacity (0.4-0.6)
  - Grayscale or desaturated
  - No hover effect
  - Cursor: not-allowed

**Toggle Switches:**

- Sliding circle animation
- Background color change (gray → accent color)
- Smooth transition (200-300ms, ease-in-out)
- Haptic feedback on mobile (optional)
- Clear on/off states

**Checkbox/Radio Buttons:**

- Checkmark animation (draw-in effect)
- Background fill animation
- Scale slightly on check
- Ripple effect (Material Design)

**Form Field Interactions:**

- [[Focus State]]

  - Border color change (gray → accent)
  - Border thickness increase (1px → 2px)
  - Subtle glow/shadow
  - Label animation (float up if inline)

- [[Input Validation]]
  - Success: Green checkmark appears
  - Error: Red X appears, field shakes, error message slides in
  - Real-time: Validate as user types (email format, password strength)

**Loading Indicators:**

- [[Spinner/Progress]]

  - Smooth rotation (linear easing)
  - Appears after ~300-500ms delay (don't flash for fast loads)
  - Indeterminate (spinning) or determinate (progress bar)

- [[Skeleton Screens]]

  - Placeholder shapes with shimmer animation
  - Less jarring than spinners
  - Shows content structure

- [[Progress Bars]]
  - Smooth fill animation
  - Percentage or time remaining
  - Color change at completion (blue → green)

**Notifications & Alerts:**

- [[Toast Notifications]]

  - Slide in from top/bottom
  - Auto-dismiss after 3-5 seconds
  - Hover to persist (pause auto-dismiss)
  - Slide out or fade out

- [[Badge Notifications]]
  - Count appears with scale-up animation
  - Bounce or pulse to draw attention
  - Color: Red (errors, alerts), blue (info)

**Drag & Drop:**

- **Drag start:** Element lifts (shadow increase, slight scale)
- **While dragging:** Cursor change, element follows
- **Drop zones:** Highlight when hovered
- **Drop:** Snap into place or bounce back if invalid

**Pull to Refresh:**

- Pull down gesture
- Loading icon appears and spins
- Bouncy release animation
- Content refreshes with smooth transition

### Animation Principles for Micro-Interactions

**Duration:**

- **<100ms:** Instant, barely perceptible (cursor changes)
- **100-300ms:** Standard UI transitions (most micro-interactions)
- **300-500ms:** Longer, more noticeable (complex animations)
- **>500ms:** Slow, use rarely (may feel sluggish)

**Rule of thumb:** Micro-interactions should be quick. Users shouldn't wait.

**Easing (Timing Functions):**

- [[Ease-Out]]: Fast start, slow end

  - Most natural for UI
  - Use for: Elements entering, buttons responding
  - Example: Button scales up quickly, settles gently

- [[Ease-In]]: Slow start, fast end

  - Use for: Elements exiting, disappearing
  - Example: Modal fades out slowly then quickly

- [[Ease-In-Out]]: Slow start, fast middle, slow end

  - Use for: Elements that move both in and out
  - Example: Modal opening and closing

- [[Linear]]: Constant speed

  - Feels robotic, use sparingly
  - Use for: Loading indicators, mechanical movements

- [[Custom Curves]]: CSS cubic-bezier, spring physics
  - Bouncy, playful effects
  - Use for: Delightful moments, brand personality

See [[Animation-Principles]] for deeper dive.

**Physics & Motion:**

- **Realistic motion:** Objects have weight, momentum
- **Overshoot:** Bounce slightly past target, settle back
- **Spring animations:** Natural, bouncy (iOS style)
- **Avoid:** Sudden stops, linear motion (feels unnatural)

### Feedback Types

**Visual Feedback:**

- Color changes
- Shape changes
- Position changes (movement)
- Opacity changes (fade)
- Size changes (scale)
- Most common and essential

**Auditory Feedback:**

- Click sounds
- Success chimes
- Error alerts
- Use sparingly (can annoy)
- Allow users to disable
- Examples: Message sent, notification arrived

**Haptic Feedback (Mobile/Wearables):**

- Vibrations
- Subtle: Success confirmation
- Strong: Error or important alert
- iOS: Haptic Touch (different patterns for different actions)
- Android: Vibration patterns
- Battery consideration (use judiciously)

**Combination:**
Most effective: Visual + Haptic (e.g., toggle switch)

### Context & Purpose

**Why Micro-Interactions Matter:**

- [[Feedback]]: Confirm action was received

  - "Yes, we heard you"
  - Reduces uncertainty

- [[Visibility of System Status]]: Show what's happening

  - Loading indicators
  - Progress bars
  - See [[Interaction-Principles]]

- [[Error Prevention]]: Guide away from mistakes

  - Disable invalid actions
  - Show real-time validation

- [[Guidance]]: Direct user attention

  - Highlight next step
  - Animated arrows or pulses

- [[Personality]]: Add brand character
  - Playful animations
  - Unique transitions
  - See [[Brand]] and [[Style-Guides]]

### Design Patterns

**State Change Indicators:**

- **Before:** Gray, inactive
- **During:** Animating (transition)
- **After:** Colored, active
- Example: Favoriting an item (heart gray → animates → red)

**Success Confirmation:**

- Checkmark animation (draw-in or scale-up)
- Green color
- Brief positive sound/vibration
- Auto-dismiss or persist

**Error Handling:**

- Shake animation (horizontal wiggle)
- Red color
- Error icon (X or alert)
- Error message appears (slide in)
- Example: Wrong password, form field shakes

**Attention-Getting:**

- Pulse animation (scale subtly in/out)
- Glow effect
- Badge bounce
- Use sparingly (can be annoying)

**Delight Moments:**

- Confetti animation (celebration)
- Fun character animations
- Playful transitions
- Use for: Achievements, milestones, onboarding completion

### Designing Micro-Interactions

**Process:**

1. **Identify Opportunity:**

   - Where does user need feedback?
   - Where can personality shine?
   - What actions need confirmation?

2. **Define Purpose:**

   - What is this micro-interaction communicating?
   - Feedback? Delight? Guidance?

3. **Sketch/Storyboard:**

   - Draw states: Before, during, after
   - Note timing and easing

4. **Prototype:**

   - Use [[Figma-Prototyping]], [[Principle]], [[Framer]]
   - Iterate on timing, easing, details

5. **Test:**

   - Does it feel right?
   - Too fast? Too slow? Too much?
   - Get feedback

6. **Refine:**
   - Adjust timing, easing
   - Simplify if needed
   - Optimize performance

**Best Practices:**

- **Subtle over flashy:** Don't distract from task
- **Fast over slow:** Users want speed
- **Purposeful over decorative:** Every animation should have a reason
- **Consistent:** Similar actions = similar animations
- **Accessible:** Works for all users (see [[Accessibility]])
- **Performant:** Smooth 60fps, no jank

### Accessibility Considerations

**Reduced Motion:**

- Some users get motion sickness
- Respect `prefers-reduced-motion` (CSS media query)
- Provide static alternative
- Essential animations only (not decorative)

**Screen Readers:**

- Animations often invisible to screen readers
- Provide text feedback alternatives
- Announce state changes
- Example: "Button pressed," "Item added to cart"

**Color Reliance:**

- Don't rely on color alone
- Use icons + color
- Example: Success = green + checkmark

**Timing:**

- Don't require fast interaction
- Allow time for users with motor impairments

See [[Accessibility]] and [[WCAG-Guidelines]].

### Tools for Micro-Interactions

**Design Tools:**

- [[Figma]] with [[Smart Animate]]

  - Great for simple micro-interactions
  - Limited physics

- [[Principle]] (Mac)

  - Timeline-based
  - Excellent for micro-interactions
  - Easy prototyping

- [[Framer]]

  - Code-based (React)
  - Powerful, realistic physics
  - Spring animations

- [[ProtoPie]]
  - Advanced interactions
  - No code
  - Sensors, conditions

**Code Libraries:**

- [[Framer Motion]] (React)

  - Spring animations
  - Gesture animations

- [[GSAP]] (JavaScript)

  - Powerful animation library
  - Complex timelines

- [[Lottie]]

  - After Effects animations
  - JSON-based, scalable

- [[Anime.js]]
  - Lightweight JavaScript animation

### Common Mistakes

**Over-Animation:**

- Too many animations = overwhelming
- Every element doesn't need to animate
- Solution: Use sparingly, purposefully

**Too Slow:**

- Users forced to wait
- Frustrating, feels sluggish
- Solution: Keep under 300ms for most UI

**Inconsistent:**

- Different animations for similar actions
- Confusing mental model
- Solution: Create animation system (consistent timings, easings)

**No Purpose:**

- Animation for animation's sake
- Doesn't communicate or delight
- Solution: Every animation needs a "why"

**Inaccessible:**

- Motion-sensitive users excluded
- No alternative provided
- Solution: Respect reduced motion preferences

### Examples from Popular Apps

**Like/Heart Animation (Twitter, Instagram):**

- Heart scales up
- Color fills (gray → red)
- Particles burst outward (optional)
- Haptic feedback (mobile)
- Duration: ~300ms

**Pull to Refresh (iOS Mail, Twitter):**

- Pull down reveals loading indicator
- Spinner appears
- Release triggers refresh
- Bouncy animation
- Content slides in when loaded

**Swipe to Delete (iOS):**

- Swipe left reveals delete button
- Button slides in from right
- Red color indicates destructive action
- Complete swipe deletes immediately
- Partial swipe shows button, tap to confirm

**Form Validation (Mailchimp, Google Forms):**

- Real-time validation as user types
- Green checkmark for valid
- Red X for invalid
- Error message appears below field
- Field border changes color

**Loading Skeleton (Facebook, LinkedIn):**

- Placeholder shapes in content layout
- Shimmer animation sweeps across
- Content fades in when loaded
- Less jarring than spinner

## Related Topics

- [[Animation-Principles]]
- [[Interaction-Principles]]
- [[Figma-Prototyping]]
- [[Hi-Fi-Prototyping]]
- [[Usability-Heuristics]]
- [[Accessibility]]
- [[Affordances]]

## Tools & Resources

**Design Tools:**

- [[Figma]] - Smart Animate
- [[Principle]] - Micro-interaction focus
- [[Framer]] - Code-based animations
- [[ProtoPie]] - Advanced no-code

**Code Libraries:**

- [[Framer Motion]] - React animations
- [[GSAP]] - JavaScript animations
- [[Lottie]] - After Effects animations
- [[Anime.js]] - Lightweight animations

**Inspiration:**

- Dribbble: Search "micro-interactions"
- UI Movement: uimovement.com
- Lottie Files: lottiefiles.com
- Codrops: Interaction demos

**Books:**

- "Microinteractions" by Dan Saffer (essential)
- "Designing Interface Animation" by Val Head
- "The Web in Motion" by Val Head

## Practice Exercises

1. **Button States:** Design a button with 4 states (Default, Hover, Active, Disabled). Prototype transitions in Figma using Smart Animate. Timing: Hover 150ms, Active 100ms. Use appropriate easing.

2. **Like Animation:** Create a "like" button that animates when clicked. Heart should scale up (1.2x), change color (gray → red), and overshoot slightly before settling. Add subtle particle effect (optional). Duration: 300ms total.

3. **Form Validation:** Design an email input field with real-time validation. Show loading state while checking, green checkmark if valid, red X if invalid with shake animation and error message. Prototype the full interaction.

4. **Toggle Switch:** Design an iOS-style toggle switch with smooth slide animation. Circle slides left/right (150px), background changes color (gray → green), include haptic feedback indicator. Duration: 200ms, ease-in-out.

5. **Loading States:** Design 3 different loading indicators: (1) spinner, (2) progress bar, (3) skeleton screen. Prototype each. Which feels best for different contexts?

6. **Notification Toast:** Create a success notification that slides in from top, displays for 3 seconds, then slides out. Add hover state that pauses auto-dismiss. Include close button.

## Further Reading

- "Microinteractions: Designing with Details" by Dan Saffer (must-read)
- "Designing Interface Animation" by Val Head
- "The Web in Motion" by Val Head
- Nielsen Norman Group: Micro-interaction articles
- Material Design: Motion guidelines
- Apple Human Interface Guidelines: Animation section
- "Animation at Work" by Rachel Nabors
