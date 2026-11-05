# Installation procedure

Use this procedure after the environment inspection in [BOOTSTRAP.md](BOOTSTRAP.md). These are installation instructions, not a claim that every client/version has been tested.

## Sources and revisions

Resolve the workflow's requested tag or commit once and retain that complete checkout. Use [dependencies.json](dependencies.json) for missing Superpowers and Stageshow installations. Obtain public source through Git or HTTPS; no GitHub account connection is required for these public downloads.

Reuse a complete working installation after checking its identity and required files. If its revision differs from the manifest, record the difference and preserve it; do not silently replace or duplicate it. For newly downloaded dependencies, check out the manifest's exact commit and verify it before installation. Do not silently switch to a moving default branch when a pin fails.

For Git downloads, the sequence is: clone the repository into a dedicated dependency directory, check out the specified commit detached, then compare `git rev-parse HEAD` with the expected revision. For a commit archive, use the immutable commit URL and record the download source. Retain the full Superpowers repository because individual skills can reference shared helpers and adjacent skills.

Keep dependency checkouts inside the permitted project area, separate from application code, for example `.workflow-deps/`. Use a different non-conflicting path if that directory already serves another purpose. Retain licenses and supporting files. Do not copy an existing Git configuration, credential file, or unrelated user environment into this project.

## Preferred path: native skill discovery

When the installed Codex version supports project skills in `.agents/skills/`:

1. Install the complete custom `hackathon-build/` directory there, including metadata, references, and assets. Retain the workflow checkout containing bootstrap, installation instructions, and the dependency manifest.
2. Install the complete `stageshow/` directory there. Keep its examples, kit, references, scripts, and notices.
3. Retain the complete pinned Superpowers repository under the dependency directory. On a platform that supports skill-directory symlinks, expose each directory under its `skills/` containing a SKILL.md through a relative symlink in `.agents/skills/`. Each link must target that skill's directory in the retained repository. Resolve supporting resources from their canonical repository paths. Do not copy only SKILL.md files or detach skills from helpers they need.
4. Check each destination for an existing skill or naming conflict before creating it. Preserve existing content. Record canonical source paths and discovery paths so workers can find the real resources.

The Superpowers source stays inside the submission tree. Relative symlinks must resolve within that tree, not into a private user directory. If the submission packager does not preserve links, or the client cannot discover them, use the fallback below. Do not claim symlink portability without checking the actual submission method.

This path installs native skill instructions. It does not assert that plugin hooks or marketplace integrations are active. Those are not prerequisites for following this workflow's explicit launch instructions.

## Fallback: supported installer or plugin facilities

If native discovery is unsupported, use the client's available skill/plugin installer and the upstream instructions for the pinned sources. Inspect the actual CLI help before selecting commands. Codex versions may differ; do not use another client's command syntax.

Prefer a supported local-source installation from the pinned checkout. If the installer only accepts a marketplace version, record the resolved version and its difference from the manifest. Preserve required resources. Do not describe a marketplace installation as pinned to the manifest unless that has been established.

Use one preferred attempt and one fallback, with a short initial setup budget appropriate to the deadline. A demonstrably progressing download may justify extending it. If installation is blocked, save the exact failure and continue independent requirements/data inspection. Required skill documents that are already readable can be followed explicitly from their canonical paths while discovery is repaired. This is a documented fallback, not a claim that registration or hooks succeeded. Do not repeatedly browse installation options or reconfigure working tools.

## Verify and record

For each required component, record in `SETUP.md` or an established equivalent:

- Repository, expected revision, resolved revision when available, and canonical local path.
- Whether the full install unit and every `required_files` entry exist.
- Whether the client lists the skill and whether the current session can read it.
- Any supporting executable actually run and its result; missing runtimes or hook functionality must remain explicit.
- Any client reload required and the exact resume instruction.

Verify discovery once after setup using the client's supported skill listing. If a reload is necessary, preserve setup state and request that minimal action. Do not repeatedly restart the client or redo installation. Check task-specific browser/tool usability when that tool is first needed.

Installation is successful only to the extent established by these checks. File presence, discovery, and executable capability are distinct. Continue into `hackathon-build` after setup and report any remaining limitation.
