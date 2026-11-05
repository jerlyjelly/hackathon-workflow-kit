---
name: hackathon-build
description: Coordinate a timed application build from an unfamiliar brief, substantial input data, a domain contact, and strict deliverables. Use for hackathon or assessment implementation with parallel discovery, explicit assumptions, durable progress, and independent verification. Not for ordinary small feature edits or researching hackathon preparation.
---

# Hackathon Build

Coordinate discovery, domain clarification, decision criteria, algorithm selection, implementation, and verification. Adapt to the current assignment; assume no starter code. Do not import business rules, algorithms, schemas, or features from a previous round.

## Choose your role

If you received a scoped worker assignment from a lead, execute that assignment instead of restarting this project workflow. Read the supplied requirement IDs, current contract revision, relevant source material, allowed files/resources, and required checks. Use only the supporting skills needed for that assignment. Do not repeat bootstrap, create another project plan, reopen settled decisions without new evidence, or dispatch more agents unless the lead explicitly assigns a bounded delegation task. Return changed artifacts, the contract revision used, actual check results, and unresolved findings. Escalate business questions to the lead's shared queue. The Sol-only restriction and project instructions apply to every role.

The lead follows the stages below, owns shared decisions and state, and integrates worker results. Name each worker's role and execution mode when assigning work. Supporting skills supply engineering practices; they do not take over project coordination.

## Start and resume

1. Read the user's round instructions, repository guidance, supplied brief, data dictionaries, output specifications, and submission rules. Inventory the environment and inputs. Keep supplied sources intact.
2. Locate Superpowers and Stageshow. Use [skill-routing.md](references/skill-routing.md) to select only the skills needed now. A skill name does not guarantee its tool or model dependencies exist. If setup was authorized and a required skill is missing, follow the package's BOOTSTRAP.md and INSTALL.md before asking the user to install it. Ask only for an actual missing permission, unsupported capability, or information you cannot establish. Continue independent discovery. Do not silently substitute another design skill. Context7 is excluded.
3. Establish the actual deadline from the brief or user. If unavailable, ask while continuing discovery. Do not assume a three-hour limit. Set short discovery/formulation budgets, usually targeting an initial design within the first fifth, without skipping mandatory source inspection. Reserve roughly the final quarter for validation and delivery. Adjust to actual uncertainty and check time at milestones; reduce optional research, refinement, and review scope when time runs short.
4. All model-backed work, including reviewers and nested tools, must use GPT-6.1 Sol. Check effective model choices before dispatch; do not use a tool that silently calls another model. If compliant delegation is unavailable, work inline and report the limitation. Prefer higher supported effort for formulation and difficult diagnosis; routine implementation can use less.
5. On resume, read current state files and relevant source requirements before editing. Inspect the repository and necessary checks. Do not restart discovery or trust old passing results after relevant code, input, or settings changed.

## Durable state

Reuse the user's established equivalents. Otherwise keep:

- `AGENTS.md`: concise working rules and pointers to state files. Merge relevant parts of [the fragment](assets/AGENTS.fragment.md); preserve existing guidance.
- `PRD.md`: requirements with source references and acceptance checks, confirmed domain answers, open questions, assumptions, justified decision criteria and priorities, algorithm rationale, and shared data/API contracts.
- `PROGRESS.md`: absolute deadline with timezone, submission directory, chatbot access/relay method, active worker IDs/assignments when available, current requirements revision, dependencies, current task, remaining work, failures, and verification evidence. Separate pending, implemented, and verified states. Record tested input/settings and code revision or working-tree state. Record unknown operational fields explicitly until resolved.

The lead owns shared state. Workers return findings or write only assigned notes. Link detailed plans/reports instead of creating competing requirement or task lists. Update after consequential discoveries and completed milestones, before handoffs, and before compaction when possible. Keep updates current rather than relying on a pre-compaction event. A fresh session must be able to identify the next action from disk.

Use the client's automatic compaction normally. This workflow does not impose context-percentage thresholds, report-length quotas, or routine manual compaction. Recover from maintained project state when needed.

## 1. Discover in parallel

Use one lead and two scoped scouts when tools and quota support them:

- The lead reads the full brief, checks runtime/submission constraints, and owns the domain question queue.
- A data scout profiles inputs programmatically: schemas, counts, keys, references, missing/duplicate values, ranges, and task-relevant anomalies. Report scan coverage, evidence, and interpretation separately. A sample cannot establish whole-dataset validity.
- A requirements scout independently extracts mandatory behavior, exact output rules, exclusions, contradictions, and acceptance checks from supplied sources.

