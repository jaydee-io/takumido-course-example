# takumido-course-example

Bilingual showcase training for the [TakumiDo](https://takumido.app) platform.

## About this course

**"Discover TakumiDo"** is a short introductory training (≈ 15 min) that demonstrates the platform's content pipeline and live session features. It serves as:

- A **test fixture** for the TakumiDo content pipeline (parsing, rendering, i18n)
- A **documentary showcase** for content creators building their own courses
- A **reference implementation** of the course repository structure (Option E)

Languages: English (default), French.

## Pedagogical coverage

### Chapter 1 — TakumiDo Concepts
- **Welcome**: what TakumiDo is, who it's for, what problem it solves
- **Anatomy of a course**: repository structure, manifests, slides, layouts
- **Beyond primitives**: authoring a custom layout (`spotlight`) with the layout DSL

### Chapter 2 — Live Session
- **Trainer & Apprentice**: roles and capabilities during a live session
- **Play & Pause loop**: apprentice navigation, resync, state machine

## Repository structure

```
takumido-course-example/
├── course.yaml                         # Root manifest (schema v1)
├── i18n/
│   ├── en.yaml                         # English translations (course + chapter titles)
│   └── fr.yaml                         # French translations
├── layouts/
│   └── spotlight.layout.yaml           # Custom layout (header band + 2-column body)
└── chapters/
    ├── 01-concepts/
    │   ├── chapter.yaml
    │   ├── 01-welcome.slide/           # Layout: takumido-columns
    │   │   ├── meta.yaml
    │   │   ├── en.md
    │   │   ├── fr.md
    │   │   └── assets/
    │   │       └── welcome-illustration.svg
    │   ├── 02-anatomy.slide/           # Layout: takumido-text
    │   │   ├── meta.yaml
    │   │   ├── en.md
    │   │   └── fr.md
    │   └── 03-custom-layout.slide/     # Layout: spotlight (custom)
    │       ├── meta.yaml
    │       ├── en.md
    │       └── fr.md
    └── 02-live-session/
        ├── chapter.yaml
        ├── 01-roles.slide/             # Layout: takumido-columns
        │   ├── meta.yaml
        │   ├── en.md
        │   └── fr.md
        └── 02-play-pause.slide/        # Layout: takumido-columns
            ├── meta.yaml
            ├── en.md
            └── fr.md
```

## Layouts

A layout describes **where content goes** on a slide. It declares typed **slots**
(content regions) and a **composition** (how those regions are arranged: `stack`,
`grid` or `flex`). A slide picks a layout by id in its `meta.yaml`, then fills the
slots from its Markdown (`::: slot <name>` blocks).

There are two kinds:

- **Primitive layouts** (`takumido-*`) — provided by the TakumiDo platform. They
  cover the common slide shapes and need no setup. The `takumido-` prefix is
  **reserved**: a custom layout may not use it.
- **Custom layouts** — defined in this repository under `layouts/<id>.layout.yaml`,
  using the exact same DSL. The pipeline exposes them to the renderer alongside the
  primitives.

### Primitive layouts

Screenshots below are POC renders with the default theme (course-specific theming
arrives in a later milestone); they illustrate the **structure** of each layout.

#### `takumido-title`

Title slide — a visible centered title with an optional subtitle.
Slots: `title` (text, required), `subtitle` (text, optional). Composition: `stack`.

![takumido-title](docs/images/layouts/takumido-title.png)

#### `takumido-text`

General prose slide. Slot: `body` (text / callout / list, one or more).
Composition: `stack`.

![takumido-text](docs/images/layouts/takumido-text.png)

#### `takumido-code`

A single code block, full width. Slot: `body` (code, exactly one).
Composition: `stack`.

![takumido-code](docs/images/layouts/takumido-code.png)

#### `takumido-mermaid`

A single, centered Mermaid diagram. Slot: `body` (mermaid, exactly one).
Composition: `stack`.

![takumido-mermaid](docs/images/layouts/takumido-mermaid.png)

#### `takumido-image`

A single, centered image with an optional caption. Slot: `body` (image, exactly
one). Composition: `stack`.

![takumido-image](docs/images/layouts/takumido-image.png)

#### `takumido-columns`

Two side-by-side columns. Slots: `left`, `right` (any block kind, each one or
more). Composition: `grid` (`1fr 1fr`).

![takumido-columns](docs/images/layouts/takumido-columns.png)

#### `takumido-grid`

A wrapping grid of cells. Slot: `cells` (any block kind, one or more).
Composition: `flex` (row, wrap).

![takumido-grid](docs/images/layouts/takumido-grid.png)

> `takumido-quiz` (slot `body`: quiz, exactly one) is **reserved for a future
> milestone** — it has no renderer yet and is intentionally not shown here.

### Custom layout: `spotlight`

Defined in [`layouts/spotlight.layout.yaml`](layouts/spotlight.layout.yaml) and
used by the **Beyond primitives** slide. It is a full-width headline band above a
two-column body (a wide `detail` column and a narrower `aside`) — an arrangement
no single primitive provides. Slots: `headline` (text, required), `detail`
(text / callout / list, required), `aside` (text / callout, optional).
Composition: `grid` with named areas.

### Layouts used by slide

| Slide | Layout | Kind |
|-------|--------|------|
| 01-welcome | `takumido-columns` (text + image) | primitive |
| 02-anatomy | `takumido-text` (text + embedded code block) | primitive |
| 03-custom-layout | `spotlight` (headline + detail + aside) | custom |
| 01-roles | `takumido-columns` (text + text) | primitive |
| 02-play-pause | `takumido-columns` (text + Mermaid diagram) | primitive |

## Versioning

This repository follows [semver](https://semver.org/). The TakumiDo backend resolves courses by git tag.

- `v0.1.0` — Initial release with 2 chapters, 4 slides, bilingual content
