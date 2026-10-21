---

# Partie 4 : Formation, exercices et évaluation (niveau 2)

Les huit semaines construisent le niveau 2. Cette partie le rend transmissible. Un niveau qui n'est pas transmissible n'est pas un niveau : c'est un moment. La formation, les exercices et l'évaluation transforment la pratique de quelques personnes en pratique d'une organisation.

**Le principe :** on ne forme pas en expliquant le modèle. On forme en faisant modéliser, en faisant automatiser, en faisant échouer, puis en faisant nommer ce qui a échoué. Chaque exercice de cette partie suit la même grammaire : une consigne claire, une contrainte qui force le discernement, une évaluation par les pairs, et un artefact publié.

## Le plan de formation de niveau 2

La formation de niveau 2 ne se déroule pas dans une salle à part. Elle est intégrée aux semaines de travail : chaque atelier du livre est déjà une séquence de formation. Mais pour les nouveaux arrivants et pour les équipes voisines, il faut un parcours explicite. Voici le plan recommandé.

**Module F1 — Lire un modèle (2 heures).** Objectif : lire un diagramme BPMN et repérer les trois ambiguïtés qui y sont volontairement cachées. Format : atelier dirigé. Évaluation : chaque participant trouve au moins deux ambiguïtés et propose une correction. Matériel : trois modèles BPMN préparés par le gardien du centre d'excellence, chacun contenant des défauts réels tirés des modèles de l'équipe.

**Module F2 — Écrire un modèle (4 heures).** Objectif : modéliser un processus réel de l'équipe, seul puis en binôme, et confronter les deux versions. Format : atelier pratique par binômes. Évaluation : les deux versions du même processus sont comparées en plénière ; les divergences deviennent la liste des ambiguïtés à lever. Matériel : un outil de modélisation (même gratuit), une charte de nommage.

**Module F3 — Du modèle aux tests (4 heures).** Objectif : dériver des cas de test d'un modèle MBT et comprendre ce qu'un couvre et ce qu'il rate. Format : atelier pratique. Évaluation : la couverture du modèle produite par chaque participant est comparée à la couverture de référence ; les écarts sont discutés. Matériel : un modèle MBT stable, la matrice de couverture de l'équipe.

**Module F4 — La documentation comme spécification vivante (2 heures).** Objectif : relier une page de documentation produit à un modèle et à des tests, et démontrer qu'une modification se propage. Format : démonstration + pratique. Évaluation : le participant modifie un modèle et met à jour la documentation sans rupture. Matériel : la chaîne documentaire de niveau 2.

**Module F5 — L'IA sur socle solide (2 heures).** Objectif : utiliser l'IA générative comme assistant de spécification et de documentation à partir d'un modèle existant, et reconnaître ses productions plausibles mais fausses. Format : atelier d'exercices. Évaluation : le participant fait produire par l'IA une spécification à partir d'un modèle, puis détecte au moins deux erreurs dans la production de l'IA. Matériel : un modèle stable, un accès IA, la liste des pièges connus.

**Règle de l'échelle :** un nouveau module ne s'ajoute que si un besoin réel a été documenté par un atelier de terrain. La formation suit la pratique, elle ne la précède pas. Un catalogue de formations sans pratique derrière est un cimetière de PDF.

## Exercices d'entraînement de niveau 2

Ces exercices s'utilisent en formation interne, en atelier d'équipe, ou en auto-apprentissage. Chacun est conçu pour être fait en 20 à 45 minutes, avec un artefact comme preuve de passage.

### Exercice E1 : Le modèle à l'épreuve des trois lecteurs

**Consigne :** donnez le même modèle BPMN à trois personnes de rôles différents (développeur, testeur, product owner). Chacun écrit ce qu'il comprend du processus en cinq phrases. Confrontez les trois lectures.

**Ce que l'exercice révèle :** là où les trois lectures divergent, le modèle est ambigu. C'est exactement l'ambiguïté qui, en production, deviendra un bug, un retard ou une guerre de versions.

**Évaluation :** le modèle est jugé ambigu si plus d'une lecture diverge sur un même point. Chaque divergence nommée devient un item de correction. L'exercice est réussi quand les divergences sont écrites, pas quand elles sont discutées.

