# Le menu chapitres

> L'outil de navigation libre de l'apprenti, intégrant la HWM.

::: slot left

Le **menu chapitres** est un panneau arborescent affiché dans la vue apprenti. Il liste tous les chapitres et leurs slides, organisés hiérarchiquement.

**Comportement selon la HWM :**

- Les slides déverrouillées (index ≤ HWM) sont **cliquables** : l'apprenti peut y naviguer directement. Cliquer sur une slide antérieure à la position actuelle déclenche automatiquement le mode **Pause**.
- Les slides verrouillées (index > HWM) sont **grisées** avec un badge de verrouillage : elles ne peuvent pas être sélectionnées.

Au fur et à mesure que le formateur avance, les badges disparaissent et de nouvelles slides deviennent accessibles — sans recharger la page.

:::

::: slot right

**Flux de navigation typique :**

1. Le formateur est à la slide 5/12, HWM = 5.
2. L'apprenti ouvre le menu → voit 5 slides accessibles, 7 verrouillées.
3. L'apprenti clique sur la slide 3 → passe en **Pause**, affiche la slide 3.
4. Le formateur avance à 6 → la slide 6 se déverrouille en temps réel dans le menu.
5. L'apprenti appuie sur **Espace** → repasse en **Play**, revient à la slide 6.

> Le menu chapitres est disponible en modes Play **et** Pause — l'apprenti peut toujours voir où il en est par rapport au formateur.

:::
