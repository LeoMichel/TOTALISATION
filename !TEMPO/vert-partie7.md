
---

# Partie 7 : Les cérémonies du niveau 4

Les cérémonies du niveau 3 (cadencées) deviennent au niveau 4 des cérémonies mesurées : chaque rituel produit ses données, chaque donnée alimente le tableau, chaque tableau déclenche une décision. La mesure n'est pas un ajout : elle est la transformation du rituel.

## Cérémonie 1 : L'ÉLICITATION mesurée

**Ce que le niveau 4 ajoute :** l'élicitation produit ses propres métriques — délai d'entrée en file, nombre d'allers-retours de clarification, taux de reformulation correcte du premier coup. Ces métriques révèlent la qualité de l'élicitation elle-même, pas seulement du besoin.

**Le déroulé du niveau 4 (60 minutes, à cadence fixe comme au niveau 3) :**

1. **La revue des métriques d'élicitation** (10 min) : la file d'attente, les allers-retours, le taux de reformulation. Les demandes qui demandent trois allers-retours sont analysées : le gabarit de demande est-il flou ? Le demandeur est-il mal préparé ? Le modèle du domaine a-t-il un trou ?
2. **L'élicitation du jour** (40 min) : le format du niveau 3, avec un ajout — la demande est classée à la fin (simple/complexe/exploratoire) et le classement est noté.
3. **L'amélioration du gabarit** (10 min) : les allers-retours de la semaine nourrissent le gabarit de demande (les questions qui manquent deviennent des champs).

**Les entrées obligatoires :** la file d'attente avec métriques, le modèle à jour, le gabarit de demande en vigueur.

**Les sorties attendues :** le besoin reformulé, le modèle enrichi, la demande classée, le gabarit de demande amélioré si nécessaire.

**Le piège du niveau 4 :** mesurer la vitesse d'élicitation (combien de demandes par semaine). Vite éliciter est souvent mal éliciter — la métrique utile est le taux de reformulation correcte du premier coup, qui mesure la qualité de l'écoute, pas sa vitesse.

**Le lien avec le niveau 3 :** la cadence reste (même heure, même durée). La mesure ne remplace pas le rituel : elle l'alimente — le rituel N4 discute ses propres métriques avant de traiter les demandes.

## Cérémonie 2 : LA DÉFINITION mesurée

**Ce que le niveau 4 ajoute :** les spécifications ont leurs métriques — respect du SLA par classe, taux de revue à trois rôles réussie au premier passage, nombre de cas limites trouvés par passerelle du modèle. La spécification N4 est mesurée à la qualité (pas seulement au délai).

**Le déroulé du niveau 4 (90 minutes, à cadence fixe) :**

