
---

# Partie 10 : Les fiches-outils du niveau 3

Chaque fiche est un outil tenu en une page, avec son usage, son format, et son exemple rempli. Elles s'impriment, se remplissent en atelier, et s'archivent au centre d'excellence.

## Fiche 13 : Le gabarit de rituel cadencé

**Usage :** pour chaque rituel forgé — le protocole qui permet à n'importe qui d'animer.

```
RITUEL — [Nom]                              Cadence : [jour, heure, durée]
Porteur : rotation (gabarit ci-dessous)

OBJECTIF (une phrase) : ______________________________________

ENTRÉES OBLIGATOIRES (ce qu'il faut pour tenir le rituel) :
- [donnée 1 — d'où elle vient, qui la prépare]
- [donnée 2]

DÉROULÉ (protocole minute par minute) :
1. [0-5 min] ________________________________
2. [5-15 min] _______________________________
3. [15-20 min] ______________________________

SORTIE OBLIGATOIRE (ce qui est produit, où il est archivé) :
________________________________________________________

SI JE DOIS LE RÉDUIRE (la version de crise, minimum vital) :
[les 5 minutes qui ne peuvent pas sauter]

SI JE DOIS LE REPORTER (ce qui est écrit au registre) :
[raison + date de reprise]

TEST DE RÉUSSITE (comment je sais que le rituel a eu lieu) :
________________________________________________________
```

**Exemple rempli (le point de qualimétrie de Sherweb, version 10 minutes) :**

```
RITUEL — Point de qualimétrie hebdo          Mardi 9h00, 10 minutes
Porteur : rotation (gabarit ci-dessous)

OBJECTIF : lire les 3 signaux, décider, noter.

ENTRÉES :
- Le tableau des 3 signaux (automatique, prêt à 8h55)
- Le registre des décisions de la semaine dernière (ouvert)

DÉROULÉ :
1. [0-3 min] Lecture des 3 signaux : valeur, tendance, seuil
2. [3-8 min] Pour chaque signal rouge : décision + porteur + levée
3. [8-10 min] Vérification des levées de la semaine dernière

SORTIE : le registre des décisions, mis à jour en séance

SI JE DOIS LE RÉDUIRE : signal 1 seul + décision + levée (5 min)
SI JE DOIS LE REPORTER : raison + date de reprise au registre.
Le report est un événement, pas un non-événement.

TEST DE RÉUSSITE : au moins une décision notée. Une réunion
sans décision n'a pas eu lieu — elle était un café.
```

## Fiche 14 : Le tableau des SLA par classe

**Usage :** la gestion des délais différenciés — le contrat de cadence de l'équipe.

```
TABLEAU DES SLA — version [n]              Décidé le : [date]

CLASSE          DÉFINITION                    SLA        VÉRIFIÉ PAR
Simple          1 passerelle, données prêtes  2 jours    Auto (pipeline)
Complexe        2+ passerelles ou données     5 jours    Porteur délai
                à construire
Exploratoire    Le besoin n'est pas clair      1 jalon    Revue de jalon
                (spike time-boxé)

MESURES DU DERNIER CYCLE :
Simple : [x] demandes, [y]% dans les délais
Complexe : [x] demandes, [y]% dans les délais
Exploratoire : [x] demandes, [y]% avec jalon tenu

RE-CLASSIFICATIONS (du registre) : [nombre] — pattern : [description]
```

**Exemple rempli (extrait réel) :**

```
TABLEAU DES SLA — version 2                Décidé le : 12/09

CLASSE          DÉFINITION                    SLA        VÉRIFIÉ PAR
Simple          ≤ 1 passerelle, données       2 jours    Auto (pipeline)
                existantes
Complexe        ≥ 2 passerelles OU données    5 jours    Porteur délai
                à construire
Exploratoire    Besoin non clarifié (spike    1 jalon    Revue de jalon
                de 2 jours max)

MESURES DU DERNIER CYCLE :
Simple : 23 demandes, 87% dans les délais (les 13% : données pas prêtes,
         classées simple par erreur — voir re-classifications)
Complexe : 8 demandes, 75% dans les délais (les 25% : revue repoussée,
         congés — pattern : les revues en fin de sprint)
Exploratoire : 2 demandes, 100% avec jalon tenu

RE-CLASSIFICATIONS : 4 (dont 3 simple→complexe : les données n'étaient
pas prêtes. Signal : le classement exige la vérification des données
AVANT le classement.)
```

