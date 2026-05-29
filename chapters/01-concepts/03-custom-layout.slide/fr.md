# Au-delà des primitives : les layouts custom

> Quand les layouts intégrés ne suffisent pas, définissez les vôtres.

::: slot headline

Composez votre propre mise en page avec le **même DSL** que les primitives.

:::

::: slot detail

Les layouts `takumido-*` (texte, code, colonnes, titre…) couvrent les cas courants. Mais un cours peut avoir besoin d'un agencement spécifique : un bandeau de titre suivi d'un corps en deux colonnes, par exemple.

Il suffit d'ajouter un fichier `<id>.layout.yaml` dans le dossier `layouts/` du dépôt. Il déclare des **slots** (zones de contenu typées) et une **composition** (grille, pile ou flex). Le pipeline l'expose au moteur de rendu exactement comme une primitive — aucun code frontend.

Ce slide utilise le layout custom `spotlight`, défini dans `layouts/spotlight.layout.yaml`.

:::

::: slot aside

> Le préfixe `takumido-` est réservé aux primitives de la plateforme : un layout custom doit choisir un autre identifiant.

:::
