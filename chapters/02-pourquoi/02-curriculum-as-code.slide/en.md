---
title: "Curriculum-as-code"
description: "The founding differentiator: the course is a versioned git repo."
---

::: slot title

Curriculum-as-code

:::

::: slot description

On most platforms, a course is a row of videos locked inside a proprietary database. At TakumiDô, a course is a ::accent[git repository] — text, versioned, open.

- **Versioned** — every course is published under a semver tag (`v1.0.0`). The version an Apprentice sees is exactly the one recorded when the session opened: reproducible, auditable.
- **Open** — YAML manifests, Markdown content, declarative layouts. No frontend code to write.
- **Alive** — fixing a typo or adding a chapter is a commit and a tag. Nothing more.

:::

::: slot visual

![Course git tree — a line of commits, one branch, and the published tag marked by the seal-red accent](@slide/assets/curriculum-as-code-git-tree.svg){.image}

:::

::: slot note

::muted[Original TakumiDô illustration.]

:::
