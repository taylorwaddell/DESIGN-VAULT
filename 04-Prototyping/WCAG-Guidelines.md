# WCAG Guidelines

## Introduction

The Web Content Accessibility Guidelines (WCAG) are the international standard for digital accessibility, developed by the W3C (World Wide Web Consortium) through the Web Accessibility Initiative (WAI). WCAG provides a comprehensive, testable framework for making web content and applications accessible to people with disabilities—including visual, auditory, motor, cognitive, and neurological impairments. These guidelines are not just best practices; they're increasingly codified into law worldwide through regulations like the ADA (USA), European Accessibility Act, and Section 508.

WCAG is organized into four principles (Perceivable, Operable, Understandable, Robust—abbreviated POUR), with each principle containing guidelines, and each guideline containing testable success criteria at three conformance levels (A, AA, AAA). Level A represents minimum accessibility, Level AA is the standard target for most organizations (and required by most laws), and Level AAA represents enhanced accessibility (often impractical to achieve across all content). Understanding WCAG means knowing not just what to do, but why—connecting technical requirements to real user needs.

Mastering WCAG enables you to design and build products that are legally compliant, ethically inclusive, and practically usable by the widest possible audience. While WCAG can seem daunting with its technical language and numerous criteria, it ultimately guides you to create clearer, more usable experiences for everyone. WCAG isn't a checklist to complete once—it's a framework for thinking about accessibility throughout the entire design and development process.

## Learning Objectives

By mastering WCAG Guidelines, you will be able to:

- Understand the POUR principles (Perceivable, Operable, Understandable, Robust)
- Navigate WCAG success criteria and conformance levels (A, AA, AAA)
- Apply specific WCAG requirements to design decisions (contrast, text alternatives, keyboard access)
- Test interfaces against WCAG success criteria
- Prioritize accessibility improvements based on impact and conformance level
- Communicate accessibility requirements to developers and stakeholders
- Stay current with WCAG updates and emerging accessibility standards

## Key Knowledge Points

### WCAG Overview

**Versions:**

- **WCAG 2.0** (2008): Original standard
- **WCAG 2.1** (2018): Current standard, adds mobile, low vision, cognitive
- **WCAG 2.2** (2023): Latest, adds more criteria
- **WCAG 3.0** (in development): Major overhaul, not yet ready

**Most commonly referenced:** WCAG 2.1 Level AA

**Structure:**

- **4 Principles:** Perceivable, Operable, Understandable, Robust (POUR)
- **13 Guidelines:** Under each principle
- **78+ Success Criteria (2.1):** Testable statements at A, AA, or AAA levels
- **Sufficient Techniques:** Ways to meet criteria
- **Advisory Techniques:** Beyond requirements (best practices)

**Conformance Levels:**

- **Level A:** Minimum (basic accessibility)
- **Level AA:** Standard target (legally required in many jurisdictions)
- **Level AAA:** Enhanced (not always achievable for all content)

**Target:** WCAG 2.1 Level AA is the goal for most organizations.

### The POUR Principles

**1. Perceivable:**
Information and UI components must be presentable to users in ways they can perceive.

**2. Operable:**
UI components and navigation must be operable by all users.

**3. Understandable:**
Information and operation of UI must be understandable to users.

**4. Robust:**
Content must be robust enough to work with current and future technologies, especially assistive technologies.

## Principle 1: Perceivable

Users must be able to perceive the information presented.

### Guideline 1.1: Text Alternatives

Provide text alternatives for non-text content.

**Success Criteria:**

**1.1.1 Non-text Content (Level A):**

- All images, icons, and non-text content must have text alternatives
- **Images:**
  - Informative images: Descriptive alt text
  - Decorative images: Empty alt (`alt=""`)
  - Functional images (buttons, links): Describe function
  - Complex images (charts, diagrams): Longer description
- **Form inputs:** Labels or aria-label
- **Icons:** aria-label or adjacent text
- **Audio/video:** Transcripts

**Examples:**

```html
<!-- Informative image -->
<img src="chart.png" alt="Sales increased 25% in Q4" />

<!-- Decorative image -->
<img src="divider.png" alt="" />

<!-- Functional image -->
<button><img src="search-icon.svg" alt="Search" /></button>

<!-- Icon with label -->
<span aria-label="Warning">⚠️</span>
```

