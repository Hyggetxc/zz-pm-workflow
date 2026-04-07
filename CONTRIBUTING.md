# Contributing

## Scope

This repository is a modular PM skill pack for Codex-style workflows.

Contributions should preserve:

- orchestrator-first routing
- single-responsibility skill boundaries
- project-rules-first behavior
- clear separation between PM workflow and prototype workflow

## Contribution Rules

1. Do not merge unrelated capabilities into one oversized skill.
2. Prefer updating an existing skill boundary before adding a new skill.
3. Keep each `SKILL.md` focused on one capability domain.
4. When a new skill is added, update [`README.md`](./README.md) and [`AGENTS.md`](./AGENTS.md) in the same change.
5. Use relative links in docs so the repository remains portable.
6. Do not commit project-specific names, personal names, or absolute local paths.

## Recommended Change Flow

1. Define the capability boundary.
2. Decide whether it belongs to:
   - `zz-pm-workflow`
   - `zz-pm-prototype-workflow`
   - an existing specialist skill
   - a new specialist skill
3. Update the target `SKILL.md`.
4. Update repository navigation in [`README.md`](./README.md).
5. Update local routing in [`AGENTS.md`](./AGENTS.md) if task routing changes.
6. Re-check naming consistency and public-facing wording.

## Naming Guidance

- Use the `zz-pm-` prefix for PM skills.
- Use `workflow` only for orchestrators.
- Use short, capability-based names such as `review-board`, `tracking-spec`, or `postmortem`.
- Avoid naming that implies multiple unrelated responsibilities.

## Public Repo Hygiene

- Keep the root README suitable for GitHub visitors.
- Keep internal validation notes out of public-facing docs.
- Sanitize repo content before publishing.

