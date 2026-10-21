
---

# Partie 5 : Cas réels, gabarits remplis et variantes contextuelles (niveau 3)

Cette partie complète les huit semaines du niveau 3 avec les gabarits remplis par une équipe réelle, les situations vécues derrière les capsules, et l'adaptation du parcours aux contextes non standards.

## 1. Les gabarits remplis d'exemples réels

### 1.1 La grille de Go/No-Go N3 — exemple rempli et annoté

> La grille du niveau 3 appliquée lors d'une vraie décision. Comparez la colonne « preuve » avec votre niveau de détail : c'est le niveau attendu.

| Critère | Preuve requise | Preuve fournie | Seuil | Résultat | Verdict |
|---|---|---|---|---|---|
| Couverture unitaire | Rapport auto du pipeline | 82,4 % (rapport lié, généré à 14h02) | ≥ 80 % | ✅ | Passé |
| Tests d'intégration | Rapport d'exécution | 214/216 — 2 échecs analysés : timeouts d'environnement, non product | 100 % des blocants | ✅ avec réserve | Passé avec note |
| Tests E2E | Rapport E2E nocturne | Exécutés à J-1, 38/38 | 100 % | ✅ | Passé |
| Documentation | Diff auto doc/modèle | 0 divergence détectée | 0 divergence | ✅ | Passé |
| IA utilisée | Registre de trajectoire | 3 usages, tous validés humain | Règles respectées | ✅ | Passé |
| Performance | Rapport de charge hebdo | 2 endpoints sous la cible (-12 %) | Seuils SLA | ⚠️ | Réserve |

**Décision : Go avec 2 réserves.** Réserve 1 : les 2 échecs d'intégration sont environnementaux, investigation ouverte (ticket ENV-88). Réserve 2 : la performance dégradée de 2 endpoints est acceptée pour cette version, plan d'optimisation daté (2 semaines), réévaluation au prochain Go.

**Ce qui fait la qualité de cet exemple :** chaque preuve est datée et localisée (on peut la retrouver). Les réserves ont une condition de levée. Sans condition de levée, une réserve est une manière polie d'oublier.

### 1.2 Tableau de bord N3 — exemple rempli

> Le tableau de bord réel de l'équipe, en fin de niveau 3. Six signaux, chacun avec décision associée.

| Signal | Valeur | Tendance | Seuil rouge | Décision si rouge | Décideur |
|---|---|---|---|---|---|
| Couverture unitaire | 82 % | ↑ | < 75 % | Bloquer le Go, sprint de tests | Lead technique |
| Divergences doc/modèle | 0 | = | > 2 | Sprint de synchronisation doc | QA |
| Tests flaky (échecs intermittents) | 3 | ↑ | > 5 | Quaran J + traitement forcé | Lead technique |
| Temps de cycle (commit→prod) | 2,1 j | = | > 3 j | Analyse du goulot en rétro | Équipe |
| Divergences IA/validations | 8 % | ↓ | > 20 % | Rappel des règles + revue des usages | Équipe |
| Dérogations actives | 1 | ↓ | > 3 | Revue de toutes les dérogations en rétro | Équipe + sponsor |

**Le registre des décisions (extrait réel) :**

| Date | Signal | Valeur | Décision | Responsable | Levée |
|---|---|---|---|---|---|
| 12/07 | Tests flaky | 6 | Quaran des 3 nouveaux + analyse (ENV-88) | L.T. | Le 19/07 |
| 05/07 | Dérogations | 4 | Revue complète en rétro : 3 levées, 1 maintenue justifiée | Équipe | Fait |

**Ce qui fait la qualité du registre :** la colonne « levée ». Une décision sans date de levée est un vœu. Le registre se lit en rétro : les décisions passées sont vérifiées.

### 1.3 Bilan d'autonomie — exemple rempli

> Le bilan de la semaine 6, rempli. Il liste ce qui tient sans le coach et ce qui ne tient pas — avec le pourquoi et le plan.

| Rituel | Tient sans coach ? | Preuve | Ce qui manque sinon |
|---|---|---|---|
| Go/No-Go | ✅ Oui | 4 Go animés par le chargé de livraison, décisions enregistrées | — |
| Point de qualimétrie | ✅ Oui | 6 points consécutifs, y compris 2 sans coach | — |
| Revue de spécification | ⚠️ Partiel | Les revues ont lieu, mais 30 % sans commentaire | Rappel : 3 commentaires minimum, sinon la revue est nulle |
| Mise à jour des modèles | ❌ Non | Dernière mise à jour : 9 jours (dépasse la règle des 5 jours) | Règle : une divergence = correction dans la semaine. Le responsable des modèles est surchargé — proposer un binôme |
| Registre des décisions | ✅ Oui | 100 % des décisions notées avec levée | — |

