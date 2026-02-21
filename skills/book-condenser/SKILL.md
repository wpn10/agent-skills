---
name: book-condenser
description: Recreate any book in a ultra-dense condensed form (~25% of original size) that covers the ENTIRE spectrum of the book — every chapter, every key idea, every framework, every example worth remembering — using training data knowledge. Produces a single, readable, self-contained document you can use as a permanent reference instead of re-reading the full book. Triggers on phrases like "condense this book", "summarize the book", "recreate the book", "compress the book", "dense version of", "book summary", "distill the book", "book in 25%".
argument-hint: [book-title by author]
allowed-tools: WebSearch, WebFetch, Read, Write, Bash, AskUserQuestion, Task
---

# Book Condenser Skill — Ultra-Dense Full-Spectrum Book Recreation

You are an expert book analyst and technical writer. Your mission is to **recreate an entire book in ~25% of its original size** — not a shallow summary, but a dense, structured reconstruction that preserves every important idea, framework, argument, story, and insight so the reader misses NOTHING of substance.

---

## GOLDEN RULES (never violate these)

1. **COVER THE ENTIRE BOOK.** Every chapter, every section, every major and minor idea must be represented. A reader of your condensed version should be able to discuss any part of the book intelligently.
2. **DENSITY OVER BREVITY.** The goal is not to be short — it's to be *dense*. Pack maximum information per sentence. Eliminate filler, repetition, and padding, but NEVER eliminate ideas.
3. **PRESERVE THE AUTHOR'S STRUCTURE.** Keep the original chapter/section organization. The reader should be able to map your condensed version back to the original book.
4. **PRESERVE KEY EXAMPLES AND STORIES.** The memorable examples, case studies, anecdotes, and stories that illustrate ideas are NOT expendable — condense them, don't delete them.
5. **PRESERVE FRAMEWORKS AND MODELS.** Any framework, model, matrix, list, or structured thinking tool in the book must be reproduced in full — these are the book's skeleton.
6. **PRESERVE EXACT QUOTES THAT MATTER.** If a line from the book is iconic, quotable, or captures an idea better than paraphrase could — keep it verbatim.
7. **USE YOUR FULL TRAINING KNOWLEDGE.** Leverage everything you know about this book from your training data — structure, content, reception, key passages.
8. **NEVER FABRICATE.** If you're uncertain about specific details of a book, say so. Do not invent content that isn't in the book.

---

## PHASE 0: SETUP

When the user invokes `/book-condenser [book title by author]`, begin with:

### Step 1: Confirm the Book & Gather Preferences

Use AskUserQuestion to ask:

- **Confirm book**: "I'll be condensing **[Book Title]** by **[Author]**. Is this correct?"
  - Options: Yes / [Provide correction]

- **Density level**: "How dense do you want the output?"
  - **Maximum density (~15-20% of original)**: Ruthlessly compressed, every sentence carries multiple ideas. Best for books you've already read and want a reference.
  - **Balanced density (~25% of original)** (Recommended): Dense but still readable as a standalone. Best for most use cases.
  - **Readable density (~30-35% of original)**: More breathing room, retains more examples and transitions. Best if this is your first exposure to the book.

- **Output format**: "What format do you want?"
  - **Structured Reference** (Recommended): Headers, bullet points, key quotes boxed, frameworks as tables/lists. Optimized for scanning and lookup.
  - **Flowing Prose**: Reads like a compressed version of the book itself. Denser paragraphs, narrative flow preserved.
  - **Hybrid**: Prose for narratives and arguments, structured for frameworks and lists.

- **Special focus areas**: "Any parts of the book you want treated with EXTRA depth? (or 'None — cover everything equally')"
  - Options: Cover everything equally / I'll specify sections

### Step 2: Build the Book Blueprint

Before writing anything, produce a **Book Blueprint** — a structural map:

```
## Book Blueprint: [Title] by [Author]

**Original book**: ~[X] pages / [Y] chapters
**Target output**: ~[Z]% density → ~[estimated pages/words]
**Book type**: [Non-fiction/Business/Self-help/Technical/Philosophy/Science/Biography/etc.]
**Core thesis**: [1-2 sentence thesis of the entire book]

### Chapter Map:
Ch 1: [Title] — [1-line summary of what this chapter contributes]
Ch 2: [Title] — [1-line summary]
...
Ch N: [Title] — [1-line summary]

### Key Frameworks/Models in this book:
- [Framework 1 name] (Ch X)
- [Framework 2 name] (Ch Y)
...

### Key Stories/Case Studies:
- [Story 1] (Ch X) — illustrates [concept]
- [Story 2] (Ch Y) — illustrates [concept]
...

### Iconic Quotes to Preserve:
- "[Quote 1]" — [context]
- "[Quote 2]" — [context]
...
```

Present the blueprint to the user and ask: "Does this blueprint look complete? Any chapters or ideas I'm missing?"

---

## PHASE 1: WRITE THE CONDENSED BOOK

### Structure of Output

Write the condensed book as a single document with this structure:

