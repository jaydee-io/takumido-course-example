# Briefs d'illustration maison — vitrine « Découvrir TakumiDô »

> Source de vérité des illustrations de la vitrine (Story 5.6). Les SVG eux-mêmes ne
> sont **pas** produits ici : ils le seront par la story de rédaction du chapitre
> concerné (5.7 / 5.8 / 5.9) ou par un lot d'assets dédié si le volume le justifie.

## Style verrouillé (table ronde Sally × Paige)

- **Trait** : trait à l'encre fin sur aplat washi, esprit *sumi-e* minimaliste.
- **Technique** : **SVG vectoriel maison** — zéro risque de droits, aucune image tierce.
- **Économie de moyens** : **5 à 12 traits** par illustration, beaucoup de vide (*ma*).
- **Accent unique** : **un seul** accent-sceau (`--color-accent-secondary`, le rouge sceau)
  par illustration — jamais deux points rouges.
- **Fond** : **transparent** (l'illustration se pose sur le washi ivoire de la slide).
- **Palette** : **restreinte aux tokens 5.1** — encre `--color-text-primary` (#1C1A17),
  gris `--color-text-muted` (#6B6358), accent-sceau `--color-accent-secondary` (#C8503C).
  Aucun hex en dur : les SVG maison reprennent ces valeurs de tokens.
- **Alt obligatoire** quand l'illustration est *informative* (slots `visual` du layout
  `feature` / `media` de `takumido-media-split`) — l'auteur renseigne un `alt` non vide.

## Illustrations structurantes (4)

| # | Illustration | Chapitre | Slide cible | Rôle |
|---|---|---|---|---|
| S1 | **Frise discipline → pratique → maîtrise** | Ch.1 | `04-discipline-practice-mastery` | Trois temps de la voie du Takumi, montée progressive ; pont narratif vers Apprenti/Formateur. |
| S2 | **Arbre git « curriculum-as-code »** | Ch.2 | `02-curriculum-as-code` | Un tronc de commits + tags semver comme métaphore du cours-as-code ; l'accent-sceau marque le tag publié. |
| S3 | **Diagramme HWM (déverrouillage progressif)** | Ch.3 | `02-progressive-unlock` | Rail de slides dont la barre High-Water Mark libère celles ≤ HWM ; l'accent-sceau marque la position du formateur. |
| S4 | **Réemploi de l'arbre git côté auteur** | Ch.4 | `03-authoring-curriculum-as-code` | **Réemploi de S2** (même SVG), recadré côté auteur (`git push` → tag). Pas de nouvel asset sauf si Sally distingue une variante formateur. |

## Illustrations *nice-to-have* (optionnelles)

| # | Illustration | Chapitre | Slide cible | Note |
|---|---|---|---|---|
| N1 | **Chat origami** | Ch.1 | `03-sixty-thousand-hours` | **Optionnelle** — la statistique « 60 000 » en Fraunces porte déjà le slide. Origami stylisé, aucune marque citée ; mention « illustration originale TakumiDô ». |
| N2 | **Aplat/gravure « Takumi à l'établi »** | Ch.1 | `02-what-is-takumi` | Optionnelle — l'anecdote est *text-forward* et tient sans image. |
| N3 | **Cockpit trois colonnes (formateur)** | Ch.4 | `02-track-progress` | Optionnelle — capture/illustration schématique du dashboard ; peut rester textuelle. |

## Anecdotes sensibles — cadre de traitement (AC4)

- **Text-forward** : chaque slide d'anecdote (Toyota Ch.1, Lexus/60 000 h Ch.1) **tient
  sans image**. L'illustration, quand elle existe, est un *plus*, jamais le porteur du sens.
- **Aucune marque protégée citée comme caution** (ni Toyota, ni Lexus dans le corps
  argumentatif). Crédit discret `::muted[inspiré de…]` uniquement.
- **Mention** « illustration originale TakumiDô » (en `muted`) dès qu'un SVG maison
  accompagne une anecdote, pour lever toute ambiguïté de source.
