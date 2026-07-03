---
title: "Curriculum-as-code côté auteur"
description: "Écrire un cours en YAML/Markdown, versionné par git."
---

::: slot title

Curriculum-as-code côté auteur

:::

::: slot description

Côté formateur-auteur, créer un cours n'est pas remplir un formulaire dans une interface : c'est écrire des fichiers dans un ::accent[dépôt git].

- **Écrire** — des manifestes YAML pour la structure, du Markdown pour le contenu, des layouts déclaratifs pour la forme. Aucun code frontend.
- **Versionner** — chaque livraison est un tag semver annoté (`v1.0.0`). La session enregistre la version exacte : ce que voit l'apprenti est reproductible, auditable.
- **Publier** — corriger une coquille ou ajouter un chapitre, c'est un commit et un `git push`. La plateforme se charge du reste.

Le cours n'est pas enfermé dans la plateforme : il t'appartient, il est diffable, il vit dans ton outillage habituel.

:::

::: slot visual

![Arbre git d'un cours côté auteur — des commits, une branche, et le tag publié par `git push` marqué par l'accent-sceau](@slide/assets/authoring-git-tree.svg){.image}

:::

::: slot note

::muted[Illustration originale TakumiDô.]

:::
