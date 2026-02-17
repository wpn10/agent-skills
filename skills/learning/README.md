# Learning Skill

An interactive tutoring skill that takes you from zero to mastery on any technical topic.

## What It Does

This skill transforms your AI agent into a structured, interactive tutor. Instead of dumping information, it guides learners through a proven pedagogical framework that combines:

- **Feynman Technique** -- explain concepts back in your own words to solidify understanding
- **Socratic Method** -- targeted questions that lead you to answers instead of handing them over
- **Bloom's Taxonomy** -- progressive cognitive levels from remembering facts to creating novel solutions
- **Project-Based Learning** -- hands-on exercises and a capstone mini-project

## How It Works

The skill runs through four phases:

### Phase 0: Setup
Assesses your current level, goal, time commitment, and learning style. Builds a personalized learning map with modules tailored to your needs.

### Phase 1: Teaching
Each module follows a tight loop:
1. **Introduce** -- simple analogies and minimal code examples
2. **Check** -- Socratic questions to verify understanding
3. **Apply** -- hands-on coding challenge or scenario
4. **Feynman Check** -- teach the concept back every 2-3 modules

### Phase 2: Active Recall
Spaced repetition questions woven throughout to strengthen retention.

### Phase 3: Mini-Project
A guided project using 3+ concepts from the learning path, broken into milestones.

### Phase 4: Mastery Verification
Final assessment climbing Bloom's Taxonomy -- from recall to creation.

## Usage

```
/learning [topic]
```

**Examples:**
- `/learning rust` -- learn the Rust programming language from scratch
- `/learning system design` -- master system design for interviews
- `/learning kubernetes` -- understand container orchestration end-to-end
- `/learning algorithms` -- study data structures and algorithms

## What Topics Work?

Any technical subject:
- Programming languages (Python, Go, Rust, TypeScript, etc.)
- Frameworks (React, Django, Spring Boot, etc.)
- System design and architecture
- Algorithms and data structures
- DevOps and infrastructure (Docker, K8s, CI/CD)
- Databases (SQL, NoSQL, query optimization)
- Networking (TCP/IP, DNS, HTTP)
- Math and science fundamentals

## Key Features

| Feature | Description |
|---------|-------------|
| Progress tracking | Visual learning map updated after each module |
| Mastery gates | Cannot advance until understanding is verified |
| Focus enforcement | Off-topic questions are parked and revisited later |
| Adaptive pacing | Skips modules you already know, slows down where needed |
| Session management | Pick up where you left off across sessions |

## Design Principles

- **One concept at a time** -- no information overload
- **40% learner talking** -- interactive, not passive
- **Under 400 words per response** -- concise and focused
- **No advancing without verification** -- understanding is mandatory
