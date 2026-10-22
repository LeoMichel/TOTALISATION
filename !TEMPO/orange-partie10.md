
---

# Partie 10 : Les cérémonies du niveau 2

Cette partie adapte les sept cérémonies de TOTALISATION au niveau 2 : les rituels du niveau 1 deviennent des cérémonies modélisées, outillées et systématiques. Chaque cérémonie garde son objectif et ses participants — elle gagne des modèles, des entrées/sorties reliées, et des preuves automatisées.

**La règle du niveau 2 :** une cérémonie n'est pas outillée tant que sa version du niveau 1 ne tient pas sans le facilitateur. L'outillage amplifie ce qui existe ; il ne remplace pas ce qui manque.

## Cérémonie 1 : L'ÉLICITATION modélisée

**Ce que le niveau 2 ajoute :** l'élicitation n'est plus une conversation libre guidée par des questions standard ; elle est structurée par le modèle du domaine. Le demandeur décrit son besoin devant le modèle existant — et les malentendus deviennent visibles sur le diagramme, pas seulement dans les reformulations.

**Le déroulé du niveau 2 (60 minutes) :**

1. **La lecture du modèle du domaine** (10 min) : le facilitateur montre où la nouvelle demande touche le modèle existant. Le demandeur voit le contexte — pas une page blanche.
2. **Le récit du demandeur** (15 min) : le demandeur raconte son besoin en suivant le modèle — « j'arrive ici, je voudrais faire cela ». Les chemins qui n'existent pas dans le modèle apparaissent : ce sont les extensions à modéliser.
3. **Les questions structurées par le modèle** (20 min) : chaque passerelle du modèle proche génère une question (« que fait-on si... ? »). Les cas limites du niveau 1 deviennent les branches non empruntées du modèle — le modèle montre ce qui n'a pas encore de règle.
4. **La mise à jour du modèle** (15 min) : le modèle est étendu en séance, sous les yeux du demandeur. La spécification suivante héritera de cette structure.

**Les entrées obligatoires :** le modèle du domaine à jour (sinon : mise à jour préalable), la demande brute, le demandeur réel.

**Les sorties attendues :** le modèle du domaine mis à jour et daté, le besoin reformulé sur le modèle, la liste des branches sans règle (à traiter en spécification).

**Le piège du niveau 2 :** le modèle qui remplace le demandeur. Le modèle éclaire l'élicitation, il ne la remplace pas : la question « quel problème cela résout-il ? » reste la source. Un modèle sans demande réelle est un exercice de style.

**Le lien avec le niveau 1 :** les cinq questions standard de l'élicitation du niveau 1 restent valables — le modèle les rend visuelles. « Qu'avez-vous déjà essayé ? » devient : « montrez-moi où vous avez essayé, dans le modèle ».

## Cérémonie 2 : LA DÉFINITION modélisée

**Ce que le niveau 2 ajoute :** la spécification n'est plus un document libre ;rivée du modèle. Chaque passerelle devient un cas, chaque chemin une règle SI/ALORS, chaque événement une frontière à tester.

**Le déroulé du niveau 2 (90 minutes) :**

1. **La lecture du modèle cible** (10 min) : le périmètre de la demande est mis en évidence sur le modèle (surlignage, filtre).
2. **La génération des règles** (30 min) : pour chaque chemin actif du périmètre, la règle SI/ALORS est écrite. Le modèle garantit la couverture : ce qui est dans le modèle doit être dans la spécification — sinon, pourquoi est-il modélisé ?
3. **La chasse aux cas limites par le modèle** (30 min) : les passerelles non couvertes par les règles sont les cas limites oubliés. Le modèle raisonne systématiquement — c'est son rôle.
4. **La revue à trois rôles contre le modèle** (20 min) : le développeur vérifie l'implémentabilité du modèle (pas seulement de la spécification), le testeur vérifie la testabilité de chaque chemin, le demandeur valide la fidélité.

**Les entrées obligatoires :** le modèle à jour (cérémonie 1), la capacité de l'équipe, le demandeur accessible.

**Les sorties attendues :** la spécification liée au modèle (référence et révision), les critères de validation couvrant chaque chemin actif, les cas limites issus des passerelles.

**Le piège du niveau 2 :** la spécification qui copie le modèle verbatim. Le modèle dit comment le système fonctionne ; la spécification dit ce qui doit être vérifié. La traduction (chemin → règle testable) reste un travail humain — le modèle le structure, il ne le remplace pas.

**Le lien avec le niveau 1 :** la revue à trois rôles du niveau 1 reste la règle. Ce qui change : les relecteurs ont le modèle pour arbitrer — la divergence de lecture se règle sur le diagramme, pas sur l'autorité.

