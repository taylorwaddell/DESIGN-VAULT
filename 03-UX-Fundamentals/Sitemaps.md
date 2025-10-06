# Sitemaps

## Introduction

A sitemap is a visual diagram that represents the hierarchical structure of a website or application—showing every page, screen, or content area and how they relate to each other. Think of it as an architectural blueprint or organizational chart for digital products: the homepage sits at the top, major sections branch below, and subsections and individual pages cascade further down. Sitemaps make the invisible information architecture tangible, turning abstract structure into concrete visual documentation.

Sitemaps serve multiple critical purposes. For designers and stakeholders, they provide a shared understanding of scope and structure before investing in detailed design. For developers, they clarify what needs to be built and how pieces connect. For content strategists, they show where content lives and highlight gaps or redundancies. A good sitemap answers questions like: "How many pages do we have?" "How deep is the navigation?" "Where does this feature belong?" "What's missing?"

Creating a sitemap is both analytical and strategic. It requires synthesizing insights from [[Content Inventory]], [[Card-Sorting]], [[User-Research]], and business requirements into a cohesive, logical structure. The sitemap becomes the foundation for [[Wireframing]], [[User-Flows]], and ultimately the entire product. It's one of the earliest artifacts in the design process—and one of the most referenced throughout.

## Learning Objectives

By mastering Sitemaps, you will be able to:

- Create clear, professional sitemaps that document site/app structure
- Determine appropriate hierarchy and depth for content organization
- Use standard sitemap notation and conventions
- Organize content based on [[User-Research]] and [[Mental Models]]
- Communicate structure to stakeholders, designers, and developers
- Validate sitemaps through [[Tree Testing]]
- Adapt sitemaps for different contexts (websites, apps, software)
- Iterate on structure based on testing and feedback

## Key Knowledge Points

### Sitemap Fundamentals

- [[Sitemap]]

  - Visual diagram of website/app structure
  - Shows hierarchy: parent-child relationships
  - Documents all pages/screens/sections
  - Created early in design process (after [[Information-Architecture]] research)

- **Purpose:**

  - **Scope definition:** What's included?
  - **Structural clarity:** How is content organized?
  - **Navigation planning:** What's the hierarchy?
  - **Communication:** Shared understanding across team
  - **Development planning:** What needs to be built?

- **When to Create:**
  - After [[Content Inventory]] and [[Content Audit]]
  - After [[Card-Sorting]] or [[User-Research]] about [[Mental Models]]
  - Before [[Wireframing]] (structure informs layout)
  - During redesigns (map current vs proposed structure)

### Sitemap Components

- [[Page/Screen]]

  - Represented as a box
  - Contains page/screen name
  - Sometimes includes:
    - Page ID or number
    - Template type
    - URL (for websites)
    - Notes or annotations

- [[Hierarchical Levels]]

  - **Level 1 (Top):** Homepage or app home
  - **Level 2:** Main sections (global navigation)
  - **Level 3:** Subsections
  - **Level 4+:** Individual pages/screens
  - **Best practice:** Aim for 3-4 levels max (minimize clicks)

- [[Connections]]

  - Lines connecting boxes show relationships
  - Vertical lines: parent-child (hierarchy)
  - Horizontal lines: siblings (same level)
  - Sometimes: cross-links (secondary connections)

- [[Annotations]]
  - Notes about specific pages
  - Examples:
    - "Requires login"
    - "Template: Product Page"
    - "New content needed"
    - "Links to external site"

### Sitemap Notation

**Standard Visual Conventions:**

- **Boxes:** Pages/screens
  - Rectangle with rounded corners (common)
  - Size often consistent (not representing importance)
- **Lines:** Relationships

  - Solid line: Direct connection
  - Dashed line: Conditional or secondary connection
  - Arrow: One-way relationship (less common)

- **Colors (optional):**

  - Different colors for page types
  - Example: Blue = content pages, Green = functionality, Orange = external

- **Grouping:**

  - Visual clustering of related pages
  - Background color or border to group sections

- **Numbering:**
  - Sequential numbering: 1.0, 1.1, 1.2, 2.0, 2.1...
  - Helps reference in documentation

### Types of Sitemaps

