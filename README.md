# Hackathon Workflow Kit

A reusable workflow for building an application from an unfamiliar brief, substantial input data, domain clarifications, and strict deliverables under a deadline.

The workflow uses GPT-6.1 Sol throughout. It coordinates Superpowers for engineering practices and Stageshow for visual guidance. Context7 is excluded.

## Start in a new VM

Paste this into the coding agent:

```text
Set up and run the workflow from https://github.com/jerlyjelly/hackathon-workflow-kit.
Read BOOTSTRAP.md and follow it. Adopt hackathon-build's workflow and Contest preferences as my project instructions.
Inspect this environment, install missing required skills using compatible methods, verify their availability, and begin with the supplied brief and data.
Use only GPT-6.1 Sol for every worker and reviewer. I will relay domain-chatbot questions and answers. Ask for consequential information you cannot determine from the supplied material, and continue independent work while waiting.
```

For a repeatable setup, use a tag or commit instead of the moving default branch. Start with [BOOTSTRAP.md](BOOTSTRAP.md), then use [PROMPTS.md](PROMPTS.md) for launch details and later steering.

## Flow

1. Inspect the environment and scout requirements and data in parallel.
2. Clarify consequential business meanings and uncertainties.
3. Define, measure, rank, and justify decision criteria.
4. Select an algorithm that follows those criteria and plan implementation.
5. Build a complete path through real input, processing, UI, and required outputs.
6. Verify mandatory behavior and solution quality independently.
7. Deliver the integrated work and required evidence.

## Package

| File | Purpose |
| --- | --- |
| [BOOTSTRAP.md](BOOTSTRAP.md) | Environment inspection and dependency installation |
| [PROMPTS.md](PROMPTS.md) | Launch, resume, clarification, and deadline prompts |
| [hackathon-build/SKILL.md](hackathon-build/SKILL.md) | Main workflow |
| [skill-routing.md](hackathon-build/references/skill-routing.md) | Which Superpowers skills to use and when |
| [ui-guidance.md](hackathon-build/references/ui-guidance.md) | Stageshow usage and Korean product copy |
| [AGENTS.fragment.md](hackathon-build/assets/AGENTS.fragment.md) | Project guidance to merge into an existing AGENTS.md |

Install the complete `hackathon-build` directory, including its references, assets, and metadata. Installing this directory alone does not install Superpowers, Stageshow, a browser, or application dependencies.

## Dependencies

- [Superpowers](https://github.com/obra/superpowers): install the complete package through a method supported by the actual coding environment.
- [Stageshow](https://github.com/benjitaylor/skills/tree/main/stageshow): install the complete skill with its references, examples, and supporting resources.
- Browser verification: use an available compatible tool, such as [Playwright CLI](https://github.com/microsoft/playwright-cli), when the task includes a web application.
- [Property-based testing](https://github.com/trailofbits/skills/tree/master/plugins/property-based-testing): optional for algorithms with useful invariants.

The required third-party skills are installed from their own repositories. Their implementations are not bundled here.

## Validation status

The skill structure and local document links have been checked. An earlier draft received an independent scenario review covering ambiguous data, changed requirements, context loss, and a failing export near the deadline. The package has not yet completed a full timed application-building rehearsal. Repository updates should be rehearsed before competition use.
