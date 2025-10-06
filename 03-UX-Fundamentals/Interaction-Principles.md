# Interaction Principles

## Introduction

Interaction principles are the fundamental guidelines that govern how users and systems communicate through interfaces. They define the rules for creating interfaces that are intuitive, responsive, and aligned with human expectations. While [[Design-Principles]] address visual composition and [[Usability-Heuristics]] provide evaluation criteria, interaction principles specifically focus on the dynamic, behavioral aspects of design—how things respond, transition, and feel during use.

These principles draw from psychology, human factors research, and decades of interface design practice. They explain why certain interactions feel natural (direct manipulation, immediate feedback) while others feel frustrating (delays, unclear responses, broken expectations). Understanding interaction principles enables designers to create experiences that align with how humans think, perceive, and act—reducing [[Cognitive Load]], preventing errors, and making digital products feel responsive and alive.

Mastering interaction principles means internalizing concepts like [[Feedback]], [[Affordances]], [[Consistency]], [[Discoverability]], and [[Forgiveness]]. These aren't arbitrary rules but patterns grounded in human cognition and behavior. They guide decisions about animation timing, button states, error handling, navigation structure, and countless micro-moments that collectively determine whether an interface feels delightful or difficult.

## Learning Objectives

By mastering Interaction Principles, you will be able to:

- Apply core interaction principles to design decisions
- Create interfaces with appropriate [[Feedback]] and [[Response]]
- Design interactions that align with [[Mental Models]] and expectations
- Balance [[Efficiency]] for experts with [[Learnability]] for novices
- Implement [[Error Prevention]] and [[Error Recovery]] strategies
- Design for [[Discoverability]] without sacrificing simplicity
- Create consistent interaction patterns across a product
- Understand when and how to apply [[Progressive Disclosure]]

## Key Knowledge Points

### Core Interaction Principles

#### 1. Feedback

- [[Feedback]]
  - System communicates what's happening
  - Every action should have a visible reaction
  - Confirms that system received input
  - Shows system state and progress

**Types of Feedback:**

- **Immediate:** Button press animation (<100ms)
- **Continuous:** Progress bar during loading
- **Completion:** Success confirmation after task
- **Error:** Clear indication when something fails

**Examples:**

- Button changes appearance when clicked
- Loading spinner while data fetches
- Form field highlights when focused
- Sound when sending message
- Haptic vibration on phone

**Why It Matters:**

- Reduces uncertainty
- Prevents repeated actions
- Builds trust
- See [[Usability-Heuristics]] (Visibility of System Status)

#### 2. Response Time

- [[Response Time]]
  - How quickly system reacts to user input
  - Perceived performance often more important than actual

**Jakob Nielsen's Response Time Limits:**

- **0.1 second:** Feels instantaneous
- **1 second:** User's flow of thought uninterrupted
- **10 seconds:** Limit of attention
- Beyond 10 seconds: User will switch tasks

**Design Implications:**

- <100ms: No feedback needed (feels instant)
- 100ms-1s: Subtle feedback (button state change)
- 1s-10s: Progress indicator (spinner, progress bar)
- > 10s: Progress indicator + time estimate + option to cancel

**Perceived Performance Techniques:**

- [[Optimistic UI]]: Show result immediately, sync later
- [[Skeleton Screens]]: Show layout while content loads
- [[Progressive Loading]]: Show content as it arrives
- [[Animation]]: Smooth transitions feel faster than abrupt changes

#### 3. Consistency

- [[Consistency]]
  - Similar things work in similar ways
  - Reduces learning curve
  - Builds predictability

**Types of Consistency:**

- [[Internal Consistency]]

  - Within your product
  - Same button style, same navigation pattern
  - Predictable behavior across features

- [[External Consistency]]

  - With platform conventions
  - iOS apps behave like iOS apps
  - Web apps follow web patterns
  - See [[Platform Conventions]]

- [[Functional Consistency]]
  - Same action has same result everywhere
  - Delete always deletes
  - Save always saves

**Examples:**

- Primary buttons always blue, always on right
- Back button always in same location
- Swipe gestures work same way throughout app

**Why It Matters:**

- Reduces [[Cognitive Load]]
- Leverages learned patterns
- See [[Usability-Heuristics]] (Consistency and Standards)

#### 4. Affordances

- [[Affordances]]
  - Design communicates how to interact
  - Buttons look pressable
  - Links look clickable
  - Sliders look draggable
  - See [[Affordances]] (dedicated topic)

**Examples:**

- Raised buttons (shadows) suggest pressing
- Underlined blue text suggests clicking
- Handle icon suggests dragging
- Input fields have cursor and borders

**Why It Matters:**

