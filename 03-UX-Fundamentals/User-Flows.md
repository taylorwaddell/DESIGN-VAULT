# User Flows

## Introduction

A user flow is a visual representation of the complete path a user takes to accomplish a specific goal within a product—from entry point through each interaction, decision, and screen, to final outcome. It's the step-by-step journey documented: "User arrives at homepage → Clicks 'Sign Up' → Enters email → Verifies email → Creates profile → Reaches dashboard." User flows transform abstract user behavior into concrete, analyzable diagrams that reveal friction points, unnecessary steps, and opportunities for improvement.

User flows serve as both design tool and communication artifact. For designers, they force explicit thinking about every decision point, edge case, and error state—making the invisible visible. For developers, they clarify implementation requirements and logic. For stakeholders, they demonstrate how users will actually experience the product, not just what it looks like. A well-crafted user flow answers: "How does someone actually do this? What if something goes wrong? Where do they end up?"

Creating user flows requires understanding both user goals (from [[User-Research]]) and system capabilities (technical constraints). They sit between [[Information-Architecture]] (what content exists and how it's organized) and [[Wireframing]] (what each screen contains). User flows are task-focused—each flow centers on one job to be done, from "create an account" to "purchase a product" to "share a post." Together, these flows form the interactive skeleton of the product.

## Learning Objectives

By mastering User Flows, you will be able to:

- Create clear, comprehensive user flow diagrams using standard notation
- Identify and document entry points, steps, decisions, and outcomes
- Handle edge cases, errors, and alternate paths in flows
- Use user flows to identify friction and optimization opportunities
- Communicate flows effectively to designers, developers, and stakeholders
- Combine user flows with [[Wireframes]] and [[Prototypes]]
- Validate flows through [[Usability-Testing]]
- Differentiate between user flows, [[Task Flows]], and [[Journey-Maps]]

## Key Knowledge Points

### User Flow Fundamentals

- [[User Flow]]

  - Visual diagram of steps to complete a task
  - Documents: Screens, actions, decisions, outcomes
  - Task-specific (one flow per goal)
  - **Purpose:**
    - Understand user paths
    - Identify friction, dead ends
    - Plan screens and interactions
    - Align team on functionality
    - Spot missing states or features

- **When to Create User Flows:**

  - Early design (before [[Wireframing]])
  - When designing new features
  - Redesigning existing flows
  - Optimizing conversion funnels
  - Documenting complex interactions

- **Components of User Flows:**
  - [[Entry Points]]: Where users start
  - [[Steps]]: Actions users take
  - [[Screens/Pages]]: What users see
  - [[Decision Points]]: Branching based on choices or conditions
  - [[Actions]]: User or system actions
  - [[Outcomes]]: End states (success, failure, exit)

### User Flow Notation

**Standard Shapes:**

- [[Rectangle]]: Screen or page
  - Example: "Homepage", "Login Screen", "Checkout"
- [[Diamond]]: Decision point

  - Branching based on condition
  - Example: "Valid email?", "Has account?", "Cart empty?"
  - Usually 2+ exit paths (Yes/No, Option A/B/C)

- [[Oval/Rounded Rectangle]]: Action or entry point

  - User action: "Click 'Sign Up'", "Enter password"
  - System action: "Send email", "Process payment"
  - Entry: "User arrives from email link"

- [[Rectangle with folded corner]]: Document or data

  - Example: "Email sent", "Receipt generated"

- [[Arrows]]: Flow direction

  - Show path from one step to next
  - Label with action when helpful ("Yes", "No", "Submit")

- [[Terminator (Rounded ends)]]: Start or end
  - Example: "Start", "Success", "Error", "Exit"

**Color Coding (optional):**

- Screens (blue)
- Actions (green)
- Decisions (yellow)
- Errors (red)
- Improves readability for complex flows

### Types of Flows

- [[Task Flow]]

  - Single, linear path to complete a task
  - No branches or decisions
  - Assumes ideal scenario
  - Example: "Happy path" for checkout
  - **When to use:** Simple processes, initial planning

- [[User Flow]]

  - Multiple paths, decisions, and branches
  - Handles variations and edge cases
  - More realistic and comprehensive
  - Example: Login flow with forgot password, new user, errors
  - **When to use:** Real-world scenarios, complex interactions

- [[Wire Flow]]

  - Combines [[Wireframes]] with flow
  - Shows actual screen content + connections
  - Visual and functional
  - **When to use:** Detailed documentation, handoff to developers

- [[Journey Map]]
  - Broader, higher level than user flow
  - Includes emotions, pain points, touchpoints over time
  - Strategic view
  - See [[Journey-Maps]]
  - **Difference:** Journey map = experience over time; User flow = specific task steps

### Creating User Flows: Process

**Step 1: Define the Goal**

- What task is the user trying to complete?
- Examples:
  - "Sign up for account"
  - "Purchase a product"
  - "Reset password"
  - "Share a photo"

**Step 2: Identify Entry Points**

- Where does the flow start?
- Can be multiple entry points:
  - Homepage
  - Email link
  - Social media ad
  - App notification
  - Direct URL

**Step 3: Map the Happy Path**

- Ideal scenario with no errors
- Simplest path to success
- Example: User enters email → enters password → clicks login → reaches dashboard

**Step 4: Add Decision Points**

- Where does the path branch?
- Examples:
  - "Has account?" → Yes: Login, No: Sign up
  - "Payment successful?" → Yes: Order confirmed, No: Error message
  - "Email valid?" → Yes: Continue, No: Show error

**Step 5: Handle Edge Cases & Errors**

- What can go wrong?
- Examples:
  - Invalid input
  - Network errors
  - Expired sessions
  - Empty states
  - User exits mid-flow

**Step 6: Define Outcomes**

- Success states
- Error states
- Alternative completions
- Exit points

**Step 7: Review & Refine**

- Walk through each path
- Is anything missing?
- Can steps be reduced?
- Are errors handled gracefully?

### User Flow Best Practices

- [[One Flow, One Goal]]

  - Focus on single task per flow
  - Don't combine multiple goals
  - Create separate flows for different tasks

- [[Start with Happy Path]]

  - Map ideal scenario first
  - Then add variations and errors
  - Prevents getting lost in edge cases

- [[Be Comprehensive]]

  - Document all paths, including errors
  - Consider: First-time users, returning users, edge cases
  - Don't ignore unhappy paths

- [[Keep It Clear]]

  - Consistent notation
  - Readable labels
  - Logical layout (usually top-to-bottom or left-to-right)
  - Not too dense (use multiple diagrams if needed)

- [[Validate with Users]]

  - Test flows with [[Usability-Testing]]
  - Do users actually follow these paths?
  - Where do they get stuck?

- [[Collaborate]]
  - Review with developers (is it feasible?)
  - Review with stakeholders (does it meet requirements?)
  - Review with users (does it make sense?)

### Analyzing User Flows

- [[Identify Friction Points]]

  - Too many steps?
  - Unnecessary decisions?
  - Confusing labels or unclear next steps?
  - High drop-off (from analytics)?

- [[Optimize for Efficiency]]

  - Reduce steps where possible
  - Combine screens if appropriate
  - Pre-fill known information
  - Progressive disclosure (don't ask for everything upfront)

- [[Error Handling]]

  - Are errors handled gracefully?
  - Clear error messages?
  - Easy recovery path?
  - See [[Usability-Heuristics]] (Error Prevention, Error Recovery)

- [[Conversion Optimization]]
  - For conversion flows (sign-up, checkout):
    - Minimize required fields
    - Show progress
    - Offer guest checkout
    - Reduce anxiety (security badges, clear policies)

### Common Flow Scenarios

**Sign-Up Flow:**

- Entry: Homepage, landing page, app store
- Steps: Email → Password → Verify email → Onboarding
- Decisions: Has account? Email valid? Password strong?
- Outcomes: Account created, Email sent, Error

**Checkout Flow:**

- Entry: Cart
- Steps: Shipping info → Payment → Review → Confirm
- Decisions: Logged in? Valid payment? Stock available?
- Outcomes: Order confirmed, Payment failed, Out of stock

**Password Reset Flow:**

- Entry: Login screen ("Forgot password?")
- Steps: Enter email → Receive link → Reset password → Confirm
- Decisions: Email exists? Link expired?
- Outcomes: Password changed, Link invalid, Email not found

**Onboarding Flow:**

- Entry: After sign-up
- Steps: Welcome → Set preferences → Tutorial → First action
- Decisions: Skip tutorial? Enable notifications?
- Outcomes: Onboarded, Skipped, Exited

### From User Flows to Design

**User Flows inform:**

- [[Wireframes]]: What screens are needed? What content on each?
- [[Prototypes]]: How do screens connect? What interactions?
- [[Information-Architecture]]: What navigation is required?
- [[Content]]: What copy, labels, instructions are needed?
- [[Development]]: What logic, API calls, validations required?

**Workflow:**

1. User flow (document steps)
2. [[Wireframing]] (design each screen in flow)
3. [[Prototyping]] (make it interactive)
4. [[Usability-Testing]] (validate with users)
5. Iterate based on findings

### Tools for User Flows

- [[Figma]] / [[FigJam]]

  - Flexible, collaborative
  - Templates available
  - Can combine with wireframes (wire flows)

- [[Miro]]

  - Whiteboard for flows
  - Great for workshops
  - Templates and flowchart shapes

- [[Lucidchart]]

  - Diagramming tool
  - Flowchart-focused
  - Professional output

- [[Whimsical]]

  - Fast, simple
  - Built for flows and wireframes

- [[Draw.io]]

  - Free, open-source
  - Desktop or web

- [[OmniGraffle]] (Mac)

  - Professional diagramming
  - Stencils for flows

- **Low-Tech:**
  - Whiteboard + markers
  - Sticky notes
  - Paper + pen

### User Flows vs Other Artifacts

- **User Flow vs [[Task Flow]]:**

  - Task flow: Single path, no branches
  - User flow: Multiple paths, decisions, edge cases

- **User Flow vs [[Journey Map]]:**

  - Journey map: Broad, emotional, strategic (days/weeks/months)
  - User flow: Narrow, functional, tactical (minutes)

- **User Flow vs [[Sitemap]]:**

  - Sitemap: All content, hierarchy
  - User flow: Specific task path through content

- **User Flow vs [[Wireframe]]:**
  - Wireframe: What's on each screen
  - User flow: How screens connect

## Related Topics

- [[Journey-Maps]]
- [[Wireframing]]
- [[Information-Architecture]]
- [[Sitemaps]]
- [[Prototyping]]
- [[Usability-Testing]]
- [[Interaction-Design]]
- [[UX-Research]]

## Tools & Resources

**Flow Tools:**

- [[Figma]] / [[FigJam]]
- [[Miro]]
- [[Whimsical]]
- [[Lucidchart]]
- [[Draw.io]]
- [[OmniGraffle]]

**Templates:**

- Figma Community (search "user flow templates")
- Miro templates
- Flowchart stencils

**Books:**

- "The User's Journey" by Donna Lichaw (journey mapping + flows)
- "Mapping Experiences" by James Kalbach
- "Don't Make Me Think" by Steve Krug (touches on flows)

## Practice Exercises

1. **Simple Flow:** Create a user flow for "liking a post on social media." Include: entry (seeing post), action (clicking like), decision (logged in?), outcomes (liked, redirected to login). Use standard notation.

2. **Complex Flow:** Design a complete sign-up flow with: email/password entry, email verification, optional profile setup, onboarding. Include all decision points (valid email? strong password? verify now or later?), error states, and exit points.

3. **Checkout Optimization:** Map an e-commerce checkout flow: Cart → Shipping → Payment → Review → Confirm. Identify 5 potential friction points. Propose optimizations to reduce steps or anxiety.

4. **Edge Case Mastery:** Take a simple "password reset" happy path. Add all edge cases: email doesn't exist, link expired, network error, user closes tab mid-flow, password too weak. Document recovery paths for each.

5. **Wire Flow:** Create a wire flow (flow + wireframes) for a 3-step process: "Book a table at restaurant" (select date/time → enter guest info → confirm). Show screen content and connections.

6. **Analysis Exercise:** Find a real product flow (e.g., Airbnb booking, Uber ride request). Reverse-engineer the user flow. Identify: entry, steps, decisions, outcomes. Critique: What works? What could be improved?

## Further Reading

- "The User's Journey" by Donna Lichaw
- "Mapping Experiences" by James Kalbach
- Nielsen Norman Group: User Flow articles
- "About Face: The Essentials of Interaction Design" by Alan Cooper
- Smashing Magazine: User Flow tutorials
- UXPin: User Flow guide
