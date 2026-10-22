
---

# Partie 16 : Le recueil des exercices — version pratique

Les douze exercices du livre (E1 à E12), rassemblés ici avec leur guide d'utilisation : quand les lancer, avec qui, et quoi en attendre. Cette partie est la page de garde du praticien : elle transforme les exercices d'un livre en programme d'entraînement d'équipe.

## Le programme d'entraînement trimestriel

| Semaine du trimestre | Exercice | Durée | Qui |
|---|---|---|---|
| 1 | E1 (spécification à trois relecteurs) | 90 min | Équipe |
| 2 | E4 (lexique à l'épreuve des nouveaux) | 45 min | Équipe + volontaire externe |
| 3 | E8 (chiffrage du flou — mise à jour) | 60 min | Équipe |
| 4 | E10 (Go/No-Go en aveugle) | 45 min | Équipe + décideur |
| 5 | E2 (la métrique du vendredi — bilan des 4 semaines) | 30 min | Chacun |
| 6 | E11 (confirmation inversée) | 60 min | Équipe + utilisateurs |
| 7 | E7 (le chiffrage des catégories — l'audit croisé) | 90 min | Équipe + pair externe |
| 8 | E12 (l'audit des cérémonies) | 90 min | Équipe |
| 9-12 | Répétition espacée : reprendre les 2 exercices qui ont le plus révélé | variable | — |

Ce programme est un rythme par défaut. L'adaptation est normale ; l'abandon du programme (les exercices « quand on aura le temps ») est le symptôme classique de la régression silencieuse.

## Les fiches d'exercices détaillées

### E1 — La spécification à trois relecteurs

**Objectif d'apprentissage :** mesurer l'ambiguïté réelle d'une spécification par la divergence des lectures.

**Protocole :** la spécification est envoyée à trois relecteurs séparément. Chacun répond à trois questions par écrit : « qu'est-ce que je dois construire/vérifier/accepter ? », « qu'est-ce qui n'est pas clair ? », « qu'est-ce qui me semble manquer ? ». Les réponses sont comparées en séance, sans préparation croisée.

**L'analyse des divergences :**
- Divergence de comportement (les trois comprennent des comportements différents) : le plus grave — correction immédiate de la spécification, entrée au lexique.
- Divergence de priorité (même compréhension, priorités différentes) : signal de flou sur le critère de tri — à traiter avec la fiche de bug.
- Divergence de vocabulaire (même chose, mots différents) : entrée au lexique, la plus facile à corriger.

**Le piège :** faire la confrontation en réunion avec discussion préalable. La confrontation à froid est tout l'exercice : une fois discuté, chacun s'aligne et l'ambiguïté se cache.

### E2 — La métrique du vendredi

**Objectif d'apprentissage :** calibrer l'intuition collective sur la mesure réelle.

**Protocole :** chaque vendredi avant le point de qualité, chaque membre écrit sa prédiction de la valeur de la métrique (et sa tendance). Après le point, la prédiction est comparée au réel. Quatre semaines de données personnelles sont compilées.

**L'analyse :** les erreurs systématiques sont instructives. Toujours optimiste → l'équipe cache ses difficultés à elle-même. Toujours pessimiste → l'équipe sous-estime ses progrès (fréquent au début du parcours). Dispersion énorme → la métrique n'est pas comprise de la même façon par tous : vérifier sa définition au lexique.

**Le piège :** transformer la prédiction en enjeu de performance (« qui prédit le mieux »). L'exercice mesure la calibration collective, pas la compétence individuelle — c'est un baromètre, pas un concours.

### E7 — L'audit croisé

**Objectif d'apprentissage :** recevoir le regard d'un pair externe sur ses propres rituels — et donner le sien.

**Protocole :** deux équipes (ou deux parties d'équipe) échangent leurs rituels : l'observation d'un Go/No-Go croisé, une spécification relue par l'autre équipe, un point de qualité visité. Chaque partie note : ce qui est différent de chez nous, ce qui nous semble risqué, ce que nous voudrions copier.

**L'analyse :** les trois catégories de notes se traitent différemment. « Différent » documente la variété (pas une faute). « Risqué » déclenche un dialogue (les deux parties expliquent leur choix — une des deux apprend). « À copier » est le compliment le plus concret du niveau 1.

**Le piège :** l'audit-jugement (« chez nous on fait mieux »). La règle de l'échange : on décrit, on questionne, on ne classe pas. Le comparatif est un outil de découverte, pas de compétition.

### E10 — Le Go/No-Go en aveugle

**Objectif d'apprentissage :** distinguer l'affirmation de la preuve dans la présentation des critères.

**Protocole :** le décideur reçoit les conclusions sans les données. Il demande la preuve de tout critère dont il doute. Chaque demande est notée et son critère est amélioré.

**L'analyse :** les critères dont la preuve est systématiquement demandée sont ceux dont le format de présentation est faible — il faut un gabarit de preuve. Les critères jamais questionnés sont ceux qui sont bien documentés — OU jamais vérifiés (le doute de tous est aussi suspect que le doute de personne).

**Le piège :** interpréter les demandes de preuve comme une absence de confiance. C'est l'inverse : la demande de preuve est la participation la plus honnête du décideur — elle prouve qu'il décide avec des données.

### E12 — L'audit des cérémonies

**Objectif d'apprentissage :** vérifier que les rituels sont réels (entrées, livrables, tenue sans facilitateur), pas seulement présents.

**Protocole :** chaque cérémonie est évaluée sur les trois questions (entrées obligatoires ? livrable daté ? tenue sans le facilitateur ?). Chaque échec reçoit une correction datée et un propriétaire.

**L'analyse :** la matrice de l'audit se relit à chaque trimestre. La colonne « tenue sans le facilitateur » est la plus lente à se remplir — c'est normal : c'est la dernière qui vient. Une cérémonie qui échoue aux trois questions doit être repensée, pas patchée.

**Le piège :** l'audit d'auto-complaisance où tout est vert. La contre-mesure : chaque « oui » exige une preuve citée (l'artefact, la date). Un « oui » sans preuve vaut un « non » — c'est la règle anti-langue-de-bois qui tient tout le niveau 1.

## Les exercices par situation

**Si l'équipe doute de l'utilité de la spécification →** E1 (trois relecteurs) et E8 (chiffrage du flou). Les divergences chiffrées sont l'argument que la discussion n'est pas.

**Si le Go/No-Go devient théâtral →** E10 (l'aveugle). Les demandes de preuve remettent le décideur au centre.

**Si le lexique est mort →** E4 (le regard neuf) et E2 (la métrique du vendredi, dont l'analyse révèle les malentendus de vocabulaire).

**Si la confirmation ne produit rien →** E11 (la confirmation inversée). L'observation de l'usage réel est plus riche que l'enquête d'opinion.

**Si l'autonomie douteuse s'installe →** E12 (l'audit des cérémonies) + le test final des cinq questions (Partie 8). La colonne « tenue sans facilitateur » est la mesure de la vraie autonomie.

## La règle d'or des exercices

Un exercice qui ne révèle rien n'est pas un échec : c'est une confirmation que le système tient. Mais dix exercices consécutifs qui ne révèlent rien sont un signal : les exercices sont devenus des rituels de confort — il faut les resserrer (plus exigeants, plus ciblés) ou les alterner (la routine tue la révélation).

L'exercice est un diagnostic, pas un traitement : il révèle où regarder. Le traitement reste les rituels du parcours — tenus, honnêtes, mesurés.
