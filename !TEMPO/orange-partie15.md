
---

# Partie 15 : Les réponses du praticien du niveau 2

Les questions que le praticien du niveau 2 affronte, avec les réponses éprouvées. Le niveau 2 a ses propres résistances — plus subtiles que celles du niveau 1, car elles s'habillent souvent en accord de principe.

## « Les modèles, c'est bien pour les équipes juniors »

La résistance la plus coriace : elle vient des seniors, elle est argumentée, et elle contient une part de vérité (un senior a moins de malentendus qu'un junior — avec les autres seniors). La réponse éprouvée : le senior n'a pas de malentendu avec lui-même, mais il en a avec le reste du monde — le PO qui change une règle sans le dire, le support qui comprend autre chose, le nouveau qui hérite d'un implicite. Le modèle n'est pas pour lui : il est pour la frontière de son expertise. La démonstration qui fonctionne : faire dessiner au senior ce qu'il croit que le PO fait (il se trompe presque toujours), et réciproquement.

Et l'argument de l'héritage : l'expertise tacite ne survit pas au départ. Le modèle est la forme que prend l'expertise quand elle accepte d'être transmissible. Ce n'est pas une perte de statut : c'est un passage du statut de sorcier au statut d'enseignant — le second est plus rare et plus précieux.

## « On modélise, mais on n'a jamais le temps de maintenir »

Cette phrase honnête mérite une réponse honnête : alors ne modélisez pas. Un modèle non maintenu est un mensonge qui inspire une confiance imméritée — pire qu'absent. La vraie question : pourquoi la maintenance ne se fait-elle pas ? Trois causes typiques : le modèle est trop gros (réduisez-le), personne ne le possède (nommez un binôme), la maintenance n'a pas de moment (greffez-la sur un rituel existant). Si aucune de ces causes n'est traitable, le problème n'est pas le modèle : c'est la capacité — et c'est une conversation de sponsor, pas un problème d'équipe.

La règle du praticien : ne défendez jamais un modèle mourant. Marquez-le « non fiable » publiquement (c'est honnête), et rouvrez la modélisation quand la capacité existe. Un modèle mort que personne ne croit est neutre ; un modèle mort que les gens croient est toxique.

## « Notre domaine est trop complexe pour un diagramme »

Le test de cette objection : complexe pour un diagramme, ou complexe pour une page ? Le niveau 2 ne demande pas un diagramme unique du monde entier : il demande un diagramme par processus discutable. Un domaine complexe a souvent des processus simples noyés dans un réseau complexe — modélisez les processus un à un. Et la complexité du domaine est exactement l'argument pour la modélisation : plus le domaine est complexe, plus le malentendu coûte cher, plus la confrontation rapporte.

Si le processus lui-même est vraiment d'une complexité non modélisable (une page impossible), c'est un diagnostic : le processus est probablement incohérent par lui-même. Le modèle ne crée pas la complexité — il la rend visible, ce qui est inconfortable pour les systèmes qui prospèrent dans l'invisibilité.

## « L'IA écrit de meilleures spécifications que nous »

Cette objection est nouvelle et elle mérite la nuance exacte. L'IA écrit des spécifications plus rapides, plus uniformes, souvent mieux rédigées. Mais la spécification n'est pas une rédaction : c'est une décision partagée. La spécification qui a de la valeur est celle que le PO, le dev, le QA et le demandeur ont négociée — parce que c'est cet accord qui prévient le malentendu, pas le texte lui-même. Une spécification parfaite écrite par l'IA et lue par personne ne prévient rien.

Le bon usage (déjà dans les règles du niveau 2) : l'IA produit des premiers jets, des variantes, des vérifications de cohérence — et l'équipe valide en confrontant à son modèle et à son demandeur. La règle du niveau 2 (l'IA assiste, l'équipe décide) est exactement la bonne frontière. La conversation avec les enthousiastes de l'IA : « oui, et alors qui a signé ? » — la signature est la prévention.

## « Le MBT ne trouve jamais rien chez nous »

Trois diagnostics possibles, à éliminer dans l'ordre : (1) votre domaine a-t-il une vraie combinatoire ? Si le processus a deux passerelles, le MBT ne peut rien trouver que vous ne sachiez — ne forcez pas. (2) Vos jeux de données sont-ils réalistes ? Le MBT avec des données triviales teste des chemins vides — la génération est correcte, les données sont le problème (l'atelier B traite ça). (3) Vos tests générés tournent-ils vraiment ? Un test généré non intégré au pipeline est un test fantôme — vert, invisible, inutile.

Si les trois diagnostics sont éliminés et que le MBT ne trouve toujours rien, alors le ratio honnête (produits / gardés / utiles) le documente : le MBT n'est pas rentable pour ce domaine — et le documenter est une connaissance, pas un échec. La méthode qui documente ses propres limites est la seule que la direction puisse croire.

## « Nos documents vivants sont lus par personne, on arrête ? »

D'abord diagnostiquer pourquoi : mauvais niveau (trop détaillé pour la lecture, trop vague pour l'action), mauvais endroit (personne ne cherche là), mauvaises questions (la doc répond à ce que personne ne demande). L'atelier C (documentation orientée lecteur) fait ce diagnostic avec trois lecteurs réels. Après correction, si la lecture ne vient pas, la règle du niveau 2 est sans pitié : taillez. La documentation se taille comme un arbre — ce qui reste est plus fort. Et la métrique honnête : les questions réelles qui reçoivent une réponse de la doc. C'est la seule mesure qui compte.

