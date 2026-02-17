<div align="center">

# Agent Skills

### Plug-and-play skill modules that make AI agents actually useful.

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)
[![GitHub stars](https://img.shields.io/github/stars/wpn10/agent-skills?style=social)](https://github.com/wpn10/agent-skills)

**Stop reinventing the wheel every time you build an AI agent.**

[Get Started](#quick-start) | [Browse Skills](#available-skills) | [Create Your Own](#creating-a-skill) | [Contribute](#contributing)

</div>

---

## The Problem

Every AI agent project starts the same way: you spend days writing prompts, chaining tools, handling edge cases, and debugging outputs for tasks that thousands of developers have already solved. Stock research, document generation, code review, data analysis -- the same patterns, rebuilt from scratch, over and over.

## The Solution

**Agent Skills** is an open collection of modular, drop-in skill packages that give AI agents superpowers. Each skill is a self-contained folder with instructions, resources, and examples that any LLM-powered agent can load and execute.

Think of it as **npm for agent capabilities** -- install a skill, and your agent instantly knows how to do something new.

```
your-agent/
├── skills/
│   ├── stock-research/     # Analyze stocks and find trade setups
│   ├── pdf-generator/      # Create professional PDFs
│   ├── code-reviewer/      # Review PRs like a senior engineer
│   └── your-custom-skill/  # Build your own in minutes
└── ...
```

## Why Agent Skills?

- **Zero config** -- Each skill is a folder with a `SKILL.md`. Drop it in and go.
- **Model agnostic** -- Works with Claude, GPT, Gemini, open-source models, or any LLM that follows instructions.
- **Battle-tested patterns** -- Skills encode best practices so your agent doesn't have to figure them out.
- **Composable** -- Mix and match skills. Stack them. An agent with 10 skills is 10x more useful.
- **Community-driven** -- The best skills come from real-world usage. Contribute yours.

## Quick Start

**1. Clone the repo**

```bash
git clone https://github.com/wpn10/agent-skills.git
cd agent-skills
```

**2. Browse available skills**

```bash
ls skills/
```

**3. Use a skill with your agent**

Point your agent at any skill's `SKILL.md` file. The file contains everything the agent needs: instructions, examples, and guidelines.

```python
# Example: Load a skill into your agent's system prompt
skill_path = "skills/stock-research/SKILL.md"
with open(skill_path) as f:
    skill_instructions = f.read()

# Add to your agent's context
system_prompt = f"You have the following skill:\n\n{skill_instructions}"
```

**4. Create your own skill**

```bash
cp -r template/ skills/my-new-skill/
# Edit skills/my-new-skill/SKILL.md with your instructions
```

## Available Skills

| Skill | Description | Category |
|-------|-------------|----------|
| `stock-research` | Analyze stocks for short-term trading setups, momentum plays, and leveraged ETF opportunities | Finance |
| `learning` | Deep-learn any technical topic with structured guidance, Socratic questioning, and mastery gates | Education |
| `pdf` | Generate and manipulate PDF documents programmatically | Documents |
| `code-review` | Review code changes with senior-engineer-level feedback | Development |
| *Your skill here* | [Submit a PR!](#contributing) | - |

> More skills are being added regularly. Star the repo to stay updated.

## Creating a Skill

A skill is just a folder with a `SKILL.md` file:

```markdown
---
name: my-skill
description: What this skill does and when to use it
---

# My Skill

Instructions that the agent will follow.

## Examples
- Example usage 1
- Example usage 2

## Guidelines
- Be specific about inputs and outputs
- Include edge cases
- Show expected behavior
```

### Skill Design Principles

1. **Be specific** -- Vague instructions produce vague results. Tell the agent exactly what to do.
2. **Include examples** -- Show, don't just tell. Real input/output pairs are gold.
3. **Handle edge cases** -- What should the agent do when something goes wrong?
4. **Keep it focused** -- One skill, one job. Compose multiple skills for complex workflows.
5. **Test it** -- Run the skill 10 times. If it fails twice, rewrite it.

## Spec

The Agent Skills specification lives in [`/spec`](./spec). It defines the standard format so skills are portable across different agent frameworks and platforms.

For the full specification, visit [agentskills.io](https://agentskills.io).

## Project Structure

```
agent-skills/
├── skills/          # Skill implementations
│   ├── skill-name/
│   │   ├── SKILL.md        # Instructions + metadata
│   │   └── resources/      # Supporting files (optional)
├── spec/            # Agent Skills specification
├── template/        # Starter template for new skills
└── README.md
```

## Contributing

This project lives and dies by community contributions. Here's how to help:

**Add a skill**

1. Fork the repo
2. Create your skill in `skills/your-skill-name/`
3. Include a well-written `SKILL.md` with examples
4. Submit a PR with a short demo or description of what it does

**Improve existing skills**

Found a skill that could be better? Open a PR. Better instructions, more examples, edge case handling -- it all helps.

**Report issues**

If a skill doesn't work as expected, open an issue. Include what you tried, what happened, and what you expected.

**Spread the word**

Star the repo. Share it. Write about it. The more people using and contributing skills, the better every agent gets.

## Philosophy

AI agents are only as good as the instructions they're given. Most "agent frameworks" focus on tool orchestration and plumbing. That matters, but the real leverage is in **what you tell the agent to do** -- the prompts, the patterns, the guardrails.

Agent Skills is a bet that the community can collectively build a library of high-quality agent instructions that make every AI application better. Not another framework. Not another wrapper. Just good instructions, organized well, shared freely.

## License

Apache 2.0 -- use it however you want.

---

<div align="center">

Built by [wpn10](https://github.com/wpn10)

If this helped you, consider giving it a star. It helps others find it.

**[Star this repo](https://github.com/wpn10/agent-skills)**

</div>