## Cérémonie 3 : LA PLANIFICATION reliée

**Ce que le niveau 2 ajoute :** le plan est relié aux modèles. Chaque élément planifié pointe vers son modèle, son état de spécification, ses preuves attendues. Le plan devient vérifiable : chaque ligne a sa colonne de preuve.

**Le déroulé du niveau 2 (90 minutes) :**

1. **La revue du plan lié** (20 min) : chaque élément du plan est relu avec son modèle et son état (modélisé / spécifié / prouvé). Les éléments « non modélisés » sont nommés comme tels — c'est une catégorie du plan, pas un aveu.
2. **La validation des prérequis** (20 min) : pour chaque élément à démarrer, le modèle est-il confronté ? La spécification est-elle dérivée ? Les données de test existent-elles ? Le DoR du niveau 2 est modélisé.
3. **Le contrat d'itération** (30 min) : comme au niveau 1, mais chaque engagement référence ses preuves attendues — tests générés, documentation mise à jour, modèle révisé.
4. **Les risques modélisés** (20 min) : les risques du niveau 1 sont enrichis : quel chemin du modèle est le plus fragile ? Quelle passerelle n'a jamais été testée ? Le modèle guide la chasse aux risques.

**Les entrées obligatoires :** les modèles à jour, les spécifications dérivées, la capacité réelle.

**Les sorties attendues :** le plan où chaque ligne pointe vers modèle, spécification et preuves ; le contrat d'itération avec références ; les risques classés par fragilité de modèle.

**Le piège du niveau 2 :** le plan décoré de références. Une ligne du plan qui « référence » un modèle non confronté est une ligne du niveau 1 avec un autocollant. La référence exige la confrontation : c'est la date de la dernière divergence trouvée qui prouve que le modèle est vivant.

**Le lien avec le niveau 1 :** la règle « pas de spécification, pas d'itération » devient « pas de modèle confronté, pas d'itération ». La rigueur monte d'un cran ; elle est vérifiable par les mêmes méthodes (dates, historiques).

## Cérémonie 4 : L'IMPLÉMENTATION outillée

**Ce que le niveau 2 ajoute :** la revue de conformité est outillée par les tests générés du modèle. Le développeur code avec la spécification ouverte ET le modèle ; le relecteur dispose des tests générés pour valider les chemins.

**Le déroulé du niveau 2 (30 minutes, comme au niveau 1, mais outillé) :**

1. **La conformité au modèle** (10 min) : le code est relu contre le modèle (les passerelles implémentées), pas seulement contre la spécification. Un chemin du modèle sans code est un manque ; un code sans chemin du modèle est un comportement non modélisé (à modéliser ou à retirer).
2. **Les tests générés** (10 min) : les tests dérivés du modèle tournent-ils ? Lesquels échouent ? Un échec de test généré est une divergence modèle/code — exactement ce que la revue cherche.
3. **La mise à jour du modèle** (10 min) : si le code révèle un comportement non modélisé, le modèle est mis à jour en séance (ou le ticket de mise à jour est créé avec date). Le modèle suit le code — jamais l'inverse en silence.

**Les entrées obligatoires :** le code, le modèle à jour, les tests générés exécutables.

**Les sorties attendues :** le code approuvé avec preuve de conformité au modèle, les tests générés passés (ou dérogés par écrit), le modèle synchronisé.

**Le piège du niveau 2 :** les tests générés considérés comme la vérité. Les tests générés sont fidèles au modèle — si le modèle est faux, ils sont faux avec confiance. La revue humaine reste la source : les tests générés sont le filet, pas le juge.

**Le lien avec le niveau 1 :** la lecture « pour la maintenabilité » du niveau 1 reste intégrale. L'outillage ajoute la conformité systématique ; il ne dispense jamais du jugement.

## Cérémonie 5 : LA DIFFUSION — le Go/No-Go N2

**Ce que le niveau 2 ajoute :** la grille s'enrichit des critères du niveau 2 : modèles à jour, tests générés exécutés, documentation synchronisée, usage de l'IA conforme aux règles.

