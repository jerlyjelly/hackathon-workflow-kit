# Supporting skill routing

Install Superpowers as a package if desired, but load skills as their jobs become relevant. Resolve names against the installed version. This file describes integration choices; read the actual skill before using it. Apply the user's adopted contest preferences when its default process differs.

The lead owns phase order, contracts, task ownership, and execution mode. Workers follow their assigned mode rather than starting the whole workflow. A generated Superpowers plan must preserve that choice; replace default template language that would require a competing execution workflow. Do not invoke both execution modes as successive mandatory phases.

Git version control is required even when worktrees and branch-finishing skills are unnecessary. In a shared working tree, the lead performs commit steps from supporting skills after reviewing the scoped changes; workers do not independently mutate the shared index. Use the main skill's baseline and milestone commit rules.

| Skill | Use in this workflow |
| --- | --- |
| `using-superpowers` | Package discovery/bootstrap. Do not ask the user to invoke it at every phase. |
| `brainstorming` | After initial scouting, clarify and justify decision factors, metrics, priorities, and tradeoffs before choosing an algorithm. Revisit them for consequential requirement changes. Adopted contest preferences replace repeated design approval gates. |
| `dispatching-parallel-agents` | Independent requirements/data discovery, separate investigations, and implementation with stable interfaces and disjoint ownership. Parallel calls do not make dependent work independent. |
| `writing-plans` | A dependency-aware plan after criteria and algorithm rationale are recorded. Reference PRD as the specification and PROGRESS as current task state. Preserve the lead's chosen execution mode rather than copying a mandatory nested-executor header. |
| `test-driven-development` | Core rules, validation, output contracts, consequential state changes, and regressions. Apply contest exceptions for visual-only work, generated scaffolding, and configuration. |
| `systematic-debugging` | Reproduce unexpected behavior and find its cause before patching. Preserve failures as evidence. |
| `requesting-code-review` | Independent review of coherent milestones and before delivery. Include source requirements, the criteria and rationale, contract revision, exact diff/revision or file set, tests, and limitations. Check business-objective alignment as well as code correctness. In a new repository without a base commit, review current files explicitly; do not invent a base SHA. |
| `receiving-code-review` | Check findings against requirements and actual behavior before changing code. Resolve uncertainty for dependent changes while continuing unrelated work. |
| `verification-before-completion` | Before marking requirements verified or reporting completion. Evidence must apply to integrated code and current inputs. |

## Conditional execution skills

- `subagent-driven-development`: for a bounded subsystem when fresh implementer/reviewer cycles justify their overhead. Not an additional orchestrator for the entire project. Name the bounded owner and prohibit recursive delegation beyond the lead's allocation.
- `executing-plans`: for work intentionally implemented inline, or when compliant subagents are unavailable. An alternative mode, not a second mandatory pass after delegated execution.
- `using-git-worktrees`: when concurrent edits justify isolation and integration back into the submitted tree is practical. Do not assume the grader finds other worktrees.
- `finishing-a-development-branch`: only if branch integration is part of the task. Local validation and submission readiness suffice when no merge/PR is requested.
- `writing-skills`: preparation only; avoid competition-time workflow maintenance unless it is materially broken.

The default is one lead coordinating a few meaningful workstreams. Installing the package does not require invoking every skill or giving every worker every reference.

## Other tools

- Stageshow: selected visual examples and craft guidance for the UI owner. Read [ui-guidance.md](ui-guidance.md).
- Browser verification: available Playwright CLI, Playwright MCP, or another authorized browser tool. Confirm it reaches the local app. If unavailable, perform executable API checks and report missing browser coverage.
- Trail of Bits `property-based-testing`: optional when useful invariants exist. Do not install its whole collection or invent a dependency requirement.
- Korean UX: an already selected writing skill if available, or the short rules and official references in ui-guidance.md. No new writing package is assumed installed.
- Documentation: local dependency documentation or official sources as needed. Do not connect or invoke Context7. No other MCP is required.

## Sources

Routing was reviewed against public source files on 2026-11-05. The package dependency manifest records revisions for new installations. Recheck the installed version when behavior differs.

- [Superpowers skills](https://github.com/obra/superpowers/tree/main/skills)
- [User-instruction precedence](https://github.com/obra/superpowers/blob/main/skills/using-superpowers/SKILL.md)
- [Stageshow](https://github.com/benjitaylor/skills/blob/main/stageshow/SKILL.md)
- [Codex skill discovery and invocation](https://learn.chatgpt.com/docs/build-skills)
