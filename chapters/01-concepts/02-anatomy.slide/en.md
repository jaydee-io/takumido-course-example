# Anatomy of a Course

> How a TakumiDô course repository is structured.

::: slot body

A course lives in its own **git repository**, versioned with semver tags. The pipeline loads the content by checking out a specific tag.

Every course starts with a **root manifest** that declares languages, chapters, and metadata:

```yaml filename="course.yaml"
schema_version: 1
id: my-training
languages: [en, fr]
default_layout: takumido-text
chapters:
  - 01-introduction
  - 02-core-concepts
```

Each chapter has its own directory under `chapters/` with a `chapter.yaml` and slide folders suffixed `.slide`. Inside each slide folder, a `meta.yaml` specifies the layout, while `en.md` and `fr.md` hold the content for each language.

Translations for course and chapter titles live in `i18n/en.yaml` and `i18n/fr.yaml` — slide content stays in its own Markdown files.

:::
