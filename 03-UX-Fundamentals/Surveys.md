# Surveys

## Introduction

Surveys are structured questionnaires used to collect data from a large number of respondents, providing quantitative insights about user behaviors, preferences, attitudes, and demographics. Unlike [[User-Interviews]] which offer depth from a small sample, surveys offer breadth—statistical patterns across hundreds or thousands of users. A well-designed survey can validate assumptions, prioritize features, measure satisfaction, and quantify the prevalence of issues discovered through qualitative research.

Surveys are powerful because they scale. While interviewing 500 users is impractical, surveying them is straightforward. This makes surveys ideal for questions like "What percentage of users want this feature?" or "How satisfied are users with our checkout process?" However, this power comes with constraints: surveys can't explore "why" as deeply as interviews, and poorly designed surveys yield misleading or meaningless data. The craft of survey design lies in asking clear, unbiased questions that respondents can answer accurately.

Surveys work best when paired with qualitative research. Use [[User-Interviews]] to discover problems and understand context, then use surveys to measure how widespread those issues are. This mixed-method approach combines the depth of qualitative insights with the statistical confidence of quantitative data, enabling evidence-based design decisions.

## Learning Objectives

By mastering Surveys, you will be able to:

- Determine when surveys are the appropriate research method
- Write clear, unbiased survey questions that yield actionable data
- Choose appropriate question types (multiple choice, scales, open-ended)
- Design survey flows that minimize dropout and bias
- Distribute surveys to reach target audiences
- Analyze survey data to extract insights and identify patterns
- Calculate and interpret key metrics (NPS, satisfaction scores, etc.)
- Avoid common survey pitfalls that compromise data quality

## Key Knowledge Points

### Survey Fundamentals

- [[Survey]]

  - Structured questionnaire administered to many respondents
  - [[Quantitative Research]] method (numerical data)
  - 5-20 questions typical (shorter = better completion)
  - Distributed digitally (email, website, app) or physically

- **When to Use Surveys:**

  - Measure prevalence ("How many users experience X?")
  - Validate findings from qualitative research at scale
  - Prioritize features (which is most important?)
  - Measure satisfaction, usability, sentiment
  - Collect demographic data
  - Track changes over time (longitudinal)

- **When NOT to Use Surveys:**

  - Exploring unknown problems (use [[User-Interviews]])
  - Understanding "why" deeply (use interviews)
  - Testing designs (use [[Usability-Testing]])
  - Asking about hypothetical future behavior (unreliable)

- **Surveys vs Interviews:**
  - Surveys: Breadth, scale, statistical confidence, "how many"
  - Interviews: Depth, context, exploration, "why"
  - Best: Use both (interviews → insights, surveys → validation)

### Survey Planning

- [[Survey Goals]]

  - What do you need to learn?
  - What decisions will this inform?
  - Be specific: "Measure satisfaction with checkout process" not "Learn about users"

- [[Target Audience]]

  - Who should take the survey?
  - Current users, potential users, specific segment?
  - Sample size needed depends on:
    - Population size
    - Desired confidence level (95% typical)
    - Margin of error (±5% typical)
  - Calculator: Sample Size Calculator (search online)
  - **Rule of thumb:** 300-400 responses for reliable stats

- [[Survey Length]]
  - Shorter = higher completion rates
  - 5-10 questions ideal
  - 15-20 max
  - **Completion time:** 5 minutes or less
  - Every question should earn its place

### Question Types

- [[Multiple Choice Questions]]

  - Respondent selects from predefined options
  - **Single Select:** Choose one answer
  - **Multi Select:** Choose all that apply
  - **When to use:** Known options, easy analysis
  - **Tip:** Include "Other (please specify)" to catch unknowns

- [[Rating Scales]]

  - **Likert Scale:**
    - 5 or 7 points
    - "Strongly disagree" to "Strongly agree"
    - "Very dissatisfied" to "Very satisfied"
    - Include midpoint (neutral) or not (forces choice)
  - **Numeric Scale:**
    - 1-5, 1-7, or 1-10
    - Label endpoints: "Not at all likely" to "Extremely likely"
  - **Star Ratings:** Visual, familiar (⭐⭐⭐⭐⭐)

- [[Ranking Questions]]

  - Order items by preference or importance
  - Example: "Rank these features from most to least important"
  - **Limitation:** Cognitively demanding (limit to 5-7 items)

- [[Matrix Questions]]

  - Rate multiple items on same scale
  - Example: Rate satisfaction with [Feature A, Feature B, Feature C]
  - **Pro:** Compact, efficient
  - **Con:** Straight-lining bias (same answer for all rows)