### Exercice E2 : Le test impossible

**Consigne :** prenez un modèle MBT et cherchez le chemin que personne ne peut tester : la donnée manquante, l'environnement inexistant, la dépendance externe. Nommez-le, et décidez : construire le moyen de le tester, ou l'assumer comme risque écrit.

**Ce que l'exercice révèle :** les zones mortes du modèle — celles qu'on ne teste pas parce qu'on ne peut pas, pas parce qu'on ne doit pas. Ce sont les mêmes zones où vivent les bugs de production.

**Évaluation :** la zone morte est nommée par écrit, avec sa décision (moyen de test construit / risque assumé et daté). Un risque assumé sans date de réévaluation n'est pas assumé : il est oublié.

### Exercice E3 : La chaîne de propagation

**Consigne :** modifiez une seule passerelle de décision dans un modèle BPMN stable. Puis traversez la chaîne : les tests dérivés changent-ils ? La documentation se met-elle à jour ? La matrice de couverture bouge-t-elle ? Chronométrez chaque étape.

**Ce que l'exercice révèle :** la santé réelle de la chaîne modèle → test → documentation. Une chaîne qui met deux jours à propager une modification est une chaîne qui ne propagera rien en pratique.

**Évaluation :** le temps de propagation complet est mesuré et écrit. Objectif de niveau 2 : moins d'une journée. S'il dépasse, l'exercice produit la liste des points de friction à corriger.

### Exercice E4 : Le test fantôme

**Consigne :** prenez trois tests automatisés qui passent et cherchez ce qu'ils ne vérifient pas : la donnée qui n'existe pas, la branche non parcourue, l'assertion absente.

**Ce que l'exercice révèle :** le passage n'est pas la couverture. Un test qui passe peut vérifier très peu de choses. L'automatisation sans modèle de référence produit des tests fantômes : verts, mais vides.

**Évaluation :** pour chaque test fantôme, écrire ce qu'il vérifie réellement et ce qu'il devrait vérifier. La différence est le travail à faire.

### Exercice E5 : Le piégeage de l'IA

**Consigne :** demandez à l'IA de générer une spécification à partir d'un modèle BPMN, puis à l'IA de générer la même spécification sans modèle. Comparez les deux productions avec la spécification réelle de l'équipe.

**Ce que l'exercice révèle :** la différence entre l'IA sur socle solide (fidèle au modèle, relue facilement) et l'IA sans socle (plausible, fausse, coûteuse à corriger). C'est la démonstration la plus convaincante pour les sceptiques.

**Évaluation :** le participant identifie au moins trois divergences entre la production IA sans socle et la réalité. Les divergences sont classées : erreur de contenu, erreur de structure, erreur de vocabulaire.

### Exercice E6 : Le rituel à l'aveugle

**Consigne :** le chargé de livraison anime le rituel Go/No-Go de niveau 2 sans préparation particulière, en utilisant seulement les preuves publiées dans le centre d'excellence. Le coach observe en silence.

**Ce que l'exercice révèle :** si le rituel tient sans le coach, la preuve est publique. S'il ne tient pas, les preuves publiées sont insuffisantes — et le problème est structurel, pas personnel.

**Évaluation :** le rituel tient en 30 minutes, la décision est prise, et le compte rendu est rempli sans aide extérieure. Sinon : identifier quel critère de Go manquait de preuve.

## L'évaluation de la maturité de niveau 2

L'évaluation n'est pas un examen. C'est un miroir avec des chiffres. Elle répond à une seule question : le niveau 2 est-il installé, fragile, ou absent ? L'évaluation se fait par les faits, jamais par les impressions.

### La grille d'observation des rituels

