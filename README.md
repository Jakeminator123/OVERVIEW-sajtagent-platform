# OVERVIEW — not the platform repo

**This repository is documentation only.** It is not `sajtagent-platform` and contains no control-panel or decision source.

SiteAgent is three GitHub repositories:

| Repo | Visibility | Role |
| --- | --- | --- |
| [`sajtagent-site`](https://github.com/Jakeminator123/sajtagent-site) | public | Web product and Builder |
| [`sajtagent-platform`](https://github.com/Jakeminator123/sajtagent-platform) | private | Architecture decisions and a local read-only control panel |
| [`sajtagent-sprites`](https://github.com/Jakeminator123/sajtagent-sprites) | private | Privileged OpenClaw/Sprites runtime |

GitHub cannot hide folders inside a public repo. This page is the family map only.

## Family

```text
[sajtagent-platform]   private — decisions, boundaries, local status panel
        |
        +-- [sajtagent-site]      public  — what users open
        |
        +-- [sajtagent-sprites]   private — worker runtime
```

A fresh clone of the platform repo does not download the other two. Each is its own Git repository.

## First-level map of the private platform repo

```text
sajtagent-platform/     private
|-- README.md           boundaries and start-here
|-- docs/               accepted architecture and workflow
|-- control-panel/      local read-only status UI
|-- scripts/            maintenance helpers
```

The control panel reports repository state. It does not deploy, write production data, or run customer code.

This overview does not include platform source, runtime source, or credentials.
