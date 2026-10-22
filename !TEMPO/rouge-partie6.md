
---

# Partie 6 : Les cérémonies du niveau 1

Cette partie adapte les sept cérémonies de TOTALISATION — documentées et éprouvées chez Opal-RT — au niveau 1. Chaque cérémonie est un rituel formel, un rendez-vous de qualité avec un objectif, des participants, des entrées et des sorties définies. Au niveau 1, on en installe trois (les essentielles) ; les quatre autres sont présentées pour que l'équipe sache où elle va.

**La différence entre une réunion et une cérémonie.** Une réunion discute. Une cérémonie produit : elle a des entrées obligatoires, des sorties attendues, et un livrable daté. Si une cérémonie ne produit rien, elle s'est dégradée en réunion — et elle doit être corrigée ou supprimée.

## Cérémonie 1 : L'ÉLICITATION

**Objectif :** obtenir le besoin réel et ses contraintes avant toute décision.

**Quand :** à chaque nouvelle demande, avant la spécification.

**Participants :** le demandeur (ou son représentant), l'équipe, le facilitateur.

**Entrées :** la demande brute (email, ticket, conversation), le contexte du demandeur.

**Sorties :** le besoin formulé en langage commun, les contraintes explicites, les critères de succès du demandeur, les non-besoins (ce qu'il ne demande pas).

**Le déroulé du niveau 1 (30 à 45 minutes) :**

1. **Le demandeur raconte** (10 min, sans interruption) : ce qu'il veut, pourquoi, pour qui. Le facilitateur note sans reformuler — la reformulation vient après.
2. **Les questions ouvertes** (15 min) : l'équipe interroge. Les cinq questions standard : « Quel problème concret cela résout-il ? », « Comment saurez-vous que c'est réussi ? », « Qu'avez-vous déjà essayé ? », « Que se passe-t-il si on ne le fait pas ? », « Qui d'autre est concerné ? ».
3. **La reformulation** (10 min) : l'équipe reformule le besoin en ses propres mots et le demandeur valide ou corrige. C'est le moment où les malentendus meurent — ou survivent.
4. **La clôture** (5 min) : le besoin reformulé est écrit, daté, signé par le demandeur. Cette écriture est le livrable de la cérémonie.

**Les pièges du niveau 1 :**
- **La cérémonie qui devient un cahier des charges.** L'élicitation du niveau 1 recueille le besoin, elle ne le spécifie pas. La spécification est l'étape suivante. Si l'équipe se met à débattre de solutions, elle a dépassé son rôle.
- **Le demandeur absent.** Une élicitation sans le demandeur est une fabrication. Si le demandeur ne peut pas venir, la cérémonie est reportée — ou se fait par écrit avec validation ultérieure explicite.
- **Les besoins cachés.** Le demandeur dit souvent ce qu'il veut (la solution) et non ce dont il a besoin (le problème). La question « quel problème cela résout-il ? » est l'outil qui remonte du problème vers la solution.

**La capsule du vécu.** Chez Opal-RT, la première élicitation formelle a révélé un écart saisissant : le besoin exprimé (« un tableau de bord des tests ») et le besoin réel (« savoir si on peut livrer sans peur ») étaient deux choses différentes. Le tableau de bord demandé aurait montré des chiffres ; le besoin réel demandait une réponse à une question. L'équipe a spécifié la réponse, pas le tableau — et le tableau qui en a résulté était différent de ce que le demandeur avait décrit, et meilleur.

## Cérémonie 2 : LA DÉFINITION (la spécification)

**Objectif :** transformer le besoin élicité en spécification testable.

**Quand :** après l'élicitation, avant l'implémentation.

**Participants :** l'auteur de la spécification, un développeur, un testeur, le demandeur (disponible pour questions).

**Entrées :** le besoin reformulé et signé (cérémonie 1), les contraintes techniques connues.

**Sorties :** la spécification IF…THEN… complète, les critères de validation, les cas limites, la revue faite.

**Le déroulé du niveau 1 (60 à 90 minutes) :**

1. **L'écriture du squelette** (20 min) : contexte, besoin, comportement attendu. L'auteur écrit, les autres complètent oralement.
2. **Les règles de validation** (20 min) : pour chaque comportement attendu, comment saure-t-on qu'il est respecté ? Les règles s'écrivent en IF…THEN… : « SI le filtre est appliqué sur une colonne vide, ALORS toutes les lignes restent visibles. »
3. **Les cas limites** (20 min) : la chasse aux frontières — valeurs nulles, données vides, volume extrême, concurrence, ordre des opérations. Chaque cas limite devient une règle de validation.
4. **La revue à trois rôles** (20 min) : le développeur lit pour l'implémentabilité, le testeur lit pour la testabilité, le demandeur lit pour la fidélité au besoin. Chaque rôle signale : ce qui n'est pas clair, ce qui est faux, ce qui manque.

**Le piège du niveau 1 :** la spécification encyclopédique. Une spécification de deux pages qui prévient le malentendu est meilleure qu'un mémoire de vingt pages que personne ne lit. Le test : le développeur la lit-il avant de coder ?

**La capsule du vécu.** La première spécification complète de la mission Fait trois cas limites que personne n'avait identifiés — dont un qui avait déjà causé une reprise six mois plus tôt. Le développeur, sceptique au départ (« une demi-page suffit pour ça »), a reconnu : « OK, ce cas-là, je l'aurais raté. » C'est le moment exact où la spécification cesse d'être une exigence externe et devient un outil personnel.

## Cérémonie 3 : LA PLANIFICATION

**Objectif :** décider quoi, quand, par qui, avec quels risques assumés.

**Quand :** après la définition, au début de chaque itération.

**Participants :** l'équipe complète, le product owner, le facilitateur.

**Entrées :** les spécifications prêtes (DoR satisfait), la capacité de l'équipe, les priorités.

**Sorties :** le plan d'itération (les items sélectionnés avec leurs spécifications), les risques connus et assumés, les critères de fin.

**Le déroulé du niveau 1 (90 minutes) :**

1. **La revue de capacité** (10 min) : qui est disponible, quels absences, quelles interruptions prévisibles. On planifie avec la capacité réelle, pas avec la capacité espérée.
2. **La sélection des items** (30 min) : chaque item candidat est évalué — sa spécification est-elle prête ? Son estimateur est-il présent ? Ses dépendances sont-elles résolues ? Les items sans spécification prête ne rentrent pas : c'est la règle du DoR (Definition of Ready) en action.
3. **Le contrat d'itération** (30 min) : pour chaque item sélectionné, l'équipe écrit ce qu'elle s'engage à livrer (comportement, critères de validation, preuves). Ce contrat est le référentiel du Go/No-Go de fin d'itération.
4. **Les risques** (20 min) : chaque item porte ses risques connus (technique, dépendance, donnée). Chaque risque a un plan : mitigé, contourné, ou assumé par écrit.

**Le piège du niveau 1 :** planifier avec la capacité espérée. L'itération surchargée est le début de la spirale : les items glissent, la confiance baisse, la planification perd son sens. Mieux vaut une itération réaliste à 80 % qu'une itération héroïque à 120 %.

**La capsule du vécu.** La première planification formelle de la mission a duré deux fois le temps prévu — parce que la moitié des items candidats n'avaient pas de spécification prête. L'équipe a dû choisir entre les déclasser (et planifier maigre) ou les écrire à la volée (et planifier au flou). Elle a déclassé. L'itération a livré 100 % de ses engagements — la première fois de son histoire. La leçon du facilitateur : *une itération maigre et tenue vaut mieux qu'une itération grasse et glissante.*

## Cérémonie 4 : L'IMPLÉMENTATION (la revue de code)

**Objectif :** garantir que le code est conforme à la spécification, pas seulement qu'il fonctionne.

**Quand :** à chaque pull request, pendant l'implémentation.

**Participants :** l'auteur du code, un relecteur, le specificateur (en cas de doute).

**Entrées :** le code, la spécification correspondante, les critères de validation.

**Sorties :** le code approuvé avec preuve de conformité, ou les corrections demandées.

**Le déroulé du niveau 1 (30 minutes par revue) :**

1. **La lecture pour la conformité** (10 min) : le relecteur vérifie d'abord le code contre la spécification, comportement par comportement. Il note chaque écart — même ceux qui « marchent quand même ».
2. **La lecture pour la maintenabilité** (10 min) : lisibilité, nommage, structure, tests. Le relecteur signale ce qui posera problème dans six mois.
3. **La décision** (10 min) : approuvé / approuvé avec réserves notées / refusé avec corrections. La décision est écrite dans la revue.

**Le piège du niveau 1 :** la revue de style sans revue de conformité. Un code élégant qui ne fait pas ce que la spécification dit est un beau bug. L'ordre des lectures (conformité d'abord) est ce qui distingue la revue TOTALISATION de la revue habituelle.

