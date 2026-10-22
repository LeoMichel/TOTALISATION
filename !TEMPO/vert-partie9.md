
---

# Partie 9 : Les fiches-outils du niveau 4

## Fiche 19 : Le gabarit de définition de mesure

**Usage :** chaque mesure du tableau N4 a sa fiche de définition — l'anti-ambiguïté de la mesure.

```
MESURE — [nom]                              Définie le : [date]

CE QU'ELLE RÉVÈLE (une phrase) : ________________________

DÉFINITION PRÉCISE :
- Début du comptage : ________________________
- Fin du comptage : ________________________
- Ce qui est inclus : ________________________
- Ce qui est exclu : ________________________

SA SOURCE (comment la donnée est collectée) :
[automatique — outil] / [manuelle — qui, quand]

SA MESURE-MIROIR (la contre-mesure d'abus) :
[nom] — détecte : [la triche probable]

SON RISQUE D'ABUS (comment on peut l'optimiser à tort) :
________________________________________________________

SA FRÉQUENCE DE REVUE : [hebdo / mensuelle]
SON DÉCLENCHEUR D'ACTION : [seuil, qui décide]

HISTORIQUE DES DÉFINITIONS :
v1 ([date]) : définition initiale
v2 ([date]) : [changement — pourquoi]
```

**Exemple rempli (extrait réel) :**

```
MESURE — Délai total de traitement          Définie le : 15/09

CE QU'ELLE RÉVÈLE : la vitesse réelle de réponse aux demandes,
vue par le demandeur (pas par l'équipe).

DÉFINITION PRÉCISE :
- Début : réception de la demande complète (tous les champs du
  gabarit remplis — une demande incomplète n'est pas comptée,
  elle est retournée avec la liste des champs manquants)
- Fin : livraison acceptée par le demandeur (pas « livrée » :
  l'acceptation explicite ou 5 jours sans objection)
- Inclus : tous les temps d'attente (y compris les nôtres)
- Exclu : les demandes retirées par le demandeur

SA SOURCE : automatique — le système de tickets, champ
"date d'acceptation" ajouté en v2

SA MESURE-MIROIR : taux de re-classification — détecte les
demandes complexes classées "simples" pour préserver le délai

SON RISQUE D'ABUS : découper les demandes longues en plusieurs
courtes (le découpage artificiel) — détecté par la mesure du
nombre de demandes par thème (une hausse soudaine = découpage)

SA FRÉQUENCE DE REVUE : hebdomadaire (rituel du mardi)
SON DÉCLENCHEUR D'ACTION : dérive > 20% de la médiane mobile
sur 4 semaines → décision du praticien

HISTORIQUE DES DÉFINITIONS :
v1 (15/09) : définition initiale, fin = "livrée"
v2 (02/10) : fin changée en "acceptée" — les livraisons
             techniquement faites mais refusées trompaient la mesure
```

**La valeur de la fiche :** la mesure v2 (acceptée vs livrée) a changé le comportement de l'équipe : les demandes techniquement livrées mais refusées ne comptaient plus comme du travail fini. Sans la fiche (et son historique), ce changement serait contesté comme « on change les règles » — avec l'historique, il est documenté comme « la règle v1 trompait la mesure, v2 la corrige ».

## Fiche 20 : Le gabarit du tableau de bord N4

**Usage :** le tableau de bord complet du niveau 4 — les résultats et les signaux, avec leurs miroirs.

```
TABLEAU DE BORD N4 — [équipe]         Cadence : [jour], 30 min

MESURES DE RÉSULTAT (avec miroir) :
| Mesure | Tendance | Miroir | Dernière action |
|--------|----------|--------|-----------------|
| Délai total | ↗ | Re-classifications | [date, quoi] |
| Taux de retour | ↘ | Ré-ouvertures | |
| Stabilité post-livraison | → | Contournements | |
| Disponibilité de capacité | ↗ | Reports non planifiés | |

SIGNAUX D'ÉQUIPE (les plus corrélés — voir carte E11) :
| Signal | Tendance | Corrélation documentée | Miroir |
|--------|----------|------------------------|--------|
| Divergences doc/modèle | | | |
| Tests flaky | | | |

RÈGLE DE ROTATION : [tout ajout = une sortie]

DERNIÈRE DÉCISION : [date, quoi, qui, levée]
PROCHAINE REVUE : [date]
```

