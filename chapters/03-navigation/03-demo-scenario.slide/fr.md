# Scénario de démonstration complet

> Reproduire toutes les transitions de la machine d'états en une seule démo.

::: slot headline

Ce scénario couvre : **Play → Pause** (raccourci, rewind, clic menu) · **Pause → Play** (resync) · **HWM** · **reconnexion**.

:::

::: slot detail

**Prérequis :** deux navigateurs ouverts sur la même session — un en rôle Formateur, l'autre en rôle Apprenti.

**Étapes :**

1. **Play par défaut** — Rejoindre la session. L'apprenti démarre en mode Play et suit automatiquement le formateur.

2. **Play → Pause via raccourci `P`** — Formateur en slide 3. Apprenti appuie sur `P` → FollowIndicator CYAN (Pause). Appuie à nouveau sur `P` → FollowIndicator VERT (Play, resync).

3. **Play → Pause via rewind** — Formateur en slide 5. Apprenti appuie sur `←` → Pause, recule en slide 4. FollowIndicator CYAN.

4. **Play → Pause via clic menu** — Apprenti appuie sur `Espace` (resync → Play). Puis ouvre le ChapterMenu et clique sur la slide 2 → déclenche la Pause depuis l'état Play. Slide 2 s'affiche.

5. **Déverrouillage HWM** — Formateur avance de slide 5 à 7. Dans le menu de l'apprenti, slides 6 et 7 se déverrouillent en temps réel (badges 🔒 disparaissent sans rechargement).

6. **Resync (Pause → Play)** — Apprenti appuie sur `Espace` → FollowIndicator VERT, revient à la slide 7 (position du formateur).

7. **Reconnexion** — Désactiver puis réactiver le Wi-Fi de l'apprenti. Après reconnexion, l'apprenti reprend en Play sur la slide courante du formateur, HWM à jour.

:::

::: slot aside

**Transitions couvertes :**

- Play → Pause ✓  
  via `←`, via `P`, via clic menu
- Pause → Play (resync) ✓  
  via `Espace` / `P`
- Navigation menu (HWM-aware) ✓
- Déverrouillage HWM progressif ✓
- Disconnected → Play ✓

:::
