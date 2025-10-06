# Usability Heuristics

## Introduction

Usability heuristics are broad rules of thumb for evaluating user interface design quality. Jakob Nielsen's **10 Usability Heuristics** (1994) remain the most influential framework, providing a systematic lens for identifying usability problems without extensive user testing. These heuristics distill decades of research into actionable principles that catch 80% of usability issues through expert review alone.

Heuristics aren't rigid laws but guidelines grounded in human psychology and interaction patterns. They help designers make confident decisions ("Is this design learnable? Does it prevent errors? Does it provide feedback?") and provide a shared vocabulary for design critique. While user testing reveals _what_ goes wrong, heuristics help explain _why_ and suggest solutions.

Mastering heuristics transforms you from someone who notices "this feels off" to someone who can diagnose "this violates error prevention—users can't undo destructive actions" and prescribe specific fixes. They're essential for [[Design Critique]], [[Usability-Testing]] analysis, and building intuitive interfaces systematically.

## Learning Objectives

By mastering Usability Heuristics, you will be able to:

- Apply all **10 Nielsen-Norman Usability Heuristics** to evaluate designs
- Conduct [[Heuristic Evaluation]] to identify usability problems
- Use heuristics to guide design decisions proactively
- Communicate design rationale using heuristic principles
- Prioritize usability issues by severity
- Apply heuristics across platforms (web, mobile, desktop)
- Combine heuristics with [[Accessibility]] and [[Design-Principles]] for comprehensive evaluation

## Key Knowledge Points

### Nielsen's 10 Usability Heuristics

#### 1. Visibility of System Status

- [[Visibility of System Status]]
  - **Principle:** System should always inform users what's going on through timely, appropriate feedback
  - **Why it matters:** Reduces uncertainty, builds trust, prevents confusion
  - **Applications:**
    - [[Loading Indicators]] (spinners, progress bars)
    - [[System Feedback]] (save confirmation, upload progress)
    - [[Current Location]] indicators (breadcrumbs, active nav item)
    - [[Submission Feedback]] ("Email sent", "Order placed")
    - [[Hover States]] (showing interactivity)
    - [[Typing Indicators]] (someone is responding)
  - **Violations:** Silent actions, unclear state, missing feedback
  - **Related:** [[Affordances]], [[Micro-Interactions]]

#### 2. Match Between System and Real World

- [[Match Between System and Real World]]
  - **Principle:** Speak users' language with familiar words, phrases, concepts; follow real-world conventions
  - **Why it matters:** Reduces cognitive load, leverages existing mental models
  - **Applications:**
    - [[Natural Language]] ("Delete" not "Destroy record")
    - [[Familiar Metaphors]] (trash can, folder, shopping cart)
    - [[Logical Order]] (name fields before address in forms)
    - [[Cultural Conventions]] (checkmark = success, X = close)
    - [[Platform Conventions]] (follow iOS/Android guidelines)
  - **Violations:** Jargon, technical terms, illogical ordering
  - **Related:** [[Mental Models]], [[Information-Architecture]]

#### 3. User Control and Freedom

- [[User Control and Freedom]]
  - **Principle:** Provide "emergency exits"; support undo and redo
  - **Why it matters:** Users make mistakes; they need escape hatches
  - **Applications:**
    - [[Undo / Redo]] (Cmd+Z)
    - [[Cancel Buttons]] (exit without saving)
    - [[Back Navigation]] (return to previous screen)
    - [[Confirmation Dialogs]] (before destructive actions)
    - [[Edit / Delete Options]] (correct mistakes)
    - [[Clear All / Reset]]
  - **Violations:** No undo, no cancel, can't exit workflows
  - **Related:** [[Error Prevention]]

#### 4. Consistency and Standards

