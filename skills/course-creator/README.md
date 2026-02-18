# Course Creator: Complete Technical Curriculum Generator

Generate structured, multi-day technical courses with hands-on labs, escalating challenges, real-world case studies, and capstone projects -- for any topic, any schedule.

## What It Does

Give it a topic and a schedule, and it builds a complete course from scratch. Not a reading list. Not a link dump. A full curriculum with day-by-day structure, exercises with progressive hints, labs that simulate real work, and a capstone project that ties everything together.

**What you get:**
- Day-by-day syllabus with time allocations
- 3-5 exercises per day across 7 different exercise types
- A hands-on lab every day with realistic scenarios
- Spaced recall built into the course structure
- 2-3 capstone project options
- Setup instructions, cheat sheets, and further reading
- Full solutions with explanations (hidden behind spoiler tags)

## How It Works

### Phase 0: Course Scoping
Uses interactive prompts (no typing required) to gather:
- Topic and depth level
- Schedule (days and hours per day)
- Audience (self-study, team training, public course)
- Prerequisites the audience already has
- Reference materials (URLs or local files to incorporate)
- Exercise style preference

### Phase 1: Course Architecture
- Decomposes the topic into concepts with dependency mapping
- Calculates time budget (15% concepts, 25% guided, 30% independent, 20% labs, 10% review)
- Designs a difficulty curve that never plateaus
- Structures each day with hook → learn → practice → integrate → preview arcs

### Phase 2: Content Generation
Produces the full course content for every day:
- Concept blocks with mental models, gotchas, and quick checks
- 7 exercise types: Build It, Fix It, Extend It, Design It, Investigate It, Debate It, Teach It
- Daily labs with realistic company scenarios and phased deliverables
- End-of-day checkpoints with self-assessment

### Phase 3: Capstone Project
Designs 2-3 capstone options with milestones, broken into the final days of the course.

### Phase 4: Packaging
Outputs a full directory structure with READMEs, exercise files, solutions, and resources.

## Usage

```
/course-creator [topic]
```

**Examples:**
- `/course-creator system design` -- 10-day deep dive into distributed systems
- `/course-creator rust` -- learn Rust from zero to production-ready
- `/course-creator kubernetes` -- hands-on K8s bootcamp
- `/course-creator machine learning` -- ML fundamentals to deployment
- `/course-creator SQL performance` -- advanced query optimization workshop

## What Topics Work?

Any technical subject that can be taught through structured progression:
- Programming languages (Python, Go, Rust, TypeScript, etc.)
- System design and distributed systems
- Cloud platforms (AWS, GCP, Azure)
- DevOps and infrastructure (Docker, K8s, Terraform, CI/CD)
- Databases (SQL, NoSQL, query optimization, data modeling)
- Machine learning and data science
- Security and penetration testing
- Algorithms and data structures
- Frontend/backend frameworks
- API design and microservices

## Exercise Types

| Type | What the Learner Does | When It's Used |
|------|----------------------|----------------|
| Build It | Build from a spec | Core skill practice |
| Fix It | Debug broken code/systems | Defensive thinking |
| Extend It | Add features to working code | Real-world modification |
| Design It | Architect a solution | System thinking |
| Investigate It | Root-cause a mystery bug | Debugging skills |
| Debate It | Argue for/against an approach | Trade-off analysis |
| Teach It | Explain to a hypothetical junior | Deep understanding |

## Course Output Structure

```
course-[topic]/
├── README.md              # Overview, schedule, setup
├── syllabus.md            # Full day-by-day syllabus
├── setup.md               # Environment and tool setup
├── day-01/
│   ├── README.md          # Concepts + exercises + lab
│   ├── exercises/         # Starter code, broken code, tests
│   └── solutions/         # Full solutions with explanations
├── day-02/
│   └── ...
├── capstone/
│   ├── README.md          # Project options and milestones
│   └── starter/           # Boilerplate code
└── resources/
    ├── cheatsheet.md      # Quick reference
    └── further-reading.md # Books, talks, articles
```

## Scheduling Formats

The skill adapts to any schedule:

| Format | Structure | Best For |
|--------|-----------|----------|
| Distributed | 1-2 hrs/day over 10-14 days | Working professionals, deep retention |
| Moderate | 3-4 hrs/day over 5-7 days | Balanced depth and pace |
| Intensive | 5-8 hrs/day over 3-5 days | Bootcamps, immersive workshops |

Cognitive load cycling is built in -- high-load concept blocks alternate with lower-load labs and discussions. Mandatory breaks are scheduled, not optional.

## Engagement Patterns Used

- **Problem-first** -- present the challenge before the theory
- **Surprising demos** -- counterintuitive examples that create curiosity
- **Constraint challenges** -- "build X without using Y"
- **Escalating problems** -- simple → add requirements → real engineering challenge
- **War stories** -- fictional outage scenarios that make concepts memorable
- **Deliberate mistakes** -- find the subtle bug in "correct-looking" code
- **Speed runs** -- 15-minute time-boxed builds that force prioritization
- **Spaced recall** -- concepts resurface 3+ times across the course
- **Fading scaffolding** -- guidance decreases as the course progresses

## Reference Material Support

The skill can incorporate your own materials:
- Paste URLs to documentation, articles, or tutorials
- Point to local PDFs, notes, or docs
- The course will weave your materials in as primary references alongside best-in-class public resources
