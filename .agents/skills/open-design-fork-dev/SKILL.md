---
name: open-design-fork-dev
description: Maintain open-design fork source, repository documentation and agent guidance with local ownership, evidence and runtime boundaries.
---

# Fork source maintenance

Read [AGENTS.md](../../../AGENTS.md), [CONTRIBUTING.md](../../../CONTRIBUTING.md)
and [docs/architecture.md](../../../docs/architecture.md). Read the owning
layer's AGENTS.md before changing apps, packages, tools, e2e or packaged skills.
The existing root guide owns all daemon data-root and lifecycle rules; link it
instead of inventing filesystem examples or a second runtime-data authority.

The daemon owns HTTP behavior and agent spawning; `packages/contracts` owns
pure app DTOs. Sidecar-proto, sidecar and platform retain their separate business,
client/protocol and OS roles. UI and CLI consume the same capability boundary.
Repository-maintainer context under `.agents/skills/` is separate from packaged
functional `skills/` and rendering `design-templates/`; source upkeep must not
silently add a product capability or broaden the runtime prompt.

Use the packageManager-selected pnpm and the supported Node runtime. Run
`pnpm guard` and `pnpm typecheck` before ready delivery, plus package-scoped
checks for changed behavior. Root aggregate test/build aliases are forbidden.
Use the existing tools-dev suite for an authorized journey and mocks for agent
stream changes; avoid unrequested provider spend. A guard/typecheck does not
prove a desktop journey, packaged updater, live agent or provider integration.
No documentation request grants daemon reconfiguration, account login, release,
installation, authenticated import or changing the live coding-agent model.
Fill the repository's PR template; route this requested fork upkeep to the
owned fork, rather than opening an unsolicited upstream PR.

## Repository delivery

Inspect the actual remotes, default branch and target GitHub repository before
publication. This task updates `jlapenna/open-design`; ownership of a fork does not
authorize an upstream merge. Use a dedicated feature worktree from the freshly
fetched configured base, preserving other branches and sessions. Read
[worktree-hygiene](https://github.com/jlapenna/repo-tools/blob/main/plugins/repo-tools/skills/worktree-hygiene/SKILL.md)
and [land-pr](https://github.com/jlapenna/repo-tools/blob/main/plugins/repo-tools/skills/land-pr/SKILL.md)
for normal checked delivery and cleanup; never bypass protection or hooks.

## Harness upkeep

Use the [shared harness-maintenance workflow](https://github.com/jlapenna/repo-tools/blob/main/plugins/repo-tools/skills/harness-maintenance/SKILL.md), adapted from
[Ryan Lopopolo's field guide](https://github.com/lopopolo/harness-engineering/tree/226c8d35fb6ea3ed55467753dba6dea2b5fd5778). Corroborate observed failures and
repair their earliest owner, keeping the root guide a route and conditional
procedures in references. Preserve current contracts separately from chronology.
A source check proves structure or consistency; comparable fresh use is required
to claim improved agent behavior. Keep fork decisions local and refer to shared
implementations rather than copying them across repositories.