Le coach (ou le gardien du centre d'excellence) observe un rituel réel et remplit cette grille, sans juger les personnes :

| Élément observé | Niveau 0 : absent | Niveau 1 : présent mais fragile | Niveau 2 : installé | Niveau 3 : transmis |
| --- | --- | --- | --- | --- |
| Le rituel commence à l'heure et finit dans le temps prévu | Jamais | Parfois | La plupart du temps | Toujours, y compris sans le coach |
| La décision est prise pendant le rituel (pas après, pas ailleurs) | Décision reportée | Décision prise hors rituel | Décision prise en rituel | Décision prise et tracée sans effort |
| Les preuves sont citées et visibles | Impression | Preuves citées de mémoire | Preuves affichées | Preuves affichées et mises à jour automatiquement |
| Le compte rendu est rempli pendant la séance | Jamais | Après coup | Pendant | Rempli par le système, relu par l'équipe |
| Les dérogations sont écrites | Orale | Écrite après coup | Écrite pendant | Écrite et reliée à un apprentissage |

**Règle d'usage :** une pratique est installée au niveau 2 seulement si elle atteint le niveau 2 sur trois observations successives. Une observation isolée ne dit rien : une bonne journée n'est pas une pratique.

### La grille d'auto-évaluation des sept éléments

Chaque membre de l'équipe pilote remplit cette grille individuellement, puis les réponses sont confrontées. Les écarts entre les auto-évaluations sont plus instructifs que les chiffres eux-mêmes : là où l'équipe se voit différemment, il y a un problème de réalité partagée.

| Élément de niveau 2 | Ma note (1-3) | Ma preuve | Ce qui me manque |
| --- | --- | --- | --- |
| Spécifications modélisées | | | |
| Outillage automatisation/documentation | | | |
| Planification des livraisons N2 | | | |
| Qualimétrie N2 | | | |
| Politiques et conventions | | | |
| Couverture par types de test | | | |
| Socle pour l'IA | | | |

**Règle d'usage :** une note sans preuve vaut zéro. La colonne « Ma preuve » doit pointer vers un artefact réel (modèle, test, page Wiki, convention signée). C'est l'anti-langue-de-bois de cette grille.

### Le test des quatre semaines

Le test final de niveau 2 est simple : après la fin des huit semaines, l'équipe continue-t-elle à tenir le niveau 2 sans le coach pendant quatre semaines ? Le test se fait à J+30 : audit de la chaîne modèle → test → documentation, point de qualimétrie observé, rituel Go/No-Go observé.

**Critères de réussite :**
- La chaîne de propagation fonctionne sans intervention du coach (exercice E3 refait par l'équipe seule).
- Le point de qualimétrie déclenche des décisions documentées.
- Le rituel Go/No-Go fonctionne avec les preuves publiées (exercice E6).
- Les politiques sont relues au moins une fois depuis la fin du niveau 2.

**Si le test échoue :** ce n'est pas un échec, c'est une information. La partie 5 de ce livre (l'ancrage et l'extension) traite exactement ce cas : quoi faire quand le niveau tient à peine, et comment décider de consolider avant d'étendre.

## Le carnet d'exercices du sponsor

Le sponsor n'est pas un spectateur du niveau 2. Il a des exercices à faire, et son échec à ces exercices coûte cher au niveau tout entier.

**Exercice S1 : La demande en trois phrases (20 minutes).** Le sponsor écrit, en trois phrases maximum, ce qu'il attend du niveau 2 en termes mesurables. S'il ne peut pas le faire en trois phrases, il ne sait pas ce qu'il demande — et l'équipe ne saura pas quand elle aura réussi.

**Exercice S2 : La preuve qu'il regardera (15 minutes).** Le sponsor nomme la preuve unique qui décidera pour lui que le niveau 2 a tenu (une métrique, un rituel observé, un incident évité). Cette preuve nommée devient le fil rouge de la qualimétrie N2.

**Exercice S3 : La demande de débloquement (30 minutes).** Le sponsor relit les demandes de débloquement de la semaine 5 et répond par écrit à chacune : accordé / refusé / reporté, avec la raison et la date. Une demande sans réponse écrite n'est pas une demande : c'est un vœu.

**Règle de facilitation :** ne laissez pas le sponsor reporter ces exercices « quand il aura le temps ». Ils se font pendant un rituel auquel il participe déjà. Un sponsor qui refuse 30 minutes d'exercice de niveau 2 refuse le niveau 2, et il vaut mieux le savoir tôt.
