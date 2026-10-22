
---

# Partie 15 : Les cas réels — trois situations vécues au niveau 3

## Cas 1 : la livraison Go sans les preuves complètes

**Contexte.** Une équipe de 9 personnes, système de facturation pour un client réglementé. Le chargé de livraison prépare la séance du vendredi. Trois des douze critères Go/No-Go sont rouges : la trace de sécurité n'a pas été revue par le spécialiste, la note de version est incomplète, et la réserve sur la migration de données a une levée prévue pour le mardi suivant — deux jours après la livraison.

**La tentation.** Le sponsor est sous pression (le client réglementé attend). La livraison peut se faire « quand même », avec trois réserves actives. Le chargé de livraison doute : est-ce que la grille est trop stricte ? Est-ce que je bloque pour rien ?

**Ce qui a été fait.** Le chargé de livraison a appliqué la formule : pas aujourd'hui, voici pourquoi, voici quand. Il a proposé le mardi suivant comme date de livraison, avec la levée de la réserve de migration comme unique condition Go. La trace de sécurité et la note de version ont été complétées dans le week-end (elles l'auraient été après la livraison, sinon — c'est le gain réel). Le sponsor a accepté, en soulignant que le client réglementé préfère un mardi propre qu'un vendredi douteux.

**Le résultat.** La livraison du mardi est passée sans incident. La réserve de migration a été levée le jour même, avec les preuves. Le sponsor, dans la rétrospective, a dit la phrase qui compte : « la grille m'a protégé de moi-même ».

**La leçon.** Le No-Go n'est pas une défiance — c'est un service rendu. La preuve du No-Go, c'est la livraison suivante sans incident. Un No-Go qui est suivi d'un Go propre dans les 5 jours ouvrables renforce la grille ; un No-Go qui n'est jamais suivi d'un Go propre la fragilise (car elle devient un blocage sans issue). Le chargé de livraison doit toujours avoir la date de rattrapage prête : c'est ce qui transforme le refus en service.

**Le piège évité.** Si le chargé de livraison avait cédé, la livraison du vendredi se serait faite avec trois réserves actives, dont une (la migration) sans levée prévue. L'incident de migration, s'il s'était produit, aurait coûté dix fois le délai de quatre jours — et l'équipe aurait perdu la crédibilité de sa propre grille.

## Cas 2 : la sur-qualification systématique des demandes

**Contexte.** Le SLA par classe est en place depuis six semaines. Les statistiques montrent un pattern : 40 % des demandes sont classées « complexes » alors que la moyenne historique était de 15 %. Le délai moyen a doublé — pas parce que le travail est plus long, mais parce que la classe est plus lente.

**La tentation.** Pointer les personnes qui sur-qualifient et leur demander d'arrêter. Ou durcir le classement avec une revue obligatoire par le chargé de livraison.

**Ce qui a été fait.** Le praticien a d'abord demandé pourquoi : l'analyse a montré que les demandes « complexes » étaient souvent des demandes dont les critères de classement (simples : ≤ 2 h,Standard : ≤ 2 j,Complexe : ≤ 1 sem) étaient flous dans les cas intermédiaires — une demande de 3 heures d'effort pouvait être classée Standard ou Complexe selon l'interprétation. La sur-qualification n'était pas de la tricherie : c'était de l'incertitude, orientée vers la prudence (prendre plus de temps que prévu plutôt que moins).

**La réponse.** La grille de classement a été révisée avec les données réelles : la classe Standard a été élargie (≤ 4 h au lieu de ≤ 2 h), et les critères de passage de Standard à Complexe ont été rendus explicites (nombre de fichiers touchés, impacts sur les intégrations, etc.). Le taux de « complexes » est revenu à 18 % en trois semaines — sans pointer personne.

