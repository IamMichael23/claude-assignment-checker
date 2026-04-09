# AI Writing Patterns Reference

This is the complete list of AI writing patterns to detect. Based on Wikipedia's
"Signs of AI writing" guide. When any pattern is found, flag the exact text and
provide a human-sounding rewrite.

## Content Patterns

### 1. Inflated Significance / Legacy Language
**Words:** stands/serves as, is a testament/reminder, a vital/significant/crucial/
pivotal/key role/moment, underscores/highlights its importance/significance, reflects
broader, symbolizing its ongoing/enduring/lasting, contributing to the, setting the
stage for, marking/shaping the, represents/marks a shift, key turning point, evolving
landscape, focal point, indelible mark, deeply rooted

**Fix:** State the actual significance plainly. "The institute was established in 1989"
not "The institute was established in 1989, marking a pivotal moment."

### 2. Notability and Media Coverage Claims
**Words:** independent coverage, local/regional/national media outlets, written by a
leading expert, active social media presence

**Fix:** Give a specific example instead of listing outlets.

### 3. Superficial -ing Analyses
**Words:** highlighting/underscoring/emphasizing..., ensuring..., reflecting/
symbolizing..., contributing to..., cultivating/fostering..., encompassing...,
showcasing...

**Fix:** Remove the -ing phrase and state the point directly.

### 4. Promotional Language
**Words:** renowned, acclaimed, prestigious, innovative, cutting-edge, world-class,
state-of-the-art, trailblazing, top-tier, highly regarded, award-winning (without
specifying awards), best-in-class

**Fix:** Describe what the thing actually does instead of using sales adjectives.

### 5. Vague Attributions
**Words:** experts say, research shows, studies indicate, many scholars argue, it is
widely accepted, it has been noted that, observers point out, critics argue

**Fix:** Name the specific source. "Smith (2023) argues..." not "experts argue..."

### 6. Em Dash and En Dash Overuse
**Pattern:** Frequent use of — and – for parenthetical statements, asides, or to
connect clauses.

**Fix:** Replace with commas, parentheses, colons, semicolons, or rewrite the sentence.
ZERO tolerance in this skill.

### 7. Rule of Three
**Pattern:** Exactly three items in a list for rhetorical effect:
"innovative, dynamic, and transformative"
"plan, execute, and deliver"
"speed, quality, and reliability"

**Fix:** Use 1-2 items if that's enough, or 4+ if genuinely needed. Three is the
AI default.

### 8. AI Vocabulary Words
These words appear disproportionately in AI-generated text:

**High-frequency AI words:**
delve, tapestry, crucial, pivotal, moreover, furthermore, additionally, multifaceted,
encompasses, facilitates, underscores, highlights, fostering, cultivating, showcasing,
leveraging, utilizing, groundbreaking, innovative, seamless, robust, comprehensive,
nuanced, intricate, landscape (metaphorical), paradigm, synergy, holistic, ecosystem
(non-biological), empower, navigate (metaphorical), reimagine, unlock (metaphorical)

**AI phrases:**
"it is worth noting", "in today's world", "plays a vital role", "at its core",
"serves as a testament", "it's important to note", "in the realm of", "shed light on",
"pave the way for", "a testament to", "the intersection of X and Y",
"in an era of", "strike a balance", "resonate with", "at the forefront of"

**Fix:** Replace each with a plain, specific alternative.

### 9. Passive Voice Overuse
**Pattern:** Heavy use of passive constructions where active voice would be clearer.
"It was determined that..." instead of "We determined..."
"The analysis was conducted..." instead of "We analyzed..."

**Fix:** Use active voice unless passive is genuinely needed (e.g., the actor is
unknown or irrelevant).

### 10. Negative Parallelism
**Pattern:**
"It's not just X; it's Y"
"It's not about X, it's about Y"
"This isn't merely X; it represents Y"

**Fix:** Just state what it IS directly.

### 11. False Ranges
**Pattern:**
"from hobbyists to professionals"
"from small startups to large enterprises"
"from X to Y, from A to B"

**Fix:** Be specific about the actual scope.

### 12. Formulaic Conclusions
**Pattern:**
"In conclusion", "To sum up", "In summary"
"the future looks bright", "exciting times lie ahead"
"further research is needed" (generic)
"As we move forward"

**Fix:** Make the conclusion say something specific and substantive.

### 13. Signposting and Announcements
**Pattern:**
"Let's dive in", "Let's explore", "Let's break this down"
"Here's what you need to know"
"In this section, we will discuss..."
"Without further ado"
"Now let's look at"

**Fix:** Remove entirely and just start the content.

### 14. Fragmented Headers
**Pattern:** A heading followed by a one-line paragraph that restates the heading.

```
## Performance
Speed matters.
When users hit a slow page, they leave.
```

**Fix:** Remove the restated line and start with the real content.

### 15. Hedging Pile-ups
**Pattern:** Stacking multiple hedging words in one sentence:
"it could potentially be argued that this might possibly suggest"

**Fix:** Pick one level of qualification: "the evidence suggests" or "this indicates."

### 16. Copula Avoidance
**Pattern:** Using "serves as", "functions as", "stands as", "acts as" instead of
plain "is" or "are."

**Fix:** Use "is" or "are" when that's what you mean.

### 17. Filler Phrases
**Pattern:**
"In order to" -> "To"
"Due to the fact that" -> "Because"
"It is important to note that" -> remove or state the thing directly
"At the end of the day" -> remove
"When it comes to" -> remove or use "For" / "Regarding"
"In terms of" -> remove or be specific
"On the other hand" -> often removable

### 18. Emoji and Decorative Formatting
**Pattern:** Using emoji, excessive bold headers, decorative bullet points in
academic writing.

**Fix:** Remove all emoji. Use formatting sparingly and consistently.

## Voice Indicators

### Signs the writing lacks human voice:
- Every paragraph is the same length
- Every sentence follows subject-verb-object without variation
- No first-person perspective when it would be natural
- No acknowledgment of uncertainty or mixed feelings
- No humor, personality, or edge anywhere
- Reads like a Wikipedia article or press release
- Suspiciously "balanced" and "comprehensive"
- No strong claims or positions taken

### Signs the writing has human voice:
- Varied sentence length and structure
- Occasional first-person where appropriate
- Acknowledges complexity and uncertainty genuinely
- Takes clear positions with reasoning
- Has moments of specificity that feel observed, not generated
- Reads like one person wrote it, not a committee
