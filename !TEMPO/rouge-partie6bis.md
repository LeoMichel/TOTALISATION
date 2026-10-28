
---

# Partie 6bis : Les cérémonies opérationnelles détaillées (le réel d'Opal-RT)

La Partie 6 a décrit les cérémonies du niveau 1 en format narratif. Cette partie les décrit en format opérationnel — avec les sources, les techniques, les critères de sortie et les pièges, tels qu'ils sont documentés chez Opal-RT. C'est le niveau de détail que le praticien N1 a besoin pour animer une cérémonie sans improviser.

## La cérémonie ÉLICITER — déroulé opérationnel complet

**L'objectif de la phase ÉLICITER** : recueillir, comprendre et consigner les besoins bruts avant même de les spécifier. L'objectif n'est pas de définir la solution, mais de faire émerger le vrai besoin et de s'assurer qu'il est suffisamment compris pour être transmis à la phase DÉFINIR.

> « On ne peut pas bien définir ce qu'on n'a pas bien élicité. »

### Les sources d'élicitation (Opal-RT)

Les besoins ne viennent pas d'un seul endroit. Il faut multiplier les canaux pour capter les signaux.

| Source | Exemples concrets chez Opal-RT |
|--------|-------------------------------|
| Client / utilisateur | Demandes de support, retours terrain, cas d'usage rapportés par les ingénieurs d'application |
| Support et incidents | Tickets, bugs récurrents, crash reports, irritants répétés |
| Qualimétrie / signaux | Métriques Grafana, tendances SonarQube, taux de défauts par version, DORA metrics |
| Stratégie et marché | Roadmap produit, positionnement concurrentiel, orientations de la direction |
| Amélioration continue | Retours post-livraison, rétrospectives, constats de la phase CARE, dette technique identifiée |
| Voix du client automatisée | Plateforme de type UserVoice, sondages, mécanismes de feedback intégrés à l'application |

### Les 7 techniques d'élicitation (Opal-RT)

**Technique 1 — Entrevues et conversations dirigées**
Rencontrer les parties prenantes — client, support, PO, développement, QA — individuellement ou en petit groupe. Poser des questions ouvertes : « Qu'est-ce qui vous empêche de… ? », « Que se passe-t-il quand… ? ». Ne pas chercher immédiatement la solution : commencer par comprendre le problème vécu.

**Technique 2 — Observation et immersion**
Observer l'utilisateur dans son contexte réel d'utilisation. Identifier les comportements non documentés, les contournements et les irritants. Utiliser les observations pour alimenter des cas concrets et mieux comprendre les impacts.

**Technique 3 — Ateliers d'élicitation collaborative**
Réunir les rôles SENSE, FORGE et CARE autour d'un cas concret. Utiliser des techniques comme l'Event Storming, le User Story Mapping ou l'Example Mapping. Faire émerger les règles, exemples, questions ouvertes et zones d'incertitude.

**Technique 4 — Analyse des données et signaux**
Consulter les métriques avant d'éliciter : « Qu'est-ce qui nous indique qu'il y a un risque ou une opportunité ? ». Utiliser les signaux pour orienter les questions et révéler des besoins implicites. Exemples : taux de défauts par module, fréquence des régressions, temps moyen de résolution.

**Technique 5 — Analyse documentaire et rétro-ingénierie**
Relire les tickets existants, incidents, notes de version et décisions passées. Extraire les besoins implicites des bugs récurrents ou des demandes répétées. Transformer les constats en besoins formulés et traçables.

**Technique 6 — Prototypage et maquettage rapide**
Esquisser un flux, un écran ou un diagramme pour valider la compréhension. Utiliser le prototype comme outil de conversation, pas comme solution finale. Valider rapidement si les parties prenantes reconnaissent leur problème dans la représentation proposée.

**Technique 7 — Utilisation de l'IA comme levier**
Soumettre un corpus de tickets, incidents ou commentaires à l'IA pour faire émerger des tendances. Générer des questions d'élicitation à partir d'un contexte produit. Valider la complétude d'une liste de besoins en confrontant plusieurs angles de lecture.

### Les critères de sortie de l'élicitation

L'élicitation est suffisamment avancée lorsque :
- Les besoins bruts sont recueillis et consignés.
- La source de chaque besoin est identifiée.
- Les signaux de qualimétrie ont été analysés et les constats sont documentés.
- Les priorités sont établies : ce qui entre en DÉFINIR et ce qui reste au backlog.
- Les besoins sont suffisamment compris pour être transmis à DÉFINIR.
- La compréhension du besoin est validée par la source, l'utilisateur ou le spécialiste concerné.

### Les pièges courants à éviter

