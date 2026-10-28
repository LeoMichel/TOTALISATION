
---

# Partie 6C : Les cérémonies opérationnelles du niveau 1 — les rôles, les métriques et les pièges (le réel d'Opal-RT)

La Partie 6 a décrit les cérémonies en format narratif, la Partie 6B en format opérationnel avec les sources et les techniques. Cette Partie 6C couvre ce qui manque encore : **qui fait quoi dans chaque cérémonie** (les rôles et leurs contributions précises), **quelles métriques mesurer dans chaque phase** (les signaux qui vérifient que la cérémonie fonctionne), et **les pièges supplémentaires** (ceux que la Partie 6B n'a pas couverts). Ces contenus viennent directement des documents ACAQ-OPAL-RT.

## ÉLICITER — les rôles, les métriques et les pièges supplémentaires

### Qui fait quoi dans la cérémonie ÉLICITER (Opal-RT)

| Rôle | Contribution à l'élicitation |
|------|------------------------------|
| Product Owner / Product Manager | Porte la vision produit, priorise les besoins et valide la pertinence stratégique. |
| Ingénieur d'application / Support | Remonte les irritants terrain, les cas d'usage réels et les demandes clients. |
| Développeur / Tech Lead | Évalue la faisabilité technique préliminaire, identifie les contraintes et la dette existante. |
| QA / Testeur | Apporte les signaux qualimétrie, les régressions récurrentes et les angles morts de couverture. |
| Architecte | Identifie les impacts transversaux, les dépendances système et les risques d'intégration. |
| UX / Designer | Observe les comportements utilisateur et propose des maquettes exploratoires pour valider la compréhension. |
| Scrum Master / Coach | Facilite les ateliers, s'assure que tous les rôles sont entendus et que le besoin reste au centre. |

**Ce que cette grille change pour le praticien N1 :** l'élicitation n'est pas une réunion à deux (le PO et le demandeur). C'est une réunion à sept rôles minimum — et chaque rôle apporte une information que les autres n'ont pas. Le PO porte la stratégie ; le support apporte le terrain ; le développeur apporte la faisabilité ; la QA apporte les angles morts ; l'architecte apporte les impacts ; l'UX apporte le comportement ; le coach garantit que tous les rôles sont entendus. Une élicitation à deux rôles produit une vision partielle — et la spécification qui suit hérite de cette partialité.

### Les métriques et signaux de l'élicitation (Opal-RT)

| Métrique / Signal | Ce qu'elle révèle | Source |
|---|---|---|
| Nombre de besoins élicités par source | Diversité des canaux d'écoute — un seul canal dominant indique un angle mort. | Jira / backlog |
| Taux de besoins rejetés en DÉFINIR | Qualité de l'élicitation — un taux élevé indique un filtrage insuffisant. | Jira workflow |
| Nombre de besoins sans source traçable | Risque de besoins fantômes qui ne sont validables par personne. | Backlog produit |
| Délai moyen entre signal et élicitation | Réactivité du processus — un délai long indique des opportunités manquées. | Jira dates |
| Taux de réouverture post-DÉFINIR | Besoins mal compris qui reviennent — signe d'élicitation incomplète. | Jira workflow |
| Signaux qualimétrie consultés avant atelier | Ancrage dans les données — zéro signal consulté indique une élicitation par intuition. | Grafana / SonarQube |

**Ce que ces métriques changent pour le praticien N1 :** l'élicitation n'est pas seulement une conversation — c'est un processus mesurable. Six métriques suffisent à vérifier si l'élicitation fonctionne : la diversité des sources (un seul canal dominant indique un angle mort), le taux de rejet (un taux élevé indique que l'élicitation filtre mal), les besoins fantômes (sans source traçable), le délai de réactivité, le taux de réouverture (les besoins mal compris qui reviennent), et l'ancrage dans les données (les signaux consultés avant les ateliers).

### Les pièges supplémentaires de l'élicitation (Opal-RT, complets)

| Piège | Pourquoi c'est un problème | Comment l'éviter |
|-------|--------------------------|------------------|
| Ignorer les signaux qualimétrie | On rate les besoins que personne ne formule, mais que les données révèlent. | Consulter les métriques et signaux avant les ateliers. |
| Éliciter avec un seul rôle | La vision est partielle et les angles morts sont nombreux. | Impliquer SENSE, FORGE et CARE dès l'élicitation. |
| Ne pas documenter la source | Il devient difficile de valider plus tard si le besoin est bien compris. | Associer chaque besoin à une source traçable. |
| Confondre ÉLICITER et DÉFINIR | On commence à spécifier trop tôt, sans avoir validé le besoin. | Garder la distinction : ÉLICITER = comprendre ; DÉFINIR = formaliser. |
| Sauter directement à la solution | On risque de spécifier quelque chose que personne n'a vraiment demandé. | Reformuler le problème avant de parler de solution. |

**Le piège qui n'apparaît pas dans la Partie 6B mais qui est le plus fréquent en pratique :** ignorer les signaux qualimétrie avant les ateliers. Le praticien N1 qui lance une élicitation sans avoir consulté Grafana, SonarQube ou les métriques du backlog élicite par intuition — et rate les besoins que personne ne formule mais que les données révèlent. C'est le piège le plus silencieux : il ne produit pas de conflit, il produit des angles morts.

## DÉFINIR — les rôles, les métriques et les pièges supplémentaires (Opal-RT)

### Les métriques et signaux de la phase DÉFINIR (Opal-RT)

| Métrique / Signal | Ce qu'elle révèle | Source |
|---|---|---|
| Taux de spécifications testables (IF…THEN) | Qualité de la formulation — un taux bas indique des spécifications déclaratives, pas testables. | Backlog / wiki |
| Nombre de cas limites identifiés par spécification | Couverture des frontières — un nombre faible indique une spécification superficielle. | Spécification |
| Taux de spécifications revues par les trois rôles | Conformité de la revue — un taux bas indique une revue de complaisance. | Jira / workflow |
| Nombre de demandes qui passent sans spécification | Friction au processus — un taux élevé indique une équipe qui contourne. | Jira / workflow |
| Délai moyen entre élicitation et définition | Cadence du pipeline amont — un délai long indique un goulot en DÉFINIR. | Jira dates |

**Ce que ces métriques changent pour le praticien N1 :** la spécification n'est pas seulement écrite — elle est mesurée. Cinq métriques suffisent : le taux de testabilité (les spécifications en IF…THEN), la couverture des cas limites, le taux de revue à trois rôles, le taux de demandes qui passent sans spécification (le contournement), et le délai entre l'élicitation et la définition. Un praticien qui mesure ces cinq métriques sait si sa phase DÉFINIR fonctionne — et si elle ne fonctionne pas, il sait où chercher.

## PLANIFIER — les rôles, les métriques et les pièges supplémentaires (Opal-RT)

### Les métriques et signaux de la phase PLANIFIER (Opal-RT)

| Métrique / Signal | Ce qu'elle révèle | Source |
|---|---|---|
| Taux de respect du DoR | Qualité des entrées — un taux bas indique des items qui entrent sans spécification prête. | Jira / workflow |
| Variance entre estimé et réel | Précision des estimations — une variance élevée indique des estimations de confort, pas de réalité. | Jira / burndown |
| Nombre de changements de scope en cours d'itération | Stabilité du contrat — un taux élevé indique une planification fragile. | Jira history |
| Taux de risques documentés avec parade | Qualité de la gestion des risques — un taux bas indique des risques sans plan. | Registre des risques |

**Ce que ces métriques changent pour le praticien N1 :** la planification n'est pas seulement une réunion — c'est un processus mesurable. Quatre métriques suffisent : le taux de respect du DoR, la variance estimé/réel, le taux de changements de scope, et le taux de risques documentés avec parade. Un praticien qui mesure ces quatre métriques sait si sa phase PLANIFIER fonctionne — et si elle ne fonctionne pas, il sait si le problème est le DoR, l'estimation, le scope ou les risques.

## IMPLÉMENTER — les rôles, les métriques et les pièges supplémentaires (Opal-RT)

### Les métriques et signaux de la phase IMPLÉMENTER (Opal-RT)

| Métrique / Signal | Ce qu'elle révèle | Source |
|---|---|---|
| Délai moyen de revue de code | Réactivité de la revue — un délai long indique un goulot de revue. | Git / pull requests |
| Taux de conformité spécification/code | Qualité de la conformité — un taux bas indique une divergence code/spécification. | Revue de code |
| Nombre de commentaires de revue par PR | Qualité de la revue — zéro commentaire indique une revue de complaisance. | Git / pull requests |
| Taux de reprise post-revue | Qualité de la première passe — un taux élevé indique des PR soumises trop tôt. | Git / pull requests |

**Ce que ces métriques changent pour le praticien N1 :** la revue de code n'est pas seulement une pratique — c'est un processus mesurable. Quatre métriques suffisent : le délai moyen de revue, le taux de conformité spécification/code, le nombre de commentaires par PR, et le taux de reprise post-revue. Un praticien qui mesure ces quatre métriques sait si sa phase IMPLÉMENTER fonctionne — et si elle ne fonctionne pas, il sait si le problème est la vitesse de revue, la conformité, la qualité de la revue ou la maturité des PR.

## DIFFUSER — les rôles, les métriques et les pièges supplémentaires (Opal-RT)

### Les métriques et signaux de la phase DIFFUSER (Opal-Go, Opal-RT)

| Métrique / Signal | Ce qu'elle révèle | Source |
|---|---|---|
| Nombre de livraisons par semaine | Cadence de diffusion — une cadence irrégulière indique une planification fragile. | Pipeline / CI |
| Taux de Go vs No-Go | Équilibre de la grille — un taux de 100% Go indique une grille décorative. | Registre des Go/No-Go |
| Temps moyen de déploiement | Efficacité du processus de déploiement — un temps long indique une automatisation insuffisante. | Pipeline / CI |
| Taux de rollback | Qualité de la diffusion — un taux élevé indique des livraisons prématurées. | Pipeline / monitoring |
| Délai entre Go et déploiement effectif | Friction post-décision — un délai long indique une friction manuelle. | Pipeline / CI |

**Ce que ces métriques changent pour le praticien N1 :** la diffusion n'est pas seulement un rituel de décision — c'est un processus mesurable. Cinq métriques suffisent : la cadence de diffusion, l'équilibre Go/No-Go, le temps de déploiement, le taux de rollback, et le délai entre la décision et le déploiement effectif. Un praticien qui mesure ces cinq métriques sait si sa phase DIFFUSER fonctionne — et si elle ne fonctionne pas, il sait si le problème est la cadence, la grille, l'automatisation, la qualité ou la friction.

## CONFIRMER — les métriques et signaux supplémentaires (Opal-RT)

### Les métriques et signaux de la phase CONFIRMER (Opal-RT)

| Métrique / Signal | Ce qu'elle révèle | Source |
|---|---|---|
| Taux de confirmations effectuées (vs diffusions) | Complétude de la boucle — un taux bas indique des confirmations sautées. | Registre des confirmations |
| Délai moyen entre diffusion et confirmation | Réactivité du retour — un délai long indique une confirmation tardive (moins utile). | Registre des confirmations |
| Nombre d'apprentissages par confirmation | Valeur de la confirmation — zéro apprentissage indique une confirmation de complaisance. | Registre des confirmations |
| Taux de besoins mal élicités détectés en confirmation | Qualité de l'élicitation — un taux élevé indique des besoins mal compris en amont. | Registre / Jira |

**Ce que ces métriques changent pour le praticien N1 :** la confirmation n'est pas seulement un rituel — c'est un processus mesurable. Quatre métriques suffisent : le taux de confirmations effectuées (vs diffusions), le délai moyen entre diffusion et confirmation, le nombre d'apprentissages par confirmation, et le taux de besoins mal élicités détectés en confirmation. Un praticien qui mesure ces quatre métriques sait si sa phase CONFIRMER fonctionne — et si elle ne fonctionne pas, il sait si le problème est la complétude, la réactivité, la valeur ou la qualité de l'élicitation.

## QUALIMÉTRIE — les rôles, les métriques et les pièges supplémentaires (Opal-RT)

### Les métriques et signaux de la phase QUALIMÉTRIE (Opal-RT)

| Métrique / Signal | Ce qu'elle révèle | Source |
|---|---|---|
| Taux de métriques regardées vs produites | Vitalité du tableau de bord — un taux bas indique un tableau de bord décoratif. | Tableau de bord |
| Nombre de décisions prises par point de qualimétrie | Valeur du point de qualimétrie — zéro décision indique un rituel de constatation. | Registre des décisions |
| Taux de métriques sans seuil | Qualité du tableau de bord — un taux élevé indique des métriques sans critère d'alerte. | Tableau de bord |
| Nombre d'alertes sans action | Vitalité du système d'alerte — un taux élevé indique des alertes décoratives. | Registre des décisions |

**Ce que ces métriques changent pour le praticien N1 :** la qualimétrie n'est pas seulement un tableau — c'est un processus mesurable. Quatre métriques suffisent : le taux de métriques regardées vs produites, le nombre de décisions par point, le taux de métriques sans seuil, et le nombre d'alertes sans action. Un praticien qui mesure ces quatre métriques sait si sa phase QUALIMÉTRIE fonctionne — et si elle ne fonctionne pas, il sait si le problème est la lecture, la décision, les seuils ou les alertes.

## Le tableau récapitulatif : les métriques par phase du SDLC (Opal-RT)

| Phase | Nombre de métriques | La métrique la plus révélatrice |
|-------|--------------------|--------------------------------|
| ÉLICITER | 6 | Taux de réouverture post-DÉFINIR (les besoins mal compris qui reviennent) |
| DÉFINIR | 5 | Taux de spécifications revues par les trois rôles (la conformité de la revue) |
| PLANIFIER | 4 | Taux de respect du DoR (la qualité des entrées) |
| IMPLÉMENTER | 4 | Taux de conformité spécification/code (la qualité de la conformité) |
| DIFFUSER | 5 | Taux de Go vs No-Go (l'équilibre de la grille) |
| CONFIRMER | 4 | Nombre d'apprentissages par confirmation (la valeur de la confirmation) |
| QUALIMÉTRIE | 4 | Nombre de décisions prises par point de qualimétrie (la valeur du rituel) |

**Total : 32 métriques opérationnelles** — réparties sur les 7 phases du SDLC TOTALISATION. Ce n'est pas trop : c'est exactement ce qu'il faut pour mesurer chaque phase. Le praticien N1 qui mesure ces 32 métriques sur un trimestre a un tableau de santé complet de son SDLC — et il sait où chercher quand une phase ne fonctionne pas.
