
---

# Partie 7 : Le vécu étendu — les histoires derrière la méthode

La méthode TOTALISATION n'est pas née d'une théorie : elle a crystallisé sur trente ans de terrain. Cette partie raconte les épisodes fondateurs — avec leurs échecs, leurs tensions et leurs leçons — et relie chacun à un atelier du livre. Ces histoires sont le matériau des capsules : le lecteur qui les connaît comprend *pourquoi* chaque atelier existe.

## Rayduf : l'origine du contrôle qualité (avant l'informatique)

**L'épisode.** Avant l'informatique, il y a eu le sous-sol de Rayduf : l'oncle qui montait des systèmes de son à partir de pièces récupérées, câblait des amplificateurs, et faisait tester le résultat au jeune neveu. « Vas-y, mets-en fort, et dis-moi si ça grésille. » L'enfant montait le volume, écoutait, décrivait. Rayduf ajustait. Encore. Encore. Le standard du son propre n'était pas écrit nulle part : il était dans l'oreille qui savait ce qu'elle cherchait, et dans la boucle tester-ajuster-retester.

**Ce que le jeune apprenait sans le savoir :**
- La qualité est une boucle, pas un verdict. On teste, on ajuste, on reteste. Personne ne « passe » un ampli au premier coup.
- Le critère est dans l'usage, pas dans la construction. Ce n'est pas Rayduf qui jugeait son ampli : c'est l'oreille de l'usage.
- Tester tôt est une gentillesse. Tester la construction de l'autre, dans son sous-sol, n'était pas un contrôle hostile : c'était la façon dont on construisait ensemble.

**Le lien avec le livre.** La cérémonie de Confirmation (cérémonie 6) est la boucle de Rayduf industrialisée : on livre, l'usage juge, on ajuste. Et la posture du testeur — celui qui met en fort et dit si ça grésille — est la posture du QA TOTALISATION : celle qui fait écouter la vérité du produit, pas celle qui pointe les fautes.

**Pour l'atelier :** la semaine 2 (spécification avant le code) peut s'ouvrir sur cette histoire. Elle désarme la résistance habituelle (« les tests nous ralentissent ») : Rayduf ne ralentissait pas, il construisait — et il construisait bien parce qu'il testait en continu.

## Exaxe : le produit sans propriétaire

**L'épisode.** Chez Exaxe, le produit d'assurance existait, se vendait, et personne ne pouvait dire ce qu'il faisait exactement. Le code avait des années, les documents avaient des hivers, et chaque modification révélait une surprise. Les développeurs experts devinaient ; les nouveaux priaient. Le QA testait ce qu'il trouvait, faute de savoir ce qui était attendu.

**La leçon du malentendu permanent :** une équipe peut livrer depuis des années et ne jamais avoir partagé une compréhension commune de son propre produit. La connaissance était distribuée, jamais consolidée — chaque départ de personne était une amputation de mémoire.

**Le lien avec le livre.** C'est l'argument le plus fort de la spécification avant le code (semaine 2) : non pas la discipline, mais la mémoire. Une spécification est un acte de mémoire collective : elle rend explicite ce qui ne vivait que dans des têtes.

**Pour l'atelier :** en semaine 1, demander à chaque participant : « décris en trois phrases ce que fait notre produit » — puis constater les divergences. L'exercice fait l'économie de trois mois de conviction : les équipes voient leur Exaxe intérieur.

## CGI : la paix des braves et le stop qualité

**L'épisode.** Chez CGI, le QA vivait dans une paix des braves : il ne remontait rien de dérangeant, les développeurs ne demandaient rien de contraignant, et les livraisons sortaient « correctes » dans un sens que personne ne définissait. Puis un jour, le QA a arrêté de jouer : il a mis un stop réel sur une livraison qui ne remplissait pas les critères. Le choc a été violent — parce que personne n'avait jamais pris le droit.

**Ce que l'épisode enseigne :**
- La paix des braves n'est pas la paix : c'est une trêve qui durera jusqu'au premier incident grave. Le stop n'est pas une déclaration de guerre : c'est le retour du contrat.
- Le QA qui ne dit jamais non n'est pas un QA tolérant : il est un QA qui n'existe pas. Son approbation ne vaut rien, puisqu'elle est inconditionnelle.
- Le droit de dire non se gagne en deux temps : d'abord par les critères écrits (le non n'est pas personnel, il est procédural), ensuite par les preuves (le non est documenté, discutable, réversible par la dérogation).

