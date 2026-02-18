# Interview: Pre-Task Requirements Gathering

A structured interview skill that asks the right questions before any work begins -- so you and Claude are on the same page from the start.

## What It Does

Instead of jumping into a task and hoping for the best, this skill runs a quick 2-5 minute interview using selectable options. It figures out what you want, how you want it, and what "done" looks like -- then summarizes everything for your confirmation before work starts.

Every question has selectable options. You never have to type unless you want to (there's always a "let me type my answer" option).

## How It Works

### 5-Step Interview Flow

1. **Understand the task** -- what type of work is this? (feature, bug, refactor, infra, research, etc.)
2. **Scope & constraints** -- how big? how urgent? what can we change?
3. **Technical context** -- language, codebase areas, dependencies, tests
4. **Acceptance criteria** -- how do we know it's done?
5. **Working style** -- autonomous, check-ins, or walk-through?

The skill adapts questions to the task type. A quick bug fix gets 2 rounds. A complex architecture task gets 4-5. Questions already answered by context are skipped.

### Post-Interview Summary

After the interview, you get a structured summary:

```
Task Summary
├── What: one-sentence description
├── Type: feature / bug / refactor / etc.
├── Scope: quick / medium / large
├── Priority: ship fast / balanced / production-grade
├── Key Details
├── Planned Approach
├── Acceptance Criteria (checkboxes)
├── Out of Scope
└── Working Style
```

You confirm, adjust, or redo -- then work begins.

## Usage

```
/interview [optional task description]
```

**Examples:**
- `/interview` -- start a blank interview
- `/interview add OAuth login to the API` -- interview with context, skips obvious questions
- `/interview fix the memory leak in the worker service` -- scoped bug investigation
- `/interview refactor the payment module` -- clarify scope and constraints

## Question Design

Every question follows this format:
- 3-4 pre-built options covering the most common answers
- Always includes "Let me type my answer" as the last option
- Max 4 questions per round (never overwhelming)
- Questions adapt based on previous answers

## When to Use

- Before starting any non-trivial task
- When a request is ambiguous or could be interpreted multiple ways
- When you want to explicitly agree on scope before work begins
- When working on someone else's codebase and need to understand conventions
- Before large refactors or architectural changes

## When NOT to Use

- One-line fixes ("fix the typo on line 42")
- Tasks with crystal-clear instructions
- When you just want Claude to explore or research freely
