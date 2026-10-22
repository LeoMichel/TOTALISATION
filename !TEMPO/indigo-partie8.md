
---

# Partie 8 : Le vécu du niveau 6

Quatre histoires vraies, tirées du vécu de l'organisation — là où la prévention et l'anticipation se sont jouées sur des personnes, pas sur des concepts. Chaque histoire est suivie de ce qu'elle enseigne au praticien du niveau 6.

## Histoire 1 : Le signal faible qui a évité l'incident — Opal-RT

C'était pendant la migration de l'infrastructure de build. L'équipe avait un canal des signaux faibles (institué au niveau 5), et un jeudi, un message passait presque inaperçu : un ingénieur mentionnait qu'un script de build « prenait un peu plus de temps ces derniers jours ». Rien d'alarmant. Personne n'aurait ouvert un ticket pour ça.

Mais le canal N6 fonctionnait autrement : les signaux faibles étaient relus chaque semaine, et les tendances étaient projetées. « Un peu plus de temps » répété trois semaines de suite était une tendance — et la projection montrait que dans six semaines, le build dépasserait le délai de l'intégration continue. Un signal faible confirmé trois fois devenait, selon la règle du canal, une élicitation proactive.

L'enquête préventive a pris deux heures : une dépendance cachée, introduite trois semaines plus tôt, téléchargeait un artefact à chaque build au lieu d'utiliser le cache. L'équipe l'a corrigée un vendredi après-midi. Coût : deux heures de travail. Coût si rien n'avait été fait : six semaines plus tard, une panne d'intégration continue au pire moment (juste avant une démonstration client), avec une équipe de dix personnes bloquée.

Ce que ce cas enseigne :

- **La prévention a un coût de détection, pas de correction.** Deux heures de détection contre des jours de crise. Le ratio était de un pour cent — et il n'était visible que dans la projection, jamais dans l'instant.
- **Le signal faible n'a pas d'urgence propre.** Il a fallu une cérémonie (la revue hebdomadaire des signaux) pour lui donner une existence. Le message passé inaperçu ne serait devenu visible pour personne : les signaux faibles ne remontent pas seuls.
- **La projection transforme l'invisible en décisionnable.** « Le build prend plus de temps » est une plainte. « Le build dépassera le délai dans six semaines » est une décision.

## Histoire 2 : La prévention sacrifiée — et ce qu'elle a coûté

C'était dans une période de pression, comme il y en a toujours. Une date de livraison, une équipe en retard, et le comité (niveau 5, alors tout jeune) a proposé de « reporter les chantiers de prévention pour ce sprint ». La règle de capacité préventive — 15 % de capacité réservée — n'existait pas encore : la prévention se faisait « quand il y avait du temps ». Il n'y avait jamais de temps.

Le report a duré un sprint. Puis deux. Puis la prévention n'a plus été re-planifiée du tout — chaque sprint, le report était reconduit, parce que chaque sprint avait sa pression. Trois mois plus tard, la dette technique invisible avait grossi au point que les estimations explosaient : les demandes simples prenaient des semaines, parce que chaque changement touchait du code fragile que personne n'avait eu le temps de consolider.

L'équipe a recalculé rétrospectivement : les deux semaines de consolidation reportées auraient économisé six semaines de retards cumulés. Le coût de la non-prévention était quatre fois supérieur à la prévention — mais ce coût était étalé et invisible, tandis que le coût de la prévention était immédiat et visible.

Ce que ce cas enseigne :

- **La prévention perd toujours l'arbitrage si elle n'a pas de règle.** Quand l'arbitrage se fait demande par demande, la prévention perd — parce que le réactif est visible et la prévention ne l'est pas. La règle de capacité (même modeste : 10 ou 15 %) est la seule protection.
- **Le report est la mort lente de la prévention.** Un report écrit avec rattrapage daté est une décision ; un report reconduit tacitement est un abandon. La règle du niveau 6 : tout report de prévention est écrit, daté, avec rattrapage — sinon il n'existe pas.
- **Les urgences sont souvent les symptômes des préventions manquantes.** Trois mois plus tard, l'équipe passait son temps en « urgences » qui étaient toutes des dettes de prévention. Le jour où la consolidation a été faite, les urgences ont diminué de moitié.

## Histoire 3 : La mémoire consultée pour la première fois

