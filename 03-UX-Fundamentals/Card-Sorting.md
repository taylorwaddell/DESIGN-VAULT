# Card Sorting

## Introduction

Card sorting is a user research method that reveals how people naturally categorize and group information. Participants organize topics (written on physical or digital cards) into categories that make sense to them, then label those categories in their own words. This simple yet powerful technique uncovers users' [[Mental Models]]—the internal frameworks they use to understand and organize information—providing invaluable insights for designing intuitive [[Information-Architecture]].

Card sorting is particularly effective because it prioritizes user thinking over designer assumptions. Instead of imposing a structure and hoping it works, designers observe how users actually group content, discovering patterns, unexpected associations, and language that resonates. These insights directly inform [[Sitemaps]], navigation labels, and content organization, creating structures that feel natural and logical because they're based on how users think, not how designers think.

The method is versatile, working for websites, apps, intranets, or any system with multiple content items that need organizing. It can be conducted in-person or remotely, with physical cards or digital tools, early in the design process (open card sort for discovery) or later (closed card sort for validation). When combined with [[Tree Testing]], card sorting becomes part of a comprehensive approach to creating findable, usable information architectures.

## Learning Objectives

By mastering Card Sorting, you will be able to:

- Conduct open, closed, and hybrid card sorting studies
- Prepare appropriate card sets for different research goals
- Recruit and guide participants through card sorting sessions
- Analyze card sorting data to identify patterns and consensus
- Translate card sorting results into actionable IA decisions
- Choose between in-person and remote card sorting methods
- Use card sorting tools effectively
- Combine card sorting with other IA research methods

## Key Knowledge Points

### Card Sorting Fundamentals

- [[Card Sorting]]

  - Research method for understanding how users categorize information
  - Participants group items (cards) into categories
  - Reveals [[Mental Models]] and natural groupings
  - Informs [[Information-Architecture]], [[Sitemaps]], [[Navigation]]

- **When to Use Card Sorting:**

  - Designing new IA (what structure makes sense?)
  - Redesigning existing IA (is there a better way?)
  - Deciding what to call categories (what labels do users use?)
  - Resolving team disagreements about structure
  - Understanding how different user groups think about content

- **Benefits:**
  - User-centered (based on real mental models)
  - Efficient (30-60 min per session)
  - Cost-effective
  - Reveals unexpected groupings
  - Generates user language for labels
  - Builds team consensus (data-driven decisions)

### Types of Card Sorting

- [[Open Card Sort]]

  - Participants create their own categories
  - No predefined groups
  - **Process:**
    1. Give participants cards
    2. "Group these in a way that makes sense to you"
    3. "Label each group"
  - **When to use:** Early discovery, new IA, understanding mental models
  - **Output:** Category names, groupings, patterns

- [[Closed Card Sort]]

  - Categories are predefined
  - Participants sort cards into given categories
  - **Process:**
    1. Give participants cards and category names
    2. "Put each card into the category where you'd expect to find it"
  - **When to use:** Validate existing IA, test proposed structure
  - **Output:** Agreement scores, misplaced cards, problem areas

- [[Hybrid Card Sort]]
  - Combines both approaches
  - Predefined categories + option to create new ones
  - **Process:**
    1. Provide some categories
    2. Allow participants to create additional categories if needed
  - **When to use:** Testing a partial structure, allowing flexibility

### Planning a Card Sort

- [[Define Goals]]

  - What do you need to learn?
  - Examples:
    - "How should we group 50 product categories?"
    - "Do users understand our proposed navigation labels?"
    - "Where would users expect to find Feature X?"

- [[Select Content Items (Cards)]]

  - **What goes on cards:**
    - Page titles, features, content topics, products
    - Use actual names from [[Content Inventory]]
  - **How many cards:**
    - 30-60 cards typical (sweet spot: 40-50)
    - Fewer than 30: Not enough to see patterns
    - More than 60: Cognitive overload
  - **Card selection:**
    - Include most important content
    - Include ambiguous items (where disagreement exists)
    - Exclude obvious items (rarely sorted differently)
    - Balance: Not all categories need equal items

- [[Card Content Guidelines]]

  - Clear, concise labels (2-5 words)
  - Consistent level of specificity
  - Avoid overlapping meanings
  - Use user language (not jargon)
  - One concept per card