Give scouts source paths and bounded deliverables. Raw datasets and long logs stay on disk. Return concise findings and reproducible queries. Preserve original data; proposed repairs need an explicit rule and audit trail. A surprising value is not automatically corrupt.

After runtime constraints are understood, scaffold and smoke-test the simplest suitable stack. Avoid domain implementation that depends on unresolved semantics.

## 2. Clarify consequential unknowns

Maintain one question queue. Prioritize answers that change eligibility, data meaning, constraints, objectives, or output. Each question names observed evidence and the implementation decision it affects.

Use an authorized domain-chatbot interface only if the user permits direct interaction. Otherwise give the user a short batch to relay, then record returned answers. Continue independent work while answers are pending. Do not invent answers or treat a general complaint as an approved feature. If an answer conflicts with the brief, surface the conflict and request resolution; do not silently discard either source. Label provisional choices and isolate their implementation so they can be changed.

Classify unresolved questions by their effect. Missing facts that determine mandatory validity, eligibility, or required outputs block only the dependent behavior unless the brief provides an applicable policy. If the brief delegates objective or engineering choices, make a justified, adjustable decision and record it as your choice; do not wait for confirmation of every preference. Reversible implementation and cosmetic choices are the lead's responsibility. Silence is not confirmation of a business fact or permission.

When new facts or requirements arrive, trace their effect through PRD, decision criteria, algorithm choice, contracts, implementation, and acceptance checks. Revisit affected priorities before continuing dependent algorithm work. Mark affected verification stale, notify the relevant workers, and interrupt or reassign only dependent work. Keep unrelated work moving. Do not silently continue against a superseded contract or restart the entire project.

## 3. Define and rank decision criteria

Perform this stage after synthesizing the initial scouting and first available domain clarifications, before selecting an algorithm. Available data determines what can be measured; it does not by itself establish business importance. Do not choose an objective merely because a familiar algorithm optimizes it.

1. Identify candidate factors from the brief, scouting evidence, affected users, and domain answers. Record the source and reason for including each factor. Label inferred priorities as assumptions; do not present a plausible preference as a confirmed requirement.
2. Separate hard constraints, optimization preferences, and tie-breakers. An ideal target is not automatically a hard limit. Hard-constraint violations cannot be compensated for by a better preference score. If no optimization is needed, document the required deterministic rules instead of inventing a ranking problem.
3. Define each factor's metric, units, desired direction, and aggregation across people, items, or time. Distinguish averages, worst cases, and the number meeting a threshold. Identify the required data, justified estimates, and measurement limitations. Do not silently substitute an available proxy for the intended outcome.
4. Choose and justify how factors interact: strict priority order, weighted tradeoffs, or another explicit rule. For strict priorities, explain what cannot be traded away. For weighted scores, address different units/scales and justify weights; avoid arbitrary numbers or double-counting the same benefit. Justify thresholds separately from their priority. Define stable tie-breaking for equally ranked outcomes. If a randomized or time-limited search is justified, record its settings and reproducibility limits rather than promising identical results.
5. Compare a few contrasting candidate outcomes using the proposed criteria before choosing an algorithm. Check that preferred outcomes match the intended business judgment, including relevant outliers or disadvantaged groups. When assumptions about thresholds or weights could change the choice, compare plausible alternatives. Investigate infeasible targets; record an authorized fallback or report infeasibility rather than silently relaxing a hard rule.
6. Record a compact decision table in PRD: factor, source/assumption, constraint/preference/tie-breaker, metric and data support, threshold or priority/weight, and rationale. Include the outcome comparisons, unresolved questions, and fallback policy. Ask about missing mandatory business facts; continue independent work. Documented choices within delegated engineering judgment can guide implementation. Clearly provisional alternatives can support reversible prototypes while blocked facts are clarified; do not describe assumptions as confirmed answers.

This is a reasoning checkpoint, not a routine user-approval gate. Once the criteria are sufficiently grounded and recorded, proceed. Revisit them when new evidence changes the objective or its interpretation.

## 4. Choose the algorithm and plan

Use the recorded criteria to state the inputs, decisions the program makes, feasible outputs, expected scale, and runtime budget. Select a simple feasible baseline and, only if useful, a stronger alternative. Explain how each respects hard constraints and pursues the chosen priorities, including computational cost, approximation, and unsupported criteria. Do not quietly change the criteria to fit an implementation shortcut.

Where applicable, distinguish invalid input, established infeasibility, a feasible result, and search exhaustion without a result. A timeout does not prove infeasibility. Specify truthful handling for each outcome relevant to the task.

Test the riskiest assumption with a small executable example. Give a separate Sol reviewer the original rules, criteria table, contrasting outcomes, and proposed algorithm to find counterexamples. Review both whether the objective is justified and whether the algorithm implements it. Where practical, compare tiny instances against an exact reference using the same criteria and quantify heuristic quality; do not claim optimality from feasibility tests.

