
---

# Partie 9 : Les fiches-outils du niveau 5 et le glossaire de gouvernance

## Fiche 24 : Le gabarit de la charte du comité

**Usage :** la charte complète du comité qualité — le document fondateur du niveau 5.

```
CHARTE DU COMITÉ QUALITÉ — v[n]               Adoptée le : [date]

MÉTIER : [nom du comité]

COMPOSITION : [x] membres — un représentant actif par équipe +
[porteur du centre d'excellence] + [sponsor non-votant]
Rotation de présidence : [trimestrielle, binôme sortant/entrant]

QUORUM : [x] membres dont [y] représentants actifs
(défini : un membre est "actif" s'il pratique le niveau de son équipe)

LE COMITÉ DÉCIDE : [liste — seuils partagés, gabarits, dérogations,
escalades inter-équipes]

LE COMITÉ NE DÉCIDE PAS : [priorités produit, backlogs, organisation
interne des équipes, architecture sauf impact sur la chaîne partagée]

STANDARD DE PREUVE : toute décision s'appuie sur une donnée mesurée.
Une demande sans preuve est renvoyée sans débat.

REGISTRE : chaque décision notée (date, décision, preuve, POUR,
CONTRE, condition de révision). Registre public en interne.

CONTESTATION : [délai] jours, par écrit, avec preuve nouvelle.
Traitée au comité suivant.

ESCALADE AUTOMATIQUE : une lettre de veille sans réponse dans son
délai est escaladée au sponsor sans décision supplémentaire.

PROCHAINE CONVENTION DE RÉVISION : [date annuelle]
```

