# Usability Testing

## Introduction

Usability testing is the practice of observing real users as they attempt to complete tasks with your product, identifying where they succeed, where they struggle, and why. Unlike other research methods that ask users what they think or want, usability testing shows you what they actually do—revealing gaps between intended design and actual user behavior. It's one of the most valuable, high-impact research methods available: even a few hours of testing can uncover critical usability issues that would otherwise frustrate users and hurt your product's success.

Effective usability testing doesn't require elaborate labs or large sample sizes. Jakob Nielsen famously demonstrated that testing with just 5 users uncovers approximately 85% of usability problems. The key is not volume but iteration: test early with rough prototypes, identify and fix major issues, then test again. This iterative approach—test, learn, fix, repeat—prevents costly late-stage redesigns and ensures you're building something users can actually use. Usability testing is not about validating your design; it's about learning where it breaks down.

Mastering usability testing means knowing how to write effective tasks, recruit appropriate participants, facilitate sessions without biasing results, observe and analyze behavior, and translate findings into actionable design improvements. It requires humility (your design will have problems), empathy (understanding user frustration), and analytical thinking (distinguishing symptoms from root causes). Good usability testing isn't just a research technique—it's a design mindset that prioritizes real user needs over assumptions.

## Learning Objectives

By mastering Usability Testing, you will be able to:

- Plan and conduct usability tests for websites, apps, and prototypes
- Write effective, unbiased task scenarios
- Recruit appropriate participants and create screener surveys
- Facilitate usability test sessions using think-aloud protocol
- Observe and document user behavior, struggles, and successes
- Analyze findings to identify patterns and prioritize issues
- Communicate results to stakeholders with actionable recommendations
- Choose between moderated vs unmoderated, remote vs in-person testing

## Key Knowledge Points

### What is Usability Testing

**Definition:**
Observing users attempting to complete specific tasks with your product to identify usability issues.

**Focus on:**

- **Effectiveness:** Can users complete tasks?
- **Efficiency:** How quickly and easily?
- **Satisfaction:** How do users feel about the experience?
- **Errors:** Where do users make mistakes?
- **Learnability:** How quickly do users learn the interface?

**What it's NOT:**

- Not focus groups (discussion about opinions)
- Not surveys (self-reported data)
- Not beta testing (finding bugs, not usability)
- Not validation ("users will love this") but discovery ("where does this fail?")

**Value:**

- Identifies problems before launch
- Saves development costs (cheaper to fix early)
- Improves conversion, retention, satisfaction
- Grounds design decisions in evidence

See [[UX-Research]] for broader research context.

### When to Test

**Throughout the process:**

**Early (Low-fidelity):**

- Sketches, wireframes, paper prototypes
- Test concepts and flows
- Catch major structural issues
- Quick, cheap iterations

**Mid (Medium-fidelity):**

- Clickable prototypes ([[Figma-Prototyping]])
- Test interactions and navigation
- Refine flows and patterns

**Late (High-fidelity):**

- Near-final designs or working code
- Test complete experience
- Catch detail issues (labels, copy, micro-interactions)

**Post-Launch:**

- Test live product
- Ongoing optimization
- Competitive testing (compare to competitors)

**Iterative:** Test → Learn → Fix → Test again

### Types of Usability Testing

**Moderated vs Unmoderated:**

**Moderated:**

- Facilitator present (in-person or remote)
- Can ask follow-up questions
- Can probe deeper
- Can clarify confusion
- Real-time observation
- **Pros:** Rich insights, flexible, can explore unexpected issues
- **Cons:** Time-intensive, requires skilled facilitator, more expensive

**Unmoderated:**

- User completes tasks alone (online platform)
- Pre-written tasks and questions
- Recorded (video, clicks, etc.)
- Review later
- **Pros:** Faster, cheaper, more participants, less scheduling
- **Cons:** Can't probe, can't clarify, may miss context

**When to use:**

- Moderated: Complex products, early stages, need depth
- Unmoderated: Simple tasks, large sample, speed matters