## Cérémonie 5 : LA DIFFUSION (le Go/No-Go)

**Objectif :** décider la livraison selon des critères écrits, avec les preuves.

**Quand :** à chaque livraison, sans exception.

**Participants :** l'équipe, le décideur de livraison, le facilitateur (en observation).

**Entrées :** le contrat d'itération, les preuves (tests passés, revues faites), les bugs ouverts.

**Sorties :** la décision Go / No-Go avec réserves, le compte rendu, la note de diffusion.

**Le déroulé du niveau 1 (30 minutes) :** voir l'annexe A6 pour le format complet. Les points critiques du niveau 1 : les critères sont écrits avant la cérémonie (jamais improvisés), les preuves sont présentées (pas affirmées), les réserves sont formulées en une phrase (ce qui manque, qui le complète, pour quand).

**La capsule du vécu.** Le premier Go/No-Go formel de la mission a duré 20 minutes au lieu des deux heures habituelles de discussion. Les critères avaient tranché avant que le débat commence. La réaction du décideur : « C'est la première fois que je sais pourquoi on livre. » La qualité qui raccourcit les réunions : voilà un argument que personne n'attendait.

## Cérémonie 6 : LA CONFIRMATION

**Objectif :** vérifier que la livraison répond au besoin élicité — dans le réel.