Use `writing-plans` for a concise plan with meaningful, independently checkable milestones, file ownership, dependencies, and contracts. Keep the design in PRD and current status in PROGRESS. Stabilize shared contracts before dependent parallel work. Avoid writing a second copy of the implementation in the plan.

## 5. Build a complete path early

Get real input through validation, core computation, required persistence, user-facing output, and the specified export/submission interface. Verify this path before substantial optional improvements.

With three agents, the lead owns core/backend integration, one worker owns functional UI, and one owns independent verification. Adjust this division to actual bottlenecks and available concurrency. The lead controls contracts and integration. Parallelize only work with stable interfaces and disjoint write ownership. Each worker gets source requirements, requirement IDs, current contract revision, allowed files/resources, execution mode, and expected checks. Assign ownership of shared manifests, lockfiles, migrations, generated outputs, test databases, and service ports as well as source files. Before integration, check that results use the current contract and rerun checks affected by later changes. Workers do not launch another project orchestrator.

Use Stageshow for the visual guide and relevant examples. Connect actual controls to application behavior. Bound UI polish by the assignment's priorities. For Korean copy, use functional labels, consistent terminology, and concise explanations; preserve facts and uncertainty. Read [UI guidance](references/ui-guidance.md) when frontend work starts.

## 6. Verify and improve continuously

Derive acceptance checks from source requirements before relying on implementation. Test core logic and consequential state transitions first. Add property-based tests when useful invariants exist and the dependency is justified; they do not choose the algorithm or prove optimality.

Measure solution quality against the recorded criteria as well as checking feasibility. Compare the baseline and improvements using the same inputs and criterion definitions. Report individual criterion values alongside any combined score. Test that ranking behavior matches the recorded contrasting outcomes; report tradeoffs and unmet preferences separately from hard-rule violations.

Once the complete path works, each improvement should address a missing requirement, observed failure, or measured improvement under the recorded criteria. Avoid optional rewrites or cosmetic expansion while required behavior remains unverified.

Use an independent checker for strict outputs where feasible. Feed it deliberately invalid outputs to check that it detects violations. Exercise normal input, relevant boundaries, modified valid input, and malformed input. Do not weaken a source requirement to fix a failing test.

Run the application and use browser tools for representative workflows and rendered screenshots. Use `systematic-debugging` for failures. Review substantive milestones for spec compliance and correctness, reproduce findings, and integrate fixes. Rerun affected checks after changes; run final required checks on the integrated state.

## 7. Finish against the current brief

Near the deadline, prioritize missing mandatory behavior, invalid outputs, and failed integration over optional optimization or cosmetic work. Time pressure never turns unverified work into a passing result.

Start diagnosis of a known mandatory failure immediately; do not wait for a final-review ceremony. A reviewer can check unaffected requirements concurrently with the owner's fix when scopes are independent. Keep required checks, and explicitly report any coverage that the deadline prevents.

Use `verification-before-completion`. Check the required startup path, persistence/container behavior when required, real output format, UI flows, and submission contents. Keep source briefs, plans, context files, and required history. Ensure worker changes and dependencies are in the submitted directory. Write required documentation from actual implementation and evidence. Report unresolved defects and untested areas precisely.

## Contest preferences

When the user adopts this workflow through the launch prompt, apply these project preferences to supporting skills:

- Proceed through reversible local work without repeated design or phase approval requests. Present material choices and ask about unresolved business facts or permissions; continue unrelated work.
- Review coherent milestones rather than tiny edits. Use test-first development for core behavior, validation, outputs, and bug fixes. Visual-only edits, generated scaffolding, and configuration use appropriate build, smoke, or visual checks. Do not delete working code merely because it preceded a test.
- Keep one lead. Supporting skills must not create a competing project workflow. Worktrees depend on isolation needs and submission compatibility. Do not move final work outside the submission directory or perform branch finishing merely because a generic workflow requests it.
- Preserve the lead's execution mode in plans and worker instructions. A supporting skill's template must not automatically introduce another mandatory executor, reviewer cycle, or project plan. Select supporting skills for each workstream and reconsider that selection when its task changes.
- Preserve task evidence. Do not automatically delete plans, history, or review artifacts. Follow actual submission retention rules.
- Use Stageshow as scoped visual guidance. Skip demonstration-only cursor choreography, filming, marketing framing, and mock-data staging unless requested. Keep screenshot verification of the real UI.
- Explicit round instructions can revise these preferences. They do not override host permissions, higher-priority instructions, or competition rules.
