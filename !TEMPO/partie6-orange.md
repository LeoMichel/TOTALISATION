
---

# Partie 6 : Le manuel de l'atelier — fiches détaillées d'animation

Cette partie transforme chaque atelier du livre en une fiche d'animation prête à l'emploi. Elle s'adresse au coach, au facilitateur, ou à tout membre de l'équipe qui reprend un atelier sans l'auteur du livre. Chaque fiche suit le même format : l'intention, le matériel, le déroulé minute par minute, les pièges, et la variante pour petit groupe.

**Comment utiliser ce manuel :** imprimez la fiche de l'atelier que vous animez. Ne l'improvisez pas de mémoire : la fiche contient les pièges qui ne se voient que quand on les a vus. Et après l'atelier, annotez la fiche avec ce qui a marché et ce qui n'a pas marché — c'est le manuel qui doit apprendre de chaque animation.

## Fiche 1.1 : Arrimage niveau 2 (2 h)

**Intention :** ancrer la continuité avec le niveau 1 sans transformer l'arrimage en réunion de bilan. L'équipe doit sortir de l'atelier avec trois processus à modéliser et des responsables nommés.

**Matériel :** les livrables du niveau 1 (lexique, contrat v0.2, premier tableau de qualimétrie), un tableau blanc, des post-its de trois couleurs.

**Déroulé :**
1. (15 min) Tour de table : chacun nomme une pratique de niveau 1 qu'il utilise encore et une qu'il a lâchée. Pas de justification : on constate.
2. (30 min) Inventaire des livrables du niveau 1 : afficher le lexique, le contrat, la qualimétrie. Chacun marque : je l'utilise / je ne l'utilise pas / je ne le connais pas.
3. (30 min) Identification des 3 à 5 processus critiques : chaque participant propose un processus qui, s'il est mal compris, coûte cher. On vote : ce qui est mal compris par le plus de personnes d'abord.
4. (25 min) Nommer les responsables de modèles : un volontaire par modèle, pas une assignation. Si personne ne se porte volontaire, le processus n'est pas assez critique ou le moment n'est pas bon.
5. (20 min) Décider l'ordre de modélisation de la semaine, et ce qui est reporté.

**Pièges :**
- L'atelier dérive en procès des pratiques du niveau 1. Ramenez : le niveau 1 a été ce qu'il devait être. On construit, on ne juge pas.
- Le coach propose lui-même les processus critiques. Non : l'équipe les propose, le coach vérifie seulement que les critères sont explicites.
- Les responsables sont nommés d'office. Un responsable nommé d'office devient un résistant.

**Variante petit groupe (moins de 5 personnes) :** fusionnez les étapes 2 et 3 : l'inventaire des livrables se fait pendant que les processus sont proposés.

## Fiche 1.2 : BPMN pour modéliser le cycle de vie produit (3 h)

**Intention :** faire produire un premier modèle BPMN réel, pas un exemple pédagogique. La confrontation des sous-groupes est le cœur de l'atelier : l'ambiguïté se voit quand deux modélisations divergent.

**Matériel :** un outil de modélisation partagé (ou des gabarits papier), les processus identifiés en fiche 1.1, la charte de nommage si elle existe.

**Déroulé :**
1. (20 min) Révision express des éléments BPMN : événements, activités, passerelles, flux, lanes. Utilisez un modèle existant de l'équipe comme support, pas un exemple générique.
2. (30 min) Modélisation en direct d'un processus simple : le facilitateur dessine sous dictée de l'équipe. Il ne décide pas : il exécute les décisions de l'équipe et nomme les ambiguïtés qu'il détecte.
3. (60 min) Modélisation par sous-groupes. Règle d'or : si le modèle ne peut pas être relu à froid par un tiers, il n'est pas fini.
4. (40 min) Confrontation : les sous-groupes présentent, l'équipe repère les divergences. Chaque divergence est écrite sur un post-it, pas discutée à l'infini.
5. (30 min) Décision : quel modèle devient référence, lequel reste brouillon, et qui corrige quoi d'ici la fin de semaine.

**Pièges :**
- L'atelier devient un cours sur BPMN. La révision express suffit : on apprend la notation en modélisant, pas avant.
- Le facilitateur corrige les modèles des sous-groupes en direct. Non : la confrontation entre sous-groupes est l'outil de correction.
- Vouloir un modèle parfait du premier coup. Un modèle de niveau 2 est un modèle relu avec divergences écrites, pas un chef-d'œuvre.