- [[Flat Sitemap]]

  - All pages on one level (rare)
  - Used for very simple sites (5-10 pages)
  - Example: Landing page portfolio

- [[Hierarchical Sitemap]]

  - Tree structure (most common)
  - Homepage → Sections → Subsections → Pages
  - Used for most websites, apps

- [[App Sitemap]]

  - Mobile/web app structure
  - Focus on screens and flows
  - May include:
    - Onboarding flow
    - Main app screens (tab bar items)
    - Settings and profile areas
    - Modal screens
  - Often combined with [[User-Flows]]

- [[Content Type Sitemap]]
  - Organized by content type
  - Example: Articles, Videos, Products, Events
  - Shows templates and taxonomies

### Creating a Sitemap: Process

**Step 1: Content Inventory**

- List all existing content (or planned content)
- See [[Information-Architecture]]

**Step 2: Grouping & Categorization**

- Use [[Card-Sorting]] results
- Apply [[Mental Models]] from [[User-Research]]
- Group related content

**Step 3: Define Hierarchy**

- Determine top-level sections (5-9 ideal)
- Decide breadth vs depth
- Consider [[Navigation]] implications

**Step 4: Label Categories**

- Clear, concise labels
- Use user language (not jargon)
- Consistent terminology
- See [[Information-Architecture]] (labeling)

**Step 5: Visual Layout**

- Start with Level 1 (homepage) at top
- Branch Level 2 below
- Continue downward for deeper levels
- Align horizontally for visual clarity

**Step 6: Review & Iterate**

- Stakeholder feedback
- [[Tree Testing]] to validate
- Adjust based on findings

**Step 7: Document**

- Add annotations, notes
- Version control
- Share with team

### Sitemap Best Practices

- [[Clarity Over Complexity]]

  - Keep it simple and readable
  - Don't cram too much info
  - Use multiple diagrams if needed (high-level + detailed)

- [[Consistent Formatting]]

  - Same box sizes
  - Aligned grid
  - Consistent spacing
  - Professional appearance

- [[Appropriate Detail]]

  - High-level sitemap: Major sections only
  - Detailed sitemap: Every page
  - Choose based on audience and purpose

- [[Breadth vs Depth Balance]]

  - Too broad: Overwhelming (15 top-level items)
  - Too deep: Too many clicks (7 levels down)
  - **Sweet spot:** 5-9 top-level, 3-4 levels deep

- [[Consider Navigation Constraints]]

  - Mobile: Limited menu space
  - Desktop: More room but still prioritize
  - Primary vs secondary navigation

- [[Version Control]]
  - Date versions
  - Track changes
  - Keep record of decisions

### Tools for Creating Sitemaps

- [[Figma]] / [[FigJam]]

  - Vector-based, flexible
  - Collaborative
  - Easy to share and iterate

- [[Miro]]

  - Whiteboard-style
  - Templates available
  - Great for workshops

- [[Lucidchart]]

  - Diagramming tool
  - Sitemap templates
  - Professional output

- [[Slickplan]]

  - Specialized sitemap tool
  - Auto-generates from structure
  - Export to various formats

- [[OmniGraffle]] (Mac only)

  - Professional diagramming
  - Templates and stencils

- [[Gloomaps]]

  - Free, simple sitemap tool
  - Fast for basic sitemaps

- **Low-Tech:**
  - Sticky notes on wall
  - Whiteboard sketches
  - Paper and pen

### Validating Your Sitemap

- [[Tree Testing]]

  - Test findability with text-only hierarchy
  - Users navigate through structure to find items
  - Validates labels and hierarchy
  - Tools: Optimal Workshop (Treejack)
  - See [[Tree Testing]], [[Information-Architecture]]

- [[First-Click Testing]]

  - "Where would you click to find X?"
  - Tests top-level navigation clarity
  - See [[Affordances]]

- [[Stakeholder Review]]

  - Present to team, clients, stakeholders
  - Walk through structure
  - Gather feedback on completeness, organization

- [[Card Sorting Validation]]
  - Closed card sort: Do users agree with your categories?
  - See [[Card-Sorting]]

### Common Sitemap Challenges

