# Accessibility

## Introduction

Accessibility (often abbreviated as "a11y") is the practice of designing products that can be used by everyone, regardless of ability, disability, or circumstance. It's not a feature or add-on—it's a fundamental requirement for inclusive, ethical, and legally compliant design. Accessible design benefits not just users with permanent disabilities (blindness, deafness, motor impairments), but also those with temporary limitations (broken arm, bright sunlight), situational constraints (loud environment, slow internet), and aging-related changes (declining vision, reduced dexterity).

The business case for accessibility is compelling: it expands your potential user base significantly (15-20% of the global population has some form of disability), improves SEO (semantic HTML helps search engines), reduces legal risk (ADA, Section 508, European Accessibility Act), and generally improves usability for everyone (clear labels, keyboard navigation, proper contrast benefit all users). Accessible design is better design—forcing clarity, simplicity, and thoughtful structure.

Mastering accessibility means understanding diverse user needs, learning technical standards like [[WCAG-Guidelines]], implementing practical solutions (semantic HTML, ARIA, keyboard navigation, color contrast), testing with assistive technologies, and cultivating empathy for experiences different from your own. Accessibility is not a checklist—it's a mindset of inclusion woven throughout the entire design and development process.

## Learning Objectives

By mastering Accessibility, you will be able to:

- Understand diverse disabilities and how users interact with technology
- Apply WCAG (Web Content Accessibility Guidelines) principles: Perceivable, Operable, Understandable, Robust
- Design interfaces with sufficient color contrast and alternatives to color
- Create keyboard-navigable interfaces without mouse dependence
- Write descriptive alt text and labels for assistive technologies
- Implement accessible forms with clear labels, instructions, and error messages
- Test designs using screen readers and accessibility tools
- Make accessibility part of your entire design process, not an afterthought

## Key Knowledge Points

### Why Accessibility Matters

**Who Benefits:**

- **Permanent disabilities:**

  - Visual: Blindness, low vision, color blindness
  - Auditory: Deafness, hard of hearing
  - Motor: Limited mobility, tremors, paralysis
  - Cognitive: Learning disabilities, memory issues, attention disorders

- **Temporary disabilities:**

  - Broken arm (motor)
  - Eye infection (visual)
  - Ear infection (auditory)