**Le lien avec le livre.** Le rituel Go/No-Go (semaine 3, cérémonie 5) est l'institutionnalisation du stop de CGI : il transforme le conflit personnel en vérification de critères. Le décideur dit non ? Il cite la grille. Personne n'est en guerre : le contrat parle.

**Pour l'atelier :** la checklist de la semaine 3 peut citer ce cas. La question aux équipes qui redoutent le Go/No-Go : « votre paix actuelle, elle tient quand le client crie ? »

## Desjardins : le sabotage par le flou

**L'épisode.** Chez Desjardins, le coach QA est arrivé avec un mandat clair — et a découvert que chaque effort d'amélioration était sabordé par une forme invisible de résistance : les réunions reportées, les accès refusés, les priorités qui changeaient, les informations qui n'arrivaient pas. Rien n'était hostile en apparence. Tout était orienté.

**Ce que l'épisode enseigne :**
- Le sabotage n'est pas toujours malveillant : il est souvent la défense des intérêts structurés par le flou. Ce qui n'est pas écrit peut toujours être renégocié — et celui qui renégocie le mieux gagne.
- La première défense n'est pas la persuasion : c'est l'écriture. Charte signée, critères documentés, décisions notées. Ce qui est écrit est plus difficile à saborder — non pas impossible, mais coûteux.
- Les demandes écrites avec preuve (la semaine 5) sont l'outil anti-sabotage par excellence : elles obligent le saboteur à s'expliquer par écrit, ce qu'il évite par nature.

**Le lien avec le livre.** La règle des irritants (semaine 1) — « ils nomment des systèmes, pas des personnes » — prend ici son sens profond : le sabotage est un système, et il se documente comme tel. La remontée au sponsor avec preuves (semaine 5) est la contre-attaque : non pas se plaindre, mais facturer.

**Pour l'atelier :** en semaine 5, ce cas est la capsule naturelle. Les équipes qui traversent leur point mort découvrent souvent leur Desjardins intérieur : le flou organisé qui protège les habitudes.

## Sherweb : reprendre après le retrait des QA

**L'épisode.** Chez Sherweb, les QA ont été retirés (réduction budgétaire) et l'équipe a découvert que la qualité, qui existait « parce que les QA en gardaient la garde », n'existait plus du tout. Les développeurs, sans filet, ont découvert qu'ils ne savaient pas tester — pas parce qu'ils étaient incompétents, mais parce qu'ils n'avaient jamais eu à le faire systématiquement.

**Ce que l'épisode enseigne :**
- La qualité déléguée n'est pas la qualité acquise. Quand la qualité est le métier de quelqu'un d'autre, personne ne l'apprend.
- Le retrait brutal est une révélation, pas une catastrophe : il montre l'état réel de la compétence. L'incident qui suit est le diagnostic gratuit.
- La reprise se fait par la compétence distribuée : chacun apprend à tester son propre travail, avec des critères écrits — pas en réembauchant les gardiens.

**Le lien avec le livre.** La spécification IF…THEN… (semaine 2) est l'outil de la compétence distribuée : quand le critère de validation est écrit, chacun peut tester — y compris celui qui code. Les critères écrits sont ce qui rend la qualité indépendante des gardiens.

**Pour l'atelier :** en semaine 2, ce cas répond à la question fréquente : « mais alors les QA ne servent plus à rien ? » Réponse : les QA ne disparaissent pas, ils changent de métier — de gardiens à auteurs de critères, de testeurs de derniers recours à concepteurs de la testabilité.

## Petal : la culture qui fait le travail

**L'épisode.** Chez Petal, la qualité n'était pas un département : c'était une posture commune. Les questions de qualité venaient de tout le monde, dans toutes les réunions, pas seulement des QA. L'encyclopédie interne du produit documentait les concepts ; les nouveaux la lisaient ; les anciens l'entretenaient. Le QA y était un catalyseur, pas un contrôleur.