**Le déroulé du niveau 2 (30 minutes, le format ne s'allonge pas) :**

1. **Les critères du niveau 1** (10 min) : revus comme au niveau 1 — avec leurs preuves.
2. **Les critères du niveau 2** (10 min) : modèle à jour (date de dernière confrontation), tests générés (exécutés, résultat), documentation (synchronisation vérifiée), IA (usages tracés et validés).
3. **La décision** (10 min) : Go / Go avec réserves / No-Go. Les réserves du niveau 2 nomment la divergence et son propriétaire (« le modèle BPM-004 est en retard d'une révision ; mise à jour par L.T. avant vendredi »).

**Les entrées obligatoires :** toutes les preuves du niveau 1, plus les preuves N2 (historique des modèles, rapports de génération, registre IA).

**Les sorties attendues :** la décision avec les réserves N2, le compte rendu, et la mise à jour du tableau de bord N2.

**Le piège du niveau 2 :** le Go/No-Go qui devient un audit de conformité de 2 heures. Le format 30 minutes tient : les preuves sont automatisées (rapports liés), la discussion porte sur les décisions, pas sur la collecte. Si la collecte prend le dessus, l'outillage est défaillant — corrigez l'outillage.

**Le lien avec le niveau 1 :** la règle du niveau 1 reste entière : les critères sont écrits avant, les preuves présentées pendant, les réserves formulées après. Le niveau 2 ajoute des critères, il ne change pas la grammaire de la décision.

## Cérémonie 6 : LA CONFIRMATION reliée

**Ce que le niveau 2 ajoute :** la confirmation confronte l'usage réel au modèle — pas seulement aux critères de succès. Les usages imprévus observés sont des chemins absents du modèle : ils l'enrichissent.

**Le déroulé du niveau 2 (45 minutes) :**

1. **Les critères de succès** (10 min) : comme au niveau 1 — confrontés au réel.
2. **La découverte des usages** (20 min) : comment les utilisateurs utilisent réellement la fonctionnalité. Chaque usage imprévu est un chemin qui manquait au modèle — noté comme extension candidate.
3. **L'enrichissement du modèle** (15 min) : les usages imprévus confirmés sont ajoutés au modèle (en séance si possible). Le modèle apprend du réel — c'est la grande boucle au niveau 2 : CONFIRMER alimente le MODÈLE, qui alimente la prochaine ÉLICITATION.

**Les entrées obligatoires :** les critères de succès de l'élicitation, le modèle livré, des utilisateurs réels accessibles.

**Les sorties attendues :** la confirmation des critères, les extensions candidates du modèle, la mise à jour datée.

**Le piège du niveau 2 :** la confirmation qui vérifie le modèle au lieu du besoin. Le demandeur ne sait pas lire votre modèle — il sait utiliser son outil. La confrontation reste dans son langage : ce qu'il fait, ce qu'il obtient, ce qui le surprend.

**Le lien avec le niveau 1 :** la grande boucle du niveau 1 (CONFIRMER → ÉLICITER) est enrichie d'une étape : CONFIRMER → MODÈLE → ÉLICITER. Le modèle est devenu la mémoire active du besoin — c'est son rôle profond.

## Cérémonie 7 : LA QUALIMÉTRIE N2

**Ce que le niveau 2 ajoute :** le tableau de bord passe d'une métrique à un système de signaux avec seuils et décideurs ; chaque signal est relié à son modèle et à ses preuves.

**Le déroulé du niveau 2 (20 minutes) :**

1. **La lecture des signaux** (10 min) : chaque signal est lu avec sa valeur, sa tendance, son seuil — et sa référence (où la donnée vient-elle, qui peut la vérifier).
2. **Les décisions** (10 min) : chaque signal rouge (ou au vert depuis trop longtemps — les seuils se resserrent) reçoit sa décision : action, propriétaire, levée. Notée au registre pendant la séance.

**Les entrées obligatoires :** le tableau de bord alimenté (automatiquement autant que possible), le registre des décisions ouvert.

**Les sorties attendues :** les décisions notées, les ajustements de seuils, les escalades si nécessaire.

**Le piège du niveau 2 :** le tableau de bord de 15 signaux. Le niveau 2 vit avec 5 à 7 signaux. Chaque signal supplémentaire dilue la lecture — ajoutez un signal seulement si un autre quitte (la règle de la rotation des signaux).

**Le lien avec le niveau 1 :** la métrique unique du niveau 1 a fait ses preuves ; le niveau 2 l'enrichit sans la remplacer. Les nouveaux signaux viennent des nouveaux risques (divergences doc/modèle, tests flaky, usage IA) — chacun justifié par un incident ou une inquiétude réelle.

## Le test des cérémonies du niveau 2

Le test à trois questions du niveau 1 est enrichi de trois questions propres au niveau 2 :

4. **Est-elle reliée aux modèles ?** (Les entrées et sorties de la cérémonie pointent vers des modèles vivants.)
5. **Ses preuves sont-elles automatisées ?** (La collecte ne dépend plus de la mémoire de quelqu'un.)
6. **Ses livrables enrichissent-ils les modèles ?** (La cérémonie nourrit le système — pas seulement le compte rendu.)

Ces six questions sont le test de passage au niveau 3 : une cérémonie qui les réussit toutes est prête à être forgée en processus ; une cérémonie qui échoue encore aux questions 1-3 doit d'abord devenir réelle au sens du niveau 1.
