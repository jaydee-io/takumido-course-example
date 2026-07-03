---
title: "Curriculum-as-code for authors"
description: "Writing a course in YAML/Markdown, versioned by git."
---

::: slot title

Curriculum-as-code for authors

:::

::: slot description

On the trainer-author's side, creating a course isn't filling in a form in some interface: it's writing files in a ::accent[git repository].

- **Write** — YAML manifests for structure, Markdown for content, declarative layouts for form. No frontend code.
- **Version** — every release is an annotated semver tag (`v1.0.0`). The session records the exact version: what the apprentice sees is reproducible, auditable.
- **Publish** — fixing a typo or adding a chapter is a commit and a `git push`. The platform handles the rest.

The course isn't locked inside the platform: it's yours, it's diffable, it lives in your usual toolchain.

:::

::: slot visual

![An author's-side git tree of a course — commits, a branch, and the tag published by `git push` marked by the seal accent](@slide/assets/authoring-git-tree.svg){.image}

:::

::: slot note

::muted[Original TakumiDô illustration.]

:::
