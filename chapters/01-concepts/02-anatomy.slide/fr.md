# Anatomie d'un cours

> Comment est structuré un dépôt de cours TakumiDô.

::: slot body

Un cours vit dans son propre **dépôt git**, versionné par tags semver. Le pipeline charge le contenu en faisant un checkout sur un tag précis.

Chaque cours commence par un **manifeste racine** qui déclare les langues, les chapitres et les métadonnées :

```yaml filename="course.yaml"
schema_version: 1
id: my-training
languages: [en, fr]
default_layout: takumido-text
chapters:
  - 01-introduction
  - 02-core-concepts
```

Chaque chapitre a son propre dossier sous `chapters/` avec un `chapter.yaml` et des dossiers de slides suffixés `.slide`. Dans chaque dossier de slide, un `meta.yaml` spécifie le layout, tandis que `fr.md` et `en.md` contiennent le contenu pour chaque langue.

Les traductions des titres de cours et de chapitres vivent dans `i18n/fr.yaml` et `i18n/en.yaml` — le contenu des slides reste dans ses propres fichiers Markdown.

:::