**Le test de la charte :** elle tient sur une page, elle est écrite par le comité (pas copiée d'un modèle), et elle contient la section « ne décide pas ». Une charte sans cette section est un organigramme, pas une gouvernance.

## Fiche 25 : Le gabarit de la décision du comité

**Usage :** chaque décision du comité suit ce format — le registre n'enregistre que les décisions complètes.

```
DÉCISION — [référence]                       Date : [date]
Présidence : [nom]          Présents : [n/total]   Quorum : oui/non

SUJET : [une phrase]

PREUVES PRÉSENTÉES :
1. [donnée, source, date]
2. [donnée, source, date]

OPTIONS CONSIDÉRÉES :
A. [option + conséquence chiffrée]
B. [option + conséquence chiffrée]

DÉCISION : [option retenue]

POUR : [noms]     CONTRE : [noms — avec leur raison, une phrase]

CONDITION DE RÉVISION : [ce qui ferait rouvrir la décision]

APPLICATION : porteur [nom], échéance [date], vérification au
comité du [date]
```

**Exemple rempli (extrait réel) :**

```
DÉCISION — CQ-2025-31                        Date : 10/10
Présidence : M.D.          Présents : 5/6   Quorum : oui

SUJET : évolution du gabarit standard de génération (gestion
des valeurs nulles).

PREUVES PRÉSENTÉES :
1. 4 dérogations identiques des équipes A, C, D en 2 mois
   (registre des dérogations)
2. 2 incidents de tests faux-positifs liés aux valeurs nulles
   (tickets INC-447, INC-451)

OPTIONS CONSIDÉRÉES :
A. Modifier le gabarit standard : ~3 jours de travail, élimine
   les dérogations futures de ce type
B. Rester au gabarit actuel : les équipes continuent de déroger,
   maintenance des dérogations ~1h/mois/équipe

DÉCISION : option A — modification du gabarit standard.

POUR : 5     CONTRE : 0

CONDITION DE RÉVISION : si les dérogations de type "valeurs
nulles" réapparaissent après l'application, la modification
sera réexaminée (probablement incomplète).

APPLICATION : porteur centre d'excellence, échéance 24/10,
vérification au comité du 07/11.
```

**La valeur du format :** la colonne CONTRE (avec raison) et la condition de révision. Une décision sans opposition enregistrée est suspecte (personne ne la lisait ?) ; une décision sans condition de révision est une décision qui se croit définitive — et les définitives finissent toujours par être fausses.

## Fiche 26 : Le gabarit de la demande de dérogation

**Usage :** toute équipe qui déroge à une règle commune suit ce format — la dérogation est une demande, pas un avertissement.

```
DEMANDE DE DÉROGATION — [référence]          Envoyée le : [date]
Équipe : [nom]   Règle concernée : [référence]

LA RÈGLE ET SON BUT (pourquoi elle existe) :
________________________________________________________

LA DÉROGATION DEMANDÉE (précise) :
________________________________________________________

POURQUOI (la contrainte réelle, avec preuve) :
________________________________________________________

DURÉE DEMANDÉE : [temporaire avec date / définitive avec raison]
CE QU'ON APPRENDRA : ____________________________________

PLAN DE RETOUR À LA RÈGLE (si temporaire) :
________________________________________________________
```

**La règle de la dérogation :** elle est une demande au comité (pas un avertissement à l'équipe), elle a une durée, et elle a un apprentissage déclaré. Une dérogation permanente est une demande de modification de règle déguisée — le comité la traite comme telle (modifier la règle pour tous, ou refuser).

## Fiche 27 : Le gabarit du bilan à l'échelle

**Usage :** le bilan trimestriel présenté au comité — dans l'ordre du vécu #5.

```
BILAN À L'ÉCHELLE — [trimestre]              Présenté le : [date]

PARTIE 1 — LA SANTÉ COLLECTIVE (d'abord) :
- Moyennes et tendances de l'organisation : [données]
- Ce qui s'améliore : [liste]
- Ce qui se dégrade : [liste]

PARTIE 2 — LES PRATIQUES DES RÉUSSITES :
- [Équipe X] : [pratique exceptionnelle + données]
- [Équipe Y] : [pratique + données]
- Plan de partage : [qui présente quoi, quand]

PARTIE 3 — LES PLANS DES RETARDS :
- [Équipe Z] : [écart + plan de rattrapage chiffré + soutien
  du comité demandé]
- [Chaque plan a : l'action, le porteur, l'échéance, le critère]

DÉCISIONS DEMANDÉES AU COMITÉ : [liste]
```

**La règle de l'ordre :** collectif d'abord (tout le monde est concerné), réussites ensuite (les sources d'apprentissage), plans enfin (les chantiers de soutien). L'ordre inverse transforme le bilan en compétition — et la compétition détruit la coopération que le comité existe pour construire.

## Fiche 28 : Le gabarit du parcours d'accueil d'une nouvelle équipe

**Usage :** toute équipe entrante suit ce parcours avant de participer à la gouvernance.

```
PARCOURS D'ACCUEIL — [équipe entrante]       Début : [date]

SEMAINE 1-2 : LA DÉCOUVERTE
- Assister à un comité (sans participer)
- Lire la charte, le registre, les règles
- Identifier les pratiques de son équipe qui devront évoluer

SEMAINE 3-4 : LE DIAGNOSTIC PARTAGÉ
- Mesurer ses propres données (avec la méthode commune)
- Comparer avec les seuils : où sont les écarts ?
- Écrire son plan de transition (avec les équivalences du système
  standard/contexte/transition)

MOIS 2 : L'APPLICATION
- Appliquer les règles communes sur un périmètre pilote
- Présenter son plan de transition au comité (première participation)

MOIS 3 : L'INTÉGRATION
- Participer pleinement au comité (avec mandat de son équipe)
- Premier bilan de son équipe au format commun

TEST DE SORTIE DU PARCOURS :
- Son plan de transition est accepté par le comité
- Ses données sont comparables (même méthode)
- Elle a un mandat réel de son équipe
```

**La règle du parcours :** une équipe qui hérite des règles sans les comprendre les contourne — c'est le vécu #6 (l'organisation qui grandit plus vite que sa gouvernance). Le parcours est l'anti-contournement structurel : il transforme l'arrivée en adhésion documentée.

## Le glossaire du niveau 5

**Comité qualité** — l'organe de gouvernance inter-équipes : périmètre écrit, quorum actif, registre public, contestation possible. Sa mesure de réalité : le taux d'application de ses décisions.

**Charte** — le document fondateur du comité : composition, quorum, périmètre (décide / ne décide pas), standard de preuve, contestation, escalade. Sa règle : écrite par le comité, attaquée par le comité (E8), révisée par convention.

**Registre** — la mémoire des décisions : date, décision, preuve, POUR, CONTRE, révision. Sa mesure : le taux de décisions survivant à l'épreuve de l'oubli (E9). Un registre unanime cache ; un registre avec CONTRE raconte.

**Dérogation** — la demande écrite d'écart à une règle commune : la règle et son but, l'écart, la contrainte réelle, la durée, l'apprentissage. Sa règle : c'est une demande au comité, jamais un avertissement à l'équipe.

**Standard/contexte/transition** — le système des seuils inter-équipes : le standard (direction commune), le contexte (l'écart assumé et documenté), la transition (le plan chiffré de convergence). Sa règle : les trois pour chaque seuil — l'un sans les autres produit maquillage ou révolte.

**Escalade automatique** — le mécanisme qui rend la gouvernance réelle : une lettre de veille sans réponse dans son délai est escaladée au sponsor sans décision humaine supplémentaire. Sa règle : l'escalade n'est pas un échec du comité — c'est la distribution correcte des décisions.

**Bilan à l'échelle** — le bilan trimestriel de toutes les équipes, présenté dans l'ordre : santé collective, pratiques des réussites, plans des retards. Sa règle : l'ordre de présentation décide si le bilan est un outil d'apprentissage ou une compétition.

**Parcours d'accueil** — le parcours obligatoire de toute équipe entrante avant de participer à la gouvernance : découverte, diagnostic partagé, application, intégration. Sa règle : hériter des règles sans les comprendre est le début du contournement.

**Convention de révision** — la réunion annuelle exceptionnelle qui révise la gouvernance elle-même : ce qui marche, ce qui ne marche pas, ce qui change. Présidée par un pair neutre. Sa règle : la réforme périodique est la prévention de la réforme forcée.

**Mandat réel** — l'autorisation écrite d'un membre du comité de la part de son équipe : ce qu'il peut décider, ce qu'il doit rapporter. Sa règle : un membre sans mandat représente sa présence, pas son équipe — et un comité de présences n'est pas un organe de gouvernance.

**Taux d'application** — la mesure de réalité du comité : le pourcentage de décisions du registre réellement appliquées dans leur délai. Sa règle : en dessous de 60 %, le comité est un fantôme — la refonte est plus urgente que la continuation.

**Présidence tournante** — la rotation de la présidence du comité : binôme sortant/entrant par trimestre. Sa règle : la rotation transmet (l'entrant apprend du sortant) et empêche la concentration du pouvoir.
