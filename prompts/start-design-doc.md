# Design Documentation Process

When planning a project, create structured design documentation as follows:

## Philosophy

This process optimizes for:

- **Honesty about unknowns** — Surface what you don't know before architecting around assumptions
- **Traceable decisions** — Every choice links back to a principle, proposal, or explicit trade-off
- **Validation over speculation** — Scenarios prove the design works; proposals prove decisions were reasoned

## Core Structure (Always)

```
docs/design/
├── README.md                # Navigation hub with reading guides for different audiences
├── 00-open-questions.md     # Living tracker: decisions made, TODOs by priority (P0-P3), risk register
├── 01-executive-summary.md  # What, why, key goals (1-2 pages max)
├── 02-core-principles.md    # Design philosophy that guides all decisions
├── proposals/               # Deep dives on P0/P1 questions that need analysis
│   └── README.md
└── scenarios/               # End-to-end walkthroughs validating the design
    └── README.md
```

## Dynamic Sections (Project-Dependent)

Add numbered documents (03+) for each major concern the project has. Ask:

- What are the core abstractions? → Data Model doc
- What's the main algorithm/logic? → Algorithm doc  
- What are the integration boundaries? → Integration doc(s)
- What could break? → Edge Cases doc
- What non-functional requirements matter? → Scalability/Reliability/Security docs as needed

Don't create sections for concerns that don't exist.

## Process

1. **Start with open questions** — Brain-dump every decision and unknown. Prioritize P0-P3.
2. **Extract core principles** — What 3-5 beliefs should guide all decisions?
3. **Identify the major concerns** — These become your numbered documents.
4. **Write proposals for hard P0/P1s** — Problem → Options → Decision → Rationale
5. **Validate with scenarios** — 2-4 realistic walkthroughs proving the design works.
6. **Build README last** — Navigation tables, reading guides by audience.

## Conventions

- `TODO(Px-TAG)` — Open question with priority
- Link everything — Questions → Proposals → Scenarios → Back to index
- One question at a time in proposals — Don't bundle unrelated decision