**Variante petite équipe :** un seul processus, modélisé par deux binômes indépendants. La confrontation de deux versions du même processus est plus riche que trois modèles différents.

## Fiche 1.3 : MBT — rendre le modèle exécutable (3 h)

**Intention :** démontrer qu'un modèle n'est pas un dessin : il génère des tests. L'atelier doit finir avec un cas de test réellement exécuté, pas un concept expliqué.

**Matériel :** le modèle choisi en fiche 1.2, l'outil MBT disponible ou la procédure d'extraction manuelle, l'environnement de test de l'équipe.

**Déroulé :**
1. (20 min) Principe MBT en trois points : le modèle décrit les états et transitions, les parcours générés sont des cas de test, la couverture du modèle devient la couverture des tests.
2. (40 min) Extraction manuelle : l'équipe extrait à la main les 5 à 8 cas de test essentiels d'un chemin critique du modèle. Cette étape manuelle est indispensable : elle forme l'intuition qui permettra de diagnostiquer les sorties de l'outil.
3. (60 min) Extraction par outil (si disponible) : comparer les cas de l'extraction manuelle aux cas générés. Les écarts sont les cas que l'intuition seule n'aurait pas trouvés.
4. (30 min) Exécution d'un cas : exécuter réellement un des cas générés sur l'environnement de test. Un cas non exécuté en atelier ne prouve rien.
5. (30 min) Décision de maintenance : qui met à jour le modèle quand le code change ? Quel délai ? Quelle preuve de synchronisation ? Écrire la règle sur une page.

**Pièges :**
- Vouloir automatiser tout le modèle. Un chemin critique suffit pour la première exécution.
- Laisser l'outil générer des centaines de cas. Le nombre n'est pas la couverture : 8 cas bien choisis valent mieux que 300 cas malléables.
- Sauter l'extraction manuelle. Sans elle, l'équipe ne comprend pas ce que l'outil fait et ne saura pas diagnostiquer ses sorties.

**Variante sans outil MBT :** l'extraction manuelle devient la méthode. L'atelier produit une règle d'extraction écrite d'une page, tenue à chaque modification de modèle.

## Fiche 2.1 : Outillage pour l'automatisation des spécifications (3 h)

**Intention :** structurer la chaîne modèle → test → documentation avec les outils déjà présents, sans achat ni migration. La boîte à outils de niveau 2 est un arrangement, pas un achat.

**Matériel :** l'inventaire des outils actuels, la chaîne de livraison actuelle, les modèles produits en semaine 1.

**Déroulé :**
1. (20 min) Carte des outils actuels : chaque outil est placé dans une colonne (modélisation, automatisation, documentation, intégration). Les cases vides sont les manques.
2. (40 min) La chaîne cible : dessiner la chaîne cible : modèle → tests générés → exécution → preuve → documentation. Marquer les maillons manquants.
3. (60 min) Fermer les manques avec ce qui existe : réutiliser les outils actuels dans le nouvel arrangement plutôt que d'introduire un nouvel outil. Un nouvel outil est un coût caché : formation, licences, maintenance.
4. (40 min) Responsabilités de maintenance : pour chaque maillon, qui maintient ? qui relit ? qui est alerté quand ça casse ? Écrire le tableau des responsabilités.
5. (20 min) Démonstration de bout en bout : modifier un modèle et regarder la chaîne propager jusqu'à la documentation. Cette démonstration est le contrat moral de l'atelier.

**Pièges :**
- Achat d'un nouvel outil en atelier. Non : la décision d'achat se prend hors atelier, sur preuve de manque réel documenté.
- La chaîne cible dessinée reste un dessin. Chaque maillon a un responsable nommé, sinon la chaîne est un vœu.
- Le facilitateur installe la chaîne lui-même. Non : l'équipe installe, le facilitateur vérifie.

**Variante sans intégration continue :** la chaîne se tient à la main, avec une checklist de propagation écrite et tenue à chaque modification de modèle. Plus lent, mais déjà du niveau 2.

## Fiche 2.2 : Documentation produit comme spécification vivante (3 h)