### Guideline 1.2: Time-based Media

Provide alternatives for time-based media (audio and video).

**Success Criteria:**

**1.2.1 Audio-only and Video-only (Level A):**

- Pre-recorded audio-only: Provide transcript
- Pre-recorded video-only (no audio): Provide transcript or audio description

**1.2.2 Captions (Level A):**

- Captions for all pre-recorded video with audio
- Synchronized text of spoken content and important sounds

**1.2.3 Audio Description or Media Alternative (Level A):**

- Audio description (narration of visual content) OR
- Full transcript for pre-recorded video

**1.2.4 Captions (Live) (Level AA):**

- Real-time captions for live video

**1.2.5 Audio Description (Level AA):**

- Audio description for all pre-recorded video
- Narrates important visual information

**Examples:**

- YouTube videos: Add captions
- Podcasts: Provide transcript
- Webinars: Real-time captions

### Guideline 1.3: Adaptable

Create content that can be presented in different ways without losing information.

**Success Criteria:**

**1.3.1 Info and Relationships (Level A):**

- Information, structure, and relationships must be programmatically determinable
- **Use semantic HTML:**
  - Headings: `<h1>`, `<h2>`, `<h3>` (not just styled text)
  - Lists: `<ul>`, `<ol>`, `<li>` (not divs with bullets)
  - Tables: `<table>`, `<th>`, `<td>` with headers
  - Forms: `<label>` associated with inputs
  - Regions: `<nav>`, `<main>`, `<article>`, `<aside>`

**1.3.2 Meaningful Sequence (Level A):**

- Reading order in code matches visual order
- Tab order is logical
- Screen readers read in correct sequence

**1.3.3 Sensory Characteristics (Level A):**

- Don't rely on sensory characteristics alone
- ❌ "Click the round button"
- ✅ "Click the Submit button (round, blue)"

**1.3.4 Orientation (Level AA) - WCAG 2.1:**

- Don't restrict to single orientation (portrait or landscape)
- Allow both unless essential

**1.3.5 Identify Input Purpose (Level AA) - WCAG 2.1:**

- Use HTML autocomplete attributes
- Helps autofill, personalization

```html
<input type="email" autocomplete="email" />
```

### Guideline 1.4: Distinguishable

Make it easier for users to see and hear content.

**Success Criteria:**

**1.4.1 Use of Color (Level A):**

- Color is not the only visual means of conveying information
- Examples:
  - Error fields: Red color + icon + text label
  - Links: Underlined, not just different color
  - Status: Color + icon (green checkmark, red X)

**1.4.2 Audio Control (Level A):**

- If audio plays automatically for >3 seconds, provide control to pause/stop

**1.4.3 Contrast (Minimum) (Level AA):**

- **Text:**
  - Small text: 4.5:1 contrast ratio
  - Large text (18pt+ or 14pt+ bold): 3:1
- **Exceptions:** Logos, decorative, disabled elements

**1.4.4 Resize Text (Level AA):**

- Text can be resized up to 200% without loss of content or functionality
- Use relative units (rem, em), not fixed pixels

**1.4.5 Images of Text (Level AA):**

- Use actual text, not images of text (unless essential like logos)
- Text is scalable, translatable, customizable

**1.4.6 Contrast (Enhanced) (Level AAA):**

- Small text: 7:1
- Large text: 4.5:1

**1.4.10 Reflow (Level AA) - WCAG 2.1:**

- Content reflows to 320px width (400% zoom) without horizontal scrolling
- Responsive design

**1.4.11 Non-text Contrast (Level AA) - WCAG 2.1:**

- UI components and graphical objects: 3:1 contrast
- Buttons, form borders, icons, charts

**1.4.12 Text Spacing (Level AA) - WCAG 2.1:**

- Content doesn't break when users adjust:
  - Line height: 1.5× font size
  - Paragraph spacing: 2× font size
  - Letter spacing: 0.12× font size
  - Word spacing: 0.16× font size

**1.4.13 Content on Hover or Focus (Level AA) - WCAG 2.1:**