- **Too Many Top-Level Items:**

  - Overwhelming navigation
  - Solution: Group into fewer, broader categories

- **Too Deep (Too Many Levels):**

  - Users have to click many times
  - Solution: Flatten by elevating important content

- **Ambiguous Labels:**

  - Users don't understand what's in a section
  - Solution: [[Tree Testing]], user feedback, clearer terms

- **Overlapping Categories:**

  - Content could fit in multiple places
  - Solution: Redefine categories to be mutually exclusive
  - Or: Provide multiple pathways (contextual navigation)

- **Missing Content:**

  - Gaps discovered during sitemap creation
  - Solution: Content strategy to fill gaps

- **Scope Creep:**
  - Sitemap keeps growing
  - Solution: Prioritize, phase approach, [[MVP]]

### Sitemaps for Different Contexts

**Website Sitemap:**

- Homepage at top
- Main sections (About, Products, Blog, Contact, etc.)
- Subsections and pages
- Include utility pages (Privacy, Terms, etc.)

**Mobile App Sitemap:**

- Splash/Onboarding
- Main app screens (often tab bar: Home, Search, Profile, etc.)
- Secondary screens (accessible from main)
- Settings, help, modals
- May show authentication flow separately

**Software/SaaS Sitemap:**

- Dashboard/home
- Main modules/features
- Settings and admin areas
- Onboarding and empty states

**Multi-Platform Sitemap:**

- Show web, iOS, Android
- Highlight differences and shared structure

### From Sitemap to Wireframes

- Sitemap defines **what** pages/screens exist
- [[Wireframing]] defines **how** each page/screen looks and functions
- Sitemap informs:
  - Navigation design
  - Page templates needed
  - Content requirements
  - [[User-Flows]]

## Related Topics

- [[Information-Architecture]]
- [[Card-Sorting]]
- [[Tree Testing]]
- [[User-Flows]]
- [[Wireframing]]
- [[Navigation Design]]
- [[Content Strategy]]
- [[UX-Research]]

## Tools & Resources

**Sitemap Tools:**

- [[Figma]] / [[FigJam]] - Design tools with sitemap capabilities
- [[Miro]] - Collaborative whiteboard
- [[Lucidchart]] - Diagramming
- [[Slickplan]] - Dedicated sitemap tool
- [[OmniGraffle]] - Mac diagramming tool
- [[Gloomaps]] - Free, simple sitemaps

**Books:**

- "Information Architecture: For the Web and Beyond" by Rosenfeld, Morville, Arango
- "Don't Make Me Think" by Steve Krug
- "The Elements of User Experience" by Jesse James Garrett

## Practice Exercises

1. **Analyze Existing Site:** Choose a website (e.g., Airbnb, Spotify, Medium). Reverse-engineer its sitemap by exploring all pages. Document structure up to Level 4. Identify organizational scheme and navigation patterns.

2. **Create Sitemap from Scratch:** Design a sitemap for an online bookstore with: 10 genres, author pages, bestsellers, new releases, reviews, blog, user accounts, shopping cart, checkout. Decide on structure. Justify your hierarchy.

3. **App Sitemap:** Create a sitemap for a fitness tracking app with: onboarding, workout logging, nutrition tracking, progress dashboard, social feed, profile, settings. Show authentication flow separately.

4. **Before & After Redesign:** Take a poorly organized website. Create two sitemaps: current (messy) and proposed (improved). Explain your restructuring decisions based on [[Information-Architecture]] principles.

5. **Tree Test Validation:** Create a sitemap with 20+ pages. Convert to text-only tree. Write 10 findability tasks ("Where would you find your order history?"). Test with 5 users. Identify problem areas. Revise sitemap.

6. **Sitemap Workshop:** Facilitate a card sorting session with 5 participants using 30 content cards. Analyze results. Create sitemap based on user-generated groupings. Present to team with rationale.

## Further Reading

- "Information Architecture: For the Web and Beyond" (sitemap sections)
- "The Elements of User Experience" by Jesse James Garrett (includes IA & sitemaps)
- Nielsen Norman Group: Sitemaps articles
- Smashing Magazine: Sitemap tutorials
- "A Practical Guide to Information Architecture" by Donna Spencer