1. **La revue des métriques de spécification** (15 min) : SLA par classe, taux de revue du premier coup, cas limites par passerelle. Les spécifications qui passent trois revues sont analysées : auteur inexpérimenté, demande mal classée, ou modèle déficient ?
2. **L'écriture du jour** (45 min) : le format N3, avec les cas limites enrichis par les données du trimestre (les cas limites trouvés en production sont réinjectés comme cas standards).
3. **La sortie mesurée** (30 min) : la spécification prête entre en file avec ses métriques de naissance (temps d'écriture, nombre de revues, cas limites). Ces métriques suivront la demande jusqu'à la confirmation.

**Les entrées obligatoires :** le modèle enrichi, les métriques de spécification du trimestre, les cas limites de production (réinjectés).

**Les sorties attendues :** la spécification complète avec ses métriques de naissance, les critères de validation, la classe de SLA confirmée.

**Le piège du niveau 4 :** mesurer les cas limites trouvés (nombre). Une spécification avec 12 cas limites n'est pas meilleure qu'une avec 4 : elle est peut-être plus complexe, ou l'auteur cherche du volume. La métrique utile : les cas limites trouvés en production qui auraient pu être anticipés — c'est la qualité de l'anticipation, pas la quantité du brainstorming.

**Le lien avec le niveau 3 :** le SLA par classe reste. La mesure de qualité (revue du premier coup, anticipation des cas limites) s'ajoute au délai — les deux sont nécessaires, l'une sans l'autre est tronquée.

## Cérémonie 3 : LA PLANIFICATION mesurée

**Ce que le niveau 4 ajoute :** la planification confronte ses prédictions au réel : le contrat d'itération promettait X, le réel a livré Y — l'écart est analysé à chaque cycle. La capacité apprise (niveau 3) devient la capacité mesurée (niveau 4).

**Le déroulé du niveau 4 (60 minutes, métronome) :**

1. **La revue du cycle précédent** (15 min) : promis vs livré, avec l'analyse des écarts. Les écarts systématiques (toujours 20 % trop optimiste) sont corrigés dans le modèle de capacité. Les écarts ponctuels sont documentés avec leur cause.
2. **La revue de capacité mesurée** (10 min) : la capacité réelle des derniers cycles (pas la capacité théorique) guide la sélection.
3. **La sélection et le contrat** (25 min) : le format N3, avec les métriques de naissance des spécifications (une demande qui a pris 3 allers-retours est présumée plus complexe que sa classe).
4. **Les risques et leurs mesures** (10 min) : les risques du registre sont relus avec leurs signaux — un risque sans signal est soit disparu (purgé), soit aveugle (un signal manque).

**Les entrées obligatoires :** les mesures du cycle précédent (promis/livré), la capacité mesurée, les spécifications avec métriques de naissance.

**Les sorties attendues :** le contrat d'itération avec prédictions mesurables, le modèle de capacité corrigé, les risques avec signaux.

**Le piège du niveau 4 :** le modèle de capacité qui devient une formule magique. La mesure améliore l'estimation ; elle ne la remplace pas. L'écart systématique se corrige ; l'écart ponctuel s'assume — et le praticien qui prétend une capacité exacte ment à son équipe.

**Le lien avec le niveau 3 :** le métronome reste. Ce qui change : le métronome est confronté à sa propre musique — chaque battement est comparé à sa promesse.

## Cérémonie 4 : L'IMPLÉMENTATION mesurée

**Ce que le niveau 4 ajoute :** le pipeline produit ses propres métriques : temps de build, taux de premier passage, taux de flaky, temps de détection des régressions. Le code est mesuré à sa vitesse de passage, pas seulement à sa conformité.

**Le déroulé du niveau 4 (30 minutes, outillé comme au niveau 3) :**

1. **La conformité au modèle** (10 min) : comme au niveau 3.
2. **La lecture des métriques du pipeline** (10 min) : temps de build en dérive ? Premier passage en baisse ? Flaky en hausse ? Chaque dérive est un signal (l'environnement, les données, ou les gabarits).
3. **La correction ou l'escalade** (10 min) : les dérives du pipeline sont traitées comme les dérives du produit — avec décideur, action, levée. Un pipeline dégradé est un produit dégradé : le tableau N4 ne fait pas de différence.

**Les entrées obligatoires :** le code, le modèle, les métriques du pipeline (temps de build, premier passage, flaky, délai de détection).

**Les sorties attendues :** le code approuvé, les dérives du pipeline traitées, le tableau N4 mis à jour.

**Le piège du niveau 4 :** le pipeline optimisé au détriment de la protection. Un pipeline de 2 minutes avec 30 % de flaky est pire qu'un pipeline de 10 minutes avec 2 % de flaky : le premier fabrique du bruit, le second fabrique de la confiance. La mesure du pipeline est au service de la fiabilité, pas de la vitesse seule.

**Le lien avec le niveau 3 :** les trois vitesses du pipeline N3 restent. La mesure ajoute la surveillance de leur santé — le praticien N4 sait que son pipeline est un produit, avec ses propres régressions.

## Cérémonie 5 : LA DIFFUSION mesurée

**Ce que le niveau 4 ajoute :** chaque Go/No-Go nourrit l'historique des décisions : les réserves levées en retard, les critères contournés, les No-Go justifiés a posteriori. La grille N4 apprend de son historique — c'est son forgeage permanent.

**Le déroulé du niveau 4 (30 minutes, au métronome) :**

1. **La revue des décisions passées** (10 min) : les réserves levées à date ? Les contournements détectés ? La grille a-t-elle été contournée par un critère mal placé ? L'historique est l'audit permanent.
2. **Les critères du jour** (15 min) : bloquants et informatifs, avec leurs preuves automatisées et leurs métriques de tendance.
3. **La décision** (5 min) : la décision est notée avec son contexte de mesure (« Go avec 2 réserves, seuil de couverture à 74 %, seuil normal 80 % ») — la décision future pourra juger celle-ci avec les données complètes.

**Les entrées obligatoires :** l'historique des décisions (registre à jour), les preuves automatisées, les tendances.

**Les sorties attendues :** la décision avec contexte mesuré, les réserves, l'historique enrichi.

**Le piège du niveau 4 :** l'historique qui devient une arme. « Vous avez accepté 74 % en septembre » — utilisé pour blâmer est toxique ; utilisé pour apprendre (quelle était la situation ? pourquoi ?) est précieux. La règle : l'historique se relit avec son contexte, jamais hors contexte.

**Le lien avec le niveau 3 :** le métronome et les réserves avec levée restent. La mesure ajoute la mémoire : la grille N4 est un organisme qui apprend, pas un formulaire qui se remplit.

## Cérémonie 6 : LA CONFIRMATION mesurée

**Ce que le niveau 4 ajoute :** les confirmations produisent des métriques d'usage : taux d'adoption, taux de contournement, apprentissages par confirmation, délai de réaction aux usages imprévus. La confirmation N4 est un système de mesure de la satisfaction réelle — pas déclarée.

**Le déroulé du niveau 4 (60 minutes, systématique) :**

1. **Les métriques d'usage** (15 min) : adoption (qui l'utilise vraiment ?), contournement (qui fait autrement ?), rétention (qui continue d'utiliser après un mois ?). Les mesures viennent des données d'usage quand elles existent, de l'observation sinon.
2. **La confrontation aux critères** (20 min) : le format N3 (critères de succès, usages imprévus, enrichissement du modèle).
3. **Le traitement des échecs d'adoption** (25 min) : une fonctionnalité livrée non adoptée est une fonctionnalité ratée — quelle que soit sa conformité technique. Chaque non-adoption est analysée : le besoin était mal élicité ? La fonctionnalité est mal conçue ? L'adoption est mal accompagnée ?

**Les entrées obligatoires :** les métriques d'usage (ou l'observation documentée), les critères de succès, le modèle livré.

**Les sorties attendues :** la confirmation des critères, les métriques d'usage, le traitement des non-adoption (avec destination : élicitation, design, ou accompagnement).

**Le piège du niveau 4 :** la mesure d'adoption par outil seul (les logs de clics). Un log mesure la présence, pas l'usage — un utilisateur peut cliquer partout et être perdu. La mesure complète combine les données (logs) et l'observation (l'exercice E11 inversé) : les deux se corrigent.