- [[Participant Recruitment]]
  - **Who:** Representative users (match target audience)
  - **How many:**
    - **15-30 participants** (industry standard)
    - Pattern saturation around 15-20
    - More participants = more confidence
    - Can segment by user type if groups differ
  - See [[UX-Research]] (recruitment)

### Conducting Card Sorting

**In-Person Card Sorting:**

- **Materials:**

  - Physical cards (index cards or printed labels)
  - Large table or wall space
  - Blank cards for category labels
  - Camera to photograph results

- **Process:**

  1. **Intro (5 min):** Explain purpose, think-aloud encouraged
  2. **Familiarization (5 min):** Participant reviews all cards
  3. **Sorting (20-30 min):** Participant groups cards
  4. **Labeling (5-10 min):** Participant labels each group
  5. **Debrief (5 min):** Ask about difficult decisions, rationale

- **Facilitator Role:**
  - Observe, don't influence
  - Note hesitations, comments
  - Ask clarifying questions: "Why did you put these together?"
  - Photograph final layout

**Remote Card Sorting:**

- **Tools:**

  - [[Optimal Workshop]] (OptimalSort) - Industry standard
  - [[UserZoom]]
  - [[UsabilityHub]]
  - [[Miro]] (for facilitated remote sessions)

- **Benefits:**

  - Scalable (many participants simultaneously)
  - Geographic diversity
  - Lower cost (no travel, venue)
  - Built-in analysis

- **Limitations:**
  - Can't probe deeply (unless moderated)
  - Miss non-verbal cues
  - Technology barriers for some users

**Moderated vs Unmoderated:**

- [[Moderated Card Sort]]

  - Researcher present (in-person or video call)
  - Can ask questions, probe reasoning
  - Think-aloud protocol
  - Richer qualitative insights

- [[Unmoderated Card Sort]]
  - Participants complete alone
  - Quick, scalable
  - Less qualitative depth
  - Good for large samples

### Analyzing Card Sorting Results

**Quantitative Analysis:**

