
---

# Partie 11 : Le vécu du praticien du niveau 4 — les histoires de mesure

Quatre histoires vraies de la mesure — là où les chiffres ont révélé, trahi, ou transformé la façon de travailler.

## Histoire 1 : La mesure qui a changé l'équipe (et pas seulement le tableau)

C'était dans une équipe de 7 personnes. Le praticien du niveau 4 a introduit sa première mesure de résultat : le délai total de traitement (réception → acceptation). Le but était simple : savoir combien de temps une demande prenait réellement, du point de vue du demandeur.

La première mesure a choqué : 12 jours en médiane. L'équipe estimait 3 jours. Le praticien n'a pas accusé l'équipe de mentir — il a demandé où passait le temps. L'analyse a révélé que 8 jours sur 12 étaient de l'attente : attente de clarification du demandeur (2 j), attente d'environnement de test (2 j), attente de revue (1 j), attente de validation du demandeur (3 j).

L'équipe n'a pas travaillé plus vite après la mesure. Ce qui a changé : elle a vu l'attente qu'elle ne voyait pas avant, et elle a pu la traiter — une demande incomplète est retournée immédiatement (le demandeur la complète), un environnement de test est dédié, la revue est planifiée au démarrage (pas en fin de semaine). Le délai médian est passé de 12 à 5 jours en deux mois.

Ce que cette histoire enseigne :

- **La mesure révèle ce que les impressions cachent.** L'équipe estimait 3 jours parce qu'elle mesurait son travail actif. Le demandeur vivait 12 jours parce que le délai total inclut l'attente. Les deux avaient raison — ils mesuraient des choses différentes.
- **La mesure ne change pas la vitesse — elle révèle l'attente.** L'attente est invisible sans mesure. Le praticien VERT qui veut améliorer la vitesse doit d'abord mesurer l'attente, pas l'activité.
- **L'équipe n'a pas à se justifier — elle a à voir ce qu'elle ne voit pas.** L'accusation (« vous êtes lents ») produit la défense ; la question (« où passe le temps ? ») produit la découverte. Le praticien VERT pose la question.

## Histoire 2 : Les mesures qui ont révélé une transformation invisible

Une équipe de développement avait introduit un nouveau pipeline automatisé (le niveau 2). Les deux mesures de résultat ont montré : le délai total a augmenté (de 5 à 7 jours), le taux de retour a baissé (de 30 % à 12 %). Deux résultats contradictoires : plus lent, mais moins de reprises.

**Le diagnostic.** Le délai a augmenté parce que le pipeline ajoutait une étape (génération des tests, exécution, revue des sorties) qui n'existait pas avant. Le taux de retour a baissé parce que les tests générés attrapaient des défauts qui passaient avant. Le calcul : 2 jours de plus dans le pipeline, contre 8 jours de reprises économisées par livraison. Le pipeline était rentable — mais l'équipe ne le voyait pas parce qu'elle comparait le délai brut sans compter les reprises évitées.

**La correction.** Le praticien a changé la mesure du délai : au lieu du délai brut (réception → livraison), il a mesuré le délai net (réception → livraison acceptée, sans compter les reprises). Le délai net a montré : 7 jours avec le pipeline, contre 5 + 8/5 = 6,6 jours en moyenne sans (le délai brut plus le coût moyen des reprises). Le pipeline était rentable en délai net — et l'équipe le voyait enfin.

**Ce que cette histoire enseigne :**
- **Le délai brut masque le coût des reprises.** Une mesure qui ne compte pas les reprises favorise les pratiques qui produisent vite mais mal. La mesure nette (avec les reprises) est plus honnête — et elle révèle ce que la mesure brute cachait.
- **Deux résultats contradictoires ne sont pas un échec de mesure — c'est une information.** Le praticien VERT qui voit des résultats contradictoires ne panique pas : il cherche la mesure qui les réconcilie (ici, le délai net).

## Histoire 3 : Le praticien qui a arrêté de mesurer (et pourquoi)

Une équipe de maintenance (5 personnes, support d'un système legacy en fin de vie) a tenté le passage au niveau 4. Le praticien a déployé les quatre mesures de résultat. Le résultat après un trimestre : les mesures étaient stables, les conversations étaient stériles, et l'équipe s'ennuyait.

Le diagnostic du praticien : l'équipe ne produisait pas de demandes — elle gérait des incidents récurrents sur un système en fin de vie. Le délai était constant (le même chaque semaine), le retour était nul (les incidents ne revenaient pas), la stabilité était inchangée (le système ne pouvait pas être plus stable sans refonte). Les mesures ne mesuraient rien d'intéressant : elles seraient stables par construction.

**La décision du praticien :** renoncer au niveau 4 — et l'assumer. L'équipe est restée au niveau 3, avec une mesure unique (le nombre d'incidents récurrents) et le rituel de maintenance. Le praticien a documenté le renoncement : « le niveau 4 mesure des flux de transformation ; notre flux n'est pas transformable. Les mesures seraient stables par construction — les tenir serait du théâtre. »

**La leçon :** le praticien VERT sait quand ne pas mesurer. La mesure est un investissement (collecte, revue, correction) — et elle n'est justifiée que si quelque chose peut régresser et être corrigé. Le renoncement argumenté est une décision de praticien, pas un échec.

## Histoire 4 : La mesure qui a réconcilié une équipe avec son sponsor

Une équipe de 6 personnes au niveau 3 avait un sponsor sceptique : il pensait que l'équipe était « lente et dispendieuse ». Les impressions du sponsor étaient basées sur des anecdotes (un incident de production, un retard visible, un budget dépassé) — pas sur des données.

Le praticien du niveau 4 a proposé au sponsor de construire le tableau de mesure ensemble : choisir les mesures, les définir, les suivre pendant un trimestre. Le sponsor a accepté — avec la promesse : « si les mesures disent que l'équipe est lente, nous le saurons, et nous pourrons décider. »

Le résultat après un trimestre : le délai médian était de 5 jours (moyenne de l'industrie : 7 jours), le taux de retour était de 6 % (moyenne : 15 %), la stabilité était bonne, la disponibilité de capacité était à 20 % (l'équipe avait de la marge). Le sponsor a vu les données — et a dit : « je croyais que vous étiez lents. Vous êtes plus rapides que la moyenne de l'industrie. Je me trompais. »

**La leçon :** la mesure construite ensemble réconcilie mieux que l'argumentaire construit séparément. Le sponsor qui a choisi les mesures ne peut pas les accuser de parti pris. Et le praticien qui propose la construction conjointe transforme un sceptique en allié — parce que le sceptique qui découvre les données positives devient le meilleur défenseur de l'équipe.

## La synthèse des quatre histoires

Les quatre histoires dessinent le praticien du niveau 4 : il mesure l'attente, pas seulement l'activité (Histoire 1) ; il choisit des mesures qui réconcilient les contradictions (Histoire 2) ; il sait renoncer quand mesurer serait du théâtre (Histoire 3) ; et il construit les mesures avec le sponsor pour transformer le scepticisme en allégeance (Histoire 4).

Le praticien VERT qui a appris ces quatre leçons mesure autrement que le praticien débutant : il mesure pour voir, pas pour juger ; il mesure ce qui compte, pas ce qui est facile à compter ; il mesure avec les gens, pas contre eux ; et il renonce à mesurer quand la mesure ne servirait qu'à décorer.