- [[Consistency and Standards]]
  - **Principle:** Follow platform and industry conventions; be consistent within product
  - **Why it matters:** Reduces learning curve, leverages prior knowledge
  - **Types:**
    - [[Internal Consistency]] (same action always works the same way)
    - [[External Consistency]] (platform conventions)
  - **Applications:**
    - [[Design-Systems]] (consistent components)
    - [[UI-Patterns]] (standard solutions)
    - [[Icon Consistency]] (trash can always means delete)
    - [[Interaction Consistency]] (links always blue/underlined)
    - [[Platform Guidelines]] (follow iOS HIG, Material Design)
  - **Violations:** Same action different results, inconsistent styling
  - **Related:** [[Design-Systems]], [[Style-Guides]]

#### 5. Error Prevention

- [[Error Prevention]]
  - **Principle:** Prevent problems from occurring in the first place
  - **Why it matters:** Better than good error messages
  - **Strategies:**
    - [[Constraints]] (disable invalid options)
    - [[Helpful Defaults]] (pre-select sensible options)
    - [[Confirmation Dialogs]] (before destructive actions: "Delete 145 items?")
    - [[Input Validation]] (prevent invalid data entry)
    - [[Inline Hints]] (format examples: (555) 123-4567)
    - [[Disable Submit]] until form valid
  - **Types:**
    - [[Slips]] (right intent, wrong action) → constraints, confirmation
    - [[Mistakes]] (wrong intent) → clear communication, helpful defaults
  - **Violations:** No guardrails, easy to make mistakes
  - **Related:** [[Inline Validation]], [[Accessibility]]

#### 6. Recognition Rather Than Recall