**Remote vs In-Person:**

**In-Person:**

- Facilitator and participant in same location
- Observe body language, environment
- Can see physical interactions (mobile, hardware)
- **Pros:** Richest observation, build rapport, fewer technical issues
- **Cons:** Geographic limits, scheduling harder, more expensive

**Remote:**

- Facilitator and participant in different locations
- Screen sharing, video call
- Tools: Zoom, Teams, UserTesting, Lookback
- **Pros:** Geographic flexibility, easier scheduling, natural environment
- **Cons:** Technical issues, limited body language, can't see full context

**When to use:**

- In-person: Physical products, need rich observation, local users
- Remote: Distributed users, faster recruitment, lower cost

**Formative vs Summative:**

**Formative (Qualitative):**

- During design process
- Identify problems and opportunities
- Small sample (5-8 users)
- Goal: Improve design

**Summative (Quantitative):**

- After design complete
- Measure success metrics (task completion rate, time on task, error rate)
- Larger sample (15-30+ users)
- Goal: Validate design, benchmark

### Planning a Usability Test

**1. Define Objectives:**

- What do you want to learn?
- What are your research questions?
- Examples:
  - Can users complete checkout?
  - Can users find account settings?
  - Do users understand the navigation?

**2. Choose Method:**

- Moderated or unmoderated?
- Remote or in-person?
- What fidelity (prototype or live)?

**3. Recruit Participants:**

- Who are your target users?
- How many? (5-8 for qualitative, more for quantitative)
- Where to find them? (User research panels, social media, existing users, recruiting agencies)
- Incentives (compensation for time)

**4. Write Test Plan:**

- Objectives
- Methodology
- Participants (number, characteristics)
- Tasks
- Metrics (if quantitative)
- Timeline

**5. Create Materials:**

- Task scenarios
- Screener survey (qualify participants)
- Consent form
- Pre-test questionnaire (demographics, experience)
- Post-test questionnaire (satisfaction, SUS)
- Note-taking template

**6. Pilot Test:**

- Test with colleague or friend
- Identify issues with tasks, timing, technology
- Refine before real sessions

### Participant Recruitment

**Who to Test:**

- Target users (match your personas)
- Mix of experience levels (new users vs experienced)
- Diverse demographics (age, gender, tech comfort, accessibility needs)

**How Many:**

- **Qualitative (formative):** 5-8 users per user group
  - Jakob Nielsen: 5 users find ~85% of issues
  - Diminishing returns after 5
- **Quantitative (summative):** 15-30+ users
  - Need statistical significance

**Screener Survey:**

- Qualify participants
- Questions to filter:
  - Demographics
  - Relevant experience (e.g., "Do you shop online at least once per month?")
  - Exclude criteria (e.g., work in industry, participated recently)

**Example Screener:**

```
1. How often do you shop for groceries online?
   [ ] Never (disqualify)
   [ ] Rarely
   [✓] Monthly (qualify)
   [✓] Weekly (qualify)

2. What is your age range?
   [ ] 18-24  [ ] 25-34  [ ] 35-44  [ ] 45-54  [ ] 55+

3. Do you or anyone in your household work in market research, user experience, or web design?
   [ ] Yes (disqualify)
   [✓] No (qualify)
```

**Incentives:**

- Pay participants for their time
- Standard: $50-150 for 1-hour session (varies by industry, location)
- Gift cards, cash, product credit

**Recruiting Sources:**

- User research panels (UserTesting, Respondent.io)
- Existing users (email list, in-app recruitment)
- Social media (Facebook groups, Reddit, Twitter)
- Recruiting agencies (more expensive)
- Friends/family (for early tests, acknowledge bias)

### Writing Tasks

**Good Tasks are:**

- **Realistic:** Based on actual user goals
- **Specific:** Clear success criteria
- **Unbiased:** Don't lead user to solution

**Task Structure:**
Scenario + Goal (not step-by-step instructions)

**Example (Good):**