**Quand :** 1 à 4 semaines après chaque diffusion.

**Participants :** l'équipe, le demandeur initial, les utilisateurs concernés.

**Entrées :** la livraison en production, les critères de succès de l'élicitation, les retours du terrain.

**Sorties :** la confirmation du besoin (ou son infirmation), les apprentissages pour la prochaine élicitation, les ajustements.

**Le déroulé du niveau 1 (30 minutes) :**

1. **La relecture des critères de succès** (5 min) : ce que le demandeur avait dit vouloir (cérémonie 1).
2. **La confrontation au réel** (15 min) : le demandeur décrit ce qu'il obtient. L'équipe écoute sans se défendre — c'est un recueil de données, pas un procès.
3. **La boucle** (10 min) : trois questions écrites — « qu'avons-nous appris ? », « qu'est-ce qui manquait dans notre élicitation ? », « qu'élicitons-nous différemment la prochaine fois ? ». C'est la grande boucle du SDLC : CONFIRMER alimente ÉLICITER.

**Le piège du niveau 1 :** sauter la confirmation parce que « le client est content ». Le contentement n'est pas la confirmation : seul le retour structuré des critères de succès est une information utilisable. Une équipe qui ne confirme jamais élicite toujours pareil — et répète donc ses erreurs d'élicitation.

**La capsule du vécu.** La première confirmation formelle de la mission a révélé que le tableau livré était utilisé par des gens qui n'avaient pas été élicités — les chefs d'équipe, pas les testeurs. Le besoin réel était chez les uns ; le tableau servait aux autres. Sans la confirmation, cette découverte serait arrivée un an plus tard, par le biais d'un conflit. Avec elle, elle a alimenté l'élicitation suivante en une semaine.

## Cérémonie 7 : LA QUALIMÉTRIE

**Objectif :** lire les signaux, décider, consigner.

**Quand :** hebdomadaire (le niveau 1 peut se contenter d'un point de 15 minutes).

**Participants :** l'équipe, le facilitateur.

**Entrées :** les métriques collectées (une au minimum au niveau 1), les décisions de la semaine.

**Sorties :** les décisions notées, les ajustements de métriques, les remontées au sponsor si nécessaire.

**Le déroulé du niveau 1 (15 minutes) :** la métrique est lue, sa tendance nommée, la décision (aucune / action / escalade) énoncée à voix haute et notée. Le format détaillé est dans la semaine 2 du livre.

## L'implémentation progressive des cérémonies

Au niveau 1, on n'installe pas sept cérémonies d'un coup. L'ordre recommandé :

| Semaine | Cérémonies installées | Pourquoi cet ordre |
|---|---|---|
| 1-2 | Élicitation, Définition | Les fondations du langage commun |
| 3 | Diffusion (Go/No-Go) | La décision formelle, avec les preuves accumulées |
| 4 | Planification | Une fois que les spécifications existent, la planification devient réelle |
| 5-6 | Confirmation | Après les premières diffusions, le retour devient possible |
| 7-8 | Implémentation (revues), Qualimétrie formalisée | La consolidation des rituels |

**La règle d'or :** une cérémonie n'est installée que lorsque celle d'avant tient sans le facilitateur. Une cérémonie qui ne tient pas est retravaillée, pas contournée.

## Le test des cérémonies

À la fin du niveau 1, chaque cérémonie installée doit passer ce test à trois questions :

1. **A-t-elle des entrées obligatoires ?** (Si tout peut entrer, la cérémonie n'est qu'une réunion ouverte.)
2. **A-t-elle un livrable daté ?** (Si rien n'est produit, elle ne s'est pas déroulée.)
3. **Tient-elle sans le facilitateur ?** (Le test de l'indépendance — le seul qui compte.)

Ces trois questions sont le test de passage au niveau 2 : une cérémonie qui les réussit est prête à être outillée et modélisée ; une cérémonie qui les échoue doit d'abord devenir réelle.
