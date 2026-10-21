
---

# Partie 7 : Cas réels, gabarits remplis et variantes contextuelles

Cette partie complète les huit semaines du niveau 2 avec ce qu'un descriptif d'atelier ne peut pas montrer : les gabarits remplis par une vraie équipe, les situations vécues derrière les capsules, et l'adaptation du parcours aux contextes non standards.

## 1. Les gabarits remplis d'exemples réels

### 1.1 Premier modèle BPMN — exemple rempli

> Exemple de la mission Faucon, semaine 1 du niveau 2. Le processus modélisé : la correction d'un bug, de la détection à la vérification.

**Éléments du modèle :**

| Élément BPMN | Contenu | Remarque |
|---|---|---|
| Événement de départ | Un bug est détecté (test automatisé, client, ou support) | Trois sources, un seul point d'entrée |
| Tâche 1 | Qualifier le bug selon les critères écrits (niveau 1) | Utilise les critères de priorisation de ROUGE |
| Passerelle 1 | Critique ? | Oui → flux urgent / Non → flux normal |
| Tâche 2 (flux urgent) | Correction immédiate + test de non-régression ciblé | |
| Tâche 2 (flux normal) | Création de la spécification de correction avant le code | La spécification d'une correction est plus courte, mais existe |
| Passerelle 2 | La correction modifie-t-elle un comportement documenté ? | Oui → mettre à jour le modèle / Non → continuer |
| Tâche 3 | Vérification selon les critères de validation écrits | |
| Événement de fin | Bug vérifié corrigé, preuves archivées | |

**Les trois divergences trouvées lors de la confrontation (atelier 1.2) :**
1. Le développeur avait modélisé la correction directement après la qualification, sans spécification. Le QA avait mis une tâche « écrire ce qui est corrigé ». → Le conflit exact que le niveau 2 veut résoudre.
2. Le modèle du développeur ne contenait pas la mise à jour du modèle lui-même. Le modèle BPMN du processus de bug ne se mettait pas à jour dans le processus de bug. → Meta-problème classique.
3. Les deux avaient oublié la vérification du correctif en production (CONFIRMER). → Le trou que la grille de couverture du niveau 2 comble.

### 1.2 Spécification de correction — exemple rempli

> La spécification courte du correctif, produite à partir du modèle. Notez la longueur : une page. C'est une correction, pas une fonctionnalité.

**Correctif BUG-1247 : le filtre combiné ignore les valeurs nulles**

**Contexte :** le filtre du rapport X combiné à un second filtre produit des résultats incorrects quand la première colonne contient des valeurs nulles.

**Comportement observé :** les lignes avec valeur nulle dans la colonne 1 sont exclues du résultat, même si elles satisfont le second filtre.

**Comportement attendu :** une valeur nulle dans la colonne 1 n'exclut pas la ligne ; elle n'est simplement pas filtrée par ce critère. Les autres filtres s'appliquent normalement.

**Règles de validation :**
1. Avec colonne 1 vide et filtre colonne 2 = « actif » : les lignes actives apparaissent.
2. Avec colonne 1 = « inactif » et filtre colonne 2 = « actif » : aucune ligne (comportement inchangé).
3. Le rapport sans filtre n'est pas affecté (non-régression).