**Le résultat.** Le délai moyen est revenu à la normale. Plus important : l'équipe a découvert que le classement était une compétence collective (pas une règle à subir), et deux personnes ont proposé d'améliorer les critères de passage (ce qu'elles ont fait dans le forgeage suivant).

**La leçon.** Un pattern de sur-qualification est presque toujours un symptôme de critères flous, pas de mauvaise foi. La règle : compter d'abord, demander ensuite, corriger les critères si le pattern persiste. Pointer les personnes avant d'avoir corrigé les critères transforme une incertitude légitime en défiance généralisée.

**Le piège évité.** Si le praticien avait durci le classement avec une revue obligatoire, le coût administratif aurait augmenté, la confiance aurait baissé, et la sur-qualification se serait déplacée (vers la sous-qualification, pour éviter la revue). Le pattern n'aurait pas disparu — il aurait changé de forme.

## Cas 3 : le rituel abandonné discrètement

**Contexte.** La revue de sécurité hebdomadaire (15 minutes, lundi matin) est tenue depuis 4 mois. Au 5e mois, le praticien remarque que les comptes rendus sont de plus en plus courts, puis absents. Personne n'a annoncé l'abandon : le rituel a juste cessé d'être tenu, sans décision explicite.

**La tentation.** Relancer le rituel avec un rappel, une relance, une sanction. Ou l'abandonner définitivement (tant pis).

**Ce qui a été fait.** Le praticien a d'abord vérifié si le rituel était toujours utile : l'analyse des comptes rendus a montré que les trois derniers mois n'avaient trouvé aucun défaut de sécurité réel (les défauts passaient par le pipeline, qui les attrapait avant). Le rituel avait été forgé pour un problème que le pipeline avait depuis résolu — il n'était plus un pilier, il était une redondance.

**La réponse.** Le praticien a proposé à l'équipe de reconnaître officiellement la fin du rituel (pas de le laisser mourir en silence), et de le remplacer par un rituel adapté : une revue de sécurité mensuelle (au lieu d'hebdomadaire), centrée sur les défauts que le pipeline ne peut pas attraper (les choix d'architecture, les dépendances, les accès). La nouvelle cadence a été tenue, et la première séance mensuelle a trouvé un défaut réel (un accès trop large) que le pipeline ne pouvait pas voir.

**Le résultat.** L'énergie de la revue de sécurité est remontée (une réunion mensuelle est mieux préparée qu'une réunion hebdomadaire devenue automatique), et le rituel est redevenu un pilier vivant.

**La leçon.** Un rituel qui meurt en silence est un rituel qui a peut-être accompli sa mission — ou qui a été mal forgé. Dans les deux cas, la mort en silence est la pire des issues : elle laisse un vide non nommé, et elle enseigne à l'équipe que les rituels peuvent disparaître sans décision. La règle : reconnaître officiellement la fin d'un rituel (une phrase dans la rétrospective suffit), et le remplacer si le besoin existe toujours sous une autre forme.

**Le piège évité.** Si le praticien avait relancé le rituel hebdomadaire par la contrainte, la réunion serait devenue une formalité sans valeur (le pipeline attrapait déjà les défauts), et l'énergie aurait baissé encore plus — le rituel aurait survécu en apparence et serait mort en réalité.

## Cas 4 : la veille qui n'envoie jamais de lettre

**Contexte.** La veille du niveau 3 est en place : un chargé de veille, des seuils, une lettre bimensuelle. Après deux mois, aucune lettre n'a été envoyée (les seuils n'ont jamais été franchis). Le chargé de veille se demande si son rôle a un sens, et l'équipe se demande si la veille sert à quelque chose.

**La tentation.** Abandonner la veille (rien ne se passe de toute façon). Ou inventer des alertes pour justifier le rôle.

**Ce qui a été fait.** Le praticien a proposé un changement de cadrage : la lettre de veille n'est pas seulement un rapport d'alertes — c'est un rapport de non-alerte. Quand les seuils ne sont pas franchis, la lettre le dit explicitement : « aucun seuil franchi ce mois-ci, voici les valeurs observées (temps de réponse moyen 240 ms, seuil 500 ms ; taux d'erreur 0,2 %, seuil 2 %) ». La lettre devient une preuve de santé, pas seulement un rapport de maladie.