**Ce que l'épisode enseigne :**
- La qualité est une propriété de la culture, pas une fonction de l'organigramme. Quand tout le monde pose les questions de qualité, les QA peuvent se concentrer sur les questions difficiles.
- La documentation vivante (l'encyclopédie) est l'infrastructure de la culture commune : elle donne un lieu au savoir partagé, et un rite (l'entretenir).
- Le catalyseur est le rôle QA adulte : celui qui rend les autres capables plutôt que celui qui les juge.

**Le lien avec le livre.** Le centre d'excellence (semaine 3, cérémonie 3) est l'institutionnalisation de la culture Petal : l'espace neutre où la mémoire commune vit. Et la posture du champion (semaine 8) est le catalyseur nommé.

**Pour l'atelier :** en semaine 3, ce cas définit le centre d'excellence par le positif : avant de dire ce qu'il fait (garde les artefacts), dire ce qu'il est (l'endroit où la culture du produit vit).

## Genius Solution : trois QA pour quarante développeurs

**L'épisode.** Chez Genius Solution (monde ERP), trois QA pour quarante développeurs : le ratio faisait rire — ou pleurer. Le QA ne pouvait pas tester tout ; les devs livraient plus vite que toute organisation de tests. La solution n'a pas été de tester plus, mais de faire tester par la structure : critères écrits dans les tickets, tests automatisables, et le fameux concours de bugs qui a transformé la détection en jeu collectif.

**Ce que l'épisode enseigne :**
- Le ratio QA/dev n'est pas une fatalité : c'est une conséquence du modèle de qualité. Avec des critères écrits et une qualité distribuée, trois QA peuvent porter quarante développeurs. Sans, quarante QA n'y suffiraient pas.
- Le jeu est un outil sérieux : le concours de bugs (recompenser la découverte documentée) a fait de la détection une activité valorisée au lieu d'une accusation. La gamification n'est pas de la légèreté : c'est de l'ingénierie des incitations.
- L'automatisation n'est pas un substitut de la culture : elle suit. On automatise ce qui est déjà systématique à la main.

**Le lien avec le livre.** Le flux de bugs avec critères écrits (semaine 2, atelier 2.2) est la version minimale de la découverte Genius : les critères remplacent le corps-de-garde. Et la qualimétrie (cérémonie 7) est la suite : mesurer la détection pour la valoriser.

**Pour l'atelier :** en semaine 2, ce cas répond à « on n'a pas assez de QA ». La vraie question n'est jamais le nombre de QA : c'est la proportion de critères écrits.

## Opal-RT : la preuve par la mission

**L'épisode complet.** Chez Opal-RT, tout ce qui précède a convergé : le mandat clair (six semaines pour implémenter TOTALISATION), l'équipe pilote réelle, le sponsor engagé, les rituels installés, la traversée (la semaine 5 y a été une perte de temps avant d'être un virage), le contrat signé, la gouvernance durable. La mission a prouvé que la méthode tient hors du livre — et elle a produit le livre.

**Ce que l'épisode enseigne (la synthèse des synthèses) :**
- La méthode est transmissible en six semaines *si* l'équipe pilote est réelle et le sponsor réel. Sinon, six ans.
- Le point mort est le rite de passage : chaque équipe qui a traversé a acquis l'autonomie ; chaque équipe qui l'a évité l'a reportée.
- La qualité devient vivante le jour où les gens la défendent sans qu'on leur demande — le jour où un développeur refuse de livrer sans spécification, de lui-même.

**Pour l'atelier :** toute la Partie 5 (cas réels) est la version étendue de cette histoire. Ce récit final sert de synthèse au lecteur qui arrive à la semaine 8 : la méthode que vous venez de pratiquer a déjà prouvé ce qu'elle promet.

## Comment utiliser ces histoires

Chaque histoire peut être racontée en ouverture de l'atelier correspondant (2 minutes), en réponse à une résistance (la bonne histoire au bon moment désarme mieux que l'argument), ou en formation des nouveaux (les histoires sont la culture qui s'apprend avant les règles).

Et la règle qui les gouverne toutes : **une histoire qui n'a pas coûté quelque chose n'enseigne rien.** Celles-ci ont toutes coûté — du temps, de la crédibilité, de la patience. C'est pourquoi elles se transmettent.
