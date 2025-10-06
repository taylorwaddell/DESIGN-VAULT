# UI Patterns

## Introduction

UI patterns are proven, reusable solutions to common interface design problems. They're the design equivalent of architectural blueprints—tested approaches that solve recurring challenges like "how should users search?", "how do we handle empty states?", or "what's the best way to show progress?". Patterns aren't copied blindly; they're understood, adapted, and applied contextually to create familiar, learnable interfaces.

The power of patterns lies in leveraging [[Convention Over Innovation]]—users already know how to use them. A shopping cart icon means "view cart," infinite scroll means "more content below," and a hamburger menu reveals navigation. Fighting established patterns means fighting learned behavior, creating unnecessary friction. Patterns enable designers to focus innovation energy on truly novel problems rather than reinventing solved interactions.

Mastering patterns requires both breadth (knowing many patterns exist) and depth (understanding when and why to use each). Pattern libraries like [[UI Patterns]], [[Mobbin]], and platform guidelines ([[Material Design]], [[Apple HIG]]) document these solutions, but understanding the underlying problems they solve makes you a better designer.

## Learning Objectives

By mastering UI Patterns, you will be able to:

- Identify and apply common [[Navigation Patterns]], [[Input Patterns]], [[Content Patterns]], and [[Social Patterns]]
- Understand [[When to Use Patterns]] vs. when to innovate
- Adapt patterns to different contexts while preserving their core benefits
- Use pattern libraries ([[Mobbin]], [[UI Patterns]], [[Pttrns]]) as research tools
- Recognize [[Anti-Patterns]] and avoid common design mistakes
- Document patterns for [[Design-Systems]] and [[Style-Guides]]
- Balance [[Familiarity]] with [[Differentiation]] in product design

## Key Knowledge Points

### Navigation Patterns

- [[Hamburger Menu]]

  - Collapsible icon (☰) revealing navigation
  - **Use when:** Many nav items, mobile space constrained
  - **Avoid when:** Few items that could fit in tab bar
  - **Trade-off:** Hides navigation (discoverability issue)

- [[Tab Bar]] (Bottom Navigation)

  - 3-5 persistent tabs at screen bottom
  - **Use when:** Mobile app with 3-5 core sections
  - **Best practices:** Current tab highlighted, icons + labels

- [[Sidebar Navigation]]

  - Vertical navigation panel (collapsible or fixed)
  - **Use when:** Desktop dashboards, admin panels, complex apps
  - **Types:** Push (shifts content), overlay (covers content)

- [[Sticky Header]]

  - Navigation bar fixed at top while scrolling
  - **Use when:** Users need constant access to navigation/actions
  - **Best practices:** Shrink on scroll (save space)

- [[Breadcrumbs]]

  - Path showing current location in hierarchy
  - **Use when:** Deep site hierarchy (e.g., e-commerce)
  - **Format:** Home > Category > Subcategory > Current

- [[Step Indicator]]
  - Visual progress through multi-step process
  - **Use when:** Onboarding, checkout, forms (3+ steps)
  - **Best practices:** Show total steps, current step, completed steps

### Search & Filter Patterns

- [[Search Bar]]

  - **Prominent Search:** Full-width, homepage (Google)
  - **Utility Search:** Top-right, smaller (e-commerce, docs)
  - **Best practices:** Auto-suggest, recent searches, clear button

- [[Filters & Sorting]]

  - **Filter Drawer:** Side panel with filter options
  - **Filter Pills:** Horizontal scrollable filter options
  - **Filter Modal:** Full-screen filters (mobile)
  - **Applied Filters:** Show active filters with remove option
  - **Best practices:** Show result count, clear all option

- [[Autocomplete / Type-ahead]]

  - Suggests results as user types
  - **Use when:** Large dataset, predictable queries
  - **Best practices:** Highlight matching text, keyboard navigation

- [[Faceted Search]]
  - Multiple filter dimensions (price, brand, color, etc.)
  - **Use when:** Large catalogs with multiple attributes
  - **Best practices:** Show available options, disable unavailable