## Fiche 15 : Le registre des réserves de Go/No-Go

**Usage :** le suivi des réserves — chaque réserve a sa levée, et la levée est vérifiée.

```
REGISTRE DES RÉSERVES — [année]

| Date Go | Version | Réserve (quoi, qui, quand) | Levée le | Comment |
|---------|---------|---------------------------|----------|---------|
```

**Exemple rempli (extrait réel) :**

```
REGISTRE DES RÉSERVES — 2025

| Date Go | Version | Réserve | Levée le | Comment |
|---------|---------|---------|----------|---------|
| 03/07 | 2.2 | Test intermittent (BUG-1301), correction sous 48h — L.T. | 05/07 | Corrigé, test ajouté au pipeline |
| 03/07 | 2.2 | Performance -12% sur 2 endpoints, optimisation sous 2 sem. — S.M. | 17/07 | Optimisé, métrique revenue au seuil |
| 24/07 | 2.3 | Documentation de l'API incomplète, complétée avant la doc client — P.G. | 31/07 | Complétée, vérifiée par le support |
| 14/08 | 2.4 | Migration des données historiques reportée au sprint suivant — Équipe | 28/08 | Migrée, 0 incident |

TAUX DE LEVÉE À DATE : 100% (4/4). Pattern : aucune réserve sans levée.
Ce taux est la preuve que les réserves sont réelles, pas décoratives.
```

**La règle de lecture :** le taux de levée à date est la métrique de crédibilité des réserves. En dessous de 80%, les réserves deviennent des excuses — et la grille perd son pouvoir.

## Fiche 16 : Le gabarit de la lettre de veille

**Usage :** quand le système de veille détecte une dérive — la lettre qui est envoyée au porteur de la dérive.

```
LETTRE DE VEILLE — [référence]              Envoyée le : [date]
Destinataire : [nom] — copie : [porteur du rituel]

CE QUE LA VEILLE A DÉTECTÉ (signaux datés) :
- [signal 1 : valeur, date, seuil franchi]
- [signal 2 : ...]

LE PATTERN (ce que les signaux dessinent ensemble) :
________________________________________________________

LES OPTIONS (chiffrées) :
A. [option 1 : action, coût, résultat attendu]
B. [option 2 : ...]
C. Ne rien faire (le coût de l'inaction : ____________)

DEADLINE DE RÉPONSE : [date — généralement 5 jours ouvrables]

Si aucune réponse à l'échéance : [escalade prévue — qui, quoi]
```

**Exemple rempli (extrait réel) :**

```
LETTRE DE VEILLE — V-2025-14               Envoyée le : 18/09
Destinataire : S.M. (porteur modèles) — copie : équipe

CE QUE LA VEILLE A DÉTECTÉ :
- Divergence doc/modèle : 4 (seuil : 2) — 3 semaines consécutives
- Dernière mise à jour du modèle BPM-004 : il y a 21 jours (seuil : 5)
- Tests flaky : 5 (seuil : 5) — dont 3 liés au modèle obsolète

LE PATTERN : le modèle BPM-004 n'est plus maintenu depuis 3 semaines,
et les signaux en dérivent tous. Ce n'est pas 3 problèmes : c'est 1
problème (l'abandon du maintien) qui en déclenche 3.

LES OPTIONS :
A. Rétablir le maintien : 2h/semaine, retour aux seuils sous 2 semaines
B. Réduire le périmètre du modèle : 1h/semaine, les signaux remontent
   partiellement
C. Ne rien faire : les divergences continueront de croître (~+2/semaine),
   le prochain Go/No-Go sera No-Go sur le critère doc/modèle

DEADLINE DE RÉPONSE : 25/09

Si aucune réponse : escalade au porteur du rituel de qualimétrie avec
recommandation de l'option A (consensus de l'équipe de veille).
```

**La règle de la lettre :** elle contient toujours l'option C (ne rien faire) chiffrée. L'inaction est une décision — et la lettre la rend visible, chiffrée, et datée. C'est ce qui distingue la veille du blame : la lettre ne dit pas « tu as mal fait », elle dit « voici les données, voici les options, voici le coût de l'inaction ».

## Fiche 17 : Le tableau de bord N3 — la version forgée

**Usage :** le tableau de bord du niveau 3 — 6 signaux, chaque signal a son risque d'origine.