**La règle de mise en page :** les résultats en premier (c'est ce qui compte), les signaux en second (c'est ce qui prédit). Et chaque ligne a sa dernière action — un tableau sans action récente est un tableau décoratif.

## Fiche 21 : Le gabarit de la revue de tableau (30 minutes)

**Usage :** le protocole du rituel de lecture — pour que n'importe qui l'anime.

```
REVUE DU TABLEAU N4 — [date]          Animateur : [rotation]

[0-5 min]  RÉSULTATS : chaque mesure, tendance, miroir.
           Question standard : « dérive ou normal ? »
           Dérive confirmée → décision immédiate (qui, quoi, levée)

[5-15 min] SIGNAUX : les signaux corrélés, leur tendance.
           Question : « un signal dérive-t-il AVANT un résultat ? »
           Si oui → action préventive (c'est l'alerte précoce)

[15-25 min] CORRÉLATIONS : la carte E11 à jour ?
            Une corrélation rompue est une information
            (le système a changé — chercher pourquoi)

[25-30 min] DÉCISIONS : résumé de la revue, decisions notées,
            vérification des levées de la dernière revue.
            Test : cette revue a-t-elle produit au moins une décision ?
```

**Le test du protocole :** la revue qui ne produit aucune décision pendant 3 semaines consécutives est soit un système parfaitement stable (rare), soit un rituel mort (fréquent) — la rotation des mesures ou le resserrement des seuils la réveille.

## Fiche 22 : Le gabarit de la carte des corrélations

**Usage :** le document qui relie les signaux aux résultats — l'intelligence du tableau.

```
CARTE DES CORRÉLATIONS — v[n]                Mise à jour : [date]

| Signal (N3) | Prédit (N4) | Délai | Force | Dernière vérification |
|-------------|-------------|-------|-------|----------------------|
| Divergences doc/modèle | Taux de retour | 2-3 semaines | forte | [date] |
| Tests flaky | Stabilité | 1 semaine | moyenne | [date] |
| [signal] | [aucune] | — | — | supprimé le [date] |

MÉTHODE DE VÉRIFICATION : alignement des séries sur 3 mois,
test visuel (les déviations coïncident-elles ?), à refaire
chaque trimestre.

LES CORRÉLATIONS ROMPUES (signal détecté, résultat non suivi,
ou inverse) : documentées avec leur explication — c'est là que
le système dit qu'il a changé.
```

**Exemple rempli (extrait réel) :**

```
CARTE DES CORRÉLATIONS — v3                  Mise à jour : 20/10

| Signal | Prédit | Délai | Force | Vérifié |
|--------|--------|-------|-------|---------|
| Divergences doc/modèle | Taux de retour | 2-3 sem | forte | 20/10 |
| Tests flaky | Stabilité | 1 sem | moyenne | 20/10 |
| Dérogations actives | Disponibilité | 3 sem | faible | 15/10 |
| Temps de pipeline | Délai total | 1 sem | forte | 20/10 |

CORRÉLATION ROMPUE (documentée) :
"Signaux IA non validées" ne corréle plus avec "retour" depuis
août. Explication : les règles d'usage IA (T7) ont changé le
comportement — les usages non validés ont été éliminés à la
source, le signal ne détecte plus rien parce qu'il n'y a plus
rien à détecter. Action : le signal reste (prévention), la
corrélation est marquée "observée historique".
```

**La valeur de la corrélation rompue :** elle raconte l'histoire du système. Une corrélation qui disparaît n'est pas un échec de la mesure : c'est souvent la preuve qu'une correction a fonctionné. La carte documente aussi les disparitions — c'est la mémoire de l'intelligence du tableau.

