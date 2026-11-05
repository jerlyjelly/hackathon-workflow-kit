## Round workflow

Use the `hackathon-build` skill for this round. Locate and read its SKILL.md before beginning or resuming implementation; use the installed path shown by skill discovery. The launch prompt adopts its contest preferences for supporting skills.

- Read PRD.md for requirements, sources, domain answers, assumptions, and contracts. Read PROGRESS.md for current tasks, owners, failures, and evidence. Reuse equivalent paths if the lead records them here.
- The lead owns shared state and execution mode. Workers follow their scoped assignment and do not repeat project setup or planning. Only the lead dispatches further work unless it grants a bounded exception.
- Use GPT-6.1 Sol for every model-backed role. Never silently substitute another model. Work inline if compliant delegation is unavailable.
- Use Superpowers selectively and Stageshow for visual guidance. Do not use Context7.
- Preserve source briefs and original data. Distinguish observations, confirmed domain answers, and assumptions. Ask about consequential unknowns while continuing independent tasks.
- After scouting and initial clarification, record and justify decision factors, metrics, priorities, and tradeoffs in PRD before choosing an algorithm. Revisit affected criteria when domain answers change; check solution quality separately from mandatory correctness.
- Treat missing mandatory business facts separately from delegated objective or implementation choices. Block only dependent work; make and document delegated choices without repeated approval requests.
- Assign ownership of shared manifests, lockfiles, migrations, test data, and ports. Worker results must identify the contract revision they used.
- Use Git for application version control: reuse or initialize the actual application repository, create a baseline, and commit working milestones and fixes. The lead owns Git mutations in a shared working tree. Preserve unrelated changes and record commit/check evidence. Do not push the competition project without explicit authorization.
- Bind user-accessible web servers to `0.0.0.0` on the environment-required ports unless explicit platform instructions differ. Verify the real listening address and access URL; `0.0.0.0` is not a port or the URL to advertise to users.
- Mark work implemented before verified. Update progress at milestones and handoffs. Recheck affected evidence after changes.
- Preserve plans and required submission evidence. Deliver integrated work in the actual submission directory.

Merge this fragment with existing project guidance. Do not replace a supplied AGENTS.md or add it to unrelated repositories.