| Piège | Pourquoi c'est un problème | Comment l'éviter |
|-------|--------------------------|------------------|
| Sauter directement à la solution | On risque de spécifier quelque chose que personne n'a vraiment demandé. | Reformuler le problème avant de parler de solution. |
| Éliciter avec un seul rôle | La vision est partielle et les angles morts sont nombreux. | Impliquer SENSE, FORGE et CARE dès l'élicitation. |
| Ne pas documenter la source | Il devient difficile de valider plus tard si le besoin est bien compris. | Associer chaque besoin à une source traçable. |
| Confondre ÉLICITER et DÉFINIR | On risque de spécifier sans avoir compris — et la spécification hérite des malentendus. | Séparer la phase ÉLICITER de la phase DÉFINIR. |

## La cérémonie DÉFINIR — déroulé opérationnel complet

**L'objectif de la phase DÉFINIR** : transformer les besoins élicités en spécifications testables. C'est la phase où le besoin devient une exigence vérifiable — et où la specification IF…THEN trouve sa place.

### Les critères de sortie de la phase DÉFINIR

La définition est suffisamment avancée lorsque :
- Les exigences sont formulées en IF…THEN… (ou en format équivalent testable).
- Les critères d'acceptation sont documentés (le demandeur les valide).
- Les cas limites sont identifiés (valeurs nulles, données vides, volume extrême, concurrence).
- La spécification est liée à son backlog item (traçabilité).
- La spécification est revue par les trois rôles (dev, QA, demandeur).
- Les règles métier sont extraites et documentées.

### Les pièges courants de la phase DÉFINIR

| Piège | Pourquoi c'est un problème | Comment l'éviter |
|-------|--------------------------|------------------|
| Spécifier ce que le demandeur n'a pas demandé | On construit quelque chose qui ne répond pas au besoin élicité. | Relire l'élicitation avant de spécifier. |
| Écrire une spécification encyclopédique | La spécification dépasse 2 pages pour une demande simple : personne ne la lira. | Visez le juste nécessaire. La spécification suit la complexité. |
| Ne pas impliquer les trois rôles | Une spécification lue par un seul rôle est incomplète. | Trois lecteurs : dev (implémentabilité), test (testabilité), demandeur (fidélité). |
| Spécifier avant d'avoir élicité | La spécification hérite des malentendus de l'élicitation. | L'élicitation précède la définition. Toujours. |

## La cérémonie PLANIFIER — déroulé opérationnel complet

**L'objectif de la phase PLANIFIER** : décider quoi, quand, par qui, avec quels risques assumés. C'est la phase où les spécifications prêtes entrent en itération — et où les risques connus deviennent des décisions explicites.

### Les critères de sortie de la phase PLANIFIER

La planification est suffisamment avancée lorsque :
- Les items sélectionnés ont une spécification prête (le DoR est satisfait).
- Les estimateurs sont présents (pas d'estimation par procuration).
- Les dépendances sont identifiées (interne, externe, environnement).
- Les risques connus sont documentés (avec parade ou acceptation écrite).
- Le contrat d'itération est écrit (ce qu'on livre, avec quels critères de fin).

### Les pièges courants de la phase PLANIFIER

| Piège | Pourquoi c'est un problème | Comment l'éviter |
|-------|--------------------------|------------------|
| Planifier avec la capacité espérée | L'itération surchargée est le début de la spirale. | Planifier avec la capacité mesurée (les données réelles). |
| Ignorer le DoR | Les items sans spécification produisent des itérations au flou. | La règle : pas de spécification, pas d'itération. |
| Oublier les risques | Les risques non documentés se transforment en incidents. | Chaque item porte ses risques connus. Chaque risque a un plan. |

## La cérémonie IMPLÉMENTER — déroulé opérationnel complet

**L'objectif de la phase IMPLÉMENTER** : produire le code conforme à la spécification, avec les preuves (tests, revues, artefacts). C'est la phase où le code est écrit, revu, testé — et où la conformité à la spécification est vérifiée.

### Les critères de sortie de la phase IMPLÉMENTER