## « Le plan lié nous ralentit »

Vérifier le coût réel : la liaison (relier chaque élément à son modèle) prend quelques minutes par élément, une fois. Ce qui ralentit, c'est ce que la liaison révèle : les éléments sans modèle, les modèles périmés, les spécifications fantômes. Le plan lié ne ralentit pas le travail — il révèle la vitesse réelle. Et l'alternative (le plan décoré) donne une illusion de vitesse dont le coût arrive en fin de trimestre, chiffré et inévitable.

La question de retour au sceptique : « préférez-vous un plan lent et vrai, ou un plan rapide et faux ? » La plupart des directions, une fois la question posée honnêtement, choisissent la vérité — c'est la seule question qui laisse au décideur son vrai pouvoir.

## « On est au niveau 2, quand passe-t-on au 3 ? »

Le test des six questions (E12) — pas le calendrier. Et surtout, la question à retourner : « pourquoi le niveau 3 ? » Si c'est pour la cadence (les livraisons régulières), vérifier que les modèles tiennent sans effort. Si c'est pour l'automatisation poussée, vérifier que les tests générés ont déjà prouvé leur ratio. Si c'est parce que « le niveau suivant, c'est la progression », alors la réponse est : le niveau suivant n'est pas une récompense, c'est une construction — on monte quand le niveau courant tient debout sans soutien, et pas un jour avant.

La règle du praticien : le saut prématuré est la cause de mort la plus fréquente des programmes. Le niveau 3 construit sur le niveau 2 comme le niveau 2 sur le niveau 1 : ce qui manque en dessous se paie au-dessus, au centuple.

## La conversation que le praticien redoute : « et vous, vous partez quand ? »

La réponse honnête du niveau 2 : le praticien part quand les six questions du test sont réussies sans lui pendant un trimestre complet. Pas avant — un départ prématuré condamne les rituels à dépendre de la volonté (qui fléchit toujours) au lieu de la structure (qui tient). Pas après non plus : le praticien qui reste devient la béquille qu'il avait promis de retirer, et chaque semaine supplémentaire enseigne le contraire de la méthode.

Le mandat du niveau 2 : construire les rituels modélisés, les tester sans soi, transmettre à l'équipe voisine, partir. La tristesse du départ est réelle ; elle est aussi le signe que le programme a réussi — l'équipe qui regrette le coach est l'équipe qui ne l'a plus besoin.

## Le dernier mot du praticien du niveau 2

Le niveau 2 a transformé vos rituels en système : des modèles vivants, des spécifications dérivées, des tests générés et triés, une documentation qui vit, un plan qui se vérifie, une confirmation qui enrichit. Ce système est plus que la somme des rituels du niveau 1 — il est devenu un organisme qui se maintient, se mesure, et se transmet.

Ce que le niveau 3 (JAUNE) ajoutera : la cadence. Les rituels deviennent des processus à rythme constant ; les livraisons se cadencent ; l'équipe prouve son autonomie dans la durée. Mais le niveau 3 ne remplacera jamais ce que le niveau 2 a construit : la vérité modélisée. Le niveau 3 forge — et on ne forge que du métal déjà extrait.

Continuez. Le niveau 2 que vous venez de construire est la colonne vertébrale de tout ce qui suit.
