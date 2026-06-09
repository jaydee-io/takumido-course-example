# La High-Water Mark

> Le verrou progressif qui libère les slides au rythme du formateur.

::: slot left

La **High-Water Mark (HWM)** est l'index de la slide la plus avancée que le formateur a présentée au cours d'une session. Elle progresse au fur et à mesure que le formateur avance — elle ne recule jamais.

Chaque fois que le formateur passe à une nouvelle slide, la HWM est mise à jour et diffusée à tous les apprentis connectés.

**Règle de verrouillage :**
- Les slides dont l'index est ≤ HWM sont **déverrouillées** — l'apprenti peut les consulter librement.
- Les slides dont l'index est > HWM sont **verrouillées** — elles apparaissent grisées dans le menu chapitres et ne peuvent pas être sélectionnées.

:::

::: slot right

**Démonstration :**

Imaginez une session avec 12 slides. Le formateur est à la slide 7 ; la HWM vaut donc 7.

| Slide | État |
|-------|------|
| 1 – 7 | Déverrouillée |
| 8 – 12 | Verrouillée 🔒 |

Quand le formateur avance à la slide 8, la HWM passe à 8 et la slide 8 se déverrouille instantanément pour tous les apprentis.

> **Objectif pédagogique :** l'apprenti ne peut pas « tricher » en lisant les slides futures. Il peut en revanche réviser tout ce qui a déjà été couvert.

:::
