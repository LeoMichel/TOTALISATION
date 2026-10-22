
---

# Partie 8 : Les exercices avancés E7-E12, FAQ et anti-patterns du niveau 4

## Les exercices avancés

### E7 — Le choix des métriques de résultat

**Durée :** 90 minutes. **Format :** atelier de décision collective, avec les données historiques de l'équipe.

L'équipe part des quatre mesures de résultat standard (délai total, taux de retour, stabilité post-livraison, disponibilité de capacité) et les adapte à son contexte : une équipe de support remplacera « délai de traitement de demande » par « délai de résolution d'incident », et ajoutera « récurrence d'incidents ». L'exercice n'est pas de choisir dans une liste : c'est de définir, pour chaque mesure, ce qu'elle révèle, ce qu'elle peut masquer, et quelle est sa mesure-miroir.

La sortie : quatre mesures de résultat adaptées, chacune avec sa définition précise (quand commence-t-on à compter ? où s'arrête-t-on ?), sa mesure-miroir, et son risque d'abus documenté. Une mesure sans risque d'abus documenté est une mesure qui n'a pas été pensée.

### E8 — La chasse aux mesures d'activité

**Durée :** 60 minutes. **Format :** atelier de nettoyage, avec l'inventaire des mesures existantes.

L'équipe liste toutes les mesures qu'elle a jamais tenues (y compris celles abandonnées), les classe en deux colonnes (activité / résultat), et pose pour chaque mesure d'activité la question de la suppression : « que perd-on si on l'arrête demain ? ». Si la réponse est « rien » ou « le confort de quelques personnes », elle est supprimée sur-le-champ — le confort d'un tableau à lire n'est pas une raison de collecter.

La règle de sortie : chaque mesure d'activité restante doit justifier son existence par une corrélation documentée avec un résultat (ex. : « le nombre de revues corrèle avec le taux de retour si le seuil est à 3 »). Une corrélation non documentée est une superstition chiffrée.

### E9 — La mesure-miroir en action

**Durée :** 90 minutes. **Format :** atelier de simulation, avec les mesures choisies en E7.

L'équipe simule six mois de mesure fictive (des données inventées mais réalistes) dans laquelle une personne (inventée) optimise pour la mesure sans servir le résultat : re-classifications de demandes, découpages artificiels, priorités inversées. L'exercice demande à l'équipe de détecter la triche avec ses mesures-miroirs — et le débrief révèle les miroirs qui fonctionnent et les angles morts qui restent.

La sortie : chaque mesure-miroir testée, corrigée, et le gabarit de détection de triche documenté (quels patterns, quelles mesures, quelles questions). La triche n'est pas un scénario imaginaire : c'est une réponse humaine prévisible à une pression humaine mal placée — et la mesure-miroir est la protection structurelle.

### E10 — Le tableau de bord comme rituel : la revue de 30 minutes

**Durée :** 30 minutes réelles, répétées. **Format :** le rituel de lecture du tableau, avec le gabarit.

L'équipe définit le gabarit de sa revue de tableau : l'ordre de lecture (résultats d'abord, signaux ensuite), la question standard pour chaque métrique (« dérive ou normal ? »), la règle de décision (une dérive confirmée = une décision avec décideur et levée). Le rituel est chronométré : 30 minutes maximum, sinon le tableau a trop de mesures (rotation).

La sortie : le gabarit de revue documenté (une page), testé sur trois revues réelles. La métrique de réussite du gabarit : chaque revue produit au moins une décision — une revue sans décision est un café avec des chiffres.

### E11 — La corrélation signal → résultat

**Durée :** 2 heures. **Format :** atelier d'analyse, avec trois mois de données réelles.

L'équipe aligne ses signaux d'équipe (divergences, flaky, dérogations — N3) et ses résultats (délai, retour, stabilité — N4) sur la même chronologie, et cherche les corrélations : est-ce qu'une dérive des signaux précède une dérive des résultats ? De combien de temps ? Quels signaux sont les meilleurs prédicteurs ?

La sortie : la carte des corrélations documentée (les signaux qui prédisent, ceux qui confirment, ceux qui ne servent à rien). Cette carte est l'intelligence du tableau : elle transforme les signaux en système d'alerte précoce — et les signaux non corrélés sont les premiers candidats à la rotation (sortie).

### E12 — L'audit de mesure du niveau 4

**Durée :** 90 minutes. **Format :** le rituel trimestriel du VERT.

L'équipe audite son système de mesure complet : les mesures sont-elles toujours les bonnes (E7-E8) ? Les miroirs fonctionnent-ils (E9) ? Le rituel de revue tient-il (E10) ? Les corrélations sont-elles à jour (E11) ? Et la question finale : « si on arrêtait de mesurer demain, qu'est-ce qui se dégraderait en premier ? » — la réponse identifie ce que la mesure protège réellement.

La sortie : le rapport d'audit (les mesures confirmées, celles modifiées, celles supprimées, celles ajoutées), et la décision sur la poursuite du niveau de mesure. Un audit qui ne supprime jamais rien n'a pas été honnête — le nettoyage est la preuve de la vitalité.

## La FAQ du niveau 4

**Q : combien de mesures au maximum ?**
R : Le tableau N4 vit avec 6 à 8 : les 4 de résultat + les 2-4 signaux les mieux corrélés. Chaque mesure ajoutée exige qu'une autre sorte. Un tableau à 15 mesures est un rapport annuel déguisé en rituel hebdomadaire — personne ne le lit vraiment, et les décisions se prennent ailleurs.

**Q : peut-on mesurer la qualité sans mesurer la quantité ?**
R : Le niveau 4 mesure des résultats (délai, retour, stabilité, disponibilité) — qui sont des mélanges de qualité et de quantité par construction. La qualité seule (ex. : le taux de bugs par ligne) est mesurable mais demande un dénominateur qui compte — et le dénominateur ramène la quantité. La vraie réponse : mesurez le résultat perçu (retour, stabilité), pas la cause présumée (bugs par ligne).

**Q : que faire quand les données sont indisponibles ou peu fiables ?**
R : Trois niveaux de réponse : (1) collecter à la main temporairement, avec la date de fin de la collecte manuelle écrite (sinon elle devient permanente) ; (2) mesurer le substitut le plus proche et documenter l'approximation ; (3) si les données ne peuvent pas exister, ne pas mesurer — et documenter le renoncement (comme l'équipe legacy du vécu). Une mesure approximative documentée vaut mieux qu'une absence cachée par une mesure fictive.

**Q : la mesure-miroir, comment la choisir quand on débute ?**
R : La méthode simple : demandez « comment pourrait-on améliorer cette mesure sans améliorer le résultat ? » — la réponse est la triche probable, et la mesure-miroir est ce qui la détecterait. Exemples : délai de traitement → re-classifications ; taux de bugs résolus → taux de ré-ouverture ; vitesse de livraison → stabilité post-livraison. La triche est humaine, donc prévisible : la miroir est sa détection prévue.

**Q : les mesures de résultat, ne sont-elles pas tardives (on ne les voit qu'après) ?**
R : C'est pourquoi le niveau 4 garde les signaux d'équipe (N3) : les signaux sont précoces (ils dévient avant), les résultats sont véridiques (ils disent la vérité après). La combinaison est le système : les signaux alertent tôt, les résultats confirment tard — et la corrélation (E11) calibre l'alerte. Un système avec un seul type de mesure est soit aveugle tôt, soit trompeur tard.

**Q : comment éviter que le tableau de bord devienne un outil de management contre l'équipe ?**
R : La règle de gouvernance du tableau : il est alimenté par l'équipe, relu par l'équipe en rituel, et partagé au management en synthèse (les tendances, pas les détails individuels). Une mesure individuelle (la vélocité de untel) est un anti-pattern VERT : elle crée la compétition interne, détruit la collaboration, et mesure l'activité (voir le vécu). Le tableau est collectif, ou il n'est pas.

## Les anti-patterns du niveau 4

### AP-N4-1 : Le tableau de couloir
Les mesures affichées en continu (écran dans le couloir, widget sur la page d'accueil). **Signal :** les comportements changent en fonction de l'affichage, pas en fonction du résultat. **Contre-mesure :** la règle du vécu K.L. — les mesures sont discutées au rituel, jamais affichées en continu. L'affichage crée la pression ; le rituel crée la conversation.

### AP-N4-2 : La collection de mesures
Le tableau grossit chaque trimestre (une mesure ajoutée pour chaque préoccupation nouvelle, rien ne sort jamais). **Signal :** la revue de tableau dépasse 45 minutes, certaines mesures n'ont pas été regardées depuis 2 mois. **Contre-mesure :** la rotation obligatoire : chaque ajout = une sortie. Et l'audit E12 qui supprime les mesures non corrélées.

### AP-N4-3 : La mesure punitive
Une mesure utilisée en évaluation individuelle (« ta vélocité est en baisse »). **Signal :** les gens cachent les mauvaises semaines, les demandes sont découpées, l'entraide disparaît. **Contre-mesure :** la règle du tableau collectif — les mesures individuelles n'existent pas au tableau (elles existent dans le coaching, qui n'est pas une mesure). Un tableau punitif détruit exactement ce qu'il prétend améliorer.

### AP-N4-4 : La mesure sans levée
Une dérive détectée, une discussion eue, aucune décision notée — et la dérive continue. **Signal :** le registre des décisions du tableau est vide ou ancien. **Contre-mesure :** la règle du niveau 3 transportée : chaque dérive confirmée = décision + décideur + levée. Une dérive sans levée est une dérive acceptée — et si elle est acceptée, le seuil doit être re-calibré honnêtement (c'est une décision, pas une dérive).

### AP-N4-5 : La corrélation fantôme
Le praticien affirme qu'un signal prédit un résultat, sans l'avoir vérifié (« les divergences prédisent les retours, tout le monde le sait »). **Signal :** la carte des corrélations (E11) n'existe pas, ou est datée de plus d'un trimestre. **Contre-mesure :** l'exercice E11 sur données réelles, refait chaque trimestre. Une corrélation non vérifiée est une croyance — elle peut être vraie, mais elle n'est pas une connaissance.

### AP-N4-6 : Le renoncement non documenté
L'équipe arrête de mesurer (fatigue, indisponibilité des données) sans documenter pourquoi. **Signal :** des trous dans la chronologie des mesures, des rituels de tableau sautés en silence. **Contre-mesure :** la règle du vécu S.B. : le renoncement est une décision argumentée et documentée (ce qu'on ne mesure pas, pourquoi, ce qui le remplacerait). Le silence sur la mesure est une dérive de la mesure.

## La situation difficile du niveau 4 : quand les mesures contredisent l'intuition

**La situation.** L'équipe mesure le délai total et le taux de retour depuis un trimestre. Les mesures disent : délai stable, retour en baisse — tout va bien. Et pourtant, l'équipe ressent le contraire : les journées sont plus dures, les urgences plus fréquentes, la fatigue réelle. Les mesures disent « ça va », l'équipe dit « ça ne va pas ».

**Le diagnostic.** Le praticien N4 doit considérer que l'intuition de l'équipe est une donnée — pas une opinion. Trois hypothèses à tester : (1) les mesures mesurent le flux des demandes, mais pas la charge émotionnelle ou la variabilité (des demandes stables en nombre mais imprévisibles en nature fatiguent différemment) ; (2) les mesures manquent une dimension (la complexité moyenne des demandes a peut-être augmenté sans que le délai ne bouge) ; (3) les mesures sont bonnes mais la période de comparaison est trompeuse (le trimestre de référence était anormalement dur, et « stable » signifie « toujours dur »).

**La correction.** Ajouter la mesure manquante : la charge perçue (une enquête d'équipe, 3 questions, chaque mois) comme mesure-miroir des mesures objectives. Et l'analyse de complexité : classer les demandes du trimestre par complexité réelle, et voir si la moyenne a bougé. Dans la plupart des cas, les mesures objectives étaient justes mais incomplètes : la charge était réelle, la complexité avait augmenté, et le « délai stable » cachait « délai stable malgré plus de complexité » — ce qui est une amélioration invisible, ou une montée de fatigue réelle.

**La leçon :** le praticien N4 prend l'intuition de l'équipe au sérieux — pas comme une vérité, mais comme une donnée qui demande une investigation. Les mesures objectives ne capturent pas tout ; la dissonance entre les chiffres et le ressenti est elle-même une mesure (de l'angle mort du tableau). L'équipe qui ressent mal alors que les chiffres disent bien, ou l'inverse, a un problème de mesure — pas un problème de perception.
