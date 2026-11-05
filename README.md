# Hackathon Workflow Kit

A reusable workflow for building an application from an unfamiliar brief, substantial input data, domain clarifications, and strict deliverables under a deadline.

The workflow uses GPT-6.1 Sol throughout. It coordinates Superpowers for engineering practices and Stageshow for visual guidance. Context7 is excluded.

## Start in a new VM

Paste this into the coding agent:

```text
Set up and run my hackathon workflow from:
https://github.com/jerlyjelly/hackathon-workflow-kit/tree/v0.3.0

Read BOOTSTRAP.md, INSTALL.md, and dependencies.json from that version.
Inspect the actual environment and existing project instructions.
Install missing hackathon-build, Superpowers, and Stageshow resources
using the documented installation path and fallback. Preserve existing
files and verify what is installed, discoverable, and usable.
Do not use Context7.

Adopt hackathon-build's workflow and Contest preferences as my project
instructions. Use only GPT-6.1 Sol for every worker and reviewer.
Use one lead and two scoped scouts when supported. Workers should
follow their assignments without repeating project setup or planning.

Find and read the supplied brief, data documentation, datasets, output
specifications, and submission rules. Establish the deadline and
submission directory from the supplied material, asking me if missing.
I will relay domain-chatbot questions and answers.

After scouting and initial clarification, explicitly define and justify
decision factors, metrics, priorities, and tradeoffs before choosing an
algorithm. Ask about missing mandatory business facts, continue
independent work, and make documented choices where the brief delegates
engineering judgment. Do not ask for routine phase-by-phase approval.

Use Git for local application version control, with a baseline commit
and commits for working milestones and verified fixes. The lead owns
Git mutations when workers share a working tree.
Bind user-accessible web servers to 0.0.0.0 on the environment-required
ports unless explicit platform instructions differ. Verify the actual
listening address and document the real access URL.

Keep AGENTS.md, PRD.md, and PROGRESS.md current. Carry the task through
a working application, independent verification, and required deliverables.
```

The prompt selects `v0.3.0`; its dependency manifest pins newly downloaded supporting skills. Start with [BOOTSTRAP.md](BOOTSTRAP.md) and [INSTALL.md](INSTALL.md), then use [PROMPTS.md](PROMPTS.md) for launch details and later steering. Reuse existing working installations with their revision differences recorded.

## Flow

1. Inspect the environment and scout requirements and data in parallel.
2. Clarify consequential business meanings and uncertainties.
3. Define, measure, rank, and justify decision criteria.
4. Select an algorithm that follows those criteria and plan implementation.
5. Build a complete path through real input, processing, UI, and required outputs.
6. Verify mandatory behavior and solution quality independently.
7. Deliver the integrated work and required evidence.

Use local Git throughout implementation, including a baseline and working milestone commits. Bind user-accessible web servers to `0.0.0.0` on the environment-required ports unless explicit platform instructions differ, and verify the listening configuration and actual access URL.

## Package

| File | Purpose |
| --- | --- |
| [BOOTSTRAP.md](BOOTSTRAP.md) | Environment inspection and dependency installation |
| [INSTALL.md](INSTALL.md) | Preferred installation path, fallback, and concrete checks |
| [dependencies.json](dependencies.json) | Pinned source revisions and required files |
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

The skill structure and local document links have been checked. An earlier draft received an independent scenario review covering ambiguous data, changed requirements, context loss, and a failing export near the deadline. Version 0.2.0 incorporated a source review of installation, worker roles, workflow boundaries, and decision criteria. Version 0.3.0 adds explicit application Git checkpoints and web-server binding/access checks. Pinned source revisions and required files have been checked. A live VM rehearsal was stopped before the agent ran; this package has not completed an end-to-end installation or timed application-building rehearsal.
