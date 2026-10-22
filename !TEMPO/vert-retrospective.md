
---

# PARTIE 23 — LA RÉTROSPECTIVE D'ORIGINE : comment l'équipe Amélie a vécu le passage au VERT

## Le contexte avant

L'équipe Amélie (7 personnes, une équipe de développement applicatif dans une entreprise de services financiers) avait terminé le niveau 3 avec confiance : les rituels tenaient à cadence fixe, le SLA par classe fonctionnait, la lettre de veille était envoyée bimensuellement. Le sponsor était convaincu. L'équipe était fière.

Le praticien a proposé le passage au niveau 4 avec une phrase qui a marqué : « Vous avez construit une cadence. Maintenant, vous pouvez la voir. » L'équipe n'a pas compris immédiatement. Voir la cadence ? Ils la vivaient tous les jours.

## Les 8 premières semaines

### Semaine 1-2 : les définitions

La première étape a été de définir les quatre mesures. L'équipe a passé deux semaines sur les définitions — et c'était la partie la plus difficile de tout le niveau.

Le délai total : qu'est-ce qui compte ? La réception ? Mais la réception du courriel ou la réception du ticket ? Que se passe-t-il quand une demande arrive par les deux ? Et l'acceptation : comment la définit-on ? Une acceptation tacite après 5 jours compte-t-elle ?

L'équipe a écrit, corrigé, re-corrigé, jusqu'à ce que chaque définition soit précise. Le praticien ne donnait pas les réponses : il posait les questions. « Comment saurez-vous, dans six mois, si une demande a été traitée dans le délai ? »

Le résultat : quatre fiches de définition précises (début, fin, inclus, exclu) — chacune révisée trois fois. Ce n'était pas un exercice de documentation : c'était un exercice de vocabulaire commun. L'équipe a découvert qu'elle ne parlait pas la même langue sur les concepts qu'elle vivait chaque jour.

### Semaine 3-4 : les premières données

La collecte a démarré. Le résultat a choqué : le délai total était de 14 jours en médiane, alors que l'équipe estimait 3 jours. Le praticien n'a pas accusé l'équipe de mentir — il a demandé où passait le temps.

L'analyse a révélé que 8 jours sur 14 étaient de l'attente : attente de clarification du demandeur (2 j), attente d'environnement de test (2 j), attente de revue (1 j), attente de validation du demandeur (3 j).

L'équipe n'a pas travaillé plus vite après la mesure. Ce qui a changé : elle a vu l'attente qu'elle ne voyait pas avant.

### Semaine 5-6 : les miroirs

La définition des miroirs a été la deuxième surprise. L'équipe a dû imaginer : « Comment pourrait-on améliorer cette mesure sans améliorer le résultat ? »

Les réponses ont été instructives. Le délai pouvait être "amélioré" en re-classifiant les demandes complexes comme simples. Le taux de retour pouvait être "amélioré" en cessant de compter les retours mineurs comme des retours. La disponibilité de capacité pouvait être "améliorée" en sous-estimant les demandes.

Chaque triche imaginable a reçu son miroir : la mesure de re-classification, la définition stricte du retour, la mesure de la capacité réelle (pas théorique).

### Semaine 7-8 : le premier sponsor honnête

La présentation au sponsor a été le moment le plus tendu et le plus important. L'équipe a présenté les données brutes, avec le délai réel (14 jours au lieu de 3 espérés), sans maquillage.

Le sponsor a dit : « Je croyais que vous étiez plus rapides. Je me trompais. » Et il a proposé une action : « Comment puis-je vous aider à réduire les 8 jours d'attente ? » — l'équipe n'avait jamais entendu cette phrase de son sponsor.

L'attente de clarification du demandeur (2 j) a été réduite par le sponsor lui-même : il a mis en place une session hebdomadaire de clarification pour ses équipes. Le délai est passé de 14 à 9 jours en six semaines.