**Le lien avec le niveau 3 :** la systématisation reste. Ce qui change : la confirmation N4 mesure le résultat (l'adoption), pas seulement l'activité (la confirmation tenue).

## Cérémonie 7 : LA QUALIMÉTRIE N4

**Ce que le niveau 4 ajoute :** le tableau de bord N4 dépasse les signaux d'équipe : il intègre les mesures de résultat (délai total, retour, stabilité, disponibilité — les quatre du vécu S.B.), et il est relu à cadence fixe avec la règle de la mesure-miroir (chaque métrique a sa contre-mesure d'abus).

**Le déroulé du niveau 4 (30 minutes) :**

1. **La lecture des métriques de résultat** (15 min) : les quatre (délai, retour, stabilité, disponibilité) avec leurs tendances et leurs mesures-miroirs.
2. **La lecture des signaux d'équipe** (10 min) : les signaux N3 (divergences, flaky, dérogations) — reliés aux métriques de résultat (une dérive des signaux précède-t-elle une dérive des résultats ?).
3. **Les décisions** (5 min) : chaque dérive a sa décision, chaque décision a son décideur, chaque levée est vérifiée.

**Les entrées obligatoires :** les métriques de résultat (automatisées quand possible), les signaux d'équipe, les mesures-miroirs.

**Les sorties attendues :** les décisions notées, les corrélations signal→résultat documentées, les escalades.

**Le piège du niveau 4 :** le tableau à 20 métriques. Le niveau 4 vit avec 6 à 8 mesures : les 4 de résultat + les 2-4 signaux d'équipe les plus corrélés. Chaque métrique ajoutée exige qu'une autre sorte — la rotation est ce qui maintient la lecture. Un tableau illisible ne protège rien.

**Le lien avec le niveau 3 :** les signaux N3 restent (ils sont les premiers indicateurs). La mesure de résultat ajoute la vision conséquence : les signaux disent « ça dérive », les résultats disent « ça a réellement un effet » — et la corrélation entre les deux est la vraie intelligence du tableau.

## Le test des cérémonies du niveau 4

Le test à huit questions du niveau 3 gagne deux questions N4 :

9. **Produit-elle ses propres métriques ?** (La cérémonie N4 se mesure elle-même — délai, qualité, adoption.)
10. **Ses métriques ont-elles leurs mesures-miroirs ?** (Chaque métrique a sa contre-mesure d'abus — la loi de Goodhart est prévenue, pas subie.)

Ces dix questions sont le test de passage au niveau 5 : une cérémonie qui les réussit toutes est prête à être gouvernée à l'échelle de l'organisation ; une cérémonie qui échoue encore aux questions de mesure (9-10) doit d'abord mesurer ce qu'elle fait avant de l'étendre.
