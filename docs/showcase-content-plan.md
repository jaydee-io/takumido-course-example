# Plan de contenu de la vitrine — source de vérité (Story 5.6)

> **Ce document fige le plan slide-par-slide validé** des 4 chapitres narratifs de la
> vitrine « Découvrir TakumiDô ». Il est la **source de vérité humaine** pour les
> Stories de rédaction 5.7 (Ch.1+Ch.2), 5.8 (Ch.3) et 5.9 (Ch.4).
>
> Validé par JayDee le 2026-07-02 (Point de validation #1 — plan des 4 chapitres ;
> Point de validation #2 — placement des slides « Bientôt »).

## Principe : la forme est finie, le fond commence

Les Stories 5.1→5.5 (tokens, composants enrichis, primitives `takumido-cover` /
`takumido-media-split`, layouts custom `concept`/`feature`/`comparison`/`closing`/
`pause`/`spotlight`, bloc `roadmap`) sont **done**. Ce plan ne consomme que ces
livrables — **aucun** nouveau layout, composant ou token.

**Invariant honnêteté radicale (Paige)** : aucun slide ne mêle livré (**MONTRÉ**) et
promis (**Bientôt**). Les features à venir vivent sur un slide « Bientôt » dédié
(bloc `roadmap` isolé, statuts `soon`/`exploring`, teinte muted).

## Outline cible

```
course-opening  (standalone, brand lockup)
Ch.1 — L'esprit du Takumi      chapters/01-esprit-takumi
Ch.2 — Pourquoi TakumiDô       chapters/02-pourquoi
intermission    (standalone, layout pause « Respire »)
Ch.3 — Côté Apprenti           chapters/03-apprenti
Ch.4 — Côté Formateur          chapters/04-formateur
course-closing  (standalone, brand lockup « Merci » — bookend de course-opening)
```

## Plan slide-par-slide

### Ch.1 — L'esprit du Takumi (`chapters/01-esprit-takumi`)

| Slide | Layout | Intention | Statut | Illustration |
|---|---|---|---|---|
| 00-chapter-opening | `takumido-chapter-opening` | Poser l'esprit | MONTRÉ | — |
| 01-opening-mantra | `concept` | Mantra d'ouverture comme accroche | MONTRÉ | — |
| 02-what-is-takumi | `takumido-text` | Qu'est-ce qu'un Takumi (Toyota, text-forward) | MONTRÉ | N2 (opt.) |
| 03-sixty-thousand-hours | `concept` | 60 000 h & chat origami (Lexus, text-forward) | MONTRÉ | N1 origami (opt.) |
| 04-discipline-practice-mastery | `feature` | Frise, pont vers Apprenti/Formateur | MONTRÉ | **S1 frise (structurante)** |
| 05-takumido-mantras | `takumido-text` | 3-5 mantras figés | MONTRÉ | — |

### Ch.2 — Pourquoi TakumiDô (`chapters/02-pourquoi`) — *tout MONTRÉ, aucun « Bientôt »*

| Slide | Layout | Intention | Statut | Illustration |
|---|---|---|---|---|
| 00-chapter-opening | `takumido-chapter-opening` | — | MONTRÉ | — |
| 01-classic-platforms-problem | `concept` | Constat, pas attaque | MONTRÉ | — |
| 02-curriculum-as-code | `feature` | Différenciateur fondateur | MONTRÉ | **S2 arbre git (structurante)** |
| 03-live-vs-replay | `comparison` | La symétrie porte le sens | MONTRÉ | — |

### Ch.3 — Côté Apprenti (`chapters/03-apprenti`)

| Slide | Layout | Intention | Statut | Illustration |
|---|---|---|---|---|
| 00-chapter-opening | `takumido-chapter-opening` | — | MONTRÉ | — |
| 01-apprentice-experience | `takumido-columns` | Rejoindre, Play/Pause | MONTRÉ | — |
| 02-progressive-unlock | `feature` | Déverrouillage progressif (HWM) | MONTRÉ | **S3 diagramme HWM (structurante)** |
| 03-resume-nothing-lost | `spotlight` | Reprendre sans rien perdre (reconnexion) | MONTRÉ | — |
| **04-soon-apprentice** | `takumido-roadmap` | **Roadmap isolée, lane Apprenti** | **BIENTÔT** | rail data-driven |

### Ch.4 — Côté Formateur (`chapters/04-formateur`)

| Slide | Layout | Intention | Statut | Illustration |
|---|---|---|---|---|
| 00-chapter-opening | `takumido-chapter-opening` | — | MONTRÉ | — |
| 01-lead-the-way | `concept` | Diriger la voie (tempo Play/Pause) | MONTRÉ | — |
| 02-track-progress | `feature` | Suivre la progression (dashboard, HWM) | MONTRÉ | N3 cockpit (opt.) |
| 03-authoring-curriculum-as-code | `feature` | Curriculum-as-code côté auteur | MONTRÉ | **S4 arbre git (réemploi S2)** |
| **04-soon-graph-edit** | `takumido-roadmap` | **Roadmap isolée, lane Formateur (édition graphique)** | **BIENTÔT** | rail data-driven |
| 05-chapter-closing | `closing` | Récap & clôture (bookend Ch.1) | MONTRÉ | — |

**Slides « Bientôt » (validation #2)** : exactement **2**, toutes deux `takumido-roadmap`
isolées — `03-apprenti/04-soon-apprentice` (lane Apprenti : gamification `exploring`) et
`04-formateur/04-soon-graph-edit` (lane Formateur : édition graphique `soon`,
notifications `soon`, analytique `exploring`). Aucune autre slide ne contient de promesse.

## Mantras TakumiDô figés (AC5)

1. **(ouverture)** *« De la discipline naît la pratique ; de la pratique, la maîtrise. »*
2. *« Mille fois le même geste, pour qu'il devienne le tien. »*
3. *« Le maître ne mesure plus : il sait. »*
4. **(pont Apprenti/Formateur)** *« Suivre la voie, puis tracer la sienne. »*

## Mapping ancien → nouveau

| Slide actuelle | Destination | Traitement |
|---|---|---|
| `course-opening` (standalone) | avant Ch.1 | ✅ réutilisé tel quel |
| `01-concepts/00-chapter-opening` | openings Ch.1/Ch.2 | 🔁 réécrit |
| `01-concepts/01-welcome` | Ch.1 (esprit) + Ch.2 (tech) | ✂️ scindé / réécrit |
| `01-concepts/02-anatomy` | Ch.2 `02-curriculum-as-code` | 🔁 réécrit (illustration S2) |
| `01-concepts/03-custom-layout` | — | ❌ supprimé (méta/notice) |
| `01-concepts/04-versioning` | Ch.2 + Ch.4 `03-authoring` | ♻️ matière réutilisée |
| `02-live-session/01-roles` | Ch.3 (Apprenti) + Ch.4 (Formateur) | ✂️ scindé |
| `02-live-session/02-play-pause` | Ch.3 `01` (+ tempo Ch.4 `01`) | 🔁 réutilisé |
| `02-live-session/03-hwm` | Ch.3 `02-progressive-unlock` | 🔁 réécrit (illustration S3) |
| `02-live-session/04-reconnection` | Ch.3 `03-resume-nothing-lost` | ♻️ réutilisé |
| `intermission` (« Respire ») | entre Ch.2 et Ch.3 | ✅ réutilisé, replacé |
| `03-navigation/01-chapter-menu` | Ch.3 `01-apprentice-experience` | ♻️ fondu |
| `03-navigation/02-shortcuts` | — | ❌ supprimé (raccourcis → `::kbd` inline) |
| `03-navigation/03-demo-scenario` | — | ❌ supprimé (notice de démo) |
| `03-navigation/04-summary` | Ch.4 `05-chapter-closing` | 🔁 réécrit |
| `platform-roadmap` (standalone) | dissous → Ch.3 `04` (Apprenti) + Ch.4 `04` (Formateur) | ❌ supprimé (standalone) |
| `course-closing` (standalone) | après Ch.4 | ✅ **conservé** (bookend, décision JayDee) |

### État transitoire (à nettoyer par 5.7/5.8/5.9)

Les dossiers `chapters/01-concepts`, `chapters/02-live-session`, `chapters/03-navigation`
et `slides/platform-roadmap` **restent sur disque hors `outline`** comme **matière de
migration**. Le bundle ne charge que l'`outline` (`CourseBundleService`), donc ils ne
sont pas rendus. **Chaque story de rédaction supprime le(s) dossier(s) source une fois
sa matière migrée** :

- **5.7** → supprime `01-concepts` (après migration Ch.1 + Ch.2).
- **5.8** → supprime `02-live-session` (après migration Ch.3) ; supprime `platform-roadmap`
  (lane Apprenti dissoute en Ch.3).
- **5.9** → supprime `03-navigation` (après migration Ch.4).

## Correspondance stories

| Chapitre(s) | Story de rédaction | Clé sprint |
|---|---|---|
| Ch.1 + Ch.2 | 5.7 | `5-7-chapitre-1-lesprit-du-takumi-chapitre-2-pourquoi-takumido` |
| Ch.3 | 5.8 | `5-8-chapitre-3-cote-apprenti` |
| Ch.4 | 5.9 | `5-9-chapitre-4-cote-formateur` |

> **Décision (5.6)** : **pas** de story « lot assets illustratifs » dédiée. Les 4
> illustrations structurantes (S1–S4, dont S4 = réemploi de S2) sont produites **au fil
> de l'eau** dans la story de rédaction du chapitre concerné. Volume maîtrisé (≤ 4 SVG),
> pas de renumérotation 5.7/5.8/5.9.