**Le résultat.** La lettre bimensuelle est envoyée (même sans alerte), le chargé de veille a un livrable visible, et l'équipe découvre que la veille ne sert pas seulement à détecter les problèmes — elle sert aussi à prouver qu'il n'y en a pas, ce qui est une information précieuse pour le sponsor.

**La leçon.** Une veille qui ne dit rien n'est pas une veille inutile — c'est une veille qui doit dire son silence. La règle : le rapport de non-alerte est aussi important que le rapport d'alerte, car il transforme l'absence de problèmes en une information mesurée (et non en une supposition).

**Le piège évité.** Si la veille avait été abandonnée, le mois où un seuil serait réellement franchi sans être détecté aurait été un aveu d'échec de la gouvernance — et la reconstruction de la veille après un incident coûte dix fois le coût de son maintien.

## Cas 5 : le sponsor qui veut un Go pour hier

**Contexte.** Un client stratégique exige une livraison « cette semaine ». Le chargé de livraison prépare la séance Go/No-Go. Deux critères sont rouges : la documentation de déploiement est incomplète, et la réserve sur les performances sous charge a une levée prévue pour le jeudi suivant. Le sponsor demande : « est-ce qu'on peut livrer quand même, et lever la réserve ensuite ? »

**La tentation.** Céder sous la pression (le sponsor est le sponsor). Ou refuser sans alternative (et perdre la relation avec le sponsor).

**Ce qui a été fait.** Le chargé de livraison a proposé la voie du milieu : la dérogation écrite. Le critère rouge (documentation incomplète) a été assumé par le sponsor dans une dérogation écrite (le risque est documenté, la condition de levée est le mardi suivant), et le critère de la réserve de performance a été traité comme un No-Go partiel : la livraison peut se faire pour 80 % des utilisateurs (les moins sensibles), les 20 % restants attendent la levée de la réserve. Le sponsor a accepté : il assume le risque de la documentation en échange d'une livraison partielle immédiate.

**Le résultat.** La livraison partielle a eu lieu le vendredi (80 % des utilisateurs), la levée de la réserve a eu lieu le jeudi suivant, et la livraison complète a eu lieu le lendemain. La documentation a été complétée le mardi (condition de la dérogation), et l'incident de documentation qui aurait pu se produire ne s'est pas produit.

**La leçon.** La dérogation écrite n'est pas un contournement de la grille — c'est une extension honnête de la grille. Elle transforme un « non » en un « oui, avec un risque assumé et nommé ». La règle : si le sponsor veut assumer un risque, la dérogation écrite lui donne le cadre pour le faire proprement (ce qui protège à la fois le sponsor et l'équipe).

**Le piège évité.** Si le chargé de livraison avait cédé sans dérogation écrite, la documentation incomplète aurait été « oubliée » (et l'incident de déploiement, s'il s'était produit, aurait été attribué à l'équipe, pas au sponsor). Si le chargé de livraison avait refusé sans alternative, la livraison se serait faite hors grille (par la hiérarchie), et la grille aurait perdu sa crédibilité pour de bon.

## Synthèse des cinq cas

**Le pattern commun :** dans les cinq cas, la décision correcte n'a pas été la plus dure ou la plus souple — c'était la plus honnête. Le No-Go avec une date de rattrapage est un service. La révision des critères est une amélioration. La reconnaissance officielle de la fin d'un rituel est un respect. Le rapport de non-alerte est une preuve de santé. La dérogation écrite est un « oui » assumé.

**Ce que le praticien du niveau 3 retient :**
- La grille est un outil de service, pas une arme de blocage — la date de rattrapage est toujours la contrepartie du refus.
- Les patterns de comportement (sur-qualification, sur-dérogation, abandon silencieux) sont des symptômes à diagnostiquer, pas des fautes à punir.
- La mort en silence d'un rituel est toujours une perte : nommez-la, ou remplacez-la.
- La veille doit dire son silence autant que ses alertes.
- La dérogation écrite est la soupape de la grille — elle transforme les pressions en risques assumés, et les risques assumés en apprentissages.
