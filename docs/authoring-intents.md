# Accentuer un mot : les intents inline `::role[…]`

TakumiDô permet d'appliquer **l'identité de ta marque à un simple mot**, au milieu
d'un paragraphe, sans jamais écrire de CSS. Tu nommes une **intention** (un rôle
sémantique) ; la plateforme se charge du rendu (couleur d'accent, style, animation).

## Syntaxe

```markdown
Un mot ::accent[important] dans une phrase.
```

→ rend le mot « important » dans la **couleur d'accent de ta marque** (définie une
seule fois dans `theme/theme.yaml`, cf. les rôles de thème).

La forme générale est `::role[texte]` :

- `::` ouvre la directive,
- `role` est un **rôle du vocabulaire fermé** (voir ci-dessous),
- `[texte]` est le texte à habiller (un mot, un groupe de mots).

## Rôles disponibles

| Rôle      | Usage                                                            |
| --------- | --------------------------------------------------------------- |
| `accent`  | Met un terme en **couleur d'accent** de la marque               |
| `muted`   | Atténue un texte secondaire                                     |
| `kbd`     | Présente une **touche clavier** (style « touche »)              |
| `badge`   | Petite **pastille** (étiquette courte)                          |
| `cursor`  | Curseur clignotant (réservé surtout aux slides de marque)       |

Exemples :

```markdown
Appuie sur ::kbd[Espace] pour avancer.
Le statut ::badge[beta] est temporaire.
Ce détail est ::muted[optionnel].
```

## Règles et garde-fous

- **Tu nommes une intention, jamais une valeur.** Aucune classe CSS, aucune couleur
  brute : impossible d'écrire `style="…"` ou `class="…"`. C'est le thème de ton cours
  qui décide à quoi ressemble chaque rôle (multi-marque).
- **Vocabulaire fermé.** Un rôle inconnu (`::glow[…]`) n'est pas interprété : il
  s'affiche **tel quel** (texte littéral inerte), sans casser le rendu.
- **Granularité du mot.** Les intents servent le **contenu courant** (paragraphes,
  listes…). Pour une slide d'identité complète (logo + wordmark), utilise plutôt le
  bloc `:::brand`.
- **Échappement.** Pour inclure un crochet **fermant** littéral dans le texte, échappe-le :
  `::accent[a\]b]` rend « a]b ». Le premier `]` non échappé **ferme** la directive : un
  crochet **ouvrant** interne n'est pas apparié (`::accent[a[b]c]` rend « a[b » accentué
  puis « c] » en littéral). Pour un texte riche en crochets, échappe les `]`.
- **Casse souple.** Le rôle est insensible à la casse : `::ACCENT[…]` équivaut à `::accent[…]`.
- **Intent vide ignoré.** `::accent[]` (sans texte) ne produit rien — ni balise vide, ni littéral.
- **Frontière de mot.** La directive doit débuter sur une frontière de mot (début de ligne,
  espace, ponctuation). Collée à un identifiant (`mot::accent[x]`), elle n'est **pas**
  interprétée — c'est ce qui protège la résolution de portée C++ comme `std::array[i]`.
- **Pas dans le code.** À l'intérieur d'un bloc ou d'un span de code (`` `::accent[x]` ``),
  la directive n'est pas interprétée — pratique pour documenter la syntaxe elle-même,
  et sans surprise sur du C++ comme `std::vector`.

## Exemple réel dans ce dépôt

La slide d'ouverture du chapitre 1 (`chapters/01-concepts/01-welcome.slide`) accentue
« temps réel » / « real time » :

```markdown
… dispenser des cours interactifs à leurs apprentis en ::accent[temps réel].
```
