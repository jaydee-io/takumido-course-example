# Reconnexion — La résilience en session

> Une coupure réseau ne fait pas perdre sa place.

::: slot headline

TakumiDo préserve la **posture Play/Pause** de l'apprenti à travers les coupures réseau.

:::

::: slot detail

Quand la connexion WebSocket est interrompue (perte Wi-Fi, mise en veille, changement de réseau), l'apprenti entre dans l'état **Disconnected**. Un indicateur visuel signale la déconnexion.

À la reconnexion, le serveur rétablit l'état complet :

- **Posture préservée :** si l'apprenti était en **Play**, il reprend en Play ; s'il était en **Pause**, il reprend en Pause à la même slide.
- **HWM synchronisée :** la High-Water Mark est mise à jour avec la valeur courante du serveur, ce qui peut déverrouiller de nouvelles slides si le formateur a avancé pendant la déconnexion.
- **Slide synchronisée :** en mode Play, l'apprenti revient automatiquement à la slide courante du formateur.

Le mécanisme de reconnexion est automatique — aucune action de l'apprenti n'est requise.

:::

::: slot aside

**États de la machine :**

`Play` → `Disconnected` → `Play` ✓

`Pause` → `Disconnected` → `Pause` ✓ (même slide)

:::
