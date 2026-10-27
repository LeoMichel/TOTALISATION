
---

# Annexe : Le carnet du praticien N4 et les gabarits remplis

Le praticien du niveau 4 a une matière première nouvelle : la donnée. Ses fiches documentent les mesures définies, les miroirs construits, les corrélations observées, et les conversations tenues. Le carnet du praticien N4 est le carnet du praticien N3 enrichi d'une colonne : la donnée.

## Le carnet du praticien N4 (un document, cinq fiches)

1. La fiche de mesure (chaque mesure définie : début, fin, inclus, exclu, miroir, risque d'abus)
2. La fiche de miroir (chaque miroir construit : le test de la triche probable)
3. La fiche de corrélation (chaque corrélation signal→résultat : la vérification, le délai, la force)
4. La fiche de revue (chaque revue de tableau : les mesures lues, les dérives confirmées, les décisions prises)
5. La fiche de sponsor (chaque conversation avec le sponsor : les données partagées, la réaction, la décision)

## La fiche de mesure remplie (extrait réel)

```
MESURE — Délai total de traitement          Définie le : 15/09
CE QU'ELLE RÉVÈLE : la vitesse réelle de réponse aux demandes,
vue par le demandeur (pas par l'équipe).

DÉBUT : réception de la demande complète (tous les champs du
gabarit remplis — une demande incomplète n'est pas comptée,
elle est retournée avec la liste des champs manquants).

FIN : livraison acceptée par le demandeur (pas « livrée » :
l'acceptation explicite ou 5 jours sans objection).

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

## La fiche de revue remplie (extrait réel)

```
REVUE DU TABLEAU N4 — 09/10              Animateur : L.M.

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

## La fiche de sponsor remplie (extrait réel)

```
CONVERSATION SPONSOR — 09/10              Avec : le sponsor (T.B.)

DONNÉES PARTAGÉES :
- Délai total : 14 → 11 jours (tendance ↘)
- Taux de retour : 30 → 9% (tendance ↘)
- Temps de pipeline : 11 → 13 min (dérive, investigation en cours)

RÉACTION DU SPONSOR :
« Le délai de 14 jours que vous m'avez montré le mois dernier,
c'était la vérité. Je ne le savais pas — et je suis en partie
responsable des 2 jours d'attente de clarification. Je mets
une session hebdomadaire de clarification à disposition. »

ACTION DU SPONSOR :
Session hebdomadaire de clarification (lundi 11h), pour les
demandes incomplètes. À partir du 14/10.

RÉSULTAT OBSERVÉ (à 4 semaines) :
Délai total : 14 → 9 jours (les 2 jours de clarification sont
passés de 2 à 0,5 jour en médiane).

CE QUE CETTE CONVERSATION A APPRIS :
Le sponsor qui voit les données honnêtes devient un allié.
Le praticien qui présente les données brutes (sans maquillage)
fabrique un allié — pas un juge.
```

## La fiche de corrélation remplie

```
CORRÉLATION — Divergences doc/modèle → Taux de retour
Vérifiée le : 20/10    Méthode : alignement des séries sur 3 mois
| Semaine | Divergences (N3) | Retour (N4) |
|---------|-----------------|-------------|
| S1 | 4 | 18% |
| S2 | 3 | 14% |
| S3 | 2 | 11% |
| S4 | 1 | 6% |
| S5 | 0 | 4% |

CORRÉLATION : forte, négative, délai 1 semaine. Quand les
divergences baissent, le taux de retour baisse avec une semaine
de décalage. Testée sur 5 semaines : la tendance est cohérente.

ACTION : cette corrélation est documentée dans la carte (v2) —
le signal "divergences doc/modèle" devient un prédicteur du
taux de retour. Si les divergences remontent, le taux de retour
va remonter dans une semaine : agir sur les divergences prévient
le retour.
```

## La carte de sortie du carnet N4

Le carnet N4 est le test du niveau 4 : montrez-moi vos fiches de mesure (avec les miroirs), vos fiches de revue (avec les décisions), vos fiches de sponsor (avec les réactions), vos fiches de corrélation (avec les vérifications). Si ces fiches existent, votre niveau 4 est réel. Si elles n'existent pas, votre niveau 4 est un discours — et le discours ne mesure pas.

Le praticien qui transmet son carnet transmet sa lucidité. Le praticien qui transmet la méthode transmet une théorie. La collection demande les deux — mais commence toujours par le premier.