- ❌ "Click on the 'Account' link in the top right corner"
  - Too prescriptive, tests clicking not findability
- ✅ "You want to change your email address. Show me how you would do that."
  - Open-ended, tests navigation and findability

**More Examples:**

**E-commerce:**

- "You need a new pair of running shoes for under $100. Find a pair you would consider buying."
- "You want to check when your last order will arrive. Show me how you would do that."

**Banking:**

- "You need to transfer $500 to your friend Alex. Show me how you would do that."
- "You want to see how much you spent on restaurants last month. How would you find that?"

**SaaS Product:**

- "You want to invite a colleague to collaborate on this project. Show me how you would do that."
- "You need to export your data to a spreadsheet. How would you do that?"

**Number of Tasks:**

- 5-8 tasks typical for 1-hour session
- Mix of difficulty (easy, medium, hard)
- Prioritize most critical flows

**Task Order:**

- Start easy (build confidence)
- Most important tasks in middle (alertness high)
- Can end with open exploration ("What would you do next?")

### Facilitating Sessions

**Before Session:**

- Test technology (screen share, recording)
- Review materials
- Quiet, distraction-free space
- Have water, tissues available

**Introduction (5-10 min):**

- Welcome, thank you
- Explain purpose: "We're testing the design, not you"
- Think-aloud protocol: "Tell me what you're thinking as you go"
- No right or wrong answers
- Can stop anytime
- Get consent (recording, data use)
- Answer questions

**During Tasks (30-40 min):**

**Observe:**

- What they do (clicks, navigation path)
- What they say (confusion, delight, frustration)
- Facial expressions, body language
- Pauses, hesitations
- Errors, recovery

**Think-Aloud Protocol:**

- Ask user to verbalize thoughts
- "What are you looking for?"
- "What do you expect to happen?"
- "What are you thinking?"
- **Reminder if silent:** "Remember to keep talking through what you're thinking"

**When to Intervene:**