- **Situational limitations:**

  - Bright sunlight (can't see screen)
  - Loud environment (can't hear audio)
  - Holding baby (one hand only)
  - Slow internet (images don't load)

- **Aging population:**
  - Declining vision, hearing, dexterity, cognition
  - Growing demographic

**Everyone benefits:**

- Clear labels (easier to understand)
- Keyboard shortcuts (power users)
- Captions (watching video in quiet place)
- Proper structure (faster to scan)

**Legal Requirements:**

- **USA:** ADA (Americans with Disabilities Act), Section 508
- **Europe:** European Accessibility Act
- **UK:** Equality Act
- **Many countries:** Legal obligations for public sector and increasingly private sector
- **Lawsuits:** Increasingly common (Domino's, Target, Netflix)

**Business Case:**

- Larger potential user base (15-20% of population)
- Better SEO (semantic HTML)
- Improved usability for all
- Reduced legal risk
- Corporate social responsibility

### The Four Principles (WCAG)

WCAG (Web Content Accessibility Guidelines) organized around four principles:

**1. Perceivable:**
Information and UI components must be presented in ways users can perceive.

- **Visual:** Provide text alternatives (alt text)
- **Auditory:** Provide captions, transcripts
- **Color:** Don't rely on color alone
- **Contrast:** Sufficient contrast ratios
- **Adaptable:** Content can be presented in different ways without losing meaning

**2. Operable:**
UI components and navigation must be operable by all users.

- **Keyboard:** All functionality available via keyboard
- **Time:** Enough time to read and interact
- **Seizures:** No flashing content (can trigger seizures)
- **Navigation:** Ways to navigate, find content, determine location
- **Input:** Beyond keyboard (voice, switch)

**3. Understandable:**
Information and operation of UI must be understandable.

- **Readable:** Text readable and understandable
- **Predictable:** Pages appear and operate predictably
- **Input Assistance:** Help users avoid and correct mistakes

**4. Robust:**
Content must be robust enough to work with current and future technologies.

- **Compatible:** Works with assistive technologies
- **Semantic HTML:** Use proper HTML elements
- **ARIA:** Supplement when needed
- **Future-proof:** Works as technologies evolve

See [[WCAG-Guidelines]] for detailed success criteria.

### Visual Accessibility

**Color Contrast:**

- **WCAG Requirements:**

  - **AA (minimum):** 4.5:1 for normal text, 3:1 for large text (18pt+ or 14pt+ bold)
  - **AAA (enhanced):** 7:1 for normal text, 4.5:1 for large text
  - **UI Components:** 3:1 contrast for interactive elements and graphics

- **Tools to Check:**

  - Figma plugins: Stark, A11y - Color Contrast Checker
  - Browser extensions: WAVE, axe DevTools
  - Online: WebAIM Contrast Checker, Contrast Ratio by Lea Verou

- **Common Issues:**
  - Light gray text on white background
  - Colored buttons without enough contrast
  - Placeholder text too light

**Color Blindness:**

- **Types:**

  - **Protanopia:** Red-blind (1% men)
  - **Deuteranopia:** Green-blind (1% men)
  - **Tritanopia:** Blue-blind (rare)
  - **Achromatopsia:** Total color blindness (very rare)
  - Total: ~8% of men, 0.5% of women

- **Design Solutions:**

  - Don't rely on color alone (use icons, labels, patterns)
  - Use color + shape (success = green checkmark, error = red X)
  - Use high contrast
  - Test with color blind simulators

- **Tools:**
  - Figma plugins: Color Blind, Stark
  - Browser: Chrome DevTools (Rendering → Emulate vision deficiencies)
  - Apps: Sim Daltonism (Mac)

**Low Vision:**

- **Needs:**

  - Magnification (up to 400%)
  - High contrast
  - Large text
  - Clear fonts

- **Design Solutions:**
  - Use relative units (rem, em, not px)
  - Allow text resizing without breaking layout
  - Use clear, simple fonts (avoid decorative)
  - Generous spacing
  - Test with zoom

**Blindness:**

- **Assistive Technology:**

  - Screen readers (JAWS, NVDA, VoiceOver, TalkBack)
  - Read content aloud
  - Navigate by headings, landmarks, links

- **Design Solutions:**
  - Semantic HTML (headings, lists, buttons, links)
  - Alt text for images
  - Labels for form fields
  - Skip links (skip to main content)
  - Logical reading order
  - See Screen Readers section below

### Screen Readers

**How They Work:**

- Read content aloud (text-to-speech)
- Navigate by element type (headings, links, buttons, form fields)
- Announce element roles and states
- Use keyboard shortcuts extensively

**Popular Screen Readers:**

- **JAWS** (Windows, paid, most popular in US)
- **NVDA** (Windows, free, open source)
- **VoiceOver** (Mac/iOS, built-in)
- **TalkBack** (Android, built-in)
- **Narrator** (Windows, built-in)

**What They Need:**

- **Semantic HTML:**

  - Use `<button>` not `<div onclick="...">`
  - Use `<nav>`, `<main>`, `<article>`, `<header>`, `<footer>`
  - Use heading hierarchy (`<h1>`, `<h2>`, `<h3>`)

- **Alt Text:**

  - Describe images concisely
  - Decorative images: Empty alt (`alt=""`)
  - Complex images: Longer descriptions (longdesc or adjacent text)

- **Labels:**

  - All form fields have associated labels
  - Use `<label for="...">` or `aria-label`

- **ARIA (Accessible Rich Internet Applications):**
  - Supplement HTML when needed
  - Roles: `role="navigation"`, `role="dialog"`, `role="alert"`
  - Properties: `aria-label`, `aria-labelledby`, `aria-describedby`
  - States: `aria-expanded`, `aria-selected`, `aria-checked`
  - Don't overuse (semantic HTML first)

**Testing:**

- Turn on screen reader (VoiceOver on Mac: Cmd+F5)
- Close your eyes
- Navigate using keyboard only
- Can you complete tasks?

### Keyboard Navigation

Many users can't or don't use a mouse:

- Motor impairments
- Screen reader users
- Power users (faster)

**Requirements:**

- All interactive elements must be keyboard accessible
- Logical tab order
- Visible focus indicators
- Keyboard shortcuts (optional but helpful)

**Key Interactions:**

- **Tab:** Move to next focusable element
- **Shift+Tab:** Move to previous focusable element
- **Enter/Space:** Activate button, link
- **Arrow keys:** Navigate within component (radio buttons, dropdowns, tabs)
- **Esc:** Close modal, cancel action

**Focus Management:**

- **Visible Focus Indicator:**

  - Clear outline or highlight on focused element
  - Don't remove outline (don't use `outline: none` without replacement)
  - WCAG: 3:1 contrast ratio for focus indicator

- **Focus Order:**

  - Should match visual order (left to right, top to bottom)
  - Don't jump around unexpectedly

- **Focus Trapping (Modals):**

  - When modal open, focus stays within modal
  - Tab cycles through modal elements only
  - Esc closes modal, returns focus to trigger

- **Skip Links:**
  - "Skip to main content" link at page start
  - Allows skipping navigation (saves time)
  - Often visually hidden until focused

See [[Keyboard-Navigation]] for deep dive.

### Forms Accessibility

**Labels:**

- Every input needs a label
- Use `<label for="inputId">` (associated)
- Don't rely on placeholder text (disappears when typing)
- Position: Usually above input (better for mobile, zooming)

**Instructions:**

- Provide clear instructions before form
- Indicate required fields (not just color)
- Explain format (e.g., "MM/DD/YYYY")

**Validation & Errors:**

- **Real-time validation:** Helpful but can be distracting
- **On submit:** Show clear error summary at top
- **Individual errors:** Show error message below field
- **Color + icon:** Don't rely on color alone (red = error + X icon)
- **Focus on error:** Move focus to first error
- **Clear messages:** "Email is required" not "Error in field 3"

**Grouping:**

- Use `<fieldset>` and `<legend>` for related fields
- Example: "Shipping Address" fieldset with multiple fields

**Autocomplete:**

- Use HTML autocomplete attributes
- Helps users with cognitive disabilities
- Speeds up form completion

### Cognitive Accessibility

Users with cognitive, learning, or neurological disabilities:

- Dyslexia, ADHD, autism, memory issues, anxiety

**Design Principles:**

- **Simplicity:**

  - Clear, simple language (avoid jargon)
  - Short sentences and paragraphs
  - Break complex tasks into steps

- **Consistency:**

  - Predictable layouts and interactions
  - Familiar patterns
  - Consistent navigation

- **Clarity:**

  - Clear headings and labels
  - Meaningful link text ("Learn more about accessibility" not "Click here")
  - Visual hierarchy

- **Forgiveness:**

  - Undo functionality
  - Confirmation for destructive actions
  - Autosave drafts

- **Reduce Distractions:**

  - Avoid auto-playing videos/audio
  - Limit animations (respect prefers-reduced-motion)
  - Focus on primary task

- **Memory Support:**
  - Show progress in multi-step flows
  - Provide reminders
  - Allow saving and returning

### Motor Accessibility

Users with limited mobility, tremors, or paralysis:

**Design Solutions:**

- **Large Click Targets:**

  - Minimum 44×44px (Apple), 48×48px (Material Design)
  - Especially important for mobile
  - Space out interactive elements

- **Generous Spacing:**

  - Avoid crowded interfaces
  - Prevent accidental clicks

- **Keyboard Access:**

  - Full keyboard support (no mouse required)
  - See Keyboard Navigation section

- **Avoid Time Limits:**

  - Or provide way to extend/disable
  - Users may need more time

- **Alternative Inputs:**
  - Voice control (Siri, Alexa, Dragon)
  - Switch access (single button input)
  - Eye tracking

**Gestures (Mobile):**

- Provide alternatives to complex gestures
- Don't require precision (e.g., small drag handles)
- Support tap as alternative to swipe

### Auditory Accessibility

Users who are deaf or hard of hearing:

**Video Content:**

- **Captions/Subtitles:**

  - Synchronized text of spoken content
  - Include sound effects, music descriptions
  - Required for WCAG AA

- **Transcripts:**
  - Full text version of audio/video
  - Allows searching, skimming

**Audio Cues:**

- Don't rely on sound alone
- Provide visual alternatives
- Example: Notification sound + visual notification

**Video Calls/Conferencing:**

- Real-time captions
- Sign language interpretation

### Motion & Animation

See [[Animation-Principles]] for full details.

**Motion Sensitivity:**

- Some users experience nausea, dizziness, migraines from animations
- Vestibular disorders

**Prefers-Reduced-Motion:**

- CSS media query: `@media (prefers-reduced-motion: reduce)`
- User sets in OS settings (Mac, Windows, iOS, Android)
- **When enabled:**
  - Remove non-essential animations
  - Use fade instead of slide/zoom
  - Instant transitions for decorative effects
  - Keep essential feedback (loading, success)

**Best Practices:**

- Make animations optional
- Avoid auto-playing videos
- No parallax scrolling (can cause motion sickness)
- No flashing content (can trigger seizures)

### Responsive & Mobile

**Accessibility on Mobile:**

- Touch targets: 44-48px minimum
- Zoom enabled (don't disable)
- Readable text (16px+ body text)
- TalkBack (Android), VoiceOver (iOS) support
- Landscape and portrait orientations

**Responsive Text:**

- Use relative units (rem, em)
- Allow text scaling (200% minimum)
- Don't break layout when zoomed

### Testing for Accessibility

**Automated Tools:**

- Browser extensions: axe DevTools, WAVE, Lighthouse
- Figma plugins: Stark, A11y - Color Contrast Checker
- Automated testing: axe-core, Pa11y
- Catches ~30-50% of issues (not comprehensive)

**Manual Testing:**

- **Keyboard Only:**

  - Unplug mouse
  - Navigate using keyboard only
  - Can you reach everything?

- **Screen Reader:**

  - VoiceOver (Mac): Cmd+F5
  - NVDA (Windows): Free download
  - Navigate, close your eyes

- **Zoom/Magnification:**

  - Zoom to 200%, 400%
  - Does layout still work?

- **Color Blindness Simulators:**
  - Chrome DevTools, Figma plugins
  - Is information still conveyed?

**User Testing:**

- Test with people with disabilities
- Invaluable insights
- Consider hiring accessibility consultants

### Accessibility in Design Process

**Throughout, Not Afterthought:**

- **Research:** Include users with disabilities
- **Wireframing:** Plan heading structure, keyboard flow
- **Design:** Check contrast, plan focus states, write alt text
- **Prototyping:** Test keyboard navigation, screen reader
- **Development:** Semantic HTML, ARIA, testing
- **QA:** Automated + manual accessibility testing
- **Launch:** Accessibility statement, feedback mechanism
- **Ongoing:** Regular audits, user feedback

### Common Mistakes

**Don't:**

- ❌ Remove focus outlines (keyboard users need them)
- ❌ Rely on color alone (add icons, labels)
- ❌ Use placeholder as label (disappears when typing)
- ❌ Disable zoom on mobile
- ❌ Low contrast text (fails WCAG)
- ❌ Auto-play videos with sound
- ❌ Keyboard traps (can't escape with keyboard)
- ❌ Treat accessibility as last-minute checklist

**Do:**

- ✅ Use semantic HTML
- ✅ Provide text alternatives (alt text)
- ✅ Ensure keyboard accessibility
- ✅ Sufficient color contrast
- ✅ Clear labels and instructions
- ✅ Test with assistive technologies
- ✅ Include users with disabilities in research
- ✅ Make accessibility part of process

## Related Topics

- [[WCAG-Guidelines]]
- [[Keyboard-Navigation]]
- [[Contrast-and-Accessibility]]
- [[Animation-Principles]]
- [[Usability-Heuristics]]
- [[Interaction-Principles]]
- [[Typography]]

## Tools & Resources

**Contrast Checkers:**

- WebAIM Contrast Checker
- Contrast Ratio by Lea Verou
- Figma: Stark, A11y - Color Contrast Checker

**Color Blind Simulators:**

- Chrome DevTools (Rendering tab)
- Figma: Color Blind plugin, Stark
- Sim Daltonism (Mac app)

**Screen Readers:**

- VoiceOver (Mac/iOS, built-in)
- NVDA (Windows, free)
- JAWS (Windows, paid)
- TalkBack (Android, built-in)

**Testing Tools:**

- Browser: axe DevTools, WAVE, Lighthouse
- Automated: axe-core, Pa11y
- Figma: Stark (comprehensive)

**Guidelines:**

- WCAG 2.1 (w3.org/WAI/WCAG21)
- Apple Human Interface Guidelines: Accessibility
- Material Design: Accessibility
- Microsoft Inclusive Design toolkit

**Learning:**

- WebAIM (webaim.org) - articles, resources
- A11y Project (a11yproject.com) - checklist
- Deque University - courses
- Inclusive Components (inclusive-components.design)

## Practice Exercises

1. **Contrast Audit:** Take a design (yours or from Dribbble). Check all text and UI elements for WCAG AA contrast (4.5:1 text, 3:1 UI). Identify failures. Fix them. Use WebAIM Contrast Checker or Figma plugin.

2. **Keyboard Navigation:** Take a prototype (e.g., sign-up form). Navigate using keyboard only (no mouse). Can you complete the task? Are focus indicators visible? Is tab order logical? Make improvements.

3. **Screen Reader Test:** Turn on VoiceOver (Mac) or NVDA (Windows). Close your eyes. Try to use a website (your design or popular site). What's confusing? What works well? Document findings.

4. **Alt Text Practice:** Find 10 images (icons, photos, infographics). Write appropriate alt text for each. Remember: Describe content and function concisely. Decorative images get empty alt (`alt=""`).

5. **Color Blind Simulation:** Take a design with color-coded information (e.g., error states in red). View with color blind simulator (Chrome DevTools or Figma plugin). Is information still conveyed? Add icons/labels if needed.

6. **Accessible Form:** Design a sign-up form (email, password, confirm password). Include: Labels (not just placeholders), required field indicators (not just color), clear error messages, visible focus states. Prototype and test with keyboard.

## Further Reading

- **"Inclusive Design Patterns" by Heydon Pickering** (practical guide)
- **"Accessibility for Everyone" by Laura Kalbag** (great introduction)
- **"Inclusive Design for a Digital World" by Regine Gilbert** (comprehensive)
- WCAG 2.1 Guidelines (official standard)
- WebAIM (webaim.org) - articles and resources
- A11y Project (a11yproject.com) - checklist and resources
- Microsoft Inclusive Design toolkit (download.microsoft.com)
- Apple Accessibility (developer.apple.com)
- Material Design Accessibility (material.io)
- "Invisible Women" by Caroline Criado Perez (data bias, includes disability)
