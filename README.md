# Public overview of Sajtagent

Updated: 2026-10-04.

**Active development uses one private repository:
[`sajtagent-platform`](https://github.com/Jakeminator123/sajtagent-platform).**
This public repository contains only an overview, not executable product source.

| Repository | Current role |
| --- | --- |
| [`sajtagent-platform`](https://github.com/Jakeminator123/sajtagent-platform) | Active monorepo: web product, runtime, shared contracts and documentation |
| Former `sajtagent-site` | Deleted on 2026-10-04; active web source is in `site/` |
| Former `sajtagent-sprites` | Deleted on 2026-10-04; active runtime source is in `runtime/` |
| This overview | Public documentation only |

## Source layout

```text
sajtagent-platform/
|-- site/             web product and Builder
|-- runtime/          OpenClaw/Sprites runtime
|-- docs/             architecture and workflow
|-- system-model/     shared flow model
|-- control-panel/    local read-only status UI
|-- scripts/          development and maintenance helpers
```

A clone of the active platform repository includes both `site/` and `runtime/`.
New development agents should start in that repository and read its current
`AGENTS.md` and `docs/workflow/HANDOFF.md`.

## Source and hosting

The Vercel web project retains the name `sajtagent-site`, but builds
`site/` from `sajtagent-platform/main`. The public web product is
[https://sajtagent.se](https://sajtagent.se).

Runtime execution is a separate service; its source belongs to `runtime/`.
The local control panel reports repository state and does not deploy or run
customer code. The retired component repositories and their branches were
deleted after the hosting cutover was verified. Their historical source is
preserved in private backups and platform archive tags. This overview remains
display material; it does not build or deploy either service.

This overview contains no private source or credentials.