- [[Open-Ended Questions]]
  - Free-text response
  - **When to use:**
    - "Why?" follow-ups to closed questions
    - Discover unexpected insights
    - Final question: "Anything else?"
  - **Limitation:** Time-consuming to analyze, lower completion
  - **Tip:** Use sparingly (1-2 per survey)

### Writing Good Questions

- [[Question Clarity]]

  - Simple language, avoid jargon
  - One question per question (not double-barreled)
  - ❌ "How satisfied are you with the speed and reliability of our app?"
  - ✅ "How satisfied are you with the speed?" (separate question for reliability)

- [[Avoid Leading Questions]]

  - Don't suggest desired answer
  - ❌ "How much do you love our new feature?"
  - ✅ "What do you think of our new feature?"
  - ❌ "Don't you think dark mode would improve the app?"
  - ✅ "Would dark mode improve your experience? Why or why not?"

- [[Avoid Loaded Language]]

  - Neutral phrasing
  - ❌ "Do you prefer our elegant, modern design?"
  - ✅ "Do you prefer the new design or the old design?"

- [[Provide Complete Response Options]]

  - Cover all possibilities
  - Include "Other," "Prefer not to say," or "N/A" when appropriate
  - For ranges, avoid gaps:
    - ✅ "18-24, 25-34, 35-44..." (no overlaps or gaps)
    - ❌ "18-25, 25-35, 35-45..." (overlap at 25, 35)

- [[Recall Period]]
  - Be specific about timeframe
  - ❌ "How often do you use our app?"
  - ✅ "In the past 7 days, how many times did you use our app?"
  - Shorter periods = more accurate recall

### Survey Structure

**Typical Flow:**

1. **Introduction (1 screen)**

   - Purpose of survey
   - Time estimate
   - Privacy/anonymity assurance
   - Incentive (if any)

2. **Screening (if needed)**

   - Qualify respondents
   - "Do you use [product type] at least once a week?"
   - Disqualify gracefully: "Thank you, but this survey is for active users."

3. **Warm-Up (1-2 questions)**

   - Easy, non-threatening questions
   - Builds momentum

4. **Core Questions**

   - Most important questions
   - Logical grouping
   - Similar question types together (all ratings, then all open-ended)

5. **Demographics (end)**

   - Age, gender, location, etc.
   - Put at end (less likely to abandon after completing core)
   - Always make optional

6. **Thank You**
   - Appreciation
   - What happens next
   - Incentive delivery info

### Survey Flow Best Practices

- [[Progressive Disclosure]]

  - One question per screen (especially mobile)
  - Or logical groups per screen
  - Show progress bar

- [[Required vs Optional]]

  - Make questions optional when possible
  - Required questions increase dropout
  - Mark required clearly (\*)

- [[Conditional Logic]]

  - Show/hide questions based on previous answers
  - Example: If "Yes" to "Do you use Feature X?", ask "How satisfied are you with Feature X?"
  - Reduces irrelevant questions