- [[Recognition Rather Than Recall]]
  - **Principle:** Minimize memory load by making objects, actions, options visible
  - **Why it matters:** Recognition easier than recall (multiple choice vs. fill-in-blank)
  - **Applications:**
    - [[Autocomplete]] (don't make users remember)
    - [[Recent Searches]] / [[History]]
    - [[Visible Navigation]] (vs. hidden hamburger)
    - [[Tooltips]] (remind what icons do)
    - [[Breadcrumbs]] (show where you are)
    - [[Auto-fill]] (remember previous entries)
    - [[Previews]] (show before committing)
  - **Violations:** Hidden features, no hints, forcing memorization
  - **Related:** [[Progressive Disclosure]], [[Affordances]]

#### 7. Flexibility and Efficiency of Use

- [[Flexibility and Efficiency of Use]]
  - **Principle:** Cater to both novice and expert users; allow customization
  - **Why it matters:** Accelerate workflows for experienced users without confusing beginners
  - **Applications:**
    - [[Keyboard Shortcuts]] (for power users)
    - [[Customization]] (rearrange dashboard, favorite features)
    - [[Bulk Actions]] (select multiple, act once)
    - [[Templates / Presets]]
    - [[Search]] (faster than clicking through menus)
    - [[Quick Actions]] / [[Jump To]]
    - [[Macros / Automation]]
  - **Violations:** One-size-fits-all, no shortcuts, can't customize
  - **Related:** [[Progressive Disclosure]], [[Advanced Features]]

#### 8. Aesthetic and Minimalist Design

- [[Aesthetic and Minimalist Design]]
  - **Principle:** Every element should serve a purpose; remove the unnecessary
  - **Why it matters:** Reduces cognitive load, highlights important information
  - **Applications:**
    - [[Progressive Disclosure]] (show only what's needed now)
    - [[White-Space]] (breathing room)
    - [[Visual Hierarchy]] (emphasize important, de-emphasize secondary)
    - [[Remove Clutter]] (every element earns its place)
    - [[Clear Information Architecture]]
  - **Not about:** Being minimal for minimalism's sake
  - **Violations:** Cluttered interfaces, decorative elements, everything prominent
  - **Related:** [[White-Space]], [[Visual Hierarchy]], [[Design-Principles]]

#### 9. Help Users Recognize, Diagnose, and Recover from Errors

- [[Help Users Recognize, Diagnose, and Recover from Errors]]
  - **Principle:** Error messages in plain language, precisely indicate problem, constructively suggest solution
  - **Why it matters:** Errors happen; good error handling turns frustration into resolution
  - **Applications:**
    - [[Error Messages]]
      - **Recognize:** Clear something went wrong (red color, icon)
      - **Diagnose:** Explain what happened (not "Error 402")
      - **Recover:** Suggest fix ("Password must be 8+ characters")
    - [[Inline Validation]] (catch errors early)
    - [[Error Summaries]] (list all errors)
    - [[Contextual Help]] (link to docs)
    - [[404 Pages]] (helpful, not dead-end)
  - **Violations:** Vague errors, no solution, technical jargon
  - **Related:** [[Error Prevention]], [[Accessibility]]

#### 10. Help and Documentation

- [[Help and Documentation]]
  - **Principle:** System should be usable without docs, but provide help when needed
  - **Why it matters:** Some tasks require explanation; help should be accessible
  - **Applications:**
    - [[Contextual Help]] (? icon, inline hints)
    - [[Tooltips]] (brief explanations)
    - [[Onboarding Tutorials]]
    - [[Help Center]] / [[Knowledge Base]]
    - [[Search in Help]] (easy to find answers)
    - [[Video Tutorials]]
    - [[Contact Support]] (when all else fails)
    - [[Empty States]] (explain feature before use)
  - **Best Practices:**
    - Task-oriented (not feature-oriented)
    - Searchable, concise
    - Concrete steps, examples
  - **Violations:** No help, hard-to-find help, outdated docs
  - **Related:** [[Onboarding]], [[Documentation]]

### Heuristic Evaluation Method

- [[Heuristic Evaluation]]
  - **Process:**
    1. **Preparation:** Define scope, user tasks, heuristics to use
    2. **Individual Review:** 3-5 evaluators independently review interface
    3. **Document Issues:** Note violations, affected heuristic, severity
    4. **Debrief:** Consolidate findings, prioritize
    5. **Report:** List issues with severity, recommendations
- [[Severity Ratings]]

  - **0 - Not a problem**
  - **1 - Cosmetic:** Fix if time permits
  - **2 - Minor:** Low priority fix
  - **3 - Major:** Important to fix, affects usability
  - **4 - Catastrophic:** Must fix before release (blocks tasks)

- **Benefits:**

  - Fast, cheap (vs. full usability testing)
  - Finds 75-80% of usability problems
  - No users needed
  - Can be done early (wireframes, mockups)

- **Limitations:**
  - Misses user-specific issues
  - Evaluator bias
  - Better with multiple evaluators (3-5 ideal)

## Related Topics

- [[Usability-Testing]]
- [[Accessibility]]
- [[Design-Principles]]
- [[UI-Components]]
- [[Affordances]]
- [[Micro-Interactions]]
- [[Error Prevention]]
- [[User-Flows]]

## Tools & Resources

- Nielsen Norman Group: Heuristics articles
- Usability.gov: Heuristic Evaluation guide
- Heuristic evaluation templates (checklists)
- "Don't Make Me Think" by Steve Krug

## Practice Exercises

1. **Heuristic Audit:** Choose 3 apps/websites. Evaluate each against all 10 heuristics. Document violations and severity.

2. **Heuristic Application:** Design a checkout flow explicitly addressing each of the 10 heuristics. Annotate how you addressed each.

3. **Error Message Redesign:** Find 10 bad error messages. Rewrite following heuristic #9 (recognize, diagnose, recover).

4. **Comparative Analysis:** Take one interface. Create two versions: one that maximally violates heuristics, one that maximally adheres. Present side-by-side.

5. **Heuristic Evaluation Practice:** Team exercise: 3-5 people independently evaluate the same interface. Consolidate findings. Compare what each person caught.

## Further Reading

- "Usability Engineering" by Jakob Nielsen
- Nielsen Norman Group: 10 Usability Heuristics (article series)
- "Don't Make Me Think" by Steve Krug
- "The Design of Everyday Things" by Don Norman
- Usability.gov: Heuristic Evaluation documentation