```
TABLEAU DE BORD N3 — [équipe]              Cadence : hebdo, [jour]

| Signal | Risque d'origine | Seuil rouge | Valeur | Décision en cours |
|--------|-----------------|-------------|--------|-------------------|
| Divergences doc/modèle | L'incident du 12/03 (doc fausse en production) | > 2 | | |
| Tests flaky | La mise en prod du 24/05 (3 bugs intermittents) | > 5 | | |
| Temps de cycle commit→prod | La promesse client du T1 | > 3 jours | | |
| Divergences IA non validées | Le risque de dérive de l'IA (règles T7) | > 20% | | |
| Dérogations actives | Le précédent du 03/07 (réserves sans levée) | > 3 | | |
| Modèles non mis à jour > 5 jours | Le modèle BPM-004 abandonné (lettre V-14) | > 0 | | |
```

**La colonne « risque d'origine » est la colonne la plus importante du niveau 3 :** elle rappelle pourquoi le signal existe. Un seuil sans risque d'origine est un nombre arbitraire — et les nombres arbitraires finissent toujours par être contestés, puis ignorés.

## Fiche 18 : Le gabarit de l'audit de cadence

**Usage :** le rituel de fin de cycle du niveau 3 — une fois par trimestre, 90 minutes.

```
AUDIT DE CADENCE — [trimestre]             Tenu le : [date]

PILIER 1 : Les critères vivants (grille, SLA, seuils)
- Tiennent-ils sans le coach ? [oui/non/preuve]
- Ont-ils survécu à une urgence ? [récit ou non]
- La relève existe-t-elle ? [noms ou non]

PILIER 2 : Le pipeline cadencé
- Même interrogation, 3 questions

PILIER 3 : La confirmation systématique
- Même interrogation, 3 questions

PILIER 4 : La veille et les seuils
- Même interrogation, 3 questions

LA CARTE DE FRAGILITÉ :
- Piliers qui échouent : [liste]
- Chantiers de la forge suivante : [actions datées]
- Ce qui est solide : [ce qu'on ne touche plus]
```

**La règle de l'audit :** il ne cherche pas la perfection, il cherche les fragilités. Un audit de cadence qui ne trouve aucune fragilité n'a pas été honnête — et la fragilité la plus dangereuse est celle du pilier qui a toujours réussi : c'est celui qu'on a cessé de tester.

## Le glossaire du niveau 3

**Cadence** — le rythme fixe d'un rituel : même heure, même durée, même protocole, indépendamment des urgences. La règle : jamais reporté, parfois réduit, toujours écrit. La cadence est ce qui distingue un système vivant d'une collection d'intentions.

**SLA par classe** — le délai différencié par type de demande : simple, complexe, exploratoire. La règle : chaque classe a son délai, chaque demande est classée à l'entrée, chaque re-classification est notée. Le SLA uniforme est un piège de simplification.

**Réserve** — ce qu'on accepte malgré tout dans un Go, avec sa levée datée. La règle : une réserve sans levée n'est pas une réserve — c'est une excuse. Le taux de levée à date est la métrique de crédibilité.

**Pipeline à trois vitesses** — la hiérarchie des tests : bloquants au commit (rapides, fiables), bloquants au merge (conflits), informatifs la nuit (exploratoires). La règle : un test bloquant doit être fiable ; un test fragile ne protège rien.

**Confirmation systématique** — chaque défaut résolu a un statut de confirmation explicite. La règle : un défaut sans statut n'est pas fermé. Le protocole varie par classe ; l'absence de statut, jamais.

**Lettre de veille** — la communication formalisée d'une dérive détectée : signaux datés, pattern, options chiffrées, deadline. La règle : toujours l'option C (ne rien faire) chiffrée. La veille n'est pas du blame : c'est une décision rendue visible.

**Seuil forgé** — un seuil posé sur des données réelles, avec son risque d'origine. La règle : un seuil sans risque d'origine est un nombre arbitraire. Les seuils se forgent sur 2-3 semaines de données, pas sur une intuition.

**Audit de cadence** — le rituel trimestriel qui confronte les quatre piliers de la forge aux trois tests (urgence, relève, transmission). La règle : un audit sans fragilité trouvée n'a pas été honnête.

**Rotation outillée** — la charge tournante rendue possible par le protocole : gabarit d'animation, données prêtes, binôme de transition. La règle : si la rotation tue le rituel, le rituel était décoratif.

**Forge** — le processus qui rend une pratique indépendante du coach, des porteurs initiaux et des urgences. La règle : la forge n'est terminée que quand la pratique survit au départ de ceux qui l'ont construite.