**Cas limite :** les données historiques migrées contiennent des valeurs nulles pour une raison métier (non renseigné à l'époque) : elles doivent apparaître comme les autres valeurs nulles, sans traitement spécial.

**Pourquoi ce format :** trois règles de validation numérotées, un cas limite métier explicite. Le développeur qui code ce correctif n'a aucune question à poser. C'est le standard du niveau 2 pour une correction.

### 1.3 Documentation liée au modèle — extrait rempli

> Page de documentation produit générée à partir du modèle, niveau 2.

**Comportement du filtre du rapport X** *(source : modèle BPM « correction de bug », révision 3, à jour)*

Le filtre du rapport X s'applique aux colonnes sélectionnées. Règles :

- Chaque filtre s'applique indépendamment aux autres.
- Une valeur nulle dans une colonne filtrée **n'exclut pas** la ligne (elle échappe au filtre de cette colonne).
- Les filtres se combinent par ET logique.

*Cette page est mise à jour automatiquement à chaque révision du modèle. Dernière synchronisation : automatique, pipeline du 12 juillet. Référence du modèle : BPM-004, révision 3.*

**Pourquoi la référence du modèle compte :** la documentation qui ne cite pas sa source ne peut pas être vérifiée. Avec la référence, un lecteur qui doute de la page peut ouvrir le modèle et comparer — la documentation devient falsifiable, donc digne de confiance.

## 2. Cas vécus étendus : le niveau 2 de la mission Faucon

### Cas de la semaine 1 : le modèle que personne ne voulait dessiner

**Situation.** L'atelier de modélisation BPMN a commencé par une résistance inattendue : le tech lead a déclaré que son équipe « pense en code, pas en diagrammes », et que le BPMN était « une perte de temps pour gens qui ne lisent pas le code ».

**Le tournant.** Le coach n'a pas défendu le BPMN. Il a proposé un test : modélisez le processus de correction de bug comme vous le faites vraiment, et ensuite, chacun décrit le processus de l'autre à partir du modèle. Le développeur a décrit le processus du QA à partir du modèle du QA — et a découvert qu'il croyait que le QA testait avant la correction, alors que le modèle disait le contraire. Le QA croyait l'inverse. Les deux avaient tort sur le processus de l'autre depuis des mois.

**La suite.** La discussion qui a suivi a duré 40 minutes et a produit trois corrections de processus — pas du modèle, du processus réel. Le tech lead a conclu : « Le diagramme n'a rien appris au code. Il a appris ce qu'on fait chacun. »

**Ce que ce cas enseigne.**
- Le BPMN n'est pas un exercice de documentation : c'est un instrument de découverte des malentendus entre rôles. Sa valeur se mesure au nombre de « attends, toi tu fais ça ? » qu'il provoque.
- Ne vendez jamais l'outil. Proposez le test : « décris le processus de l'autre à partir de son modèle ». Si le modèle ne révèle rien, il n'était pas nécessaire — et vous l'aurez prouvé par le test, pas par l'argument.
- La résistance au modèle est souvent la résistance à être lu. Un processus modélisé devient discutable ; un processus oral reste invérifiable. Certaines personnes préfèrent l'invérifiable — le dialogue sur ce point vaut mieux que l'imposition.

### Cas de la semaine 3 : le plan qui est devenu honnête

**Situation.** Le plan de livraison du trimestre promettait six fonctionnalités. L'exercice de la semaine 3 (lier chaque élément à un modèle et à des preuves) a révélé que deux des six n'avaient aucun modèle, et qu'une troisième avait un modèle décrivant un comportement différent de la demande originale.

**La tentation.** Garder le plan tel quel et « créer les modèles en cours de route ». C'est le fonctionnement du niveau 1, déguisé.

**La décision.** Le plan a été présenté au sponsor avec la vérité : deux fonctionnalités étaient « non modélisées » (donc non estimables sérieusement), une était « divergente » (le modèle et la demande racontent des choses différentes — il faut trancher laquelle est la bonne). Le sponsor a réagi : « Vous me dites que la moitié du plan est du vent ? » Réponse : « Non. Nous vous disons que la moitié du plan n'a pas encore de preuve. Voici ce qu'il faut pour en avoir. » Le plan a été révisé : quatre fonctionnalités ferme, deux en « investigation de modèle » avec date de résolution.

**Ce que ce cas enseigne.**
- Le plan lié aux modèles n'est pas plus lent : il est plus honnête. La différence se voit au moment où le sponsor demande « où on en est » — la réponse devient factuelle.
- « Non modélisé » n'est pas un échec : c'est une catégorie de plan. La catégorie existe pour que les zones d'incertitude soient visibles au lieu d'être maquillées.
- Le dialogue avec le sponsor change de nature quand les réponses sont des preuves : il passe de « faites-moi confiance » à « regardez ». Le second est plus confortable pour tout le monde, y compris pour lui.

### Cas de la semaine 5 : la documentation que le client a lue

**Situation.** Pendant le point mort du niveau 2, un client a contacté le support avec une question sur le comportement d'un filtre. Le support a répondu en copiant la page de documentation liée au modèle. Le client a répondu : « C'est clair, merci — c'est rare. »

**La signification.** La documentation du niveau 2 n'a pas été écrite pour les clients — elle a été écrite à partir du modèle, pour l'équipe. Mais une documentation produite à partir d'une source de vérité est claire par construction, et la clarté ne connaît pas son public d'origine.

**Ce que ce cas enseigne.**
- La documentation vivante est reconnaissable à un signe externe : les gens la citent. Interne ou externe, peu importe — le jour où quelqu'un copie-colle votre documentation pour répondre à une vraie question, elle est vivante.
- Cet événement est arrivé pendant le point mort, la semaine où l'équipe doutait de la valeur de l'effort. Un signe externe de valeur vaut plus que tous les arguments internes. Cherchez-les activement pendant les semaines difficiles.
- Le support qui répond en copiant la documentation (plutôt qu'en réécrivant) est aussi un signal : les équipes de support deviennent les premiers consommateurs de la documentation vivante. Invitez-les à signaler ce qui n'y est pas — ils sont le capteur le plus fin des trous de documentation.

### Cas de la semaine 7 : le test généré qui a attrapé le bug

**Situation.** La matrice de couverture de la semaine 7 incluait les tests générés par le modèle. Un test généré, portant sur une combinaison de filtres que personne n'avait écrite manuellement, a détecté un défaut de comportement combiné — exactement la famille de bugs du cas BUG-1247.

**La signification.** Le modèle BPMN contenait une passerelle de combinaison de filtres ; le générateur a produit le test de la combinaison non documentée ; le test a échoué ; le défaut a été corrigé avant la livraison. Aucun test manuel ne couvrait cette combinaison : elle était dans le modèle, pas dans l'expérience de l'équipe.

**Ce que ce cas enseigne.**
- La valeur du MBT se concrétise dans les tests que personne n'aurait écrits : les combinaisons, les chemins rares, les cas que l'expérience humaine ne pense pas à couvrir. Le modèle raisonne plus systématiquement que les humains — c'est précisément son rôle.
- Ce type d'événement est le meilleur argument pour le niveau 2, et il doit être documenté : « test généré T-042, combinaison non couverte manuellement, défaut corrigé ». Ces cas deviennent les preuves du rapport de maturité.
- Ne surventez pas non plus : le même générateur a produit 40 tests sans valeur pour ce défaut. Le ratio (1 utile / 40 produits) est la donnée honnête à présenter avec le succès.

## 3. Variantes contextuelles du niveau 2

### V1 : petite équipe (2 à 4 personnes)

- Un seul modèle BPMN suffit pour démarrer : choisissez le processus le plus coûteux en malentendus. Le modèle unique est mieux qu'aucun modèle.
- La confrontation des modèles se fait entre deux personnes, pas entre sous-groupes — et elle reste la partie la plus précieuse de l'atelier.
- La documentation liée au modèle peut être une seule page wiki bien tenue plutôt qu'un générateur complet.
- Le rôle de responsable de modèle tourne : dans une petite équipe, tout le monde doit savoir maintenir le modèle.

### V2 : équipe distribuée

- La modélisation collaborative exige un outil en ligne partagé (même gratuit). Le tableau blanc vidéo ne suffit pas pour du BPMN.
- La confrontation des modèles fonctionne bien à distance : chaque binôme partage son écran, l'un décrit le modèle de l'autre. La règle « je décris ton modèle, tu me corriges » est même plus efficace à distance, où personne ne peut pointer le même écran.
- La documentation liée au modèle est l'atout du travail distribué : c'est ce que les gens lisent quand ils ne peuvent pas demander. Investissez-y davantage.

### V3 : legacy lourd

- Le premier modèle BPMN ne doit pas décrire le processus idéal : il doit décrire le processus réel, avec ses contournements et ses zones d'ombre. Le modèle du réel est le point de départ ; le modèle de l'idéal est l'objectif, atteint par itérations.
- Les tests générés sur un legacy révèlent souvent des comportements inattendus du système actuel : traitez-les comme des découvertes, pas comme des bugs du générateur. Chaque comportement inattendu est documenté : « le système fait X, le modèle disait Y, qui a raison ? »
- La documentation liée au modèle est l'outil le plus rentable sur un legacy : c'est souvent la première documentation à jour de l'histoire du produit.

### V4 : organisation réglementée

- Le modèle BPMN devient un document réglementaire : sa révision est tracée, ses versions archivées. C'est un avantage, pas une contrainte : la traçabilité réglementaire et la traçabilité du modèle sont la même chose.
- La documentation liée au modèle satisfait souvent une exigence de documentation produit : montrez le mapping à votre auditeur avant qu'il le demande.
- Les tests générés à partir du modèle peuvent servir de preuve de couverture réglementaire : la matrice de couverture devient le document d'audit.

### V5 : le sponsor sceptique

- Le niveau 2 est plus difficile à vendre que le niveau 1, car ses bénéfices sont moins immédiats (un modèle ne corrige pas un bug). La preuve par la première divergence trouvée (« nous croyions que le QA testait avant, il teste après ») est le meilleur argument : cherchez-la et montrez-la.
- Le « fait de la semaine » du niveau 2 : une phrase factuelle par semaine au sponsor. (« Cette semaine : le modèle du processus de bug a révélé 3 malentendus inter-rôles, corrigés. »)
- Le moment de bascule typique du sponsor sceptique : la première fois qu'un plan lié aux modèles lui donne une réponse factuelle à « où on en est ? ». Après cela, il demande les modèles, pas les slides.

### V6 : reprise après échec du niveau 1

- Si le niveau 1 a été abandonné, les artefacts restants (lexique, critères de bugs) sont la fondation du niveau 2 : ne repartez pas de zéro, mais ne réutilisez pas non plus aveuglément. Chaque artefact est relu et validé avant réutilisation.
- La modélisation est souvent une meilleure porte d'entrée que la spécification pour une équipe brûlée par un échec : dessiner le processus réel est moins menaçant que réécrire des spécifications « comme on vous l'a déjà demandé ».
- La règle du niveau 2 pour les reprises : un seul modèle à la fois, réussi, avant le second. La surcharge est la cause de mort la plus fréquente des reprises.

---

## Comment utiliser cette partie

- **Avant de commencer** : lisez la variante correspondant à votre contexte.
- **Pendant le parcours** : quand un atelier bloque, cherchez le cas vécu correspondant — particulièrement le cas de la semaine 1 (le modèle que personne ne voulait dessiner), qui est le point de résistance le plus fréquent du niveau 2.
- **À la semaine 8** : comparez vos gabarits remplis avec les exemples. La spécificité est la cible, pas le contenu.
