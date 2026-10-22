
---

# Partie 26 : Les gabarits remplis du niveau 4 — l'équipe Karim raconte

Cette partie présente quatre gabarits remplis par une équipe réelle — l'équipe Karim — pour montrer le niveau de spécificité attendu au niveau 4. TOTALISATION ne remplace jamais la parole de l'équipe : il la cadre, la garde, et la rend transmissible.

## Gabarit rempli : la fiche de définition du délai total

```
MESURE — Délai total de traitement          Définie le : 15/09
CE QU'ELLE RÉVÈLE : la vitesse réelle de réponse aux demandes,
vue par le demandeur (pas par l'équipe).

DÉBUT DU COMPTAGE : réception de la demande complète
(tous les champs du gabarit remplis — une demande incomplète
n'est pas comptée, elle est retournée avec la liste des champs
manquants).

FIN DU COMPTAGE : livraison acceptée par le demandeur
(pas « livrée » : l'acceptation explicite ou 5 jours sans
objection).

INCLUS : tous les temps d'attente (y compris les nôtres).

EXCLU : les demandes retirées par le demandeur.

SOURCE : automatique — le système de tickets, champ
"date d'acceptation" ajouté en v2.

MIROIR : taux de re-classification — détecte les demandes
complexes classées "simples" pour préserver le délai.

RISQUE D'ABUS : découper les demandes longues en plusieurs
courtes (le découpage artificiel) — détecté par la mesure du
nombre de demandes par thème (une hausse soudaine = découpage).

FRÉQUENCE DE REVUE : hebdomadaire (rituel du mardi)
DÉCLENCHEUR D'ACTION : dérive > 20% de la médiane mobile
sur 4 semaines → décision du praticien

HISTORIQUE DES DÉFINITIONS :
v1 (15/09) : définition initiale, fin = "livrée"
v2 (02/10) : fin changée en "acceptée" — les livraisons
techniquement faites mais refusées trompaient la mesure
```

## Gabarit rempli : le tableau de bord N4 de l'équipe Karim

```
TABLEAU DE BORD N4 — Équipe Karim          Cadence : mardi, 30 min

MESURES DE RÉSULTAT (avec miroir) :
| Mesure | Tendance | Miroir | Dernière action |
|--------|----------|--------|-----------------|
| Délai total | ↗ (14j → 9j) | Re-classifications | 02/10 : v2 de la définition |
| Taux de retour | ↘ (30% → 6%) | Ré-ouvertures | 09/10 : définition resserrée |
| Stabilité post-livraison | → | Contournements | — |
| Disponibilité de capacité | ↗ | Reports non planifiés | — |

SIGNAUX D'ÉQUIPE (les plus corrélés — carte E11 v2) :
| Signal | Tendance | Corrélation documentée |
|--------|----------|------------------------|
| Divergences doc/modèle | ↘ | → Taux de retour (2 sem) |
| Temps de pipeline | ↗ | → Délai total (1 sem) |

RÈGLE DE ROTATION : tout ajout = une sortie

DERNIÈRE DÉCISION : 02/10, v2 de la définition du délai
(accepté par l'équipe, présenté au sponsor le 09/10)
```

## Gabarit rempli : la revue hebdo de l'équipe Karim (semaine du 09/10)

```
REVUE DU TABLEAU N4 — 09/10              Animateur : rotation (L.M.)

[0-5 min]  RÉSULTATS :
| Mesure | Tendance | Dérive ? |
|--------|----------|----------|
| Délai total | ↘ 14j → 11j | non |
| Taux de retour | ↘ 30% → 9% | non |
| Stabilité | → 0 incident post-livraison | non |
| Disponibilité | ↗ 20% → 25% | non |

Toutes les mesures dans les seuils. Question standard : « normal ».

[5-15 min]  SIGNAUX :
| Signal | Tendance | Dérive ? |
|--------|----------|----------|
| Divergences doc/modèle | ↘ 4 → 2 | non |
| Temps de pipeline | ↗ 11 min → 13 min | OUI |

Décision : le temps de pipeline dérive (première alerte du
miroir E9). Causes possibles : tests plus longs (2 demandes
complexes), environnement partagé. Action : L.M. investigue,
décision au prochain tableau.

[15-25 min]  CORRÉLATIONS :
La carte E11 est à jour (v2, 20/10). Une corrélation à
vérifier : le signal "temps de pipeline" prédit-il la
stabilité post-livraison ? À re-tester dans 4 semaines.

[25-30 min]  DÉCISIONS :
1. L.M. investigue le temps de pipeline (délai : mardi prochain)
2. Re-lecture des levées de la dernière revue : 1/2 levée à date
3. Prochaine revue : mardi 16/10

TEST : la revue a produit 1 décision. ✓
```

