
---

# Partie 20 : Les gabarits remplis — trois semaines réelles du niveau 3

## Gabarit A : Semaine 3 complète (SLA et veille) — version remplie

### Lundi — forgeage du SLA avec les données réelles (2h, 14h-16h)

**Présents :** l'équipe au complet (9), le praticien.

**Entrées :** les 23 demandes traitées dans les 6 dernières semaines, avec leur délai réel (reçu → livré accepté).

**Étape 1 (30 min) — le tri des délais réels :**
L'équipe trie les 23 demandes par délai réel croissant et regarde la distribution : 8 demandes en ≤ 1 jour, 6 en ≤ 3 jours, 5 en ≤ 8 jours, 4 en > 8 jours.

**Étape 2 (30 min) — la recherche du pattern :**
Pour chaque groupe, la question : « qu'est-ce qui a rendu ces demandes rapides/lentes ? ». Les réponses convergent vers trois variables : nombre de fichiers touchés, dépendances externes, et disponibilité de l'environnement de test. Les demandes « ≤ 1 jour » touchaient en moyenne 2 fichiers sans dépendance ; les demandes « > 8 jours » touchaient 9 fichiers en moyenne avec au moins 1 dépendance.

**Étape 3 (30 min) — la forge des seuils de classement :**
Les seuils ne sont pas arbitrés : ils sont déduits des données. Le comité propose :
- **Simple** : ≤ 3 fichiers, aucune dépendance externe, environnement disponible → SLA : 2 jours
- **Standard** : 3-6 fichiers, dépendances internes → SLA : 5 jours
- **Complexe** : > 6 fichiers, dépendances externes, environnement à construire → SLA : 10 jours
- **Exploratoire** : le besoin n'est pas clair (spike time-boxé à 2 jours) → pas de SLA de résolution, jalon de décision

**Étape 4 (30 min) — le test sur les 23 demandes :**
L'équipe re-classe les 23 demandes avec les nouveaux seuils. Résultat : 18/23 concordent avec le délai réel (78 %). Les 5 discordants sont analysés : 3 étaient des demandes simples qui auraient dû être complexes (dépendance non identifiée au triage), 2 étaient des demandes complexes dont la dépendance a été plus rapide que prévu. **Conclusion :** les seuils sont bons à 78 % ; les cas limites sont documentés dans le gabarit de classement.

**Livrable :** le tableau des SLA (fiche 14), avec les seuils forgés sur données et les 5 cas limites documentés.

### Mardi — première application du classement (à chaud)

**Les 3 demandes de la semaine sont classées par les développeurs qui les prendront, avec le gabarit :**
- #2001 : 2 fichiers, aucune dépendance → **Simple** (SLA : 2 j). Le développeur vérifie : aucun fichier externe. ✓
- #2002 : 7 fichiers, 1 dépendance (API comptable) → **Complexe** (SLA : 10 j). Le développeur signale la dépendance au triage.
- #2003 : 5 fichiers, dépendance interne (module de facturation déjà testé) → **Standard** (SLA : 5 j). Le développeur note que la dépendance est stable.

**Observation :** aucune re-classification nécessaire cette semaine (les seuils forgés tiennent). Le praticien note le taux : 0 % de re-classification cette semaine (vs 60 % la semaine avant).

### Jeudi — première revue des re-classifications (30 min)

**Aucune re-classification. La revue s'est tenue en 10 minutes au lieu de 30 : l'équipe a confirmé que le classement tient, et a discuté 20 minutes d'un sujet émergent (la dépendance API comptable, qui a annoncé une version majeure).**

### Vendredi — la première lettre de veille (30 min, rédigée par S.R.)

