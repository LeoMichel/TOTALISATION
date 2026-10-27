
---

# Partie 20 : Les fautes du praticien du niveau 6

Cette partie est le miroir du praticien du niveau 6 : les erreurs réelles qui détruisent la prévention. Les cinq fautes principales, documentées avec leurs conséquences.

## Faute 1 : le praticien qui anticipe à la place de l'équipe

**Le contexte.** Une équipe (9 personnes) au début du niveau 6. Le praticien (venu du niveau 5) voit les signaux partout et les nomme lui-même : « le build va ralentir », « cette API va devenir un goulot », « cette documentation va diverger ».

**Ce qui s'est passé.** L'équipe a cessé d'observer. Chaque signal était nommé par le praticien, chaque chantier de prévention était posé par le praticien, chaque morsure était mesurée par le praticien. Au mois 3, l'équipe a arrêté de signaler : pourquoi observer si le praticien voit tout ?

**La découverte.** Le praticien a quitté pour deux semaines. Pendant son absence, aucun signal n'a été nommé — parce que l'équipe n'avait plus l'habitude d'observer. Les deux semaines d'absence ont produit un incident que le praticien aurait vu en 5 minutes s'il était là.

**La réparation.** Le praticien est revenu avec une discipline : ne plus jamais nommer à la place. Écouter, questionner, reformuler — laisser nommer. Six semaines pour que l'équipe reprenne l'habitude d'observer. Au mois 8, l'équipe nommait 3 signaux par semaine sans le praticien.

**La leçon de la faute.** Le praticien qui anticipe à la place de l'équipe fabrique une équipe aveugle — et l'équipe aveugle ne voit que ce que le praticien voit. La prévention réelle est celle qui se transmet (l'expression à l'équipe), pas celle qui se centralise (l'expression au praticien).

## Faute 2 : le praticien qui confond prévention et prudence

**Le contexte.** Une équipe (12 personnes) au niveau 6 depuis 4 mois. Le praticien fait des réunions de prévention où il dit : « attention au déploiement », « attention à l'API », « attention à la migration ». Chaque attention est un conseil — jamais un chantier.

**Ce qui s'est passé.** Au mois 4, l'équipe a cessé d'écouter. Chaque conseil était une inquiétude — jamais une action. Les incidents sont arrivés (le build, l'API, la migration), et l'équipe a découvert que les conseils du praticien étaient justes. Trop tard.

**La découverte.** Le praticien, dans son bilan, a réalisé : il avait fait 12 avertissements et posé 0 chantier. Les 12 avertissements avaient été corrects. Zéro avait été traité.