- **Generally:** Let user struggle (that's the point)
- **Intervene if:**
  - Completely stuck (not learning anything)
  - Too frustrated (ethical consideration)
  - Technical issue (not usability issue)
- **How to intervene:**
  - Minimal prompting
  - "What would you expect to do next?"
  - "Where would you look for that?"
  - Avoid leading: "Have you tried...?" "What about...?"

**Neutral Language:**

- ✅ "What are you thinking?"
- ✅ "Tell me more about that."
- ✅ "What did you expect to happen?"
- ❌ "That's frustrating, isn't it?" (leading)
- ❌ "Did you see the button?" (leading, biased)

**Post-Tasks (10-15 min):**

- Debrief questions:
  - "Overall, how was that experience?"
  - "What worked well?"
  - "What was confusing or frustrating?"
  - "What would you change?"
- Post-test questionnaire (SUS, satisfaction rating)
- Thank you, provide incentive

**Total:** ~60 minutes typical

### Note-Taking & Recording

**Recording:**

- Video: Capture screen + user (if in-person or video call)
- Audio: Backup if video fails
- Screen recording: Essential for remote
- Get consent
- Tools: Zoom, Lookback, UserTesting, QuickTime

**Note-Taking:**

- Designate note-taker (or facilitator takes notes)
- Template with task list
- Note:
  - Task completion (yes/no)
  - Time on task
  - Errors
  - Quotes (verbatim)
  - Observations (confusion, delight)
  - Severity (critical, moderate, minor)

**Example Template:**

```
Participant #3 | Date | Time

Task 1: Find running shoes under $100
- Completion: ✅ Yes / ❌ No
- Time: 2:30
- Path: Home → Search "running shoes" → Filters → Price
- Issues:
  - Couldn't find price filter at first (Severity: Moderate)
  - Quote: "Where's the price filter? Oh, it's hidden under 'More Filters'—I didn't see that."
- Observations: Scrolled past filter initially, then returned
```

### Analyzing Results

**Watch/Review Sessions:**

- Watch recordings
- Review notes
- Look for patterns (not one-off issues)

**Identify Issues:**

- What tasks failed? Why?
- Where did users hesitate or struggle?
- What errors occurred?
- What surprised you?

**Categorize by Severity:**

**Critical:**

- Prevents task completion
- Affects all or most users
- High business impact
- **Priority:** Fix immediately

**Moderate:**

- Causes frustration or inefficiency
- Affects some users
- Medium business impact
- **Priority:** Fix soon

**Minor:**

- Small annoyance
- Affects few users
- Low business impact
- **Priority:** Fix when possible

**Calculate Metrics (if quantitative):**

- **Task completion rate:** % of users who completed task
- **Time on task:** Average time to complete
- **Error rate:** Number of errors per task
- **SUS score:** System Usability Scale (standard questionnaire, 0-100 scale, >68 is average)

**Affinity Mapping:**

- Write observations on sticky notes
- Group related issues
- Identify patterns
- See [[UX-Research]]

**Prioritization:**

- Severity + Frequency = Priority
- Critical + Frequent = Fix first
- Minor + Rare = Fix later or not at all

### Reporting Findings

**Report Structure:**

**Executive Summary:**

- Key findings (3-5 top issues)
- Recommendations
- Impact on business goals

**Methodology:**

- Participants (number, characteristics)
- Tasks tested
- Test format (moderated remote, etc.)

**Detailed Findings:**

- For each issue:
  - What happened
  - Why it's a problem
  - Evidence (quotes, screenshots, video clips)
  - Severity
  - Recommendation
  - Examples

**Example Finding:**

```
Issue: Users couldn't find price filter

Evidence:
- 7 out of 8 participants struggled to locate price filter
- Average time to find: 45 seconds
- Quote: "Where's the price filter? I expected it to be visible, not hidden."

Severity: Moderate

Recommendation:
- Make price filter visible by default (don't hide under "More Filters")
- Consider prominently placing on left sidebar
```

**Metrics Dashboard (if quantitative):**

- Task completion rates
- Time on task (average)
- Error rates
- SUS score

**Video Clips:**

- Highlight reel (3-5 min) showing key issues
- Powerful for stakeholders (seeing is believing)

**Prioritized Recommendations:**

- What to fix first, second, third
- Quick wins vs long-term improvements

**Presentation:**

- Stakeholder meeting (30-60 min)
- Show video clips
- Focus on top 5-10 issues (don't overwhelm)
- Actionable recommendations (not just "it's broken")

### Common Mistakes

**Bad Practices:**

- ❌ Leading participants ("Don't you think this button is confusing?")
- ❌ Testing with friends/family who are too nice or not representative
- ❌ Arguing or defending design ("Actually, it's supposed to work like this...")
- ❌ Testing too late (code already written)
- ❌ Not testing at all (assuming you know what users need)
- ❌ Testing only once (no iteration)
- ❌ Ignoring findings because "users just don't get it"

**Good Practices:**

- ✅ Test early and often
- ✅ Neutral, non-leading facilitation
- ✅ Observe behavior, not just listen to opinions
- ✅ Let users struggle (that's how you learn)
- ✅ Test with representative users
- ✅ Iterate based on findings
- ✅ Share findings widely (democratize insights)

### Tools & Platforms

**Moderated Testing:**

- Zoom, Microsoft Teams, Google Meet (screen share + video)
- Lookback (user research platform)
- UserZoom (enterprise solution)

**Unmoderated Testing:**

- UserTesting.com (recruit + test)
- Maze (prototype testing)
- UsabilityHub (quick tests)
- Optimal Workshop (specialized tasks like tree testing)

**Recording:**

- Zoom (built-in recording)
- QuickTime (Mac screen recording)
- OBS Studio (free, open-source)
- Lookback, UserTesting (built-in)

**Note-Taking:**

- EnjoyHQ, Dovetail (research repositories)
- Notion, Airtable (databases)
- Miro (affinity mapping)
- Google Docs/Sheets (simple, collaborative)

**Surveys:**

- Typeform, Google Forms (screeners, post-test)
- SUS (System Usability Scale) questionnaire

### Specialized Testing Methods

**A/B Testing:**

- Compare two versions quantitatively
- Large sample (hundreds/thousands)
- Measures specific metrics (conversion, clicks)
- Different from usability testing (observational)

**Tree Testing:**

- Test [[Information-Architecture]] without visual design
- Users navigate text-only menus to find items
- Tools: Optimal Workshop, Treejack

**First-Click Testing:**

- Where do users click first to complete task?
- Tests navigation intuitiveness
- Quick, unmoderated

**5-Second Test:**

- Show design for 5 seconds, hide, ask what they remember
- Tests first impression, visual hierarchy

**Guerrilla Testing:**

- Quick, informal testing in public (coffee shop, library)
- Low cost, fast
- Less control over participant quality

See [[Testing-Methods]] for more.

## Related Topics

- [[UX-Research]]
- [[User-Interviews]]
- [[Personas]]
- [[User-Flows]]
- [[Journey-Maps]]
- [[Figma-Prototyping]]
- [[Hi-Fi-Prototyping]]
- [[Testing-Methods]]

## Tools & Resources

**Testing Platforms:**

- UserTesting.com - Recruit + test
- Maze - Prototype testing
- UsabilityHub - Quick tests
- Optimal Workshop - IA testing
- Lookback - Moderated testing

**Video/Recording:**

- Zoom - Screen share + recording
- QuickTime - Screen recording (Mac)
- OBS Studio - Free recording

**Analysis:**

- Dovetail - Research repository
- EnjoyHQ - Insights management
- Miro - Affinity mapping
- Notion - Documentation

**Surveys:**

- Typeform, Google Forms
- SUS Calculator (measuringu.com/sus)

**Books:**

- "Rocket Surgery Made Easy" by Steve Krug (practical guide)
- "Handbook of Usability Testing" by Jeffrey Rubin & Dana Chisnell
- "Observing the User Experience" by Elizabeth Goodman et al.

## Practice Exercises

1. **Plan a Test:** Choose a product (website or app). Write a test plan: objectives, 3 target users types (personas), 5 task scenarios. Create a screener survey with 5 questions to qualify participants.

2. **Facilitate a Session:** Recruit a friend or colleague (not in design/tech). Facilitate a 30-minute usability test on a website (your design or popular site like Airbnb). Practice think-aloud protocol. Take notes. Debrief. What did you learn?

3. **Write Tasks:** For an e-commerce website, write 6 task scenarios covering: product search, filtering, adding to cart, checkout, account management, help/support. Ensure tasks are realistic, specific, unbiased.

4. **Analyze a Recording:** Watch a usability test video on YouTube (search "usability testing session"). Take notes: What issues did you observe? Categorize by severity. Write 3 recommendations.

5. **Remote Unmoderated Test:** Use a platform like Maze or UsabilityHub. Create a test for a prototype or website. Write 3-5 tasks. Recruit 5 participants (friends or online panel). Analyze results. What patterns emerged?

6. **Report Findings:** From any usability test (your own or exercise above), create a 1-page summary: Key findings (3-5 issues), evidence (quotes, metrics), prioritized recommendations. Present to a colleague or friend.

## Further Reading

- **"Don't Make Me Think" by Steve Krug** (classic usability book, includes testing)
- **"Rocket Surgery Made Easy" by Steve Krug** (practical guide to DIY usability testing)
- **"Handbook of Usability Testing" by Jeffrey Rubin & Dana Chisnell** (comprehensive reference)
- **"Observing the User Experience" by Elizabeth Goodman, Mike Kuniavsky, Andrea Moed** (broader research methods, includes testing)
- Nielsen Norman Group: Usability testing articles (nngroup.com)
- **"Moderating Usability Tests" by Joseph Dumas & Beth Loring** (facilitation skills)
- **"Measuring the User Experience" by Tom Tullis & Bill Albert** (quantitative methods)
