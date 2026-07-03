---
title: "Curriculum-as-code"
description: "Le différenciateur fondateur : le cours est un dépôt git versionné."
---

::: slot title

Curriculum-as-code

:::

::: slot description

Sur la plupart des plateformes, un cours est une rangée de vidéos enfermée dans une base de données propriétaire. Chez TakumiDô, un cours est un ::accent[dépôt git] — du texte, versionné, ouvert.

- **Versionné** — chaque cours est publié sous un tag semver (`v1.0.0`). La version vue par l'Apprenti est exactement celle enregistrée à l'ouverture de la session : reproductible, auditable.
- **Ouvert** — manifestes YAML, contenu Markdown, layouts déclaratifs. Aucun code frontend à écrire.
- **Vivant** — corriger une coquille ou ajouter un chapitre, c'est un commit et un tag. Rien de plus.

:::

::: slot visual

![Arbre git d'un cours — une ligne de commits, une branche, et le tag publié marqué par l'accent-sceau](@slide/assets/curriculum-as-code-git-tree.svg){.image}

:::

::: slot note

::muted[Illustration originale TakumiDô.]

:::
