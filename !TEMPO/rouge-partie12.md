
---

# Partie 12 : Le glossaire du praticien et les réponses détaillées

## 1. Le glossaire du niveau 1, étendu

Le lexique de l'équipe (semaine 1) définit les mots de l'équipe. Ce glossaire définit les mots de la méthode — avec les distinctions fines que les équipes demandent toujours.

**Élicitation (recueillir, clarifier)** — première phase du SDLC TOTALISATION. À ne pas confondre avec la récolte de besoins (qui recueille ce qu'on dit) : l'élicitation cherche ce qui n'est pas dit. L'outil central : la question « quel problème cela résout-il ? », qui remonte de la solution demandée au problème réel.

**Spécification IF…THEN (si… alors)** — format de spécification où chaque comportement s'écrit « SI [condition], ALORS [résultat observable] ». À ne pas confondre avec la user story (qui décrit pour qui et pourquoi) : la spécification IF…THEN décrit le comportement testable. Les deux se complètent ; seule la spécification sert au Go/No-Go.

**Critère de validation** — la règle qui transforme un comportement attendu en test exécutable. Un comportement sans critère de validation est une intention ; un critère sans comportement est une contrainte technique déguisée.

**Cas limite** — la frontière du comportement : valeur nulle, volume extrême, concurrence, ordre des opérations, donnée historique. La chasse aux cas limites est la partie la plus rentable de la spécification : c'est là que les bugs vivent.

**Dérogation** — l'écart documenté à une règle : qui décide, pourquoi, jusqu'à quand, ce qu'on apprend. À ne pas confondre avec l'exception silencieuse (l'écart non écrit) : la dérogation préserve la règle en la transgressant formellement ; l'exception silencieuse tue la règle en la contournant.

**Go / No-Go** — la décision de livraison selon des critères écrits. À ne pas confondre avec la revue de sprint (qui constate) : le Go/No-Go décide. Trois résultats possibles : Go, Go avec réserves (chaque réserve : quoi, qui, quand), No-Go.

**Qualimétrie** — la pratique de mesure et de lecture des signaux au service des décisions. À ne pas confondre avec le reporting (qui décrit) : la qualimétrie déclenche. Un signal sans décision associée est de la décoration.

**Grande boucle (CONFIRMER → ÉLICITER)** — le mécanisme par lequel les apprentissages de la confirmation alimentent l'élicitation suivante. À ne pas confondre avec la rétrospective (qui regarde en arrière) : la grande boucle transforme le passé en question pour le futur.

**Chargé de livraison** — le membre de l'équipe qui anime les rituels et tient la trace, sans décider à la place du groupe. À ne pas confondre avec le chef de projet (qui décide) : le chargé anime, l'équipe décide.

**Champion** — le gardien du centre d'excellence, avec mandat écrit et temps alloué. À ne pas confondre avec le référent (l'expert qu'on consulte) : le champion maintient la mémoire, il n'est pas la mémoire.

**Centre d'excellence** — l'espace neutre qui protège les standards, décisions, spécifications et apprentissages. « Neutre » est la condition de survie : dès qu'il appartient à une fonction, il devient un outil de territoire.

**DoR (Definition of Ready, définition de prêt)** — les conditions qu'un item doit satisfaire pour entrer en itération : spécification prête, estimateur présent, dépendances résolues. Le DoR est ce qui empêche la planification du flou.

**Grande conception vs petite conception** — la distinction du niveau 1 : la grande conception (architecture, choix structurants) n'est pas le sujet du livre ; la petite conception (le comportement d'une demande) est exactement le sujet. La spécification IF…THEN est une petite conception — et les petites conceptions bien faites construisent les grandes.

**Reprise** — le travail refait parce que le résultat initial ne correspondait pas à l'attente. La métrique de la semaine 1 mesure le taux de reprises ; l'exercice E8 chiffre leur coût. La reprise est le symptôme universel du flou.

**Preuve** — un artefact daté et localisable qui étaye une affirmation. « Les tests passent » est une affirmation ; « 47/49, rapport du 03/07 14h02 » est une preuve. La règle du niveau 1 : pas de preuve, pas d'affirmation — dans les Go/No-Go, les audits, les rapports.

## 2. Les réponses détaillées aux situations fréquentes

### « Notre spécification est trop longue à écrire »

Trois vérifications, dans l'ordre : (1) la demande est-elle vraiment petite ? Si la spécification dépasse deux pages pour une demande « simple », la demande n'était pas simple — ou la spécification confond spécification et documentation. (2) Écrivez-vous les règles de validation ou les explications ? Les règles sont de l'IF…THEN sèches ; les explications sont de la prose. Coupez la prose. (3) L'élicitation a-t-elle eu lieu ? Une spécification écrite sans élicitation remplacé les questions manquantes par des hypothèses explicatives — d'où la longueur.

Le test final : le développeur lit-il la spécification avant de coder ? Si personne ne la lit, peu importe sa longueur : elle ne sert pas. Réduisez jusqu'à ce qu'elle soit lue.

### « Nos cas limites sont infinis »

Non — vos cas limites sont mal classés. Trois familles seulement comptent au niveau 1 : les données (nulles, vides, extrêmes, historiques), les flux (ordre, concurrence, interruption), les règles (exceptions, combinaisons). Chaque famille a une question type : « que se passe-t-il si la donnée est vide ? », « que se passe-t-il si deux opérations arrivent en même temps ? », « que se passe-t-il si la règle générale ne s'applique pas ? ». Trois questions, posées systématiquement, couvrent 80 % des cas limites qui coûtent.

### « Le demandeur ne sait pas ce qu'il veut »

Le demandeur sait toujours ce qu'il veut — ce qu'il ne sait pas, c'est comment le dire. L'élicitation existe pour ça. Et deux outils aident : le passé (« montrez-moi comment vous le faites aujourd'hui, à la main ») et le négatif (« qu'est-ce qui ne doit PAS arriver ? »). Les demandes impossibles à élucider après deux cérémonies d'élicitation ne sont pas des demandes : ce sont des explorations — traitez-les comme telles (spike time-boxé), pas comme des livrables.

### « Le Go/No-Go retarde tout »

Non — il rend les retards visibles. Comparez : sans Go/No-Go, les retards se paient en incidents de production (le plus cher des retards). Avec, ils se paient en attente de critères (le moins cher des retards). Et si les Go/No-Go retardent systématiquement, la question n'est pas « supprimons-les » mais « pourquoi les critères ne sont-ils pas prêts ? » — chaque retard systématique pointe un maillon faible (tests lents, environnement, données) que la suppression du rituel enterrerait en silence.

### « On perd la spontanéité »

Les rituels n'interdisent pas la spontanéité : ils la rendent inutile pour les décisions importantes. La spontanéité était souvent la seule voie d'expression d'une équipe sans rituel — et elle servait alors à la décision improvisée, la plus coûteuse des deux. Avec les rituels, la spontanéité revient là où elle est productive : l'exploration, l'innovation, la discussion. La discipline n'est pas l'ennemie de la créativité : elle est sa condition de survie dans une équipe qui livre.

### « Et si on rate une cérémonie ? »

La cérémonie ratée se rattrape, se documente, et informe. La règle : une cérémonie sautée est notée au registre avec sa raison et son rattrapage daté. Ce n'est pas la punition qui compte : c'est la visibilité. Une cérémonie sautée en silence devient la norme ; une cérémonie sautée documentée reste une exception. Et la métrique saine : le taux de cérémonies tenues par mois. En dessous de 80 %, le système est en dérive — c'est un signal, pas une faute.

### « Le niveau 2 nous apportera quoi de plus ? »

Trois choses que le niveau 1 ne peut pas donner : (1) les modèles — le processus écrit en diagrammes, discutable par tous, exécutable par les outils ; (2) l'automatisation — les tests générés à partir des modèles, la documentation synchronisée ; (3) l'échelle — ce qui marche pour une équipe peut se transmettre. Mais attention : le niveau 2 amplifie ce que le niveau 1 est. Si les rituels du niveau 1 ne tiennent pas sans le coach, le niveau 2 automatisera leur absence. Ne montez jamais pour échapper au travail de consolidation.

## 3. La boîte à mots pour les conversations

Le praticien a besoin de phrases. Voici les siennes, éprouvées :

- « Montrons-moi la preuve » — au lieu de « je ne te crois pas ».
- « C'est une dérogation, alors : qui décide, pourquoi, jusqu'à quand ? » — au lieu de « on ne peut pas ».
- « Quel problème cela résout-il ? » — au lieu de « c'est hors sujet ».
- « Et donc ? » — après chaque métrique lue, pour transformer la constatation en décision.
- « La grille ne dit pas non pour toujours : elle dit pas aujourd'hui, et voici pourquoi, et voici quand. » — le No-Go constructif.
- « Ce qui est écrit est discutable ; ce qui est oral se dispute. » — pour défendre l'écriture.
- « Faisons-le à ta façon, et mesurons. » — pour les sceptiques : la donnée tranche, pas l'argument.
- « Je ne sais pas — cherchons. » — la phrase qui construit plus de confiance que toutes les certitudes.

## 4. Le dernier mot du praticien

Le niveau 1 ne fait pas de vous un expert de la qualité. Il fait de votre équipe une équipe qui sait ce qu'elle livre, qui le prouve, et qui en parle. C'est moins que la maîtrise — et c'est plus que la plupart des organisations n'ont.

La méthode tient parce qu'elle est simple : des mots partagés, des critères écrits, des preuves visibles, des décisions documentées, des apprentissages réinjectés. Chaque pièce est évidente. L'ensemble est rare — parce que l'évident est difficile à tenir, et que le tenir, semaine après semaine, sans applaudissement, est l'art exact du praticien.

Le niveau 2 vous attend avec ses modèles, ses outils et son automatisation. Mais d'abord, terminez ce niveau : huit semaines, six fiches, un lexique vivant, une équipe qui ne dépend plus de vous. C'est la fondation. Le reste s'y construit — et rien ne s'y construit sans elle.