**Ce qui fait la qualité de ce bilan :** le ❌ n'est pas caché. La ligne « mise à jour des modèles » a généré une décision de rétro : binôme sur la maintenance des modèles. Un bilan sans ❌ est un bilan incomplet — l'autonomie n'est jamais uniforme.

## 2. Cas vécus étendus : le niveau 3

### Cas de la semaine 1 : la grille que le sponsor a voulu simplifier

**Situation.** La grille de Go/No-Go N3 avait 12 critères. Le sponsor, en revue, a demandé : « Douze critères, c'est trop. Gardez les cinq importants. »

**Le dilemme.** Le sponsor a raison sur le principe (une grille de 40 lignes n'est pas lue) et tort sur le nombre (les 12 critères étaient tous liés à un incident réel passé).

**La résolution.** L'équipe a proposé une structure à deux niveaux : 5 critères bloquants (ils doivent être verts pour le Go), 7 critères informatifs (ils s'affichent, alimentent les réserves, mais ne bloquent pas seuls). Le sponsor a accepté : « Ça, je peux le lire. » La distinction bloquant/informatif est devenue la structure standard de la grille de l'équipe.

**Ce que ce cas enseigne.**
- Le sponsor qui simplifie une grille n'attaque pas la rigueur : il attaque la lisibilité. La réponse est une structure plus lisible, pas une grille plus faible.
- La distinction bloquant/informatif est la bonne réponse au dilemme « tout vérifier » vs « aller vite ». Elle préserve les 12 préoccupations tout en rendant la décision lisible.
- Un critère bloquant doit pouvoir être tracé à un incident réel. Si vous ne pouvez pas raconter l'incident derrière un critère bloquant, il est probablement informatif.

### Cas de la semaine 2 : le chargé de livraison qui a trop bien fait

**Situation.** Le chargé de livraison de la semaine 2 a été excellent : rituels animés avec brio, décisions nettes, équipe satisfaite. Le coach a noté un problème : le chargé décidait seul des points que l'équipe aurait dû trancher. Personne ne s'en plaignait — c'était plus efficace.

**Le risque.** Le niveau 3 n'est pas « une personne compétente décide vite ». C'est « l'équipe décide avec des preuves ». Un chargé de livraison trop centralisateur crée une autonomie de façade : retirez-le, et le rituel s'effondre — exactement comme si le coach était resté.

**Ce qui a fonctionné.** Le coach a attendu la semaine 6 (autonomie) et a fait le test de la manière la plus neutre possible : une semaine complète avec un autre chargé de livraison, désigné par rotation. Le résultat a été révélateur : trois rituels ont tenu, deux ont dérapé exactement là où le premier chargé avait pris l'habitude de décider seul. La rotation a transformé la dépendance en problème visible — et donc solvable. La solution : une règle écrite « les décisions de Go/No-Go se prennent en rituel, jamais en couloir », signée par l'équipe.

**Ce que ce cas enseigne.**
- Un rituel qui tient grâce à une personne n'est pas un rituel autonome : c'est une personne avec un rituel pour décor. Le test de la rotation est le seul qui le révèle.
- La compétence excessive d'un membre peut masquer une faiblesse collective. C'est le paradoxe du héros : plus il est bon, plus l'équipe s'appuie, moins elle apprend.
- Le moment de corriger n'est pas quand le héros décide seul (l'équipe est satisfaite, la correction sonne comme une critique) mais lors d'un événement neutre (la rotation) qui rend la dépendance factuelle.

### Cas de la semaine 3 : le signal rouge qui a divisé l'équipe

**Situation.** Le signal « divergences doc/modèle » est passé à 4 (seuil : 2). Le point de qualimétrie a voté la décision prévue : sprint de synchronisation. Deux développeurs ont protesté : « On a un deadline client vendredi. La doc attendra. »

**Le dilemme.** La décision prévue par le tableau exige des ressources que le contexte de la semaine n'a pas. Suivre le tableau mécaniquement = rater le deadline. Ignorer le tableau = casser la règle qui fait la valeur du système.

