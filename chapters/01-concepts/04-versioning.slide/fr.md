# Versionner et publier un cours

> Un cours TakumiDô est un dépôt git versionné par tags semver.

::: slot body

Le **pipeline de contenu** de TakumiDô charge un cours en faisant un checkout sur un tag semver précis. Cela garantit la reproductibilité des sessions : la version affichée à l'apprenti est toujours celle enregistrée au moment de la création du cours.

Pour publier une nouvelle version d'un cours :

```bash
# 1. Valider les modifications locales
git add .
git commit -m "feat: add chapter 03-navigation"

# 2. Poser un tag annoté semver
git tag -a v1.2.0 -m "Add navigation chapter — 3 chapters, 12 slides"

# 3. Pousser le tag vers le dépôt distant
git push origin v1.2.0
```

Le backend TakumiDô résout la **dernière version compatible** (ex. `^1.0.0`) via la liste des tags du dépôt. Dès que le tag est visible, la nouvelle version est disponible pour les formateurs.

> **Bonne pratique :** utilisez des tags annotés (`-a`) plutôt que des tags légers — ils portent un message et une date, ce qui facilite l'audit des versions.

:::