**Intention :** faire de la documentation un produit du cycle, pas un document à côté. La démonstration clé : une modification de modèle met à jour la documentation sans réécriture manuelle.

**Matériel :** la chaîne de niveau 2 (fiche 2.1), les pages de documentation produit actuelles, les modèles BPMN de l'équipe.

**Déroulé :**
1. (20 min) Diagnostic de la documentation actuelle : quelles pages sont vivantes (reliées au produit) ? lesquelles sont mortes (non mises à jour depuis le début du projet) ? Les pages mortes sont marquées.
2. (40 min) Choisir une page morte : la ressusciter en la reliant au modèle correspondant. Cette résurrection est la démonstration du principe.
3. (60 min) Réécriture d'une page vivante : la réécrire à partir du modèle, pas à partir de l'ancienne version. La réécriture doit être plus courte que l'original : plus courte, plus reliée, plus testable.
4. (40 min) Convention de maintenance : qui met à jour la documentation quand le modèle change ? Quelle preuve de synchronisation ? Quelle fréquence de relecture ? Écrire la convention, une page.
5. (20 min) Publication : la page réécrite est publiée, l'ancienne version archivée avec sa date de mort.

**Pièges :**
- Ressusciter toutes les pages mortes d'un coup. Une page à la fois : la chaîne doit démontrer la propagation avant le grand nettoyage.
- La documentation générée n'est relue par personne. Une page générée sans relecture humaine devient fausse avec plus d'assurance qu'une page écrite.
- La convention de maintenance est écrite mais jamais tenue. Prévoir la date de relecture dans la convention elle-même.

**Variante sans génération automatique :** la page est mise à jour à la main à partir du modèle, avec une checklist de synchronisation. Plus lent, mais déjà du niveau 2.

## Fiche 3.1 : Le plan relié aux modèles (3 h)

**Intention :** faire du plan de livraison une projection des modèles, pas un document parallèle. Le plan de niveau 2 répond à « quand » à partir de « qu'est-ce qui est prouvé », pas à partir d'optimisme.

**Matériel :** le plan actuel, les modèles BPMN/MBT de l'équipe, les résultats d'automatisation, la matrice de couverture.

**Déroulé :**
1. (20 min) Diagnostic du plan actuel : chaque ligne du plan a-t-elle un modèle ? une preuve ? Les lignes sans preuve sont marquées comme zones d'ambiguïté.
2. (40 min) Relier chaque ligne du plan à un modèle et à une preuve. Les lignes qui ne peuvent pas être reliées deviennent des décisions explicites : modéliser, reporter, ou assumer le risque par écrit.
3. (60 min) Reconstruire le plan : chaque ligne pointe vers un modèle, un test et une preuve. Les dates ne sont plus des promesses : ce sont des conséquences d'un état de preuves.
4. (40 min) Revue à contre-courant : un participant qui n'a pas participé à la construction relit le plan à froid et pose les questions que le plan ne répond pas.
5. (20 min) Décision : le plan reconstruit devient la référence ; l'ancien plan est archivé avec sa date de mort.

**Pièges :**
- Relier des lignes fictives. Si une ligne n'a ni modèle ni preuve, elle ne se relie pas : elle se décide.
- Le plan reconstruit est plus lent que l'ancien et l'équipe s'en inquiète. C'est normal : il dit la vérité. La vitesse revenue viendra de la réduction des ambiguïtés, pas du plan.
- La revue à contre-courant est sautée « par manque de temps ». C'est l'étape qui révèle ce que le groupe ne voit plus.

