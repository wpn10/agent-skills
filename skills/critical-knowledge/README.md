# Critical Knowledge: High-Precision Research Agent

A research agent that finds the most valuable, non-obvious, and decision-relevant information on any topic -- going far beyond standard answers.

## What It Does

This skill transforms your AI agent into a sharp, skeptical researcher that prioritizes signal over noise. Instead of generic summaries, it delivers:

- **Non-obvious insights** -- what most people miss about the topic
- **Triangulated facts** -- claims verified across multiple credible sources
- **Hidden tradeoffs** -- costs and risks that standard advice ignores
- **Actionable conclusions** -- specific next steps prioritized by impact
- **Explicit uncertainty** -- clear about what is known vs. unknown

## How It Works

The skill runs through three phases:

### Phase 0: Understand the Real Question
Identifies the actual decision or problem behind the user's question. Maps the research space and determines where the highest-value information lives.

### Phase 1: Research
Systematic search following a strict source hierarchy:
1. Primary sources (original research, official documents, raw data)
2. Authoritative analysis (domain experts, peer-reviewed work)
3. High-quality secondary sources (well-sourced journalism)
4. Recent sources (when freshness matters)
5. Contrarian views (when backed by strong evidence)

### Phase 2: Synthesis and Analysis
Cross-checks key claims, resolves source conflicts, and applies critical thinking to separate facts from interpretations.

### Phase 3: Deliver the Answer
Structured output format:
- **Bottom line** -- most important conclusion first
- **What most people miss** -- highest-value non-obvious insights
- **Evidence and reasoning** -- key facts organized by importance
- **Risks / tradeoffs** -- failure modes and hidden costs
- **Best next actions** -- concrete, prioritized steps
- **Confidence and uncertainty** -- what's solid vs. what needs more investigation

## Usage

```
/critical-knowledge [topic or question]
```

### Examples

```
/critical-knowledge Is Rust worth learning for backend development in 2026?
/critical-knowledge What are the real risks of microservices migration?
/critical-knowledge Best approach to invest $50k in the current market
/critical-knowledge How does mRNA vaccine technology actually work?
/critical-knowledge What should I know before negotiating a Series A term sheet?
```

## What Makes It Different

Most research produces summaries. This skill produces **insights**:

| Standard Research | Critical Knowledge |
|---|---|
| Lists common facts | Finds what's overlooked |
| Treats all info equally | Prioritizes by decision-relevance |
| Single-source answers | Triangulated, cross-checked claims |
| Hides uncertainty | States confidence levels explicitly |
| Generic advice | Context-dependent recommendations |
| Safe, shallow conclusions | Sharp, specific, actionable insights |

## Best For

- Making important decisions with incomplete information
- Understanding complex topics beyond surface-level
- Finding what conventional wisdom gets wrong
- Evaluating tradeoffs between competing options
- Pre-decision research before committing time or money
- Any question where the obvious answer isn't good enough