- Tooltips and popovers:
  - Dismissible (Esc key)
  - Hoverable (can move mouse over without disappearing)
  - Persistent (doesn't disappear on its own)

**Contrast Examples:**

- Black text on white: 21:1 ✅ (AAA)
- Dark gray (#595959) on white: 7:1 ✅ (AAA)
- Medium gray (#767676) on white: 4.5:1 ✅ (AA)
- Light gray (#959595) on white: 2.8:1 ❌ (fails AA)

Use contrast checker: WebAIM, Figma plugins

## Principle 2: Operable

Users must be able to operate the interface.

### Guideline 2.1: Keyboard Accessible

Make all functionality available from keyboard.

**Success Criteria:**

**2.1.1 Keyboard (Level A):**

- All functionality available via keyboard
- No mouse required
- Standard keys: Tab, Enter, Space, Arrow keys, Esc

**2.1.2 No Keyboard Trap (Level A):**

- Users can navigate away from any component using keyboard
- Can't get "stuck"
- Modals: Esc closes, focus returns

**2.1.4 Character Key Shortcuts (Level A) - WCAG 2.1:**

- If single-character shortcuts exist, allow users to:
  - Turn off
  - Remap
  - Only active when component focused
- Prevents conflicts with assistive tech

**Keyboard Testing:**

- Unplug mouse
- Use Tab to navigate
- Enter/Space to activate
- Esc to cancel/close
- Can you complete all tasks?

See [[Keyboard-Navigation]] for details.

### Guideline 2.2: Enough Time

Provide users enough time to read and use content.

**Success Criteria:**

**2.2.1 Timing Adjustable (Level A):**

- For time limits:
  - Turn off, OR
  - Adjust before time expires, OR
  - Extend (at least 10× original)
- Exceptions: Real-time events (auctions), essential time limits (exams)

**2.2.2 Pause, Stop, Hide (Level A):**

- Auto-updating, blinking, scrolling content (>5 seconds):
  - User can pause, stop, or hide
- Examples: Carousels, live news tickers

### Guideline 2.3: Seizures

Do not design content that causes seizures.

**Success Criteria:**

**2.3.1 Three Flashes or Below Threshold (Level A):**

- No content flashes more than 3 times per second
- Can trigger seizures (photosensitive epilepsy)
- Applies to flashing, blinking, rapid color changes

### Guideline 2.4: Navigable

Provide ways to help users navigate, find content, and determine location.

**Success Criteria:**

**2.4.1 Bypass Blocks (Level A):**

- Mechanism to skip repeated blocks (navigation)
- **Skip links:** "Skip to main content"
- **Landmarks:** `<nav>`, `<main>` help screen readers jump

**2.4.2 Page Titled (Level A):**

- Pages have descriptive, unique titles
- `<title>` element in HTML
- Shows in browser tab, search results, bookmarks

**2.4.3 Focus Order (Level A):**

- Tab order is logical and meaningful
- Matches visual order (left to right, top to bottom)

**2.4.4 Link Purpose (Level A):**

- Purpose of link can be determined from link text (or link + context)
- ❌ "Click here"
- ✅ "Read more about accessibility guidelines"

**2.4.5 Multiple Ways (Level AA):**

- Multiple ways to find pages (except in processes)
- Examples: Menu, search, sitemap, breadcrumbs

**2.4.6 Headings and Labels (Level AA):**

- Headings and labels are descriptive
- Clearly describe topic or purpose

**2.4.7 Focus Visible (Level AA):**

- Keyboard focus indicator is visible
- Don't remove outline without replacing
- 3:1 contrast minimum (WCAG 2.2)

### Guideline 2.5: Input Modalities (WCAG 2.1)

Make it easier to operate functionality through various inputs beyond keyboard.

**Success Criteria:**

**2.5.1 Pointer Gestures (Level A):**

- Multipoint or path-based gestures have single-pointer alternative
- Pinch-to-zoom: Also provide +/- buttons
- Complex swipes: Also provide buttons

**2.5.2 Pointer Cancellation (Level A):**

- For single-pointer actions:
  - Down-event doesn't trigger action (wait for up-event)
  - OR can abort/undo
- Prevents accidental activation

**2.5.3 Label in Name (Level A):**

- If UI component has visible label, accessible name includes that text
- "Submit" button: Accessible name includes "Submit"

**2.5.4 Motion Actuation (Level A):**

- Functionality triggered by device motion (shake, tilt) has alternative
- Not everyone can shake device

## Principle 3: Understandable

Users must be able to understand the information and operation.

### Guideline 3.1: Readable

Make text content readable and understandable.

**Success Criteria:**

**3.1.1 Language of Page (Level A):**

- Page language is programmatically determined
- `<html lang="en">`
- Helps screen readers pronounce correctly

**3.1.2 Language of Parts (Level AA):**

- Language of passages/phrases is indicated
- `<span lang="fr">Bonjour</span>`

### Guideline 3.2: Predictable

Make pages appear and operate in predictable ways.

**Success Criteria:**

**3.2.1 On Focus (Level A):**

- Receiving focus doesn't trigger change of context
- No surprise navigation, form submission, popups

**3.2.2 On Input (Level A):**

- Changing setting doesn't automatically trigger change of context
- Example: Changing dropdown shouldn't submit form (need explicit button)

**3.2.3 Consistent Navigation (Level AA):**

- Repeated navigation is in same relative order across pages
- Menu doesn't rearrange

**3.2.4 Consistent Identification (Level AA):**

- Components with same functionality are identified consistently
- Same icon = same meaning throughout site

### Guideline 3.3: Input Assistance

Help users avoid and correct mistakes.

**Success Criteria:**

**3.3.1 Error Identification (Level A):**

- Errors are identified in text
- Not just red border (color + text)
- "Email is required"

**3.3.2 Labels or Instructions (Level A):**

- Labels or instructions provided for user input
- Don't rely on placeholder alone
- Indicate required fields

**3.3.3 Error Suggestion (Level AA):**

- Suggestions provided for correcting errors (when known)
- "Email must include @"
- "Password must be at least 8 characters"

**3.3.4 Error Prevention (Level AA):**

- For legal, financial, data submissions:
  - Reversible (can undo), OR
  - Checked (validation before submit), OR
  - Confirmed (review and confirm step)

## Principle 4: Robust

Content must work with current and future technologies.

### Guideline 4.1: Compatible

Maximize compatibility with assistive technologies.

**Success Criteria:**

**4.1.1 Parsing (Level A) - Deprecated in WCAG 2.2:**

- Valid HTML (no duplicate IDs, proper nesting)
- Modern browsers handle this

**4.1.2 Name, Role, Value (Level A):**

- For all UI components:
  - Name: Accessible label
  - Role: What it is (button, link, checkbox)
  - Value/State: Current state (checked, expanded)
- Use semantic HTML or ARIA

**Examples:**

```html
<!-- Semantic HTML (best) -->
<button>Submit</button>

<!-- Custom element needs ARIA -->
<div role="button" tabindex="0" aria-label="Submit">Submit</div>

<!-- Checkbox state -->
<input type="checkbox" checked aria-checked="true" />
```

**4.1.3 Status Messages (Level AA) - WCAG 2.1:**

- Status messages can be programmatically determined
- Announced by screen readers without moving focus
- Use ARIA live regions: `aria-live="polite"` or `role="status"`
- Examples: "5 items in cart," "Saving complete," "Error occurred"

## Conformance Levels

**Level A (Minimum):**

- Essential accessibility
- Major barriers removed
- Still significant limitations

**Level AA (Target):**

- Addresses most common barriers
- Standard for legal compliance
- Reasonable to achieve

**Level AAA (Enhanced):**

- Highest level
- Not always possible for all content
- Some criteria very difficult
- Not typically required legally

**Most organizations target Level AA.**

## WCAG 2.2 New Success Criteria

**2.4.11 Focus Not Obscured (Minimum) - AA:**

- Focused element not entirely hidden by author-created content
- Sticky headers shouldn't hide focused element

**2.4.12 Focus Not Obscured (Enhanced) - AAA:**

- Focused element not obscured at all

**2.4.13 Focus Appearance - AAA:**

- Focus indicator meets minimum size and contrast
- More specific than 2.4.7

**2.5.7 Dragging Movements - AA:**

- Functionality using dragging has single-pointer alternative
- Drag-to-reorder: Also provide up/down buttons

**2.5.8 Target Size (Minimum) - AA:**

- Click/touch targets at least 24×24 CSS pixels
- Exceptions: Inline links, essential size, controlled by user agent

**3.2.6 Consistent Help - A:**

- Help mechanism in same relative order across pages

**3.3.7 Redundant Entry - A:**

- Information previously entered can be auto-populated or selected
- Don't make users re-enter same data

**3.3.8 Accessible Authentication (Minimum) - AA:**

- Cognitive function test (CAPTCHA, memorization) not required, unless alternative provided
- Support password managers

**3.3.9 Accessible Authentication (Enhanced) - AAA:**

- No cognitive function test required

## Testing for WCAG Compliance

**Automated Tools (catch ~30-50%):**

- Browser extensions: axe DevTools, WAVE, Lighthouse
- Figma plugins: Stark
- CI/CD: axe-core, Pa11y

**Manual Testing (essential):**

- Keyboard navigation
- Screen reader testing
- Zoom/resize text testing
- Color blind simulation
- User testing with people with disabilities

**Process:**

1. Automated scan (find obvious issues)
2. Manual testing (keyboard, screen reader)
3. User testing (real users with disabilities)
4. Remediation
5. Re-test
6. Ongoing monitoring

## Accessibility Statement

Document your accessibility efforts:

**Include:**

- Conformance level (e.g., "WCAG 2.1 Level AA")
- Known issues
- Contact for feedback
- Date of last review

**Example:**
"We aim to conform to WCAG 2.1 Level AA. We welcome feedback: accessibility@company.com"

## Related Topics

- [[Accessibility]]
- [[Keyboard-Navigation]]
- [[Contrast-and-Accessibility]]
- [[Screen-Readers]]
- [[Animation-Principles]] (prefers-reduced-motion)
- [[Forms]]
- [[Usability-Testing]]

## Tools & Resources

**Official WCAG Resources:**

- WCAG 2.1: w3.org/WAI/WCAG21/quickref/ (quick reference)
- Understanding WCAG 2.1: w3.org/WAI/WCAG21/Understanding/
- How to Meet WCAG: w3.org/WAI/WCAG21/quickref/

**Testing Tools:**

- axe DevTools (browser extension)
- WAVE (browser extension)
- Lighthouse (Chrome DevTools)
- Stark (Figma plugin)

**Contrast Checkers:**

- WebAIM Contrast Checker
- Contrast Ratio by Lea Verou
- Figma: Stark, A11y plugin

**Screen Readers:**

- NVDA (Windows, free)
- JAWS (Windows, paid)
- VoiceOver (Mac/iOS)
- TalkBack (Android)

**Learning:**

- WebAIM (webaim.org)
- A11y Project (a11yproject.com)
- Deque University (courses)
- Microsoft Inclusive Design toolkit

## Practice Exercises

1. **WCAG Audit:** Take a website (yours or popular site). Check against WCAG 2.1 Level AA checklist. Use axe DevTools. Find 10 violations. Document which success criteria they violate. Propose fixes.

2. **Contrast Check:** Review a design. Check all text and UI components for WCAG AA contrast (4.5:1 text, 3:1 UI). Use WebAIM Contrast Checker. Fix any failures.

3. **Keyboard Test:** Navigate a complex interface (e.g., multi-step form, dashboard) using keyboard only. Can you reach everything? Is focus visible? Is order logical? Document issues with reference to specific WCAG criteria (2.1.1, 2.4.3, 2.4.7).

4. **Alternative Text:** Find 10 images on a website. Evaluate the alt text. Does it meet WCAG 1.1.1? Is it descriptive, concise, functional? Rewrite poor alt text.

5. **Form Accessibility:** Evaluate a form against WCAG 3.3 (Input Assistance). Are labels present (3.3.2)? Are errors identified in text (3.3.1)? Are error suggestions provided (3.3.3)? Make improvements.

6. **Error Identification:** Design an error state for a form field (e.g., invalid email). Ensure it meets: 1.4.1 (color not alone), 3.3.1 (text identification), 3.3.3 (suggestion). Include icon + color + text message.

## Further Reading

- **WCAG 2.1 Guidelines** (w3.org/WAI/WCAG21) - Official standard
- **"Web Accessibility" by Jenny Craven & Mary Dixon** - Introduction to WCAG
- **"Accessibility for Everyone" by Laura Kalbag** - Practical guide
- **"Inclusive Design Patterns" by Heydon Pickering** - Code examples
- WebAIM articles (webaim.org) - In-depth explanations
- A11y Project checklist (a11yproject.com/checklist)
- Deque University - WCAG training courses
- Understanding WCAG 2.1 (w3.org/WAI/WCAG21/Understanding/) - Official explanations
