# Bootstrap in an unfamiliar environment

Use this procedure when the user asks to install and run this workflow. The user-authorized project is the competition workspace, not this kit's download directory. Preserve supplied files and follow the actual environment and competition rules.

## 1. Inspect before installing

- Identify the operating system, shell, working directory, repository/project root, writable locations, network access, and current coding client/version. Read existing AGENTS.md guidance and supplied setup instructions before changing anything.
- Inventory the supplied brief, data dictionaries, output schemas, datasets, and submission instructions with targeted file searches. Do not recursively dump data, logs, home directories, environment variables, or secrets into context.
- Check available runtimes, package managers, Git/download utilities, skill/plugin installation support, browser tools, and subagent capabilities once. Read the actual client's help or official documentation for unfamiliar commands; do not assume commands from another client are supported. Record the result and do not repeat successful setup investigation without a new failure.
- Confirm the active model and permitted worker configuration through available settings/tools. Every model-backed role must use GPT-6.1 Sol. Do not silently substitute a model or infer that a tool uses Sol merely from its name. If worker configuration cannot be verified, use the compliant main session inline and report the limitation.
- Determine the deadline, application workspace, submission directory, and domain-chatbot access from the brief. Ask for consequential missing facts while continuing independent setup. The default is that the user relays chatbot questions and answers.
- Determine the application's Git repository boundary and existing status. Reuse it or initialize a repository in the actual application workspace, then create an appropriate baseline before implementation. Follow SKILL.md's Git rules; downloading this kit is not application version control.
- For a web task, identify the required service ports and preview/forwarding mechanism. Plan to bind user-accessible web servers to `0.0.0.0` on the required ports, unless the platform explicitly specifies another binding. Record this configuration before launching servers.

## 2. Install the workflow and required skills

Read `hackathon-build/SKILL.md` and its `Contest preferences` before invoking supporting workflows. Preserve existing installations; inspect their identity and location before downloading another copy.

Required sources:

| Component | Source | What to install |
| --- | --- | --- |
| Hackathon Build | https://github.com/jerlyjelly/hackathon-workflow-kit | Complete `hackathon-build/` directory at the selected tag/commit |
| Superpowers | https://github.com/obra/superpowers | Complete package, including skill references and helper resources |
| Stageshow | https://github.com/benjitaylor/skills | Complete `stageshow/` directory and its supporting resources |

Follow [INSTALL.md](INSTALL.md), using [dependencies.json](dependencies.json) for missing dependency revisions. The preferred path is native project skill discovery with complete resources; the fallback is a compatible client installer or plugin facility. Use a short setup budget, one preferred attempt, and one fallback. Do not overwrite an existing installation or replace the supplied project with this kit. Do not claim discovery, hooks, or tool capability merely from a successful download.

Keep a temporary kit/dependency checkout separate from the application source. Keep installed assets in locations allowed by the environment. If submission rules require the actual skill/context files, ensure they are included in the submitted directory rather than relying on external symlinks or user-level installations.

Record the sources, resolved revisions when available, installation locations, and any restart or permission step in SETUP.md or an established equivalent. A version pin identifies the dependency used; it is not evidence that a new dependency combination has passed a rehearsal.

## 3. Add only task-relevant tools

- For a web app, reuse an available browser tool or install a compatible browser-verification tool and browser runtime, such as Playwright CLI. Prefer headless operation when required by the environment. Verify browser capability against the application once it exists.
- Consider the Trail of Bits property-based-testing skill only when the core logic has useful invariants and this would improve verification. It is optional, not a setup blocker.
- Korean copy guidance is already included in `hackathon-build/references/ui-guidance.md`; no extra writing package is required.
- Do not install or invoke Context7. Do not install Impeccable or another design workflow as a substitute for the user's chosen Stageshow.
- Application runtimes, frameworks, solver libraries, databases, and containers depend on the actual brief and discovered constraints. Install them when the selected implementation needs them, not as a large speculative tool bundle.

## 4. Verify setup and continue

Confirm that the complete custom skill and required supporting skills can be read and discovered by the client. Check referenced resources exist. Distinguish installed, discoverable, and usable capabilities. If a client reload is needed, save the setup state and give the user the exact minimal restart/resume instruction; do not pretend the current session gained unavailable tools.

Merge relevant project guidance from `hackathon-build/assets/AGENTS.fragment.md` into AGENTS.md without replacing existing instructions. Initialize or reuse PRD.md and PROGRESS.md in the application workspace. Record deadline/timezone, submission path, model restriction, setup limitations, and the next action. A missing registration should not stop independent source inspection or explicit use of already readable skill instructions. Do not substitute another skill silently or claim unavailable executable capabilities.

Give a brief setup report with the detected environment, skill locations, verified capabilities, and any necessary user action. Then continue using `hackathon-build` without requesting routine phase approval:

1. Scout the brief, data, and output requirements.
2. Ask consequential domain questions.
3. Define and justify ranking factors and their tradeoffs in PRD.
4. Choose the algorithm and implement a complete working path.
5. Verify, improve, and prepare the required submission.

Use one lead and two scoped scouts initially when compliant delegation is available. Adopt the user's selected Contest preferences, including targeted Superpowers use, Stageshow as visual guidance for a functional app, and retention of submission evidence. Never infer that setup permission authorizes publishing the competition project or messaging unrelated people.

Only the lead performs project bootstrap. Dispatched workers follow the worker entry point in SKILL.md and their assigned scope. Keep the client's normal automatic compaction behavior; no manual context budget or compaction schedule is required.