## Gabarit rempli : la carte des corrélations de l'équipe Karim

```
CARTE DES CORRÉLATIONS — v2                Mise à jour : 20/10

| Signal (N3) | Prédit (N4) | Délai | Force | Vérifié |
|-------------|-------------|-------|-------|---------|
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

## Gabarit rempli : l'épilogue du praticien du niveau 4 (l'équipe Karim)

```
ÉPILOGUE DU PRATICIEN — Année 2025        Rempli le : 15/12
Nom : Karim    Rôle : praticien du niveau 4

1. CE QUE CETTE ANNÉE M'A APPRIS :
a) La mesure révèle l'attente, pas la lenteur — 8 jours sur 14
   étaient de l'attente, et l'attente se traite.
b) Les définitions sont plus importantes que les mesures —
   deux semaines sur les définitions ont été le meilleur
   investissement du niveau.
c) Le sponsor qui co-crée les mesures devient un allié — la
   session hebdomadaire de clarification (proposée par le
   sponsor) a réduit le délai de 5 jours.

2. LE MOMENT DONT JE SUIS LE PLUS FIER :
Le jour où M.T. a animé la revue du tableau sans moi. Elle a
posé la question standard (« dérive ou normal ? »), elle a pris
une décision, elle a noté au registre. Je n'ai pas dit un mot.
C'est le moment où j'ai su que la mesure avait changé l'équipe.

3. LE MOMENT QUI M'A LE PLUS DÉFIÉ :
Le premier sponsor honnête (Histoire 4). J'ai présenté les
données brutes (14 jours au lieu de 3 espérés). J'attendais une
réaction négative. J'ai eu : « je croyais que vous étiez plus
rapides. Je me trompais. Comment puis-je vous aider ? » — et
c'est le sponsor qui a proposé la session de clarification. La
mesure n'a pas changé l'équipe : elle a changé le sponsor.

4. LE RITUEL QUI FONCTIONNE LE MIEUX :
La revue hebdo de 30 minutes. Elle tient, elle produit des
décisions, elle est animée en rotation. C'est le rituel que
l'équipe protège quand les semaines sont dures — parce qu'il
leur donne la lucidité quand ils en ont le plus besoin.

5. LE RITUEL QUI FONCTIONNE LE MOINS BIEN :
L'audit de mesure trimestriel (E12). Il a été fait une fois —
et il a révélé deux fragilités (le miroir E9, les corrélations
E11). Mais il n'a pas été refait — le trimestre était chargé.
C'est la fragilité de l'année : le rituel qui protège le régime
n'est pas fait. À corriger l'année prochaine.

6. MA CONVICTION LA PLUS SOLIDE :
La mesure ne remplace pas le jugement — elle l'éclaire. Elle ne
remplace pas la conversation — elle l'ancre. Elle ne remplace
pas la confiance — elle la prouve. Une équipe qui mesure son
délai découvre l'attente, corrige l'attente, améliore le délai
— et apprend à mesurer. Ce que le niveau 4 fabrique d'abord,
ce n'est pas de meilleurs produits : c'est des équipes qui
savent ce qui se passe, et qui peuvent en décider.

7. MA CONVICTION LA PLUS FRAGILE :
Je me demande si les miroirs d'abus sont vraiment nécessaires.
Ils n'ont détecté qu'une triche (la sur-classification) — et
cette triche était bénigne. Peut-être que la confiance suffit ?
Mais je sais que cette pensée est le début du glissement : la
confiance est ce qu'on fabrique, pas ce qu'on présuppose. Les
miroirs restent.

8. CE QUE JE VEUX DIRE À MOI-MÊME DANS UN AN :
Karim, tu as construit un système de mesure honnête. Tu as
traversé la triche, le sponsor sceptique, le premier renoncement
à un rituel (l'audit E12), la carte des corrélations qui a
survécu à la réalité. L'année prochaine, la question n'est pas
"as-tu encore un système de mesure ?" — c'est "as-tu encore le
courage de regarder ce que tu mesures ?". Le courage de la
lucidité est plus rare que la compétence de la mesure. Garde-le.
```

---

*Fin des gabarits remplis du niveau 4.*