**Rapport de non-alerte (gabarit B2 de l'annexe B, rempli).**
**Une veille → deux actions :** (1) le point de vigilance sur l'API comptable est noté ; (2) la lettre est envoyée au sponsor et aux équipes.

**Livrable de la semaine :** le tableau des SLA (forgé sur données), les 3 demandes classées sans re-classification, la lettre de veille avec un point de vigilance. **Ce qui a tenu :** les seuils forgés sur données tiennent sans re-classification — la preuve que le forgeage sur données vaut mieux que le forgeage sur opinion.

---

## Gabarit B : Semaine 5 complète (le point mort du niveau 3) — version remplie

### Lundi — le diagnostic sans illusion (2h, 9h-11h)

**Entrée :** les comptes rendus des 4 semaines écoulées, le registre des décisions, les lettres de veille.

**Étape 1 (30 min) — l'inventaire des rituels :**

| Rituel | Prévu | Tenu en version complète | Tenu réduit | Reporté | Vide |
|--------|-------|-------------------------|-------------|---------|------|
| Point de qualimétrie | 4 | 2 | 2 | 0 | 0 |
| Go/No-Go | 2 | 1 | 1 | 0 | 0 |
| Revue hebdo | 4 | 1 | 2 | 1 | 0 |
| Confirmation | 6 | 3 | 2 | 1 | 0 |

**Le pattern est clair :** les rituels sont tenus, mais la version complète est minoritaire (7/16 = 44 %). La question n'est pas « tenons-nous ? » mais « tenons-nous avec le contenu ? ».

**Étape 2 (30 min) — le diagnostic de chaque rituel réduit :**

Le point de qualimétrie réduit (2 fois) : réduit à cause des urgences, pas à cause du désintérêt. Les signaux sont lus, les décisions prises. **Verdict : le rituel survit en réduction — c'est son rôle.**

La revue hebdo réduite (2 fois) : réduite à 5 minutes sans le tour des nouveaux. **Verdict : les nouveaux n'ont pas été entendus — c'est une perte réelle à corriger.**

La confirmation réduite (2 fois) : réduite à « critère atteint, statut confirmé » sans l'analyse de l'usage réel. **Verdict : la confirmation devient partielle — le taux de statuts explicites baisse (68 % au lieu de 85 %).**

Le report de revue hebdo (1 fois) : reporté pour l'incident de production, repris le lendemain avec le gabarit réduit. **Verdict : le report a été écrit et repris — c'est le fonctionnement normal.**

**Étape 3 (45 min) — les remontées au sponsor :**

Trois blocages structurels sont identifiés et remontés avec preuves :
1. **Le temps de revue de spécification n'est pas dans la capacité planifiée** — les revues sont faites en marge, donc réduites ou sautées. **Preuve :** les 6 spécifications du mois ont toutes eu une revue < 10 min. **Demande :** ajouter 2 h/semaine dans la planification.
2. **L'environnement de test des migrations est partagé avec l'équipe voisine** — les tests de migration sont retardés de 2-3 jours par contention. **Preuve :** 3 blocages documentés. **Demande :** un environnement dédié ou un calendrier de partage.
3. **Le chargé de livraison n'a pas de capacité reconnue** — il anime les rituels sur son temps personnel. **Preuve :** 4 h/semaine non planifiées. **Demande :** reconnaissance officielle dans la charge.

**Réponse du sponsor (obtenue dans les 48 h) :**
1. **Accordé** : 2 h/semaine ajoutées à la planification dès le prochain sprint.
2. **Accordé** : environnement dédié commandé, disponibilité sous 3 semaines.
3. **Refusé** : le rôle est déjà reconnu dans la fiche de poste — le praticien doit négocier avec le manager direct. (La négociation a eu lieu la semaine suivante et a abouti à 2 h/semaine reconnues.)

### Vendredi — le plan d'allégement sans abandon

**Le plan est forgé sur le diagnostic :**
- Le point de qualimétrie reste hebdomadaire (jamais reporté).
- La revue hebdo reste hebdomadaire mais gagne 5 minutes dédiées au tour des nouveaux.
- La confirmation reste systématique mais le format « critère atteint + usage réel » est un gabarit (plus rapide que l'analyse libre).
- Le chargé de livraison tourne par binôme pour éviter l'épuisement.

**Livrable de la semaine :** le diagnostic documenté, les 3 remontées avec réponses, le plan d'allégement écrit. **Ce qui a tenu :** le diagnostic a identifié les causes (capacité non planifiée, environnement partagé) — pas les symptômes (rituels réduits). Les remontées ont produit 2 accordés sur 3, et le 3e a trouvé son chemin par la négociation directe.

---

## Gabarit C : Semaine 6 complète (le passage de relais) — version remplie

### Mardi — le passage de relais (2h, coach silencieux)

**Le chargé de livraison (M.T.) anime la séance Go/No-Go du jour, sans que le coach n'intervienne.**

**Ce qui s'est passé (chronologique) :**
1. 10h00 : M.T. ouvre la séance, présente les 12 critères.
2. 10h05 : les preuves automatisées sont affichées (pipeline #4834 : 418/412 bloquants passés, 2 informatifs rouges).
3. 10h10 : le critère informatif « divergence doc/modèle » est à 3 (seuil : 2). M.T. note : « signal au-dessus du seuil, informatif — pas bloquant pour cette livraison, chantier de correction ouvert #2005, levée prévue le 15/03 ».
4. 10h15 : le critère bloquant « tests bloquants au commit » est à 412/412. **Go.**
5. 10h20 : le critère bloquant « réserves bloquantes » : 0 réserves. **Go.**
6. 10h25 : décision : **Go pour la livraison de jeudi**. Conditions : le chantier #2005 de divergence est noté dans le compte rendu avec sa levée.
7. 10h30 : fin de séance. Le coach n'a pas ouvert la bouche. Le compte rendu est publié à 10h35.

**Le débrief (15 min, après séance) :**
Le coach partage ses notes : « ce qui a bien fonctionné — tu as nommé le signal informatif sans le transformer en bloquant, c'est exactement la distinction forgée en semaine 4. Ce qui reste fragile — tu n'as pas vérifié la marge du temps de réponse API (elle est passée de 52 % à 41 % cette semaine) ; le prochain Go/No-Go pourrait la noter. »

**Le chargé de livraison note l'amélioration dans son carnet.**

### Jeudi — la démonstration aux voisins (1h30)

**Présents :** l'équipe voisine (4 personnes), l'équipe pilote (9), le coach (silencieux).

**Contenu de la démonstration (artefacts réels, pas de slides) :**
1. Le tableau des SLA forgé sur données (les 23 demandes et leur distribution) — 10 min
2. La grille Go/No-Go avec la distinction bloquant/informatif, illustrée par la séance de mardi — 20 min
3. La lettre de veille de la semaine 3 (le rapport de non-alerte) — 10 min
4. Le gabarit d'animation des rituels (le protocole de 15 min de préparation) — 15 min
5. Questions-réponses — 35 min

**Les questions de l'équipe voisine (et les réponses réelles de l'équipe pilote) :**
- « Et si vous n'avez pas les données pour forger les seuils ? » → « Vous les collectez d'abord. Le forgeage sur opinion produit des seuils décoratifs. »
- « Combien de temps par semaine ? » → « 2 h de rituels + 1 h de lettre de veille + 1 h de revue des SLA. Soit 4 h, planifiées. »
- « Et si le chargé de livraison part ? » → « Le gabarit d'animation permet à n'importe qui d'animer en 15 minutes de préparation. La rotation tient parce qu'elle ne coûte presque rien. »
- « Vous avez dit que la confirmation devient partielle au point mort. Comment vous en êtes sortis ? » → « Un gabarit de confirmation (critère + usage) est plus rapide que l'analyse libre — et il maintient le taux de statuts explicites au-dessus de 80 %. »

**Livrable de la semaine :** la démonstration réalisée, 4 artefacts partagés, les questions notées pour la suite (l'équipe voisine démarre son propre forgeage le trimestre suivant).

### Vendredi — autonomie confirmée

**Le test final de la semaine 6 : le praticien ne vient pas.** La lettre de veille est envoyée (par S.R., le chargé de veille, sans intervention du praticien). Le point de qualimétrie est tenu (par L.M., rotation). Le Go/No-Go est préparé (par M.T.). La revue hebdo est tenue (par L.N.).

**Aucun de ces quatre rituels n'a eu besoin du praticien.** C'est la confirmation de l'autonomie — et elle est documentée dans le registre.

---

## Gabarit D : Semaine 8 complète (le bilan de fin) — version remplie

### Mardi — l'audit de maturité niveau 3 (3h, 9h-12h)

**Les 8 éléments du niveau 3, audités avec preuves :**

| # | Élément | Niveau (1-3) | Preuve | Faible/Fort |
|---|---------|-------------|--------|-------------|
| 1 | Planification des livraisons N3 (SLA par classe) | 3 | Tableau des SLA forgé sur données, 23 demandes, 78 % concordance | Fort |
| 2 | Rituels d'implémentation N3 (forgeage, cadence) | 3 | 4 rituels forgés, tenu 6 semaines sans coach, rotation outillée | Fort |
| 3 | Qualimétrie N3 (tableau, seuils forgés) | 2 | Tableau en place, seuils forgés, mais pas encore de tendance documentée sur 3 mois | Moyen |
| 4 | Couverture par types de test N3 (matrice approfondie) | 2 | Matrice remplie sur 3 fonctionnalités, mutation non couverte | Moyen |
| 5 | Usage de l'IA N3 (règles d'usage, registre) | 2 | Règles signées, registre actif, 1er usage encadré réussi | Moyen |
| 6 | Documentation vivante N3 | 3 | Documentation citée par le support, mise à jour automatique testée | Fort |
| 7 | Centre d'excellence N3 (enraciné, catalyseurs) | 2 | 3 catalyseurs nommés, mais le plan de maintenance n'a pas encore été testé | Moyen |
| 8 | Prévention et veille N3 (lettre, seuils, dérogations) | 3 | Lettre bimensuelle envoyée à toutes les échéances, rapport de non-alerte testé, 1 dérogation levée à date | Fort |

**Les 2 faiblesses majeures identifiées (sans filtre) :**
1. **La qualimétrie N3 n'a pas de tendance documentée sur 3 mois** — le tableau est en place mais jeune. Action : documenter la tendance sur le prochain trimestre (avec les 3 premières lettres de veille comme référence).
2. **Le plan de maintenance du centre d'excellence n'a pas été testé** — les catalyseurs sont nommés mais n'ont pas encore maintenu l'artefact sans le praticien. Action : confier la maintenance de 3 artefacts aux catalyseurs au trimestre suivant, avec bilan.

**Les 2 forces identifiées :**
1. **La planification et les rituels forgés** — le forgeage sur données et la rotation outillée sont les points les plus solides.
2. **La veille et les dérogations** — la lettre de non-alerte et la levée à date sont des pratiques exemplaires.

### Mercredi — le contrat qualité v3.0 (2h, 9h-11h)

**Relire le v2.0 (15 min) :** qu'est-ce qui tient ? Tout le socle N2 tient. Qu'est-ce qui évolue ? Les quatre engagements N3 ajoutés (voir gabarit ci-dessous).

**Le gabarit v3.0 rempli :**

**Engagements de l'équipe (les 4 nouveaux N3 ajoutés aux 7 du N2) :**
1. La planification est cadencée avec SLA par classe forgé sur données — re-classification notée, taux surveillé (seuil : 15 %).
2. Les rituels sont forgés à cadence fixe — report écrit, réduction documentée.
3. Le Go/No-Go distingue bloquants (5 max) et informatifs — les réserves ont une levée datée.
4. La veille est systématique — lettre bimensuelle, rapport de non-alerte inclus, escalade en 3 jours.

**Engagements de l'organisation :**
5. La capacité de planification (2 h/sem) est reconnue dans la charge.
6. La capacité du chargé de livraison (2 h/sem) est reconnue (négociation manager directe).
7. L'environnement de test des migrations est dédié (disponibilité sous 3 semaines).
8. Le comité valide les seuils forgés sur données (jamais sur opinion).

**Règle des dérogations :** s'écarter du contrat si nécessaire, mais écrire la dérogation : qui décide, pourquoi, jusqu'à quand, ce qu'on apprend.

**Révision :** le contrat est relu [trimestriellement].

**Signatures :** équipe ____ sponsor ____ décideur de livraison ____

### Jeudi — le centre d'excellence enraciné (2h)

**Revue du centre (20 min) :** les artefacts actuels (17, dont 4 modèles, 3 gabarits d'animation, 3 gabarits d'arbitrage, 2 lettres de veille, 5 fiches-outils).

**Les catalyseurs (20 min) :** trois catalyseurs nommés, chacun responsable d'une famille :
- **S.R.** : les lettres de veille et le registre des SLA
- **L.M.** : les gabarits d'animation et le protocole des rituels
- **L.N.** : les modèles et leur confrontation

**Les leviers de pérennité (20 min) :** ce qui fait durer : (1) les gabarits d'animation (rotation possible), (2) la lettre bimensuelle (rythme visible), (3) le contrat v3.0 signé (engagement). Ce qui fait mourir : le départ des 3 catalyseurs sans relève (plan de transmission de chacun : 1 binôme + 1 trimestre).

**Plan de maintenance après le coach (40 min) :** les 3 catalyseurs maintiennent les artefacts, la lettre de veille est envoyée par le chargé de veille en rotation, l'audit de cadence est trimestriel avec un praticien différent chaque fois (rotation).

### Vendredi — rapport + célébration (2h, 9h-11h)

**Le rapport de maturité N3 (3 pages, présenté à la direction) :**
- Où nous étions : niveau 2 avec des artefacts vivants mais dépendants du coach.
- Ce que nous avons construit : SLA forgé sur données, 4 rituels forgés à cadence fixe, veille bimensuelle avec rapport de non-alerte, Go/No-Go N3 avec dérogation écrite, centre d'excellence avec 3 catalyseurs.
- Les chiffres : 78 % de concordance de classement, 44 % → 85 % de rituels tenus en version complète (sem 1 → sem 5), 100 % de taux de levée des réserves, 0 % de report non écrit.
- Ce qui reste fragile : qualimétrie jeune, plan de maintenance non testé.
- Recommandation : pérenniser le niveau 3 avec 2 corrections (tendance qualimétrie + test de maintenance), viser le niveau 4 au trimestre +2.

**La célébration :** l'équipe partage ce qu'elle fera différemment (chacun 1 phrase), et une chose qu'elle retient de l'équipe. Le coach rend le mandat. Le sponsor confirme la suite.

**Livrable de la semaine :** audit de maturité avec preuves, contrat v3.0 signé, centre d'excellence avec catalyseurs nommés et plan de transmission, rapport présenté, célébration tenue. **Le niveau 3 est ancré.**
