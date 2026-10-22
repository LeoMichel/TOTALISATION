
---

# Partie 10 : Les fiches-outils du niveau 6

## Fiche 29 : Le gabarit du signal faible

**Usage :** déposer un signal au canal — le format qui distingue l'observation de l'opinion.

```
SIGNAL — [date]                 Déposé par : [nom]

J'AI REMARQUÉ (observation factuelle, une phrase) :
________________________________________________________

QUAND / COMBIEN DE FOIS :
[première observation : date] — répété : [n fois / période]

CONTEXTE (où, dans quel travail) :
________________________________________________________

(je ne sais pas encore ce que ça veut dire — c'est pour ça
que je le dépose.)
```

**Exemple rempli (tiré du cas Opal-RT) :**

```
SIGNAL — 04/09                 Déposé par : M.G.

J'AI REMARQUÉ : le build de nuit prend plus de temps que
d'habitude (plus de 40 minutes, contre ~28 avant).

QUAND / COMBIEN DE FOIS : première fois le 02/09, répété
4 fois en 8 jours de build.

CONTEXTE : sur les branches de la nouvelle infrastructure
de build (post-migration).

(je ne sais pas encore ce que ça veut dire — c'est pour ça
que je le dépose.)
```

**La valeur du format :** la dernière ligne (« je ne sais pas encore ») est structurelle — elle désarme le jugement (« est-ce que c'est grave ? ») et oriente vers l'observation. Un signal n'est pas une alarme : c'est une graine.

## Fiche 30 : Le gabarit de la revue des signaux

**Usage :** la cérémonie hebdomadaire de 20 minutes — le protocole qui donne vie au canal.

```
REVUE DES SIGNAUX — [date]          Animation : [rotation]
Présents : [l'équipe]

SIGNAUX DE LA SEMAINE : [n]
| Signal | Déposé par | Répété ? | Tendance |
|--------|-----------|----------|----------|
|        |           |          |          |

TENDANCES CONFIRMÉES (3 fois ou plus) :
→ [signal] → élicitation proactive ? oui/non (pourquoi)
→ [signal] → chantier de prévention ? oui/non (pourquoi)

SIGNALS SANS SUITE (et pourquoi c'est normal) :
[la plupart des signaux ne confirment pas — c'est le
fonctionnement normal du canal, pas son échec]

PROCHAINES ACTIONS : [quelques mots]
```

**La règle de la revue :** elle observe, elle ne décide pas. Les décisions viennent des confirmations — et les signaux non confirmés restent listés (ils peuvent se confirmer plus tard). La revue qui juge les signaux tue le canal : personne ne dépose pour être jugé.

## Fiche 31 : Le gabarit du chantier de prévention

**Usage :** au registre de prévention — chaque chantier avec sa preuve attendue.

```
CHANTIER DE PRÉVENTION — P-[n]       Cré le : [date]
Origine : [signal confirmé / apprentissage / incident évité]

LE PROBLÈME (le scénario d'incident évité, une phrase) :
SI rien n'est fait, ALORS ____________________________

LA PRÉVENTION (ce qu'on construit) :
________________________________________________________

PREUVE ATTENDUE (la morsure mesurable) :
- l'incident évité : ________________________
- le temps épargné : ________________________
- la tendance corrigée : ____________________

PORTEUR : [nom — avec capacité réservée]
ÉCHEANCE : [date]
STATUT : [à venir / en cours / livré — morsure mesurée le : ___]

APRÈS LA MORSURE (rempli à la livraison) :
La morsure réelle : ________________________
Chiffrée : _________________________________
Documenté dans la mémoire : [référence]
```

**Exemple rempli (tiré du cas Opal-RT) :**

```
CHANTIER DE PRÉVENTION — P-7         Cré le : 12/09
Origine : signal du 04/09 confirmé (build +40 min, tendance)

LE PROBLÈME : SI rien n'est fait, ALORS le build dépasse le
délai d'intégration continue dans ~6 semaines — panne de
build pour toute l'équipe, au pire moment (démonstration client).

LA PRÉVENTION : investiguer la régression de build, identifier
la cause, corriger.

PREUVE ATTENDUE :
- l'incident évité : la panne de build (délai dépassé)
- le temps épargné : les jours de blocage de l'équipe
- la tendance corrigée : le temps de build retourne sous 30 min

PORTEUR : M.G. — 4 heures réservées (capacité préventive)
ÉCHEANCE : 30/09
STATUT : livré le 06/09 — morsure mesurée

APRÈS LA MORSURE :
La morsure réelle : dépendance cachée (téléchargement à chaque
build au lieu du cache), introduite 3 semaines plus tôt.
Chiffrée : 2 heures de détection/correction vs ~1 semaine de
blocage (8 personnes) évitée. Ratio : 1:20.
Documenté dans la mémoire : entrée MEM-042, thème "infrastructure
de build", apprentissage : "les dépendances cachées se voient
dans le temps de build, pas dans les erreurs — surveiller la
tendance, pas les échecs."
```

## Fiche 32 : Le gabarit de l'entrée de mémoire

**Usage :** enrichir la mémoire organisationnelle — le format indexé et réutilisable.

```
MÉMOIRE — MEM-[n]                    Cré le : [date]
THÈME : [thème indexé (recherche par thème)]

L'APPRENTISSAGE (une phrase testable) :
________________________________________________________

D'OÙ ÇA VIENT (l'expérience qui l'a appris) :
[event — incident, chantier, confirmation, échec d'anticipation]
Chiffré : [le coût ou le gain mesuré]

LA RÈGLE ACTIVE (ce qu'on fait différemment maintenant) :
________________________________________________________

RELIONS : [autres apprentissages similaires — MEM-x, MEM-y]
TYPE : [règle active / cas limite / hypothèse à surveiller /
       anti-pattern]
```

**Exemple rempli (tiré du cas Histoire 3) :**

```
MÉMOIRE — MEM-042                    Cré le : 07/09
THÈME : intégrations API tiers ; infrastructure de build

L'APPRENTISSAGE : les dépendances cachées (téléchargements
à chaque build) se voient dans le TEMPS de build, pas dans
les erreurs — surveiller la tendance, pas les échecs.

D'OÙ ÇA VIENT : chantier P-7 (signal faible confirmé).
Chiffré : 2 heures de correction vs ~1 semaine de blocage
d'équipe évitée.

LA RÈGLE ACTIVE : toute modification de l'infrastructure de
build est suivie d'une semaine de surveillance du temps de
build (tendance, pas seulement succès/échec).

RELIONS : MEM-017 (les API tiers changent sans préavis),
MEM-031 (les régressions silencieuses).
TYPE : règle active.
```

**La valeur du champ RELIONS :** c'est lui qui transforme des notes en réseau. L'apprentissage des dépendances cachées relié à celui des API changeantes dessine une famille : « les systèmes externes se comportent différemment de ce qu'ils promettent ». Les familles d'apprentissages sont ce que la consultation (fiche 33) cherche.

## Fiche 33 : Le gabarit de consultation mémoire

**Usage :** les vingt minutes obligatoires du DoR N6 — la consultation qui fait vivre la mémoire.

```
CONSULTATION MÉMOIRE — [thème de la spécification]
Date : [date]   Consulté par : [nom]   Durée : 20 min

THÈMES CHERCHÉS : [les mots-clés de la spécification]

ENTRÉES TROUVÉES : [liste MEM-x]
- Applicables directement : [lesquels]
- Applicables avec adaptation : [lesquels, comment]
- Inapplicables : [lesquels, pourquoi — c'est utile aussi]

RÈGLES ACTIVES HÉRITÉES (à intégrer à la spécification) :
________________________________________________________

CAS LIMITES HÉRITÉS (à ajouter) :
________________________________________________________

NOUVEAU APPRENTISSAGE (ce que la consultation révèle
que la mémoire n'avait pas) :
________________________________________________________
→ nouvelle entrée MEM-[n] : oui/non
```

**Le test de la consultation :** elle doit trouver quelque chose — sinon c'est l'indexation qui est défaillante. Et elle doit souvent produire une nouvelle entrée : la consultation d'un thème révèle ce que la mémoire ignorait du thème.

## Fiche 34 : Le gabarit de projection

**Usage :** chaque projection du tableau N6 — datée, signée, à valider rétroactivement.

```
PROJECTION — [métrique]              Faite le : [date]
Par : [nom]                          Horizon : 4 semaines

TENDANCE OBSERVÉE (8 semaines de données) :
[valuer initiale → valeur actuelle, direction]

PROJECTION : dans 4 semaines, la métrique sera à [valeur]
SI la tendance continue (condition explicite)

ZONE D'ALERTE : [valeur — au-delà, décision préventive]

VALIDATION RÉTROACTIVE (remplie à l'échéance) :
Valeur réelle : ______ | Écart : ______ | Verdict : fiable / faux
Si faux : [pourquoi — l'hypothèse, la tendance, la mesure ?]
Action : [corriger la projection / la retirer]
```

**La règle de la projection :** elle porte sa condition (« SI la tendance continue ») et son verdict rétroactif. Une projection sans condition prétend à la vérité ; une projection sans validation reste une opinion. Le tableau des projections validées est la carte de crédibilité du système prédictif — c'est lui qu'on montre à la direction.

## Le glossaire du niveau 6

**Signal faible** — une observation neutre déposée au canal, sans interprétation, sans jugement. Sa règle : « j'ai remarqué que », jamais « il faudrait ». Un signal n'est pas une alarme : c'est une graine.

**Règle des trois confirmations** — un signal confirmé trois fois (trois sources ou trois semaines) devient une élicitation proactive ou un chantier. Sa règle : elle protège de l'ivresse de l'anticipateur — la confirmation demande du temps, et le temps est le filtre.

**Élicitation proactive** — une élicitation lancée par le système prédictif (signal confirmé), toujours AVEC le demandeur pressenti, jamais POUR lui. Sa règle : les signaux ouvrent la conversation, ils ne la remplacent pas (Histoire 4).

**Capacité préventive** — la part de capacité réservée aux chantiers de prévention (règle du comité, typiquement 10-15 %). Sa règle : tout report est écrit, daté, avec rattrapage — le report reconduit tacitement est un abandon (Histoire 2).

**Chantier de prévention** — un travail préventif au registre, avec sa preuve attendue (l'incident évité, le temps épargné, la tendance corrigée). Sa règle : sans preuve attendue, pas de chantier — la prévention sans morsure mesurable est du perfectionnisme.

**Morsure** — le résultat mesuré d'une prévention livrée : l'incident évité, chiffré. Sa règle : la morsure est la monnaie de la prévention — elle se mesure à la livraison, et elle se documente dans la mémoire. C'est elle qui défend la capacité préventive à chaque arbitrage.

**Mémoire organisationnelle** — le réseau des apprentissages indexés (MEM-x), consulté au DoR, enrichi à chaque spécification. Sa règle : elle vit par les deux sens (consultation ET enrichissement) — une mémoire seulement consultée devient obsolète, une mémoire seulement enrichie devient un placard.

**Consultation mémoire** — les vingt minutes obligatoires du DoR N6 : chercher le thème, hériter des règles actives et des cas limites. Sa règle : elle doit trouver quelque chose — si jamais, c'est l'indexation qui est défaillante.

**Projection** — la prédiction d'une métrique à quatre semaines, avec sa condition (SI la tendance continue) et sa validation rétroactive. Sa règle : une projection sans condition prétend à la vérité ; une projection sans validation reste une opinion.

**Validation rétroactive** — la comparaison de la projection passée avec le réel. Sa règle : c'est le test de crédibilité du système prédictif — les projections toujours fausses sont corrigées ou retirées, et le taux de fiabilité est public.

**Post-mortem d'anticipation** — la rétrospective d'une anticipation manquée : le signal existait-il, pourquoi n'a-t-il pas été confirmé. Sa règle : la faute est toujours une cérémonie, jamais une personne — un post-mortem qui nomme un coupable tue le canal.

**Régime** — ce que le niveau 6 devient après l'installation : un ensemble de pratiques nourries en continu (canal, règle, mémoire, projections), entretenues par le bilan trimestriel. Sa règle : le niveau 6 n'est pas un état, c'est un régime — l'exercice s'achève, le régime commence.