- [[Randomization]]
  - Randomize answer order (prevent order bias)
  - Exception: Scales (don't randomize "Strongly agree" to "Strongly disagree")

### Survey Distribution

- **Email:**

  - To existing user list
  - Personalized invite
  - Reminder emails (1-2)

- **In-App / On-Site:**

  - [[Intercept Survey]]: Pop-up during usage
  - Timing: After task completion or on exit intent
  - **Pro:** High response rate, contextual
  - **Con:** Can be intrusive

- **Social Media:**

  - Post survey link
  - Broader reach, less targeted

- **Paid Panels:**

  - Services: UserTesting, Respondent, Prolific
  - Pay participants
  - Control demographics

- **Response Rate:**
  - Email surveys: 10-30% typical
  - In-app: 1-5% (but contextual)
  - Incentives increase response rate

### Survey Analysis

- [[Descriptive Statistics]]

  - **Frequency:** How many chose each option?
  - **Percentage:** What % chose each?
  - **Mean (average):** For numeric scales
  - **Median:** Middle value (less affected by outliers)
  - **Mode:** Most common response

- [[Cross-Tabulation]]

  - Compare responses across segments
  - Example: Satisfaction by age group
  - Reveals patterns

- [[Qualitative Coding]]

  - For open-ended responses
  - Tag themes
  - Count frequency of themes
  - See [[UX-Research]] analysis section

- [[Visualization]]
  - Charts make data understandable
  - Bar charts (categorical data)
  - Pie charts (parts of whole, use sparingly)
  - Line charts (trends over time)
  - Tools: Excel, Google Sheets, Tableau

### Common Survey Metrics

- [[Net Promoter Score (NPS)]]

  - "How likely are you to recommend [product] to a friend?" (0-10)
  - **Calculation:**
    - Promoters: 9-10
    - Passives: 7-8
    - Detractors: 0-6
    - NPS = % Promoters - % Detractors
  - **Score range:** -100 to +100
  - **Benchmark:** >50 excellent, 0-50 good, <0 needs work

- [[Customer Satisfaction (CSAT)]]

  - "How satisfied are you with [product/feature]?" (1-5 or 1-7)
  - **Calculation:** (# satisfied + # very satisfied) / total responses × 100
  - Report as percentage

- [[System Usability Scale (SUS)]]

  - 10-question standardized usability survey
  - Odd questions positive, even negative (detects straight-lining)
  - **Score:** 0-100 (not a percentage)
  - **Benchmark:** >68 above average

- [[Task Completion Rate]]
  - "Were you able to complete the task?" (Yes/No)
  - Percentage who completed successfully

### Survey Pitfalls to Avoid

- **Survey Fatigue:**

  - Too many questions
  - Too frequent surveys
  - Solution: Keep short, space out over time

- **Sampling Bias:**

  - Survey only reaches certain users
  - Example: Email survey excludes users without email
  - Solution: Multiple distribution channels

- **Nonresponse Bias:**

  - People who respond differ from those who don't
  - Example: Very happy or very unhappy more likely to respond
  - Solution: Incentives, reminders, but acknowledge limitation

- **Acquiescence Bias:**

  - Tendency to agree with statements
  - Solution: Mix positive and negative statements

- **Social Desirability Bias:**

  - Respondents answer what sounds good, not truth
  - Solution: Anonymity, neutral wording

- **Order Effects:**
  - Question order influences answers
  - Solution: Randomize when appropriate

## Related Topics

- [[UX-Research]]
- [[User-Interviews]]
- [[Quantitative Research]]
- [[Analytics]]
- [[A/B Testing]]
- [[Usability-Testing]]
- [[Data Analysis]]

## Tools & Resources

**Survey Platforms:**

- [[Typeform]] - Beautiful, conversational surveys
- [[Google Forms]] - Free, simple
- [[SurveyMonkey]] - Feature-rich
- [[Qualtrics]] - Enterprise, academic
- [[Alchemer]] (formerly SurveyGizmo)

**In-App Survey Tools:**

- [[Hotjar]] - On-site surveys and heatmaps
- [[Qualaroo]] - Targeted surveys
- [[UserVoice]] - Feedback collection

**Analysis:**

- [[Excel]] / [[Google Sheets]]
- [[SPSS]] (statistical analysis)
- [[Tableau]] (visualization)

**Books & Resources:**

- "Handbook of Survey Research" (comprehensive)
- "Measuring the User Experience" by Tullis & Albert (includes survey design)
- Nielsen Norman Group: Survey Design articles
- SurveyMonkey: Sample size calculator

## Practice Exercises

1. **Survey Design:** Create a 10-question survey to measure satisfaction with a food delivery app. Include: satisfaction scale, NPS, multiple choice, open-ended. Identify question type and rationale for each.

2. **Question Critique:** Find 10 survey questions online. Identify problems: leading language, double-barreled, unclear options, etc. Rewrite them correctly.

3. **Survey Flow:** Map out a 15-question survey about fitness app usage. Group logically, add conditional logic, determine required vs optional. Explain your choices.

4. **Analysis Practice:** Create a survey with 5 questions. Distribute to 20 people. Analyze results: calculate percentages, mean scores, identify patterns. Create 3 visualizations.

5. **NPS Calculation:** Given responses: [10, 9, 8, 7, 9, 10, 6, 5, 9, 8, 7, 10], calculate NPS. Show your work (# promoters, passives, detractors).

6. **Bias Identification:** Review 3 real surveys (from companies, apps, etc.). Identify biases: leading questions, incomplete options, sampling issues. How would you fix each?

## Further Reading

- "Measuring the User Experience" by Tullis & Albert (Chapter on surveys)
- "Don't Make Me Think" by Steve Krug (includes survey tips)
- Nielsen Norman Group: Surveys articles
- "Survey Methodology" by Groves et al. (academic, comprehensive)
- Pew Research Center: Survey methodology resources (excellent standards)