**La résolution.** L'équipe a fait ce que le niveau 3 autorise : modifier la décision, mais documenter la modification. Le sprint de synchronisation a été remplacé par une synchronisation minimale (les 2 divergences les plus risquées corrigées, les 2 autres mises en file), avec date de rattrapage. La décision modifiée a été notée au registre avec sa raison et sa levée. Le deadline client a été tenu, la dette documentaire a été rattrapée la semaine suivante.

**Ce que ce cas enseigne.**
- Le tableau de bord n'est pas un tyran : c'est un dispositif de décision explicite. La décision peut être adaptée au contexte — à condition que l'adaptation soit documentée avec la même rigueur que la décision standard.
- La différence entre le niveau 2 et le niveau 3 n'est pas la rigidité : c'est la visibilité. Le niveau 2 improviserait en silence ; le niveau 3 adapte par écrit.
- Une règle sans mécanisme d'exception documentée est une règle qui sera contournée en silence dès la première pression. Le mécanisme d'exception (décision modifiée notée au registre) est ce qui sauve la règle.

### Cas de la semaine 5 : le diagnostic qui a déplacé le problème

**Situation.** Le diagnostic du point mort a identifié comme premier blocage : « les rituels prennent trop de temps ». La solution évidente était de les alléger. Le coach a proposé de creuser : pourquoi prennent-ils trop de temps ?

**La découverte.** Le point de qualimétrie durait 50 minutes au lieu de 15. En creusant : chaque signal rouge déclenchait un débat sur la décision — parce que le décideur n'était pas clair. Le temps n'était pas dans le rituel : il était dans l'indécision. La vraie correction n'était pas d'alléger le rituel mais de clarifier les décideurs de chaque signal (la colonne qui manquait au tableau).

**Le résultat.** Le tableau a gagné une colonne « décideur ». Le point de qualimétrie est passé à 18 minutes. Le rituel n'a pas été allégé : il a été précisé.

**Ce que ce cas enseigne.**
- Le premier diagnostic est rarement le bon. « Trop de temps » cache presque toujours une indécision, un flou de responsabilité, ou un manque de préparation — jamais un rituel intrinsèquement trop long.
- La question « pourquoi trois fois de suite » est l'outil du diagnostic : à chaque réponse, demandez pourquoi. La troisième réponse est généralement la vraie.
- Un rituel long n'est pas un rituel riche : c'est souvent un rituel indécis. La précision (qui décide quoi) vaut mieux que la brièveté imposée.

### Cas de la semaine 6 : le No-Go contre le sponsor

**Situation.** La décision de Go pour la version 3.2 était attendue par le sponsor : le client principal avait une date. La grille a montré 2 critères bloquants au rouge (couverture sous seuil, divergence doc/modèle non résolue). Le chargé de livraison a annoncé le No-Go. Le sponsor a contesté en séance : « Vous comprenez que le client attend ? »

**La réponse.** Le chargé de livraison n'a pas débattu : il a lu la grille, énoncé les critères rouges, proposé le chemin de rattrapage (2 jours de travail ciblé, Go Wednesday suivant). Le sponsor a insisté. Le chargé de livraison a ajouté une phrase devenue célèbre dans l'équipe : « Je comprends la pression client. La grille ne dit pas non pour toujours : elle dit pas aujourd'hui, et voici pourquoi, et voici quand. »

**Le dénouement.** Le sponsor a accepté le report. Le Go a eu lieu 2 jours plus tard, complet. Le client a reçu la version 2 jours après la date initiale — avec zéro incident. Le sponsor a cité cet épisode dans une réunion de direction : « L'équipe m'a dit non, elle avait raison. »

**Ce que ce cas enseigne.**
- Le No-Go face au sponsor est le test ultime de l'autonomie. Il ne se gagne pas par la confrontation : il se gagne par la précision (les critères rouges, le chemin de rattrapage, la date du Go).
- La formule « pas aujourd'hui, voici pourquoi, voici quand » est le format qui rend un No-Go acceptable : il transforme un refus en plan.
- L'équipe qui n'a jamais dit non à son sponsor n'a pas encore prouvé son autonomie — elle a peut-être juste jamais eu le cas. La préparation mentale au No-Go face au sponsor fait partie du niveau 3.

## 3. Variantes contextuelles du niveau 3

### V1 : petite équipe (2-4 personnes)

- La grille bloquant/informatif devient une liste unique de vérification : dans une petite équipe, la séparation formelle coûte plus qu'elle ne rapporte.
- La rotation du chargé de livraison est hebdomadaire dès la semaine 2 : avec 3 personnes, la dépendance à un héros se forme en une semaine.
- Le point de qualimétrie peut être l'occasion de tout le reste (rétro, planification) : un seul rituel enrichi vaut mieux que trois rituels pauvres.
- Le bilan d'autonomie est bi-directionnel : chacun évalue sa propre autonomie sur chaque rituel, pas seulement l'équipe.

