
---

# Partie 14 : Les ateliers d'approfondissement du niveau 2

Six ateliers de trois heures pour les équipes qui veulent creuser chaque facette du niveau 2. Chaque atelier a sa question centrale, son exercice principal, et son livrable concret.

## Atelier A : Le modèle comme instrument de design

**La question centrale :** peut-on concevoir une fonctionnalité sur le modèle AVANT d'écrire du code ?

**L'exercice (150 minutes).** Une demande réelle en attente. Les équipes construisent d'abord le modèle du processus modifié (le chemin actuel du BPMN, la variante désirée), puis dérivent la spécification, puis les cas limites. Le code n'est écrit qu'à la troisième heure — et seulement pour le chemin principal.

**La comparaison qui enseigne :** le même exercice sans modèle (à l'ancienne). Les participants mesurent la différence : la version modélisée a trouvé deux cas limites en amont (la passerelle du processus modifié), la version directe les a découverts en implémentation. Le coût des mêmes cas limites : 10 minutes sur le modèle, 2 heures en code.

**Le livrable :** la spécification dérivée de l'atelier, avec son gabarit rempli (fiche 9). Si elle est réellement implémentée, le calendrier du trimestre la contiendra avec sa référence de modèle.

**Le point de vigilance :** le modèle de design ne remplace pas l'élicitation — il l'outille. La demande est toujours discutée avec le demandeur ; le modèle rend la discussion concrète (les passerelles sont visibles), pas abstraite (les exigences en prose).

## Atelier B : Le MBT avancé — combiner, prioriser, tracer

**La question centrale :** comment la génération produit-elle une couverture que l'écriture manuelle ne peut pas atteindre ?

**L'exercice (150 minutes).** Un modèle à 4 passerelles imbriquées (16 combinaisons théoriques). Les participants listent d'abord à la main les combinaisons qu'ils testeraient (la moyenne : 5). Puis la génération produit les 16 (ou plus, selon les données de test). Puis le tri : les 16 sont classés. Le test final : combien des combinaisons générées n'étaient pas dans la liste manuelle ? (La réponse typique : 8 à 10 — dont une qui révèle une vraie question.)

**La discussion sur les données de test :** les combinaisons générées ne valent que si les données de test sont réalistes. L'exercice inclut la rédaction des jeux de données pour chaque test gardé — et la découverte que les jeux réalistes sont plus longs à écrire que les tests eux-mêmes. C'est ici que l'IA du registre aide (la génération de jeux de données plausibles) — avec la vérification humaine qui reste obligatoire.

**Le livrable :** la campagne de tri de l'atelier, avec son rapport (fiche 10), et les jeux de données des tests gardés, intégrés au dépôt.

**Le point de vigilance :** la combinatoire complète n'est pas toujours nécessaire — c'est exactement le rôle du tri. Mais sans génération, les combinaisons non écrites sont des combinaisons inconnues : l'équipe ne peut même pas décider de les ignorer. La génération transforme « je n'ai pas pensé à ce cas » en « j'ai examiné ce cas et décidé ».

## Atelier C : La documentation orientée lecteur

**La question centrale :** qui lit la documentation, et que lui manque-t-il ?

**L'exercice (120 minutes).** Trois lecteurs réels (ou simulés : support, nouveau dev, demandeur) reçoivent les trois pages les plus lues de la documentation. Chaque lecteur cherche la réponse à une vraie question (les questions réelles de la semaine). L'équipe observe : chaque échec de réponse est classé (trou, jargon, mauvais niveau, périmé).

**La reprise structurée :** chaque échec rejoint le modèle (si le trou vient du modèle), le gabarit (si le trou vient de la génération), ou la rédaction (si la page dérive du modèle mais répond mal). Les trois sources de correction sont distinguées — sinon tout devient « il faudrait réécrire », qui ne se fait jamais.

**Le livrable :** les pages corrigées, et la règle d'orientation : les questions réelles de la semaine alimentent la documentation suivante (la question est une unité de documentation, pas le sujet).

**Le point de vigilance :** la documentation vivante n'est pas une documentation complète. Le test n'est pas « tout est documenté » mais « les questions posées ont des réponses ». La complétude est un mythe ; l'utilité est une pratique.

## Atelier D : Les métriques du niveau 2 et leur anti-jeu

**La question centrale :** comment mesurer sans détruire ce qu'on mesure ?

**L'exercice (150 minutes).** Les équipes reçoivent les six métriques de leur tableau de bord (fiche 12) et jouent les deux rôles : celui qui optimise les métriques (une semaine de travail), puis celui qui détecte l'optimisation perverse. L'anti-jeu est riche :

- Le ratio de tri baissé en supprimant la génération des chemins complexes (les tests nuls disparaissent, mais les chemins ne sont plus couverts).
- Les flaky réduits en désactivant les tests instables (le signal disparaît avec le problème).
- Les modèles « confrontés < 30 jours » maximisés par des confrontations fictives de 10 minutes.
- Le pipeline accéléré en réduisant la couverture.

**La contre-mesure à chaque fois :** chaque métrique a une métrique jumelle qui détecte son abus (le ratio de tri avec la couverture des chemins ; les flaky avec le nombre de tests actifs ; les confrontations avec les divergences trouvées — une confrontation sans divergence est suspecte, cf. l'anti-pattern 1).

**Le livrable :** le tableau de bord révisé avec ses métriques jumelles, et la règle du duo : chaque métrique du niveau 2 est publiée avec sa jumelle. Une métrique seule est un outil de manipulation ; un duo est un outil de pilotage.

**Le point de vigilance :** le tableau de bord sert la semaine suivante, pas le management. S'il devient un rapport de gestion, il sera optimisé pour le management — et perdra sa fonction. Les métriques jumelles le protègent aussi de ça : le management qui veut un joli chiffre reçoit aussi son jumelle qui raconte la vérité.

## Atelier E : Le niveau 2 sans coach

**La question centrale :** que reste-t-il de la méthode quand le coach n'est plus là ?

**L'exercice (150 minutes).** Le coach (ou le porteur de méthode) est volontairement exclu de l'atelier. L'équipe rejoue une semaine type du niveau 2 (confrontation, spécification dérivée, tri, confirmation) sans lui. Un observateur note chaque moment où l'équipe a cherché le coach (même un regard) : ce sont les dépendances.

**L'analyse :** chaque dépendance est soit une lacune de rituel (la documentation de la méthode est insuffisante), soit une lacune de rôle (personne ne porte la responsabilité). Les lacunes de rituel se corrigent en écrit (le gabarit existe-t-il ? la règle est-elle nommée ?) ; les lacunes de rôle se corrigent en nomination (le propriétaire du modèle, le maître du tri, le responsable du tableau).

**Le livrable :** les rôles nommés (avec des noms, pas des sigles), et la page de méthode de l'équipe — leur résumé du niveau 2 en une page, écrit par eux (pas copié de la guidance ; l'écriture est l'exercice).

**Le point de vigilance :** la méthode sans coach n'est pas la méthode avec coach plus du silence : c'est une méthode simplifiée mais tenue. Il vaut mieux trois rituels tenus que six rituels dont deux se désagrègent. L'atelier E est aussi le moment de tailler : quels rituels sont essentiels, lesquels peuvent être simplifiés pour la tenue à long terme ?

## Atelier F : La transmission à l'équipe voisine

**La question centrale :** comment le niveau 2 se propage-t-il sans s'appauvrir ?

**L'exercice (150 minutes).** Les participants préparent et jouent la transmission : chaque binôme joue l'équipe voisine qui découvre la méthode (le premier modèle, la première confrontation). Les transmetteurs jouent leur rôle avec les contraintes réelles : l'équipe voisine est occupée, sceptique, et a déjà « essayé des méthodes ».

**Ce que l'exercice révèle :** la transmission ne passe pas par l'exposé (les sceptiques écoutent poliment et continuent comme avant). Elle passe par le premier modèle de l'équipe voisine : le moment où TOUTE l'attention va à LEUR processus, pas à votre méthode. La règle apprise : parlez 20 % du temps, modélisez 80 % du leur.

**Le livrable :** le plan de transmission de l'équipe voisine réelle (qui, quand, quel processus), et la révision de la démonstration (1 heure, Partie 13, §4) avec les leçons de l'atelier.

**Le point de vigilance :** la transmission est un investissement de l'équipe qui transmet (un binôme en observateur pendant deux semaines). Si l'équipe n'a pas ce budget, la transmission attendra — une méthode transmise en survol s'appauvrit en se propageant, et une méthode appauvrie est pire qu'une méthode absente (elle discrédite la riche).

## Le programme des six ateliers

| Atelier | Durée | Livrable principal | Moment conseillé |
|---|---|---|---|
| A — Modèle comme design | 3 h | Spécification dérivée d'une demande réelle | Mois 2 |
| B — MBT avancé | 3 h | Campagne de tri + jeux de données | Mois 3 |
| C — Documentation orientée lecteur | 2 h | Pages corrigées + règle d'orientation | Mois 4 |
| D — Métriques et anti-jeu | 3 h | Tableau de bord avec métriques jumelles | Mois 5 |
| E — Sans coach | 3 h | Rôles nommés + page de méthode | Mois 6 |
| F — Transmission | 3 h | Plan de transmission de l'équipe voisine | Mois 7 |

**La règle du programme :** un atelier par mois, jamais deux — l'approfondissement ne remplace pas la pratique, il l'accompagne. Les équipes qui rattrapent deux ateliers en une semaine en sortent avec pas des compétences.