**La réparation.** Le praticien a appris la différence : la prudence est une parole (attention), la prévention est une discipline (SI rien n'est fait, ALORS — chantier, porteur, preuve, échéance). Neuf avertissements sont devenus 9 chantiers de prévention, avec des porteurs et des échéances. Trois ont été traités. Six ont été abandonnés (pas de temps disponible) — et documentés comme tels.

**La leçon de la faute.** Le praticien qui confond prévention et prudence fabrique de l'inquiétude — jamais de la prévention. La prévention est une discipline : le SI/ALORS, le chantier, le porteur, la preuve, l'échéance, la morsure. Le conseil est une parole qui se dissipe dans l'air.

## Faute 3 : le praticien qui surveille au lieu de veiller

**Le contexte.** Une équipe (8 personnes) au niveau 6 depuis 6 mois. Le praticien a installé un dashboard : les temps de réponse, les taux d'erreur, les temps de build. Chaque valeur est vérifiée manuellement chaque jour.

**Ce qui s'est passé.** Les valeurs étaient dans les seuils — toujours. Mais une tendance se montait : le temps de build passait de 28 à 42 minutes en 8 semaines. Le praticien ne l'a pas vu, parce que chaque valeur était dans le seuil. L'incident est arrivé au mois 8 (build 55 minutes — dépassement).

**La découverte.** Le praticien, dans son bilan, a réalisé : il avait surveillé (les valeurs vs les seuils) mais pas veillé (les tendances). 8 semaines de montée, visibles dans les données — jamais vues, parce que chaque valeur était dans le seuil.

**La réparation.** Le praticien a installé la veille : la lettre hebdomadaire qui montre les tendances (pas seulement les valeurs), les marges (la distance au seuil), et les projections (« dans 4 semaines, la valeur sera X »). La première lettre a révélé 2 tendances montantes — traitées avant les incidents.

**La leçon de la faute.** Le praticien qui surveille au lieu de veiller voit les dépassements — jamais les montées avant les dépassements. La veille regarde le futur (les tendances, les projections) ; la surveillance regarde le présent (les valeurs, les seuils). Une lettre de veille qui ne montre que les valeurs est une surveillance déguisée.

## Faute 4 : le praticien qui documente à la place de l'équipe

**Le contexte.** Une équipe (10 personnes) au niveau 6 depuis 8 mois. Le praticien documente tout : les entrées de mémoire, les gabarits, les lettres de veille, les projections. Chaque document est bien écrit, bien structuré, bien relié.

**Ce qui s'est passé.** L'équipe a cessé de documenter. Pourquoi documenter si le praticien le fait ? Au mois 10, le praticien a pris un mois de congé — et la mémoire a cessé de se mettre à jour. Les apprentissages du mois n'ont pas été documentés. Les consultations de mémoire ont trouvé les entrées obsolètes.

**La découverte.** Le praticien, à son retour, a réalisé : il avait documenté à la place de l'équipe — et l'équipe n'avait plus la pratique. La mémoire était riche mais morte : elle dépendait d'une personne.

**La réparation.** Le praticien a cessé de documenter (sauf les entrées qu'il a lui-même initiées). L'équipe a repris la documentation, avec un gabarit simple (une entrée = une page, pas quatre). Au mois 14, l'équipe documentait 3 entrées par semaine sans le praticien.

**La leçon de la faute.** Le praticien qui documente à la place de l'équipe fabrique une mémoire morte — et une mémoire morte ne protège pas. La mémoire réelle est celle qui se transmet (l'équipe documente), pas celle qui se centralise (le praticien documente).

## Faute 5 : le praticien qui fait du niveau 6 une technique au lieu d'une discipline

**Le contexte.** Une équipe (14 personnes) au niveau 6 depuis 12 mois. Le praticien a installé les techniques : les gabarits de signal, les gabarits de chantier, les gabarits de mémoire, les lettres de veille, les projections. Tout est en place. Tout est utilisé.

**Ce qui s'est passé.** L'équipe a suivi les techniques. Les gabarits étaient remplis, les lettres étaient envoyées, les projections étaient faites. Mais les pratiques de prévention (l'observation, l'anticipation, la morsure) n'étaient pas vécues — elles étaient exécutées. Au mois 14, l'équipe a demandé : « est-ce qu'on peut arrêter les gabarits ? On ne voit plus à quoi ça sert. »

**La découverte.** Le praticien, dans son bilan, a réalisé : il avait installé les techniques (les gabarits, les lettres, les projections) sans installer la discipline (l'observation, l'anticipation, la morsure). Les techniques sans la discipline sont des formalités — et les formalités sont abandonnées.

**La réparation.** Le praticien a repris la discipline : les ateliers de prévention (l'observation réelle, pas les gabarits), la morsure mesurée (la valeur réelle, pas le chiffre), la transmission (l'équipe qui nomme, pas le praticien qui remplit). Au mois 18, les techniques étaient utilisées comme outils de la discipline — pas comme fin en soi.

**La leçon de la faute.** Le praticien qui fait du niveau 6 une technique fabrique des formalités — jamais une prévention. La discipline (l'observation, l'anticipation, la morsure) est la substance ; les techniques (les gabarits, les lettres, les projections) sont les outils. Les outils sans la substance sont vides.

## La synthèse des cinq fautes

**Faute 1** : le praticien anticipe à la place de l'équipe → l'équipe aveugle.
**Faute 2** : le praticien confond prévention et prudence → l'inquiétude sans l'action.
**Faute 3** : le praticien surveille au lieu de veiller → les dépassements sans les montées.
**Faute 4** : le praticien documente à la place de l'équipe → la mémoire morte.
**Faute 5** : le praticien fait du niveau 6 une technique → les formalités sans la discipline.

**La même correction pour les cinq fautes** : le praticien se met au service de la discipline (l'équipe observe, la prévention est une discipline, la veille regarde le futur, l'équipe documente, la substance avant les outils) — et la prévention devient réelle.

---

*Fin des fautes du praticien du niveau 6.*