### V2 : équipe distribuée

- Le Go/No-Go reste synchrone (décision = conversation), mais le rassemblement des preuves est asynchrone : chaque preuve est postée dans un canal dédié 24h avant, avec un thread de questions.
- Le point de qualimétrie est asynchrone par écrit la plupart des semaines, synchrone une fois par mois. La règle de la décision notée au registre est encore plus critique à distance : c'est ce qui remplace le « on s'est dit ».
- La rotation du chargé de livraison est l'outil anti-dépendance le plus important à distance : à distance, les habitudes de centralisation se forment plus vite (qui décide = qui répond le plus vite, et le fuseau décide).
- Le bilan d'autonomie gagne une colonne : « tient sans le coach ET sans coïncidence de fuseaux ».

### V3 : legacy lourd

- La couverture unitaire (80 %) est souvent inatteignable au début sur un legacy : la grille N3 doit définir des seuils progressifs (ex. : 40 % la première version, +10 % par trimestre). Un seuil inatteignable est un seuil décoratif.
- Les tests flaky sont fréquents sur les legacy (environnement instable, données partagées) : le budget flaky doit être plus large, et la règle de quaran plus agressive.
- Le No-Go pour divergence doc/modèle est le plus précieux sur un legacy : c'est souvent le seul mécanisme qui révèle que la documentation ne correspond plus au système. Attendez-vous à beaucoup de divergences au début — c'est le signe que le système fonctionne.
- La performance est le signal le plus difficile à stabiliser sur un legacy : considérez-la comme informatif au début, bloquant après 2 trimestres de stabilisation.

### V4 : organisation réglementée

- La grille de Go/No-Go devient un document réglementaire : ses versions sont archivées, ses critères tracés aux exigences. La traçabilité réglementaire et la grille sont la même chose.
- Les dérogations écrites sont vos meilleures amies : dans un contexte réglementé, la dérogation est souvent le seul mécanisme légitime pour documenter un écart acceptable. Formalisez le format de dérogation comme document réglementaire.
- Le registre des décisions satisfait souvent une exigence de traçabilité des décisions : montrez-le à votre auditeur, il couvrira deux exigences avec un seul outil.
- Le bilan d'autonomie doit prouver que les rituels réglementaires (revues formelles) sont tenus par l'équipe, pas par le coach : c'est exactement le test de l'autonomie réglementaire.

### V5 : le sponsor sceptique

- Le niveau 3 a un avantage unique pour les sceptiques : la grille et le registre sont des preuves objectives. Le « fait de la semaine » du niveau 3 : « cette semaine, le point de qualimétrie a déclenché 2 décisions notées, dont 1 a évité une régression en production ».
- Le sponsor sceptique teste souvent l'équipe en demandant une exception. C'est le moment du No-Go préparé : la grille tranchera à votre place, avec les critères et les réserves. Préparez ce moment mentalement — il arrive presque toujours.
- Le moment de bascule du sponsor sceptique au niveau 3 : la première fois que le registre des décisions prouve qu'une décision a évité un problème. Les décisions documentées sont l'argument ultime : elles montrent que le système pense, pas que les gens obéissent.

### V6 : reprise après échec du niveau 2

- Si le niveau 2 s'est arrêté, la grille N3 doit être plus simple au départ : la surcharge est la cause de mort fréquente des reprises. Commencez avec 5 critères, ajoutez les autres après 2 Go réussis.
- Le registre des décisions est le premier rituel à réinstaller : c'est celui qui prouve le plus vite la valeur (les décisions passées deviennent des preuves).
- Le No-Go de la reprise : le premier No-Go d'une reprise est le plus important de son histoire. Préparez-le — il arrivera, et il sera le moment où l'équipe prouve que cette fois est différente.

---

## Comment utiliser cette partie

- **Au démarrage** : lisez la variante de votre contexte.
- **Pendant le parcours** : quand une semaine bloque, cherchez le cas vécu correspondant — particulièrement le cas du chargé de livraison trop bon (semaine 2) et du No-Go contre le sponsor (semaine 6), qui sont les deux moments de vérité du niveau 3.
- **À la semaine 8** : comparez votre grille et votre registre avec les exemples. La précision des preuves est la cible, pas le nombre de lignes.