- [[Agreement Score]]

  - How often participants put two cards in same group
  - **Formula:** (# of times paired) / (# of participants)
  - High agreement (>70%): Strong pattern, confident grouping
  - Low agreement (<40%): Unclear, may need separate category or better labeling

- [[Similarity Matrix]]

  - Shows which cards are most often grouped together
  - Heatmap visualization
  - Tools generate this automatically

- [[Dendrogram]]

  - Tree diagram showing clustering
  - Visualizes relationships and hierarchy
  - Tools like Optimal Workshop generate this

- [[Popular Category Names]]
  - What labels did users create (open sort)?
  - Count frequency of terms
  - Informs navigation labels

**Qualitative Analysis:**

- [[Patterns]]

  - What groupings occurred most often?
  - What surprises emerged?
  - What did participants struggle with?

- [[Outliers]]

  - Cards that went in many different places
  - May indicate:
    - Card is ambiguous (rewrite)
    - Belongs in multiple places (tag it)
    - Needs its own category
    - Should be removed

- [[Participant Comments]]
  - Reasoning for decisions
  - Confusion or hesitation
  - Alternative labelings considered

**Synthesis:**

- [[Create Groupings]]

  - Based on high-agreement pairs
  - Form categories where cards were frequently grouped
  - Aim for 5-9 top-level categories

- [[Label Categories]]

  - Use language from participants (open sort)
  - Test labels with [[Tree Testing]] or closed card sort
  - Prefer user terms over internal jargon

- [[Build Sitemap]]
  - Translate groupings into hierarchy
  - See [[Sitemaps]]

### Card Sorting Best Practices

- **Card Preparation:**

  - Review cards with team before testing
  - Pilot test with 1-2 participants
  - Remove or rewrite confusing cards

- **Instructions:**

  - Clear, simple directions
  - "Group these in a way that makes sense to _you_"
  - No right or wrong answers
  - Emphasize thinking aloud

- **Avoid Leading:**

  - Don't suggest groupings
  - Don't show disapproval of choices
  - Stay neutral

- **Allow Flexibility:**

  - Participants can change their mind
  - No required number of groups
  - Cards can be "ungroupable" (create "I don't know" pile)

- **Combine with Other Methods:**
  - [[User-Interviews]] (understand context)
  - [[Tree Testing]] (validate resulting structure)
  - [[Usability-Testing]] (test final IA)

### Common Pitfalls

- **Too Many Cards:**

  - Overwhelming, participant fatigue
  - Solution: 40-60 max

- **Too Few Participants:**

  - Unreliable patterns
  - Solution: Aim for 15-30

- **Cards at Different Levels:**

  - Mixing high-level categories with specific items
  - Example: "Shoes" and "Nike Air Max 90" on same card set
  - Solution: Keep cards at same level of specificity

- **Biased Cards:**

  - Card names suggest groupings
  - Solution: Neutral, clear names

- **Ignoring Results:**
  - Collecting data but not using it
  - Solution: Share findings, involve team in synthesis

### From Card Sort to IA

**Typical Workflow:**

1. **Card Sort (Open):** Discover how users group content
2. **Analysis:** Identify patterns, create proposed IA
3. **[[Sitemap]] Creation:** Document structure
4. **Card Sort (Closed) or [[Tree Testing]]:** Validate structure
5. **Iteration:** Refine based on validation
6. **[[Wireframing]]:** Design navigation and layouts
7. **[[Usability-Testing]]:** Test with real prototypes

### Example Scenario

**Goal:** Design IA for e-commerce clothing site

**Cards (50):**

- T-Shirts, Jeans, Dresses, Sneakers, Boots, Jackets, Hoodies, etc.

**Open Card Sort (20 participants):**

- **Results:**
  - Most grouped by product type (Tops, Bottoms, Shoes, Outerwear)
  - Some grouped by gender (Men's, Women's)
  - Some grouped by occasion (Casual, Formal, Athletic)

**Synthesis:**

- **Primary structure:** Product type (matches strong consensus)
- **Filters:** Gender, occasion, brand (for secondary navigation)

**Closed Card Sort (Validation):**

- Test: Can users correctly place 50 products into: Tops, Bottoms, Shoes, Outerwear, Accessories?
- **Results:** 85% agreement → Good structure

**Outcome:** [[Sitemap]] with product-type hierarchy and gender/occasion filters

## Related Topics

- [[Information-Architecture]]
- [[Sitemaps]]
- [[Tree Testing]]
- [[Mental Models]]
- [[User-Research]]
- [[Navigation Design]]
- [[Taxonomy]]
- [[Content Strategy]]

## Tools & Resources

**Card Sorting Tools:**

- [[Optimal Workshop]] (OptimalSort) - Industry standard, excellent analysis
- [[UserZoom]] - Remote research platform
- [[UsabilityHub]] - Simple, affordable
- [[Miro]] - For facilitated remote sessions
- **Physical:** Index cards, sticky notes, markers

**Books & Articles:**

- "Card Sorting: Designing Usable Categories" by Donna Spencer (definitive guide)
- Nielsen Norman Group: Card Sorting articles
- "A Practical Guide to Information Architecture" by Donna Spencer

## Practice Exercises

1. **Conduct Open Card Sort:** Choose a domain (e.g., recipe website, music streaming). Create 40 cards with content items. Conduct open card sort with 5 participants (physical or Optimal Workshop). Analyze for patterns. What categories emerged? What surprises?

2. **Analysis Practice:** Use Optimal Workshop's free demo data or sample data. Analyze dendrogram, similarity matrix, popular categories. What IA would you propose? Document in a [[Sitemap]].

3. **Closed Card Sort Validation:** Take your proposed IA from Exercise 1. Create closed card sort with the same 40 items and your proposed categories. Test with 5 new participants. What % agreement? Where did participants struggle? How would you revise?

4. **Card Creation:** Choose a complex website (e.g., university, government). Create 50 cards representing key pages/content. Justify your selections (why these 50?). What did you exclude and why?

5. **Comparison Study:** Conduct the same card sort with two user groups (e.g., beginners vs experts, young vs older). Do their [[Mental Models]] differ? How would you accommodate both groups in your IA?

6. **End-to-End Project:** Pick a product. Do: Content inventory (50 items) → Open card sort (10 people) → Analysis → [[Sitemap]] → [[Tree Testing]] (validate) → Revise. Document entire process with rationale for decisions.

## Further Reading

- "Card Sorting: Designing Usable Categories" by Donna Spencer (essential)
- "Information Architecture: For the Web and Beyond" (card sorting chapter)
- Nielsen Norman Group: Card Sorting guide
- Optimal Workshop: Card sorting best practices
- Boxes and Arrows: Card Sorting articles