### Input & Form Patterns

- [[Inline Validation]]

  - Immediate feedback as user types/exits field
  - **Best practices:** Success indicators (checkmark), error messages below field

- [[Progressive Disclosure]] (Forms)

  - Show fields conditionally based on previous answers
  - **Use when:** Long forms, conditional logic
  - **Best practices:** Smooth transitions, clear why field appeared

- [[Multi-Step Forms]]

  - Break long forms into digestible steps
  - **Use when:** 10+ fields, logical groupings
  - **Best practices:** Progress indicator, save progress, back button

- [[Input Masking]]

  - Format input automatically (phone: (555) 123-4567)
  - **Use when:** Formatted data (dates, phones, credit cards)
  - **Best practices:** Show format hint in placeholder

- [[Smart Defaults]]
  - Pre-fill likely values
  - **Examples:** Current date, user's country, "Remember me" checked
  - **Best practices:** Make obvious, easy to change

### Content Patterns

- [[Infinite Scroll]]

  - Load more content as user scrolls
  - **Use when:** Continuous feeds (social media, image galleries)
  - **Avoid when:** Users need footer, need to find specific item
  - **Best practices:** Loading indicator, handle scroll position

- [[Load More Button]]

  - Explicit button to fetch next page
  - **Use when:** Users need control, footer access important
  - **Best practices:** Show how many more items

- [[Pagination]]

  - Discrete pages with numbers
  - **Use when:** Search results, product listings, tables
  - **Best practices:** Show current page, total pages, first/last links

- [[Card Grid / Masonry Layout]]

  - Grid of cards (often varying heights)
  - **Use when:** Visual content (images, products, articles)
  - **Best practices:** Responsive columns, consistent spacing

- [[Feed / Timeline]]

  - Chronological or algorithmic content stream
  - **Use when:** Social media, activity logs, news
  - **Best practices:** Pull-to-refresh, clear timestamps

- [[Empty States]]

  - Screen shown when no content exists
  - **Elements:** Illustration, message, primary action
  - **Best practices:** Explain why empty, provide action to populate

- [[Zero Data State]]

  - First-time user experience (no history yet)
  - **Best practices:** Welcome message, tutorial, sample data

- [[Error States]]
  - 404 (not found), 500 (server error), offline
  - **Best practices:** Friendly message, explain what happened, provide action

### Data Display Patterns

- [[Data Table]]

  - Structured, sortable, filterable data
  - **Best practices:** Sortable columns, row selection, pagination/virtual scroll

- [[Data Visualization]]

  - Charts, graphs, dashboards
  - **Patterns:** Card layout, drill-down, comparison views
  - **Best practices:** Clear labels, legends, tooltips

- [[Stats / Metrics Display]]

  - Key numbers with context
  - **Patterns:** Number + trend (↑ 12%), sparklines, comparison bars
  - **Best practices:** Make numbers scannable, show change

- [[Timeline]]
  - Chronological events on vertical/horizontal line
  - **Use when:** History, process steps, project milestones
  - **Best practices:** Clear dates, visual hierarchy

### Action Patterns

- [[Undo / Redo]]

  - Reverse recent actions
  - **Best practices:** Toast with "Undo" button, keyboard shortcuts (Cmd+Z)

- [[Swipe Actions]]

  - Reveal actions by swiping list item (mobile)
  - **Common:** Swipe left = delete, swipe right = archive/complete
  - **Best practices:** Destructive actions require confirmation

- [[Long Press]]

  - Hold to reveal contextual menu
  - **Use when:** Touch interfaces, secondary actions
  - **Best practices:** Haptic feedback, visual hint

- [[Pull to Refresh]]

  - Pull down at top of list to reload
  - **Use when:** Dynamic content feeds
  - **Best practices:** Loading spinner, last updated timestamp