C'était au moment d'une nouvelle spécification pour un client tiers. L'équipe avait construit, au niveau 5, les débuts d'une mémoire des apprentissages — une centaine de notes, indexées sommairement. Personne ne la consultait : elle était « là », comme un placard bien rangé qu'on n'ouvre jamais.

Le praticien a imposé une étape à la cérémonie de définition : vingt minutes de consultation mémoire avant d'écrire. Le thème était « intégration API tiers » — et la mémoire contenait quatre apprentissages d'intégrations précédentes, dont un qui était une mine : « les API de ce fournisseur changent sans préavis ; toute intégration doit prévoir un contrat de version et un test de non-régression sur le format de réponse ». Écrit six mois plus tôt, après trois jours de debugging d'une panne incompréhensible.

La spécification a intégré le contrat de version et le test de non-régression dès le départ. Six mois plus tard, le fournisseur a changé son format de réponse sans préavis — exactement comme la mémoire le prédisait — et le test a échoué avant la mise en production, une heure de correction au lieu d'une panne client.

Ce que ce cas enseigne :

- **Une mémoire non consultée est une mémoire morte.** L'infrastructure ne suffit pas : il faut une cérémonie (la consultation obligatoire au DoR) pour que la mémoire vive. La consultation a coûté vingt minutes ; elle a épargné une panne.
- **Les apprentissages douloureux sont les plus précieux.** L'apprentissage le plus utile de la mémoire était celui des trois jours de debugging — la douleur est le meilleur moteur d'indexation. Une mémoire qui n'enregistre que les succès apprend la complaisance.
- **L'enrichissement est réciproque.** La spécification a consulté la mémoire — et la spécification a enrichi la mémoire (un nouveau cas limite : « que faire si le fournisseur envoie le changement sans changement de version ? »). Une mémoire qu'on consulte sans l'enrichir devient obsolète.

## Histoire 4 : L'anticipation qui a failli tuer l'écoute

C'était après une série de succès de prévention. L'équipe, enivrée par ses projections justes, a lancé une vague d'élicitations proactives : des fonctionnalités prédites par les signaux faibles, construites sans consultation, parce que « les signaux le montraient ». Quatre fonctionnalités en deux mois.

Aucune n'a été adoptée. Pas une. Les demandeurs réels — ceux dont les signaux avaient été interprétés — n'avaient jamais eu ces besoins précis : les signaux montraient des tendances larges, et l'équipe avait extrapolé des solutions précises. La projection disait « les utilisateurs de ce module travaillent de plus en lot » — l'équipe avait construit une interface de traitement par lot. Ce que les utilisateurs voulaient, c'était un export réutilisable ; le lot n'était qu'un moyen.

Le praticien a institué la règle définitive : une élicitation proactive se fait toujours avec le demandeur pressenti, jamais pour lui. Les signaux ouvrent la conversation ; ils ne la remplacent pas. Les quatre fonctionnalités non adoptées ont été archivées avec leur post-mortem dans la mémoire — elles sont devenues les apprentissages anti-pattern les plus cités.

Ce que ce cas enseigne :

- **La prévision n'est pas la demande.** Un signal montre une tendance ; il ne montre pas la solution. L'anticipation sert à savoir qui contacter et quoi demander — pas à décider à la place de.
- **L'excès de confiance est le piège du praticien avancé.** Les premiers succès de projection créent une ivresse : le praticien se croit voyant. La règle « avec le demandeur, jamais pour lui » est la garde-fou de cette ivresse.
- **Les échecs sont des apprentissages de premier ordre.** Le post-mortem des quatre fonctionnalités archivées (« ce que la projection ne voyait pas ») est devenu un apprentissage cité chaque fois qu'une élicitation proactive se discute. Une mémoire qui intègre ses échecs d'anticipation anticipe mieux.

## La synthèse des quatre histoires

Les quatre histoires dessinent le profil du praticien du niveau 6 : il a un canal pour les signaux faibles (Histoire 1), une règle pour protéger la prévention (Histoire 2), une mémoire consultée et enrichie (Histoire 3), et la modestie de l'anticipateur — l'anticipation éclaire la conversation, elle ne la remplace pas (Histoire 4). Sans modestie, l'anticipation devient de l'arrogance méthodique ; sans mémoire, elle devient de l'intuition ; sans règle, la prévention devient du bon vouloir.