L'implémentation est suffisamment avancée lorsque :
- Le code est conforme à la spécification (revue faite, divergences documentées).
- Les cas de validation sont exécutés (preuves collectées).
- La revue de code est faite (conformité d'abord, style ensuite).
- Les tests sont passés (ou les échecs documentés avec raison).

### Les pièges courants de la phase IMPLÉMENTER

| Piège | Pourquoi c'est un problème | Comment l'éviter |
|-------|--------------------------|------------------|
| Revue de style sans revue de conformité | Un code élégant qui ne fait pas ce que la spécification dit est un beau bug. | Revue : conformité d'abord, style ensuite. |
| Coder sans spécification ouverte | Le développeur code à partir de son interprétation, pas de la spécification. | La spécification ouverte à côté du code. Toujours. |
| Ignorer les divergences code/spécification | Une divergence non traitée est un bug silencieux. | Chaque divergence est documentée : spécification corrigée ou code corrigé. |

## La cérémonie DIFFUSER (le Go/No-Go) — déroulé opérationnel complet

**L'objectif de la phase DIFFUSER** : décider la livraison selon des critères écrits, avec les preuves. C'est le moment où la qualité parle le langage de la direction : la décision de livrer.

### Les critères de sortie de la phase DIFFUSER

La diffusion est suffisamment avancée lorsque :
- Les critères de Go sont écrits (et connus de tous avant la séance).
- Les preuves sont collectées (pas affirmées).
- La décision est prise (Go, Go avec réserves, No-Go).
- Le compte rendu est rempli (pendant la séance, pas après).
- Les réserves ont une condition de levée (quoi, qui, quand).

### Les pièges courants de la phase DIFFUSER

| Piège | Pourquoi c'est un problème | Comment l'éviter |
|-------|--------------------------|------------------|
| Le Go/No-Go toujours vert | La grille ne filtre rien si aucun critère n'est jamais rouge. | Resserrer les seuils jusqu'à ce que la grille ait du pouvoir. |
| La décision prise hors séance | La cérémonie devient un théâtre de légitimation. | La décision se prend en séance, jamais en couloir. |
| Les réserves sans condition de levée | Une réserve sans levée est une excuse — pas une réserve. | Le format : quoi, qui, quand. Sinon le facilitateur refuse. |
| Le compte rendu rempli après | Un compte rendu après-coup est un souvenir. | Rempli pendant la séance. Toujours. |

## La cérémonie CONFIRMER — déroulé opérationnel complet

**L'objectif de la phase CONFIRMER** : vérifier que la livraison répond au besoin élicité — dans le réel. C'est le moment où la grande boucle se referme : ce que la confirmation apprend alimente la prochaine élicitation.

### Les critères de sortie de la phase CONFIRMER

La confirmation est suffisamment avancée lorsque :
- Les critères de succès de l'élicitation sont confrontés au réel (atteint, partiel, non).
- Les usages réels sont observés (pas demandés : observés).
- Les apprentissages sont écrits (qu'avez-vous appris ? qu'est-ce qui manquait dans l'élicitation ? qu'élicitons-nous différemment ?).
- Les apprentissages ont une destination (prochaine élicitation, backlog, mémoire).

### Les pièges courants de la phase CONFIRMER

| Piège | Pourquoi c'est un problème | Comment l'éviter |
|-------|--------------------------|------------------|
| Sauter la confirmation parce que « le client est content » | Le contentement n'est pas la confirmation : seul le retour structuré des critères de succès est une information utilisable. | Confronter les critères de succès, pas l'opinion. |
| Confirmer à chaud (trop tôt) | L'usage réel se mesure 1 à 4 semaines après la diffusion — pas le jour de la livraison. | Attendre 1 à 4 semaines. Mesurer l'usage, pas la première impression. |
| Ne pas documenter les apprentissages | Un apprentissage non écrit est un apprentissage perdu. | Trois questions écrites : qu'avons-nous appris ? qu'est-ce qui manquait ? qu'élicitons-nous différemment ? |

## La cérémonie QUALIMÉTRIE — déroulé opérationnel complet

**L'objectif de la phase QUALIMÉTRIE** : lire les signaux, décider, consigner. C'est le battement de cœur de la méthode : le point où les métriques servent les décisions, pas le reporting.

### Les critères de sortie de la phase QUALIMÉTRIE

La qualimétrie est suffisamment avancée lorsque :
- La métrique est lue (valeur, tendance, seuil).
- La décision est énoncée à voix haute et notée (aucune / action / escalade).
- Le tableau de bord est mis à jour (la métrique de la semaine, pas la métrique du mois dernier).
- Les apprentissages sont reliés à la prochaine action.

### Les pièges courants de la phase QUALIMÉTRIE

| Piège | Pourquoi c'est un problème | Comment l'éviter |
|-------|--------------------------|------------------|
| La métrique lue mais jamais discutée | Une métrique qui ne déclenche pas de décision est une décoration. | Chaque métrique lue est suivie de « et donc... ». |
| Les métriques produites mais plus regardées | Le tableau de bord devient un artefact mort. | Si l'équipe ne regarde plus le tableau, le problème n'est pas le tableau — c'est la cadence. |

---

*Fin des cérémonies opérationnelles détaillées — adaptées depuis les documents ACAQ-OPAL-RT, pour l'usage du praticien N1 dans les quatre premières semaines du niveau ROUGE.*
