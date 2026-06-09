# Scénario de démonstration complet

> Reproduire toutes les transitions de la machine d'états en une seule démo.

::: slot headline

Ce scénario couvre : **Play → Pause → rewind → menu → HWM → reconnexion → resync**.

:::

::: slot detail

**Prérequis :** deux navigateurs ouverts sur la même session — un en rôle Formateur, l'autre en rôle Apprenti.

**Étapes :**

1. **Play par défaut** — Rejoindre la session. L'apprenti démarre en mode Play et suit automatiquement le formateur.

2. **Pause via rewind** — Formateur en slide 5. Apprenti appuie sur `←` → passe en Pause, revient en slide 4. L'indicateur de suivi devient orange.

3. **Navigation menu** — Apprenti ouvre le menu chapitres → clique sur slide 2. Slide 2 s'affiche ; slides 6+ grisées.

4. **Déverrouillage HWM** — Formateur avance de slide 5 à 7. Dans le menu de l'apprenti, slides 6 et 7 se déverrouillent en temps réel.

5. **Resync** — Apprenti appuie sur `Espace` → repasse en Play, revient à slide 7 (position du formateur).

6. **Reconnexion** — Désactiver puis réactiver le Wi-Fi de l'apprenti. Après reconnexion, l'apprenti reprend en Play sur la slide courante du formateur, HWM à jour.

:::

::: slot aside

**Transitions couvertes :**

- Play → Pause ✓
- Pause → Play (resync) ✓
- Navigation menu (HWM-aware) ✓
- Déverrouillage HWM progressif ✓
- Disconnected → Play ✓

:::