**Variante petit groupe :** la revue à contre-courant se fait par un seul relecteur externe (un membre d'une équipe voisine), ce qui prépare en même temps la démonstration aux voisins de la semaine 6.

## Fiche 3.2 : L'engagement de livraison comme contrat testable (2 h)

**Intention :** réécrire les engagements de livraison en forme contractuelle SI/ALORS, avec preuve. Un engagement qu'on ne peut pas tester est un engagement qu'on ne peut pas tenir.

**Matériel :** les engagements de livraison de la période, les critères de Go du rituel Go/No-Go, les preuves d'automatisation disponibles.

**Déroulé :**
1. (20 min) Prendre un engagement typique et le disséquer : « la version 2.4 sera livrée le 30 ». Qu'est-ce que ça veut dire ? Qui décide ? Sur quelle base ?
2. (40 min) Le réécrire en SI/ALORS : « SI les tests de type [X] passent sur les flux critiques du modèle [Y], ALORS la version 2.4 est livrée le 30 ». Identifier ce qui manque pour que le SI soit vérifiable : données, environnement, modèle à jour, couverture.
3. (40 min) Répéter l'exercice sur tous les engagements de la période. Compter combien deviennent testables immédiatement, combien demandent un travail, combien sont impossibles à tester en l'état.
4. (20 min) Publier les engagements réécrits et les engagements impossibles à tester (assumés, avec la raison).

**Pièges :**
- Le SI devient une liste de 15 conditions. Un SI qui ne tient pas en trois conditions n'est pas un critère : c'est un rapport.
- Les engagements impossibles à tester sont cachés. Nommez-les : ce sont eux qui produiront les surprises de fin de cycle.
- Le sponsor n'est pas associé. Un contrat testable que le sponsor n'a pas lu n'engage personne.

**Variante :** l'exercice se fait directement en rituel Go/No-Go sur l'engagement de la semaine : la réécriture devient l'ordre du jour permanent.

## Fiche 4.1 : Des métriques aux signaux de décision (2 h)

**Intention :** passer des métriques qui décrivent (ce qui s'est passé) aux signaux qui décident (ce qu'il faut faire maintenant). Un signal sans décision est une curiosité.

**Matériel :** la liste des métriques actuelles, les décisions prises au cours du dernier mois, le tableau des responsabilités.

**Déroulé :**
1. (20 min) Inventaire des métriques actuelles. Pour chacune : quelle décision a-t-elle déclenchée au cours du dernier mois ? Les métriques sans décision sont marquées.
2. (30 min) Pour chaque métrique utile : définir le seuil (à partir de quand on agit), le décideur (qui agit), l'action attendue (quoi se passe quand le seuil est franchi).
3. (30 min) Transformer les métriques sans décision : soit leur donner un seuil et un décideur, soit les éliminer. Une métrique éliminée fait gagner du temps à chaque point de qualimétrie.
4. (20 min) Relier chaque signal à son contexte : un chiffre sans contexte (modèle concerné, périmètre, période) n'est qu'un chiffre. Écrire la règle de contexte d'une ligne.

**Pièges :**
- Donner un seuil à une métrique qui n'a jamais déclenché de décision. C'est un faux signal : il décorera le tableau sans rien décider.
- Le seuil est fixé pour que le signal soit toujours vert. Un seuil qui ne se franchit jamais n'est pas un seuil : c'est une décoration.
- Le décideur est « l'équipe ». Un décideur collectif n'est pas un décideur : nommez une personne.

**Variante :** l'exercice se limite aux cinq métriques du tableau de bord qui sera construit en fiche 4.2. Moi de focaliser l'énergie.

## Fiche 4.2 : Le tableau de bord lu en rituel (3 h)

**Intention :** construire un tableau de bord minimal (5 à 7 signaux), alimenté automatiquement autant que possible, lu en rituel, et vivant.

**Matériel :** les signaux définis en fiche 4.1, les outils d'extraction disponibles, le rituel de revue de plan.

**Déroulé :**
1. (30 min) Sélection des 5 à 7 signaux essentiels : état des modèles critiques, tests passés/échoués, couverture, dérogations actives, temps de cycle, bugs post-livraison. Pas plus : un tableau de bord de 15 lignes n'est plus lu au bout de trois semaines.
2. (40 min) Source de chaque signal : outil, extrait, calcul, fréquence de mise à jour. Un signal alimenté à la main est nommé comme tel : c'est un risque de mort lente.
3. (60 min) Construction du tableau le plus simple possible : une page Wiki, une feuille de calcul, ou une page générée. La beauté n'est pas un critère : la lecture en rituel l'est.
4. (40 min) Première lecture en rituel : le tableau est lu comme il sera lu chaque semaine. Qui parle ? Dans quel ordre ? Qu'est-ce qui déclenche une discussion et qu'est-ce qui est constaté en silence ?
5. (10 min) Convention : fréquence de mise à jour, responsable, et règle de retrait (un signal qui ne déclenche rien pendant quatre semaines sort du tableau).

**Pièges :**
- Le tableau est beau mais ne dit rien. Chaque ligne doit avoir un seuil et une action, sinon c'est de la décoration.
- La mise à jour manuelle est présentée comme provisoire et devient définitive. Écrivez la date de revue de la provision.
- Le tableau remplace la conversation. Non : il l'ouvre. Si le rituel lit le tableau en silence et se termine, le tableau est un alibi.

**Variante :** le tableau de bord est construit par un binôme de l'équipe (pas par le facilitateur), ce qui garantit qu'au moins deux personnes savent le maintenir.

## Fiche 5.1 : Diagnostic sans illusion niveau 2 (2 h)

**Intention :** faire un état des lieux honnête des modèles, de l'automatisation et de la documentation, sans langue de bois et sans chasse aux coupables.

**Matériel :** les modèles, les résultats d'automatisation, les pages de documentation, des cartes ou post-its.

**Déroulé :**
1. (15 min) Cadrage : ce diagnostic n'est pas un procès. On regarde les systèmes, pas les personnes. Chaque blocage est nommé avec le système en cause.
2. (30 min) Tour de la modélisation : chaque membre répond : « quel modèle n'avez-vous pas touché depuis deux semaines ? pourquoi ? » Les réponses sont écrites, pas discutées.
3. (30 min) Tour de l'automatisation : combien de tests générés passent ? échouent ? depuis quand ? Les échoués depuis plus de deux semaines sont marqués comme dérive.
4. (30 min) Tour de la documentation : quelles pages sont synchronisées ? lesquelles vivent leur propre vie ?
5. (15 min) Classement : chaque blocage est classé par système (outil, processus, compétence, temps, décision) et le tableau est photographié puis publié.

**Pièges :**
- Le diagnostic devient un échange d'excuses. La consigne : une cause, pas une excuse. « Le modèle est obsolète parce que X n'a pas eu le temps » → système : temps alloué à la maintenance.
- Le coach classifie seul à la fin. Non : l'équipe classifie ensemble, le coach photographie.
- Rien n'est écrit après l'atelier. Le tableau non publié est un diagnostic qui n'a pas eu lieu.

**Variante :** le diagnostic se fait par écrit d'abord (chacun remplit le questionnaire seul), puis la plénière confronte. C'est plus honnête : à l'oral, la politesse filtre.

## Fiche 5.2 : Remontage au sponsor avec preuves (1 h 30)

**Intention :** transformer les blocages en demandes structurées avec preuve, impact et destinataire. Une demande orale à un sponsor occupé n'existe pas.

**Matériel :** le tableau des blocages (fiche 5.1), un modèle de demande en quatre champs.

**Déroulé :**
1. (20 min) Sélection : parmi les blocages, quels sont ceux qui exigent une décision hors de l'équipe ? Les autres restent sous responsabilité d'équipe.
2. (40 min) Rédaction des demandes : pour chaque blocage retenu — la preuve (capture, métrique, temps perdu, incident), l'impact (sur la livraison ou la qualité), le destinataire (qui peut débloquer), la demande (une phrase).
3. (30 min) Répétition du remontage : le porte-parole présente chaque demande en deux minutes. Le sponsor répond par écrit à chacune : accordé / refusé / reporté, avec la raison et la date.

**Pièges :**
- Les demandes sont des doléances. Une demande sans preuve ni impact est une doléance : elle sera ignorée, et ce sera mérité.
- Le sponsor répond « on verra ». Refusez : la réponse est accordé / refusé / reporté, avec date. « On verra » est un report sans date, donc un refus déguisé.
- Le coach remonte lui-même les demandes. Non : c'est l'équipe qui remonte. Le coach qui remonte crée une dépendance.

**Variante :** le remontage se fait par écrit (un document d'une page par demande) et la réunion ne sert qu'aux réponses. Plus efficace pour un sponsor à agenda serré.

## Fiche 7.1 : Matrice de couverture par types de test (3 h)

**Intention :** rendre la couverture visible et honnête : quels types de test existent, sur quels flux, avec quelles preuves. La matrice est un instrument de vérité, pas un rapport de conformité.

**Matériel :** la liste des types de test (unitaire, intégration, système, performance, sécurité, accessibilité, etc.), les flux critiques des modèles, les preuves d'exécution.

**Déroulé :**
1. (20 min) Définir les types de test pertinents pour l'équipe (pas la liste complète du monde : la liste de l'équipe).
2. (40 min) Construire la matrice : lignes = types de test, colonnes = flux critiques. Chaque case : une des quatre valeurs — fait avec preuve / fait sans preuve / pas fait, décidé / pas fait, non décidé.
3. (60 min) Remplir la matrice honnêtement. Les cases « fait sans preuve » et « pas fait, non décidé » sont les plus instructives : ce sont les angles morts.
4. (40 min) Décider de trois cases à changer d'ici la fin du niveau 2 : soit construire la preuve, soit faire le test, soit assumer le non-fait par écrit avec la raison.
5. (20 min) Publier la matrice et prévoir sa revue : une matrice non relue devient une décoration.

**Pièges :**
- La matrice devient un rapport de conformité où tout est vert. La valeur est dans les cases honnêtes, pas dans le vert.
- Trop de types de test. La liste de l'équipe, pas celle du référentiel : cinq types réels valent mieux que quinze théoriques.
- La matrice n'est reliée à aucune exécution. Une ligne de matrice sans preuve d'exécution est une déclaration, pas une mesure.

**Variante :** la matrice est remplie par sous-groupes (un sous-groupe par flux), puis confrontée. Les désaccords entre sous-groupes révèlent qui sait quoi.

## Fiche 8.1 : Audit de maturité niveau 2 (3 h)

**Intention :** auditer les sept éléments de niveau 2 avec preuves, sans indulgence et sans autocensure. L'audit est la matière première du rapport de maturité.

**Matériel :** la grille d'auto-évaluation des sept éléments (partie 4), les artefacts publiés au centre d'excellence, les tableaux de bord.

**Déroulé :**
1. (20 min) Cadrage : l'échelle est 1 (absent), 2 (présent mais fragile), 3 (installé). Une note sans preuve vaut zéro.
2. (60 min) Élément par élément : l'équipe note, puis confronte les notes individuelles. Les écarts de deux points ou plus entre membres sont discutés : là où l'équipe se voit différemment, il y a un problème de réalité partagée.
3. (40 min) Collecte des preuves : pour chaque note de 3, pointer l'artefact réel. Un élément sans artefact retombe à 2.
4. (40 min) Nommer les deux faiblesses : les deux éléments les plus bas, sans filtre, avec un plan de correction minimal (action, responsable, date).
5. (20 min) Photographie de fin : la grille remplie est publiée. Elle sera comparée à la grille de J+30.

**Pièges :**
- L'audit devient une cérémonie de satisfaction. Les faiblesses nommées sans filtre sont la partie la plus précieuse : protègez-les de l'auto-promotion.
- Les preuves sont des affirmations. « On fait du MBT » n'est pas une preuve ; le modèle et les tests générés le sont.
- L'audit est fait seul par le coach. Non : l'équipe audite, le coach garantit la méthode.

**Variante :** l'audit croisé : une équipe voisine audite l'équipe pilote avec la même grille, et réciproquement. Le regard externe est le meilleur antidote à l'indulgence.

## Le registre des fiches

Chaque fiche utilisée est annotée après l'animation : ce qui a marché, ce qui a déraillé, le temps réel par rapport au temps prévu, et une suggestion d'amélioration. Le registre des fiches vit dans le centre d'excellence. Après trois animations d'une même fiche, le facilitateur relit les annotations et fait évoluer la fiche : une fiche d'animation qui ne change jamais est une fiche morte.

| Fiche | Utilisée le | Temps réel | Ce qui a marché | Ce qui a déraillé | Modification proposée |
| --- | --- | --- | --- | --- | --- |
| 1.1 | | | | | |
| 1.2 | | | | | |
| 1.3 | | | | | |
| 2.1 | | | | | |
| 2.2 | | | | | |
| 3.1 | | | | | |
| 3.2 | | | | | |
| 4.1 | | | | | |
| 4.2 | | | | | |
| 5.1 | | | | | |
| 5.2 | | | | | |
| 7.1 | | | | | |
| 8.1 | | | | | |

**Règle :** le registre est rempli le jour même de l'atelier, en cinq minutes, par l'animateur. Un registre rempli « plus tard » n'est jamais rempli.