- Self-explanatory interfaces
- Reduces need for instructions
- Intuitive interactions

#### 5. Direct Manipulation

- [[Direct Manipulation]]
  - Interact with objects themselves, not through intermediaries
  - Visual representation of actions
  - Immediate, visible feedback
  - Reversible actions

**Examples:**

- Drag file to trash (vs "Delete" menu command)
- Pinch to zoom (vs zoom buttons)
- Drag slider (vs entering numbers)
- Rearrange items by dragging (vs up/down buttons)

**Benefits:**

- Intuitive (maps to physical world)
- Engaging and satisfying
- Reduces errors (see what you're doing)
- Easy to learn

**Challenges:**

- Touch targets must be large enough
- May not work for all interactions (complex commands)
- Discoverability (hidden gestures)

#### 6. Discoverability

- [[Discoverability]]
  - Users can find features without instruction
  - Balance: visible enough to find, unobtrusive enough to not clutter

**Techniques:**

- [[Visual Hierarchy]]: Important features prominent
- [[Onboarding]]: Guide first-time users
- [[Contextual Help]]: Tooltips, hints
- [[Progressive Disclosure]]: Reveal advanced features gradually
- [[Search]]: Let users find what they need

**Challenge:**

- Too obvious = cluttered
- Too hidden = undiscoverable
- Balance depends on:
  - Frequency of use (frequent → visible)
  - Importance (critical → visible)
  - Target user expertise (novices need guidance)

#### 7. Learnability

- [[Learnability]]
  - How quickly new users can accomplish tasks
  - First-time experience matters

**Design for Learnability:**

- [[Intuitive Patterns]]: Leverage familiar conventions
- [[Clear Labels]]: Avoid jargon
- [[Onboarding]]: Teach key features
- [[Helpful Defaults]]: Pre-fill forms, suggest options
- [[Forgiving Errors]]: Easy undo, clear recovery

**Measure Learnability:**

- Time to first success
- Number of errors
- Need for help/support

#### 8. Efficiency

- [[Efficiency]]
  - How quickly experienced users can accomplish tasks
  - Minimize steps, optimize for experts

**Techniques:**

- [[Keyboard Shortcuts]]: For power users
- [[Batch Actions]]: Act on multiple items at once
- [[Smart Defaults]]: Remember preferences
- [[Autocomplete]]: Predict and suggest
- [[Recently Used]]: Quick access to frequent items

**Balance with Learnability:**

- Novices need guidance → Learnability
- Experts want speed → Efficiency
- Solution: [[Progressive Disclosure]] (simple by default, power features accessible)

#### 9. Error Prevention

- [[Error Prevention]]
  - Design to avoid errors before they happen
  - Better than good error messages

**Techniques:**

- [[Constraints]]: Disable invalid options (gray out, hide)
- [[Validation]]: Check input as user types (real-time feedback)
- [[Confirmation]]: "Are you sure?" for destructive actions
- [[Helpful Defaults]]: Pre-select sensible options
- [[Clear Instructions]]: Guidance before errors occur

**Examples:**

- Date picker (can't enter invalid date)
- Disabled "Submit" until form valid
- Confirm before deleting account
- Show password requirements upfront

See [[Usability-Heuristics]] (Error Prevention)

#### 10. Error Recovery

- [[Error Recovery]]
  - When errors happen, make recovery easy
  - Graceful, helpful, not punishing

**Good Error Recovery:**

- [[Clear Error Messages]]: What happened? Why? How to fix?
- [[Preserve User Input]]: Don't clear form on error
- [[Undo]]: Reverse destructive actions
- [[Inline Validation]]: Show errors next to problematic field
- [[Helpful Suggestions]]: "Did you mean...?"

**Example Error Message:**

- ❌ "Error 403"
- ✅ "Email address is invalid. Please check for typos and try again."

See [[Usability-Heuristics]] (Error Recognition and Recovery)

#### 11. Progressive Disclosure

- [[Progressive Disclosure]]
  - Show only what's needed now
  - Reveal complexity gradually as needed
  - Reduces overwhelming interfaces

**Techniques:**

- [[Expand/Collapse Sections]]: Hide advanced options
- [[Wizard / Steps]]: One step at a time
- [[Tooltips]]: Details on hover
- [[Advanced Mode Toggle]]: Simple by default, power mode available

**Examples:**

- Gmail: "Show more options" in compose
- iPhone settings: Basic settings visible, advanced hidden in submenus
- Forms: Required fields first, optional later or hidden

**Benefits:**

- Reduces [[Cognitive Load]]
- Approachable for novices
- Power available for experts

#### 12. Forgiveness

- [[Forgiveness]]
  - Easy to undo mistakes
  - Encourage exploration without fear

**Techniques:**

- [[Undo / Redo]]: Ctrl+Z everywhere possible
- [[Auto-Save]]: Don't lose work
- [[Confirmations]]: Before destructive actions
- [[Drafts]]: Save incomplete work
- [[Trash / Archive]]: Soft delete (recoverable)

**Examples:**

- Gmail: Undo send (5-second window)
- Photo editing: Non-destructive (always revert to original)
- Text editors: Version history

**Why It Matters:**

- Users feel safe to explore
- Reduces anxiety
- Encourages experimentation

#### 13. Constraints

- [[Constraints]]
  - Limit actions to valid options
  - Prevents errors
  - Guides user to correct path

**Types:**

- [[Physical Constraints]]: Can't fit wrong way (USB-C is reversible, finally!)
- [[Logical Constraints]]: Can't proceed without required info
- [[Semantic Constraints]]: Meaning guides action (red = stop/danger)
- [[Cultural Constraints]]: Conventions (checkmark = done)

**Examples in UI:**

- Disabled buttons (can't click)
- Date picker (can't select past dates for future events)
- Max character count visible
- Can't send empty message (send button disabled)

### Mental Models

- [[Mental Models]]
  - User's internal understanding of how system works
  - Shaped by experience with similar products
  - **Design goal:** Match or teach mental models

**Aligning with Mental Models:**

- Use familiar metaphors (folders, trash, desktop)
- Follow conventions (conventions exist for a reason)
- Provide clear conceptual model through design
- If introducing new model, teach it explicitly

**Example:**

- Mental model: "Folders contain files"
- Design: Visual folders users can open, drag files into
- Violating model: Folders that don't behave like folders (confusion)

### Conceptual Models

- [[Conceptual Models]]
  - Designer's explanation of how system works
  - Communicated through interface
  - Should match user's [[Mental Models]]

**Good Conceptual Model:**

- Consistent across product
- Clearly communicated
- Maps to user expectations

**Example: Email as Conversation (Gmail):**

- Conceptual model: Email threads = conversations
- Implementation: Group related emails, hide quoted text
- Aligns with mental model: "I'm having a conversation"

## Related Topics

- [[Usability-Heuristics]]
- [[Affordances]]
- [[Design-Principles]]
- [[Micro-Interactions]]
- [[Animation-Principles]]
- [[Accessibility]]
- [[Mental Models]]
- [[User-Flows]]

## Tools & Resources

**Books:**

- "The Design of Everyday Things" by Don Norman (foundational, mental models, affordances)
- "About Face: The Essentials of Interaction Design" by Alan Cooper (comprehensive interaction principles)
- "Designing Interfaces" by Jenifer Tidwell (pattern library with principles)
- "Microinteractions" by Dan Saffer (details of interaction design)

**Articles & Resources:**

- Nielsen Norman Group: Interaction Design articles
- Laws of UX (lawsofux.com) - Principles with examples
- Apple Human Interface Guidelines (interaction patterns)
- Material Design Guidelines (interaction principles)

## Practice Exercises

1. **Feedback Audit:** Analyze an app you use daily. Document feedback for 10 interactions: button presses, form submissions, errors, loading. Rate each: Immediate? Clear? Appropriate? What could improve?

2. **Response Time Evaluation:** Time 10 actions in a web app (search, save, load page, etc.). Categorize: <0.1s, 0.1-1s, 1-10s, >10s. Does feedback match response time (per Nielsen's guidelines)? Suggest improvements.

3. **Consistency Check:** Review a product's interface. Find 5 examples of consistency (buttons, navigation, terminology). Find 3 inconsistencies. Propose fixes.

4. **Error Prevention Design:** Design a form with 5 fields. Apply error prevention techniques: constraints (dropdowns for known options), validation (real-time feedback), clear instructions, helpful defaults. Show all states (empty, filling, error, valid).

5. **Progressive Disclosure:** Redesign a complex settings page (20+ options). Group by importance/frequency. Apply progressive disclosure: show 5 most-used options, hide rest behind "Advanced" section. Justify your choices.

6. **Forgiveness Feature:** Choose a destructive action (delete account, cancel subscription, remove file). Design the flow with forgiveness: confirmation, undo option, and grace period. What feedback does user receive at each step?

## Further Reading

- "The Design of Everyday Things" by Don Norman (essential)
- "About Face" by Alan Cooper (interaction design bible)
- "Designing Interfaces" by Jenifer Tidwell (patterns)
- "Microinteractions" by Dan Saffer (details matter)
- "Laws of UX" by Jon Yablonski (principles with science)
- Nielsen Norman Group: Interaction Design category (free articles)
- "100 Things Every Designer Needs to Know About People" by Susan Weinschenk (psychology)