## Les 4 semaines suivantes

### Les corrélations

La carte des corrélations a été la découverte inattendue. L'équipe a trouvé que son signal N3 « divergences doc/modèle » prédisait le taux de retour N4 avec deux semaines d'avance — et que le signal « temps de build » prédisait la stabilité post-livraison.

Cette carte a transformé la revue hebdo : l'équipe ne réagit plus aux résultats (trop tard) mais aux signaux (à temps). Le praticien a documenté la carte, avec la méthode de vérification.

### Le premier miroir qui a détecté une triche

Au trimestre suivant, le miroir du délai (la mesure de re-classification) a détecté une hausse : 3 demandes "simples" étaient en réalité des demandes "standard" déguisées pour respecter le SLA. L'équipe a découvert la triche — et a discuté de la pression qui l'a provoquée (le SLA de 2 jours était trop serré pour ce type de demande).

La réaction n'a pas été punitive : le SLA a été révisé avec les données (de 2 à 3 jours), et la triche a été documentée dans la jurisprudence (le pattern de contournement quand un seuil est trop serré).

## Ce que l'équipe Amélie a appris

Les trois leçons de l'équipe Amélie :

1. **La mesure ne révèle pas la vitesse — elle révèle l'attente.** L'attente est invisible sans mesure. Le praticien VERT qui veut améliorer la vitesse doit d'abord mesurer l'attente, pas l'activité.

2. **Les miroirs sont la protection structurelle contre la triche.** Chaque mesure a son miroir : ce qui détecte l'optimisation perverse. Un miroir qui ne détecte rien est mal conçu. Un miroir qui détecte tout est mal calibré.

3. **Le sponsor qui co-crée les mesures devient un allié.** Le sponsor qui définit seul les mesures les conteste. Le praticien qui propose la construction conjointe transforme le sceptique en défenseur.

## Ce que l'équipe Amélie n'avait pas prévu

Le praticien a demandé à l'équipe ce qu'elle n'avait pas prévu dans le passage au niveau 4. Trois réponses :

1. **Le temps passé sur les définitions.** « On a passé deux semaines sur des définitions — c'était frustrant, et c'était la chose la plus importante du niveau. »
2. **Le temps réel vs le temps estimé.** « On croyait qu'on était rapides. On ne l'était pas. »
3. **Le sponsor qui propose de l'aide.** « On n'avait jamais entendu notre sponsor proposer de l'aide. Le changement a été plus dans lui que dans nous. »

## Ce que le praticien a retenu

Le praticien du niveau 4 a retenu trois leçons qui n'apparaissent pas dans les gabarits :

1. **Les définitions sont plus importantes que les mesures.** Une mesure bien définie révèle tout ; une mesure mal définie fabrique de l'opacité même quand elle est automatisée.

2. **Le sponsor qui voit les données honnêtes est le meilleur allié de la méthode.** Le sponsor qui voit les données maquillées fabrique de la méfiance. L'honnêteté N4 se mesure à la réaction du sponsor.

3. **La triche détectée est une information, pas une faute.** Le miroir qui détecte une triche révèle une pression mal placée. Le praticien qui traite la triche par le blâme détruit la transparence ; celui qui la traite par la correction du système la renforce.

## La synthèse

L'équipe Amélie est passée du niveau 3 au niveau 4 en 12 semaines. Ce qu'elle a construit : un système de mesure complet (4 mesures de résultat, 4 miroirs, un tableau de bord, une carte des corrélations). Ce qu'elle a appris : le vocabulaire commun (les définitions), l'attente invisible (8 jours sur 14), la triche comme information (pas comme faute), et le sponsor comme allié (pas comme juge).

Ce que la mesure a changé : pas la vitesse de travail (l'équipe travaillait déjà bien) — la lucidité collective. L'équipe voit ce qui se passe vraiment, peut le prouver, et peut en décider avec des données. C'est la définition de la lucidité opérationnelle.
