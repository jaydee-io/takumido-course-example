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
└── chapters/
    ├── 01-concepts/
    │   ├── chapter.yaml
    │   ├── 01-welcome.slide/           # Layout: takumido-columns
    │   │   ├── meta.yaml
    │   │   ├── en.md
    │   │   ├── fr.md
    │   │   └── assets/
    │   │       └── welcome-illustration.svg
    │   └── 02-anatomy.slide/           # Layout: takumido-text
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

## Layouts used

| Slide | Layout |
|-------|--------|
| 01-welcome | `takumido-columns` (text + image) |
| 02-anatomy | `takumido-text` (text + embedded code block) |
| 01-roles | `takumido-columns` (text + text) |
| 02-play-pause | `takumido-columns` (text + Mermaid diagram) |

## Versioning

This repository follows [semver](https://semver.org/). The TakumiDo backend resolves courses by git tag.

- `v0.1.0` — Initial release with 2 chapters, 4 slides, bilingual content
