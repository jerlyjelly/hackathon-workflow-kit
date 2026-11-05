# Using the workflow

For a new VM, start with [BOOTSTRAP.md](BOOTSTRAP.md) to inspect the environment and install the workflow and its dependencies. For repository-local discovery, copy `hackathon-build/` to the target project's `.agents/skills/hackathon-build/`; alternatively use a compatible skill installer for a user-scoped installation. Superpowers and Stageshow are separate dependencies.

## Setup and start in a new VM

```text
Set up and run the workflow from https://github.com/jerlyjelly/hackathon-workflow-kit.
Read BOOTSTRAP.md and follow it. Adopt hackathon-build's workflow and Contest preferences as my project instructions.
Inspect this environment, install missing required skills using compatible methods, verify their availability, and begin with the supplied brief and data.
Use only GPT-6.1 Sol for every worker and reviewer. I will relay domain-chatbot questions and answers. Ask for consequential information you cannot determine from the supplied material, and continue independent work while waiting.
```

Use the setup prompt above for a new environment, or the launch prompt below when setup is complete. The agent should move through phases itself. The other prompts are recovery or steering controls, not mandatory steps to paste sequentially. Replace brace-delimited fields with the current round's information. If unknown, say `unknown` rather than guessing.

## Launch

```text
Use $hackathon-build for this round. Adopt its workflow and Contest preferences as my project instructions, including its scoped use of supporting skills. Delegate routine engineering choices and continue reversible local work without phase-by-phase approval. Ask about consequential business unknowns and continue independent work while waiting.

Brief and specifications: {paths}
Input data: {paths}
Deadline: {date, time, timezone}
Submission directory: {path}
Domain chatbot: I will relay your questions and its answers.

Use only GPT-6.1 Sol, including every worker and reviewer. Start with one lead and two scouts when supported. Use Superpowers selectively and Stageshow for the visual guide. Do not use Context7. Preserve source materials and required submission evidence. Keep AGENTS.md, PRD.md, and PROGRESS.md current, reusing existing equivalents.

Begin by inspecting supplied material, profiling data, and independently checking requirements. After scouting and initial clarification, explicitly define and justify decision factors, metrics, priorities, and tradeoffs before choosing an algorithm. Then carry the task through a working application, verification, and required deliverables.
```

For permitted direct chatbot interaction, replace the relay sentence with the authorized interface and interaction scope. The default prompt does not authorize messaging through unrelated services.

## Resume after interruption or context loss

```text
Resume $hackathon-build under the existing round instructions. Read AGENTS.md, PRD.md, PROGRESS.md, and source requirements relevant to the current task. Check actual repository state and active workers before editing. Continue the next incomplete milestone without restarting discovery. Rerun checks whose evidence is stale. Preserve the existing deadline and Sol-only restriction.
```

## Incorporate a domain answer or changed requirement

```text
Continue $hackathon-build. Here is new information from {source}:
{answer or revised requirement}

Record its source, reconcile it with the brief, and identify affected assumptions, decision criteria, algorithm choices, contracts, implementation, and tests. Revisit affected rankings before continuing dependent algorithm work. Reassign or interrupt only affected work. Keep unrelated work moving. Do not treat suggestions as mandatory features without support from the task.
```

## Deadline review

```text
Continue $hackathon-build in delivery mode. Remaining time: {duration}. Freeze optional expansion. Have an independent Sol reviewer compare the integrated application and actual outputs with the original requirements and recorded clarifications. Fix mandatory failures first, rerun affected and required final checks, and preserve submission evidence. Report verified behavior, remaining defects, and anything not tested. Do not claim completion merely because time is ending.
```

## Before installation

Replace `$hackathon-build` with `the workflow in /absolute/path/to/hackathon-build/SKILL.md`. Reading a draft explicitly works without changing global configuration. Superpowers and Stageshow must still be available.
