# Claude Assignment Checker Skill

A Claude Code superpowers skill that reviews your homework or assignment before submission using a team of 3 specialist agents. Built for graduate-level academic work submitted as LaTeX.

## What It Does

Upload your `.tex` file and rubric, and this skill runs a full pre-submission review:

1. **Rubric Grader** — marks your work like a professor, estimates your grade band, and flags rubric requirements you're missing
2. **Academic Critic** — reviews argument quality, evidence, structure, and writing voice like a tough peer reviewer
3. **Copy Editor** — proofreads grammar, spelling, LaTeX health, formatting, and AI-sounding language

After all three agents report, the skill merges everything into one prioritized **Grade Report** — critical issues first, sorted by grade impact.

## How to Trigger It

Say any of the following to Claude:

- "check my assignment"
- "review before submitting"
- "is this ready to hand in?"
- "proofread my paper"
- "grade my work"
- "how can I improve my grade?"
- "check my tex file"

Or just upload a `.tex` file + rubric and say "check this."

## What You Get

```
## GRADE REPORT — Iteration [N]

### Predicted Grade
### Rubric Scorecard
### Critical Issues (Fix These First)
### Warnings (Should Fix)
### Minor Issues (Nice to Fix)
### AI Writing Flags
### Dash Violations
### Summary
```

Every issue includes: **WHAT**, **WHERE**, **WHY IT COSTS MARKS**, and a **FIX**.

## Feedback Loop

Re-upload after fixing and the skill re-runs all three agents from scratch. The new report shows exactly what changed:

```
### Changes Since Iteration [N-1]
- RESOLVED: ...
- STILL OPEN: ...
- NEW ISSUES: ...
- GRADE CHANGE: B+ -> A-
```

Repeat until you're satisfied.

## Hard Rules (Enforced on Every Run)

- **No em dashes (— ) or en dashes (–)** — every instance is flagged and replaced
- **No AI vocabulary** — delve, tapestry, crucial, pivotal, moreover, furthermore, leverage, utilize, robust, comprehensive, seamless, groundbreaking, and more
- **No signposting** — "let's dive in", "in this section we will", "without further ado"
- **No rule of three** — lists of exactly three adjectives/phrases used for rhetorical effect

## Required Inputs

1. Your assignment `.tex` source file(s)
2. The rubric or marking criteria

The skill will ask for whichever is missing before starting.

## Installation

Place the skill folder in your Claude Code superpowers skills directory. The skill is automatically triggered by the phrases above — no manual invocation needed.

## File Structure

```
assignment-checker/
├── SKILL.md                          # Main skill definition
├── agents/
│   ├── rubric-grader.md              # Professor perspective
│   ├── academic-critic.md            # Peer reviewer perspective
│   └── copy-editor.md                # Proofreader perspective
└── references/
    ├── ai-writing-patterns.md        # Full AI language pattern list
    └── latex-common-issues.md        # Common LaTeX problems reference
```
