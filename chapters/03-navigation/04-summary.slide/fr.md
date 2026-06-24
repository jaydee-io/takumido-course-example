# Récapitulatif — TakumiDô en un coup d'œil

> Toutes les mécaniques, tous les rôles.

::: slot left

## Ce que vous avez vu

**Contenu & structure**
- Cours = dépôt git, versionné par tags semver
- Chapitres, slides, layouts déclaratifs, i18n

**Session live**
- Rôles Formateur et Apprenti
- Synchronisation temps réel des slides

**Navigation apprenti**
- Modes Play (suivi automatique) et Pause (libre)
- High-Water Mark : déverrouillage progressif
- Menu chapitres arborescent
- Raccourcis clavier universels

**Résilience**
- Reconnexion automatique
- Posture Play/Pause préservée

:::

::: slot right

## Ressources

**Créer votre propre cours :**
Clonez ce dépôt et adaptez les chapitres — le pipeline TakumiDô fait le reste.

**Structure minimale :**

```
mon-cours/
├── course.yaml
├── i18n/fr.yaml
└── chapters/
    └── 01-intro/
        ├── chapter.yaml
        └── 01-bienvenue.slide/
            ├── meta.yaml
            └── fr.md
```

**Tag et enregistrement :**
```bash
git tag -a v1.0.0 -m "Initial release"
git push origin v1.0.0
```

> **Prochaine étape :** déposer l'URL du dépôt dans TakumiDô et lancer votre première session live.

:::