## Fiche 23 : Le gabarit de la mesure d'usage (confirmation N4)

**Usage :** la mesure d'adoption réelle — ce que la confirmation N4 produit.

```
MESURE D'USAGE — [fonctionnalité]           Mesurée : [période]

ADOPTION : [x]% des utilisateurs visibles l'utilisent
  [défini par : au moins 1 usage en 30 jours]

RÉTENTION : [x]% continuent après 30 jours
  [le premier usage est facile; la rétention est la vérité]

CONTOURNEMENT : [x]% font autrement pour le même besoin
  [détecté par : observation, support, questions]

FRÉQUENCE : [médiane d'usages par utilisateur actif]

ANALYSE :
- Adoptée mais non retenue : [les raisons]
- Contournée : [les raisons — souvent une lacune de conception]
- Non découverte : [les raisons — souvent un accompagnement manquant]

DESTINATION : [élicitation / design / accompagnement — avec action]
```

**La règle de la fiche :** une fonctionnalité non adoptée est un échec, pas une statistique. La destination (élicitation, design, accompagnement) est la partie la plus importante : elle transforme la mesure en action. Une mesure d'usage sans destination est un constat de décès sans autopsie.

## Le glossaire du niveau 4

**Mesure de résultat** — ce qui mesure l'effet perçu par l'extérieur : délai total, taux de retour, stabilité, disponibilité. À ne pas confondre avec la mesure d'activité (ce que l'équipe fait) : le résultat est la santé, l'activité est le symptôme.

**Mesure-miroir** — la contre-mesure d'abus : ce qui détecte l'optimisation perverse de la mesure principale. La règle : chaque mesure a son miroir, sinon elle sera trichée — la triche n'est pas une hypothèse, c'est une réponse humaine prévisible à une pression mal placée (loi de Goodhart).

**Corrélation signal→résultat** — la relation documentée entre un signal précoce (N3) et un résultat tardif (N4). La règle : une corrélation n'est une connaissance qu'après vérification sur données réelles (E11) — le reste est une croyance utile mais non vérifiée.

**Corrélation rompue** — une corrélation qui disparaît, avec son explication. La règle : la rupture est une information précieuse (le système a changé), documentée dans la carte — jamais silencieuse.

**Taux de retour** — les demandes rouvertes ou réassignées après livraison. La mesure la plus honnête de la satisfaction réelle : elle ne demande pas d'opinion, elle observe le comportement. Son miroir : le taux de ré-ouverture réellement vérifié (un retour jamais rouvert n'est pas vérifié).

**Adoption** — le pourcentage d'utilisateurs cibles qui utilisent réellement la fonctionnalité. La règle : l'adoption se mesure par le comportement (usage observé), pas par la déclaration (enquête de satisfaction). Un utilisateur qui dit qu'il aime et n'utilise pas est un utilisateur non adopté.

**Rétention** — le pourcentage qui continuent après 30 jours. La règle : la rétention est la vérité de l'adoption — le premier usage est facile, la continuation est la preuve.

**Disponibilité de capacité** — le pourcentage de semaines où l'équipe a de la capacité pour les demandes entrantes. La mesure de la soutenabilité : une équipe toujours à 100 % d'utilisation n'a aucune capacité pour l'imprévu — et l'imprévu arrive toujours.

**Charge perçue** — la mesure subjective de la charge de l'équipe (enquête courte, mensuelle). La règle : elle est une mesure-miroir des mesures objectives — la dissonance entre les chiffres et le ressenti est elle-même un signal (de l'angle mort du tableau).

**Rotation des mesures** — la règle : tout ajout au tableau = une sortie. La règle maintient la lisibilité et force la revue : une mesure qui entre doit justifier pourquoi elle mérite plus qu'une mesure qui sort.

**Audit de mesure** — le rituel trimestriel (E12) qui confronte le système de mesure complet : les mesures, les miroirs, les corrélations, le protocole. La règle : un audit qui ne supprime jamais rien n'a pas été honnête.