- [[Drag and Drop]]
  - Reorder items by dragging
  - **Use when:** Prioritization, organization, file upload
  - **Best practices:** Visual feedback (ghost element), drop zones

### Onboarding Patterns

- [[Splash Screen]]

  - Brief branded screen while app loads
  - **Best practices:** < 3 seconds, no fake loading

- [[Welcome Tour / Tutorial]]

  - Step-by-step intro to features
  - **Patterns:** Coach marks, modal overlays, interactive tutorial
  - **Best practices:** Skippable, 3-5 steps max, task-oriented

- [[Empty State Onboarding]]

  - First use guides shown in context
  - **Best practices:** Explain feature where it lives, CTA to start

- [[Progressive Onboarding]]
  - Teach features when first encountered (not all upfront)
  - **Best practices:** Contextual, just-in-time, dismissible

### Social Patterns

- [[User Profiles]]

  - Avatar, name, bio, stats, content
  - **Best practices:** Edit profile clearly accessible, privacy controls

- [[Follow / Subscribe]]

  - Opt-in to user's content
  - **States:** Not following, following, mutual
  - **Best practices:** Clear state, unfollow easily accessible

- [[Like / Favorite / Upvote]]

  - Express appreciation
  - **Variations:** Heart, star, thumbs up, +1
  - **Best practices:** Show count, animate interaction

- [[Comments / Reviews]]

  - User-generated feedback
  - **Patterns:** Threaded replies, voting, sorting (newest, top)
  - **Best practices:** Moderation, report abuse, edit/delete own

- [[Share / Invite]]
  - Spread content or invite users
  - **Patterns:** Share sheet (iOS), share dialog, referral code
  - **Best practices:** Pre-populated message, multiple channels

### Anti-Patterns (Avoid These)

- [[Dark Patterns]]

  - Manipulative design to trick users
  - **Examples:** Hidden unsubscribe, forced account creation, disguised ads
  - **Why bad:** Erodes trust, legally questionable

- [[Mystery Meat Navigation]]

  - Unclear icons without labels
  - **Why bad:** Users don't know what things do

- [[Carousel / Slider]]

  - Auto-rotating banners
  - **Why bad:** Low interaction rates, accessibility issues, missed content
  - **When okay:** Manual control, no auto-advance

- [[Modal Overload]]
  - Too many interrupting modals
  - **Why bad:** Annoying, disrupts flow

## Related Topics

- [[UI-Components]]
- [[Usability-Heuristics]]
- [[Information-Architecture]]
- [[User-Flows]]
- [[Design-Systems]]
- [[Accessibility]]
- [[Micro-Interactions]]

## Tools & Resources

- [[Mobbin]] (mobile pattern library with screenshots)
- [[UI Patterns]] (web patterns with examples)
- [[Pttrns]] (mobile UI patterns)
- [[Page Flows]] (user flow recordings)
- [[Really Good UX]] (curated examples)
- [[Screenlane]] (mobile design inspiration)
- Material Design: Patterns section
- Apple HIG: Patterns section

## Practice Exercises

1. **Pattern Library:** Browse Mobbin or UI Patterns for 1 hour. Document 20 patterns you hadn't seen before. Create visual reference.

2. **Pattern Audit:** Analyze your 5 most-used apps. Identify and document 10 patterns in each. Note variations.

3. **Pattern Selection:** For 5 common scenarios (e.commerce product list, social feed, onboarding, checkout, settings), propose 3 different pattern approaches. Evaluate pros/cons.

4. **Anti-Pattern Hunt:** Find 10 examples of dark patterns or UI anti-patterns in the wild. Screenshot and document why they're problematic.

5. **Pattern Application:** Choose 5 patterns and implement them in a practice project. Document when/why you used each.

## Further Reading

- "Designing Interfaces" by Jenifer Tidwell (comprehensive pattern catalog)
- "UI Patterns" website documentation
- Nielsen Norman Group: Pattern articles
- Material Design: Patterns documentation
- "Mobile Design Pattern Gallery" by Theresa Neil