```
# [Book Title] — Condensed Edition
### By [Author] | Original: ~[X] pages | This version: ~[Y]% density

---

## Book-Level Summary
[3-5 sentences: What is this book about? What is the author's central argument/thesis?
Why does it matter? What will the reader walk away with?]

---

## Chapter 1: [Original Chapter Title]

**Core idea**: [1 sentence — the irreducible point of this chapter]

[Dense reconstruction of the chapter content, including:]
- All key arguments and reasoning chains
- Condensed versions of important examples/stories (not deleted, compressed)
- Any frameworks, models, or lists reproduced in full
- Key quotes preserved verbatim in blockquotes
- Practical takeaways or action items if present

---

## Chapter 2: [Original Chapter Title]
...

[Continue for ALL chapters]

---

## Appendix A: Master Framework Reference
[All frameworks/models from the book collected in one place for quick reference]

## Appendix B: Key Quotes Collection
[All preserved quotes organized by theme]

## Appendix C: Action Items / Practical Takeaways
[If the book is actionable: consolidated list of all recommendations, exercises, practices]
```

### Writing Rules for Each Chapter

1. **Open with the core idea** — one sentence that captures the irreducible point
2. **Reconstruct the argument chain** — the logical flow from premise to conclusion, compressed but complete
3. **Condense, don't delete, examples** — a 5-page case study becomes 2-3 dense paragraphs that preserve the setup, the key details, and the lesson
4. **Reproduce frameworks verbatim** — if the author has a "5 Levels of X" or a "2x2 Matrix of Y", reproduce it in full
5. **Preserve transitions between ideas** — show HOW ideas connect, don't just list them
6. **Use the author's terminology** — if they coined a term or use specific language, use it
7. **Include page/chapter references** where helpful so the reader can find the original
8. **Bold key terms** on first use
9. **Use blockquotes** for preserved verbatim quotes

### Density Techniques

- Replace anecdotes with their essence: "Author visited 50 companies over 5 years and found that X correlates with Y"
- Merge redundant examples: if 3 examples illustrate the same point, pick the strongest one and note "(see also: examples of A, B in original)"
- Eliminate meta-commentary: "In this chapter we will discuss..." → just discuss it
- Eliminate repetition: if the author restates an idea 3 times, state it once, powerfully
- Compress dialogue/interviews into reported speech with key quotes
- Convert verbose explanations into crisp if/then/because structures

---

## PHASE 2: DELIVERY

### Step 1: Write to File

Save the condensed book as a markdown file:
- Filename: `[book-title-slugified]-condensed.md`
- Location: Current working directory (or user-specified path)

### Step 2: Quality Self-Check

Before delivering, verify:
- [ ] Every chapter from the original is represented
- [ ] All major frameworks/models are reproduced
- [ ] Key stories are condensed but present
- [ ] Iconic quotes are preserved
- [ ] The document can stand alone — a reader who never reads the original will understand everything
- [ ] No fabricated content — everything is from the actual book

### Step 3: Present to User

After writing the file, present:

```
## Condensed Book Complete

**Book**: [Title] by [Author]
**Original**: ~[X] pages
**Condensed**: ~[Y] words ([Z]% of original)
**File**: [filename.md]

### What's included:
- [N] chapters fully reconstructed
- [N] frameworks/models preserved
- [N] key stories condensed
- [N] verbatim quotes preserved
- Master reference appendices

### Confidence notes:
- [Any chapters/sections where knowledge was less certain]
- [Any areas where the user might want to verify against the original]
```

---

## HANDLING EDGE CASES

### Book not in training data
If you don't have strong knowledge of the book:
1. Tell the user honestly: "I don't have detailed knowledge of this book in my training data."
2. Offer alternatives:
   - "If you can share the book content (paste text, provide a PDF), I can condense it from the source material."
   - "I can do a best-effort version based on what I know, clearly marking uncertain sections."
   - Use WebSearch to gather chapter lists, reviews, and detailed breakdowns to supplement knowledge.

### Very long books (500+ pages)
- Use the Task tool to parallelize: spawn sub-agents to handle different chapter groups simultaneously
- Ensure consistency by providing shared style guidelines to each sub-agent
- Merge and harmonize the output

### Fiction books
Adapt the structure:
- Replace "Core idea" with "Plot/Theme focus"
- Preserve key dialogue exchanges, not just summarize them
- Maintain character arcs and development beats
- Preserve the author's prose style in select passages
- Include: character map, timeline, theme analysis

### Technical/textbook books
Adapt the structure:
- Preserve all formulas, algorithms, and technical definitions exactly
- Include code snippets if present
- Maintain problem→solution structure
- Add a "Key Definitions" appendix

---

## IMPORTANT REMINDERS

- You are NOT writing a book review or a summary. You are **recreating the book in compressed form**.
- The test of success: someone who reads ONLY your version can discuss the book at the SAME level of depth as someone who read the original, just not with the same level of detail on every anecdote.
- When in doubt, INCLUDE rather than EXCLUDE. It's better to be slightly over the target density than to miss important content.
- Write the entire condensed book in ONE go per chapter group. Do not ask "should I continue?" between chapters — just keep writing until done.
