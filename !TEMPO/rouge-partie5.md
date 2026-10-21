
---

# Partie 5 : Cas réels, gabarits remplis et variantes contextuelles

Cette partie complète les huit semaines par ce qu'un livre d'atelier ne peut pas montrer autrement : ce que les gabarits donnent **remplis**, ce que les ateliers donnent **vécus**, et comment le parcours s'adapte aux contextes qui ne ressemblent pas au cas idéal.

**Comment l'utiliser :** les gabarits remplis (§1) montrent le niveau de détail attendu — copiez la forme, jamais le contenu. Les cas vécus (§2) montrent les situations réelles derrière les capsules ; ils servent de miroir, pas de script. Les variantes (§3) adaptent le parcours sans le dénaturer : la règle du livrable et l'honnêteté des preuves ne se négocient jamais.

## 1. Les gabarits remplis d'exemples réels

Chaque gabarit est présenté en deux versions : le gabarit vide (à copier) et un exemple rempli tiré de la mission Faucon (à comparer). La règle d'usage : **l'exemple montre le niveau de spécificité attendu ; le vôtre doit être aussi concret, jamais identique.**

### 1.1 Charte de mission — exemple rempli

> Exemple réel (anonymisé) de la mission Faucon, semaine 1. Comparez avec votre contexte : les différences sont normales, le niveau de spécificité est la cible.

**Charte de mission : implémentation de TOTALISATION, équipe pilote**

**Objectif :** installer les fondations minimales de TOTALISATION pour l'équipe pilote de la plateforme de simulation temps réel, en 8 semaines, et produire à chaque semaine un livrable publié.

**Durée :** 8 semaines, du 15 juin au 7 août.

**Rôles :**
- Sponsor : la directrice qualité (débloque, endosse, protège l'équipe des priorités concurrentes)
- Coach : le coach qualité externe, rejoint en semaine 4 par le coach agile interne (facilitent, ne produisent pas les livrables)
- Équipe pilote : 1 tech lead, 3 développeurs, 2 analystes QA, 1 analyste fonctionnel (produisent les livrables, portent la pratique)
- Chargé de livraison (à partir de la semaine 7) : l'analyste fonctionnel, volontaire identifié en semaine 2

**Règles :**
1. Chaque semaine produit un livrable publié dans le centre d'excellence (espace Confluence neutre).
2. Les irritants nomment des systèmes, jamais des personnes.
3. Le canal de communication unique : le canal Teams « Équipe pilote TOTAL ».
4. Les décisions sont écrites, datées et publiées — même les décisions de ne pas décider.

**Ce qui n'est pas dans le périmètre :** les autres équipes, l'outillage d'automatisation (niveau 2), les choix d'architecture.

**Signature :** sponsor (15 juin) — coach (15 juin) — équipe (16 juin)

**Pourquoi cet exemple marche :** le périmètre d'exclusion est explicite (dernière section). Sans lui, la charte promet tout et l'équipe se fera tirer hors périmètre dès la semaine 3.

### 1.2 Carte des irritants — exemple rempli

> Résultat de l'atelier 1.2 de la mission Faucon. Notez la formulation : système, pas personne.

| # | Irritant (formulation système) | Impact estimé | Vote |
|---|---|---|---|
| 1 | « Les spécifications n'existent pas avant le code ; le besoin vit dans la tête du PO » | Reprises fréquentes, tests à l'aveugle | 7/9 |
| 2 | « La priorité des bugs dépend de qui crie le plus fort » | Travail urgent en continu, planification impossible | 6/9 |
| 3 | « On découvre les problèmes à la mise en production, pas avant » | Confiance érodée, mises en production anxiogènes | 6/9 |
| 4 | « Personne ne sait qui décide quoi entre QA et dev » | Conflits de territoire, décisions retardées | 4/9 |
| 5 | « Les décisions prises en réunion ne sont pas notées » | Mêmes débats chaque mois | 3/9 |

**Ce que le top 3 a décidé du parcours :** les irritants 1, 2 et 3 correspondent exactement aux semaines 2 (spécifications et bugs) et 3 (Go/No-Go) du livre. Ce n'est pas un hasard : c'est ainsi que la séquence des semaines a été conçue. Si votre top 3 est différent, adaptez l'emphase des semaines — mais ne sautez pas de semaine, car les dépendances restent.

### 1.3 Lexique officiel — extraits remplis

> Extraits du lexique v0.1 de la mission Faucon. Chaque entrée a sa source (qui a tranché, quand).

| Terme | Décision de l'équipe | Source |
|---|---|---|
| **Terminé** | « Terminé » = code mergé + tests passés + spécification vérifiée conforme. Toute autre utilisation est interdite dans les tickets. | Équipe entière, 17 juin |
| **Bug critique** | Un défaut qui rend une fonctionnalité promettable inutilisable pour au moins un client réel, ou qui corrompt des données. « Chez nous » n'est pas un client réel. | Équipe + sponsor, 18 juin |
| **Spécification** | Document court (max 2 pages) qui contient : contexte, besoin utilisateur, comportement attendu, règles de validation, cas limites. Une user story n'est pas une spécification. | Analyste fonctionnel + tech lead, 18 juin |
| **Livraison** | Mise à disposition aux clients réels, pas « mergé sur main ». | Tech lead, 19 juin |

**Pourquoi la source compte :** six mois plus tard, quand quelqu'un contestera la définition de « terminé », la source indique que l'équipe entière a tranché le 17 juin — et non que le coach l'a imposée. La contestation s'adresse alors à l'équipe, pas au processus.

### 1.4 Grille Go/No-Go — exemple rempli

> Grille de la mission Faucon, semaine 3, appliquée à la première livraison réelle.

| Critère | Preuve attendue | Résultat | Verdict |
|---|---|---|---|
| Tests passés | Rapport d'exécution lié au ticket | 47/49 — 2 échecs analysés (défauts connus, non bloquants) | ✅ avec réserve |
| Bugs critiques | Requête Jira | 0 critique, 1 majeur reporté avec dérogation écrite | ✅ |
| Spécification conforme | Diff entre spécification et code, revue faite | Conforme, 2 écarts mineurs corrigés en revue | ✅ |
| Risques connus | Liste des risques + décision du décideur | 1 risque assumé (performance sous charge extrême, test impossible cet environnement) | ⚠️ assumé par écrit |
| Note de diffusion | Document de version | Rédigée, clients identifiés | ✅ |

**Décision : Go avec réserves.** Réserve 1 : le risque performance est assumé par le décideur, avec plan de test dès l'environnement disponible (échéance 3 semaines). Réserve 2 : le bug majeur reporté est suivi au tableau, réévaluation à la prochaine itération.

**Compte rendu archivé le jour même.** Ce compte rendu a été consulté trois semaines plus tard, quand la question de la performance est remontée : la réserve écrite a transformé un conflit potentiel (« on savait ! » / « non, on savait pas ! ») en lecture de document.

### 1.5 Rapport de maturité — squelette rempli

> Structure de l'annexe A7, illustrée par des extraits du rapport de la mission Faucon.

**1. Contexte initial (extrait) :** « En juin, l'équipe ne disposait d'aucune spécification antérieure au code, priorisait les bugs selon la pression de l'appelant, et découvrait les problèmes en production. Les trois irritants du top 3 correspondaient à ces trois constats. »

**2. Audit des 7 éléments (extraits avec preuves) :**

| Élément | Niveau | Preuve |
|---|---|---|
| Spécification IF…THEN | 2 | 14 spécifications écrites avant le code depuis la semaine 2 ; 2 ont été contestées et corrigées en revue |
| Go/No-Go | 2 | 6 livraisons passées par la grille ; 1 No-Go documenté (semaine 6) ; 3 réserves écrites |
| Qualimétrie | 2 | Métrique de reprise passée de 31 % à 12 % ; tableau consulté spontanément chaque vendredi |
| Centre d'excellence | 1→2 | 23 artefacts publiés ; 4 consultations par des non-membres de l'équipe pilote |

**3. Ce qui reste fragile (extrait) :** « La métrique de temps de cycle est collectée manuellement chaque vendredi ; si le responsable est absent, elle saute. Trois sauts en huit semaines. Action : automatiser la collecte avant l'étape du niveau 2. »

**4. Recommandation (extrait) :** « Poursuivre vers le niveau 2 avec cette équipe, avec un contrat qualité v2.0 et l'automatisation de la métrique comme prérequis. Ne pas étendre à une deuxième équipe avant que la collecte des métriques soit automatique. »

## 2. Cas vécus étendus : la mission Faucon, semaine par semaine

Les capsules des semaines racontent l'essentiel. Ces cas étendus ajoutent ce que les capsules ne pouvaient pas contenir : les chiffres, les décisions alternatives, ce qui aurait pu se passer autrement. Ils servent de miroir : cherchez le moment de votre propre parcours qui ressemble le plus à chaque cas.

### Cas de la semaine 2 : la spécification qui a divisé l'équipe

**Situation.** La première spécification avant code portait sur une demande « simple » : l'ajout d'un champ de filtre sur un rapport existant. Le tech lead estimait la tâche à 2 heures ; l'analyste fonctionnel a passé 3 heures à écrire la spécification.

**Le conflit.** En revue, le tech lead a contesté : « Pour un filtre, on n'écrit pas deux pages. C'est du sur-traitement. » L'analyste a répondu : « La spécification fait une page et demie, et elle contient trois cas limites que tu n'avais pas identifiés. » Le ton est monté. Le coach est resté silencieux — c'était l'atelier du conflit, pas celui du document.

**La résolution.** Le groupe a lu la spécification cas limites par cas limites : les trois cas (filtre sur valeur nulle, filtre combiné avec un filtre existant, filtre sur données historiques migrées) étaient réels — le second avait déjà causé une reprise six mois plus tôt. Le tech lead a conclu : « OK pour ce cas-là. Mais pour les vraies simples, une demi-page suffit. » L'équipe a écrit cette règle au lexique : *la longueur de la spécification suit la complexité, pas la cérémonie*.

**Ce que ce cas enseigne.**
- Le conflit sur la forme cache presque toujours un conflit sur le fond : ici, le tech lead défendait sa vitesse perçue, l'analyste défendait la prévention de la reprise. Les deux avaient raison sur des plans différents.
- La règle qui sort du conflit (*la longueur suit la complexité*) vaut mieux qu'une décision imposée par le coach : elle appartient à l'équipe.
- Un cas limité déjà causé par une reprise passée est l'argument le plus convaincant de tous — mieux qu'un principe de méthode.

**Variante à surveiller :** si l'analyste fonctionnel n'avait pas identifié le cas du filtre combiné (parce qu'il ne le savait pas), la spécification aurait validé un comportement faux. C'est pourquoi l'atelier 2.3 exige la revue multi-rôles : la spécification n'est pas le produit d'une personne, c'est le produit d'une confrontation.

### Cas de la semaine 3 : le premier No-Go

**Situation.** La livraison de la semaine 3 passait la grille — sauf un test d'intégration qui échouait de manière intermittente (1 fois sur 20 environ). Le tech lead proposait de livrer : « C'est un flakiness d'environnement, pas un bug. On livre et on regarde. »

**Le dilemme.** La grille disait « 100 % passés » pour l'intégration. Respecter la grille signifiait un No-Go pour un échec peut-être sans signification. Violenter la grille signifiait poser le précédent : la grille cède sous la pression.

**La décision.** L'équipe a pris une troisième voie, devenue sa règle standard : **No-Go formel, avec dérogation documentée en trois parties** — le diagnostic (test intermittent, reproduction 1/20, environnement suspecté), le risque assumé (défaut réel possible, probabilité faible, impact limité), la condition de levée (investigation du flakiness dès lundi, livraison corrective sous 48 h si défaut confirmé). Le décideur a signé la dérogation. La livraison a eu lieu sous dérogation, pas sous exception silencieuse.

**Le dénouement.** Le défaut était réel — une course conditionnelle (race condition) rare. L'équipe a corrigé en 2 jours. Le Go de la semaine suivante a été le premier « Go sans réserve » du projet.

**Ce que ce cas enseigne.**
- Une grille stricte n'est pas une grille qui bloque : c'est une grille qui oblige à écrire ce qu'on assume. La dérogation écrite est le mécanisme qui rend la rigueur compatible avec la réalité.
- Le No-Go « formel avec dérogation » préserve deux choses à la fois : la valeur de la grille (elle n'a pas cédé) et la capacité de livrer (le Go a eu lieu). Un No-Go absolu aurait été rigide ; un Go silencieux aurait été un précédent.
- Le test intermittent est toujours un test qui vous parle. Ici, il parlait d'une race condition. À vous de l'entendre.

### Cas de la semaine 5 : la réunion où personne n'est venu

**Situation.** Au cœur du point mort, l'atelier du mardi a commencé avec 2 personnes sur 7. Les autres étaient en production urgente — une mise en production de la veille posait problème.

**La tentation.** Annuler l'atelier, reporter à la semaine suivante, « puisque personne ne peut venir ». Le coach a hésité — c'est exactement le moment où un parcours s'arrête en douceur.

**La décision.** L'atelier a eu lieu à 2 : les routines minimales (revue du tableau, spécification de la demande en cours) ont été tenues, abrégées. Les 5 absents ont reçu un résumé de 10 lignes le soir même, avec la mention explicite : « atelier tenu en effectif réduit, rien d'abandonné, tout est décalé d'un jour ». Le jeudi, l'atelier plein a repris le programme complet.

**Ce que ce cas enseigne.**
- Le point mort n'attend pas que vous soyez disponibles : il frappe pendant l'urgence. La routine minimale tenue à 2 vaut mieux que l'atelier complet annulé.
- La communication de ce qui a été tenu (et de ce qui a été décalé) est ce qui empêche l'effet boule de neige : sans le résumé, les absents concluent que « l'atelier saute quand c'est dur », et la semaine suivante, ils sautent aussi.
- Le coach qui annule transmet le message le plus dangereux : la méthode est un fair-weather practice. Le coach qui tient à 2 transmet le contraire.

### Cas de la semaine 7 : le cycle incomplet

**Situation.** Le cycle complet de la semaine 7 (6 phases sans coach) s'est arrêté à la phase CONFIRMER : la diffusion a eu lieu le vendredi matin, mais le retour du terrain n'arriverait pas avant le mardi suivant — après la fin officielle de la semaine.

**Le dilemme.** Déclarer le cycle complet (la diffusion a eu lieu) ou déclarer le cycle incomplet (CONFIRMER n'a pas pu se faire).

**La décision.** L'équipe a déclaré le cycle **incomplet sur un point précis** : « CONFIRMER reporté au mardi, tout le reste est complet ». Le report a été noté dans le centre d'excellence, et le mardi suivant, le retour du terrain a été recueilli et la grande boucle a été refermée en 30 minutes.

**Ce que ce cas enseigne.**
- L'honnêteté sur l'incomplet vaut mieux que la complétude cosmétique. « Complet sauf CONFIRMER reporté avec date » est une information exploitable ; « complet » faux est une pollution du centre d'excellence.
- La grande boucle refermée en retard vaut mieux qu'une grande boucle jamais refermée : le report de 4 jours n'a rien coûté ; un CONFIRMER sauté aurait coûté la leçon du cycle entier.
- C'est la réponse concrète à la question que les équipes posent toujours : « et si on n'a pas le temps de tout faire ? » — la réponse est : faire tout ce que vous pouvez, et nommer précisément ce que vous ne faites pas.

### Cas de la semaine 8 : la direction qui demandait les chiffres

**Situation.** À la remise du rapport de maturité, le VP a demandé : « Tout ça c'est bien, mais le ROI ? Vous me montrez ça en euros ? »

**Le risque.** Inventer un ROI : des chiffres flatteurs sur des bases fragiles se retournent contre le programme dès la première contestation.

**La réponse donnée.** L'équipe a répondu en trois points : (1) les métriques de mouvement mesurées — reprise de 31 % à 12 %, temps de cycle stable malgré l'ajout des spécifications, 1 seul incident en production en 8 semaines contre 3 sur les 8 semaines précédentes ; (2) les coûts mesurés — environ 15 % de la capacité de l'équipe consacrée aux pratiques pendant le parcours ; (3) ce qui n'était pas encore mesurable — l'effet sur les prochaines livraisons, avec la promesse d'un point à 3 mois. Le VP a répondu : « Les 12 %, ça me parle. Le reste, on en reparle à 3 mois. »

**Ce que ce cas enseigne.**
- Le ROI honnête se construit sur trois colonnes : gagné mesuré, coût mesuré, pas encore mesurable (avec échéance). Les deux premières colonnes ont plus de poids que n'importe quelle projection.
- La promesse d'un point à 3 mois transforme une exigence impossible (« prouvez tout maintenant ») en engagement vérifiable. C'est une structure gagnante pour toute conversation de fin de parcours.
- Ne jamais présenter un chiffre que vous ne pouvez pas défendre : un chiffre contesté et tombé décrédibilise tout le programme, y compris les chiffres qui étaient bons.

## 3. Variantes contextuelles

Les 8 semaines supposent un contexte « standard » : une équipe colocalisée, un produit en développement actif, un sponsor disponible, un legacy modéré. Ces variantes adaptent le parcours aux contextes réels, sans dénaturer ses principes. **La règle du livrable et l'honnêteté des preuves ne s'adaptent jamais.**

### Variante V1 : petite équipe (2 à 4 personnes)

**Ce qui change :** la densité. Chacun porte plusieurs rôles ; les ateliers de groupe perdent leur sens.

- Fusionnez les ateliers : la semaine se réduit à 2 ateliers de 90 minutes au lieu de 3-4.
- Le « sponsor » peut être la personne à qui vous rendez des comptes, même si ce n'est pas son titre.
- Le rôle de chargé de livraison tourne chaque semaine dès la semaine 3 (au lieu d'attendre la 7) : tout le monde apprend à animer tôt.
- Les capsules de revue multi-rôles deviennent une auto-revue structurée : le même joueur joue les trois rôles, à des moments séparés, par écrit.

**Ce qui ne change pas :** la spécification avant le code, la métrique regardée, la grille Go/No-Go. Une équipe de 2 qui les tient est plus mûre qu'une équipe de 15 qui les joue.

### Variante V2 : équipe distribuée ou télétravail

**Ce qui change :** les rituels synchrones coûtent plus cher.

- Le constat de terrain (1.2) devient un journal individuel écrit sur 3 jours, puis un atelier de regroupement.
- Le point de qualité passe en asynchrone la plupart des semaines : chacun écrit son commentaire sur la métrique avant vendredi midi ; l'animateur synthétise et publie la décision. Une session synchrone par mois reste irremplaçable.
- Le Go/No-Go reste synchrone : c'est une conversation de décision, elle ne s'écrit pas.
- Les post-its deviennent un tableau blanc numérique ; la règle « écrit en silence, puis partagé » est encore plus importante à distance, où les voix fortes dominent encore plus qu'en présentiel.

**Ce qui ne change pas :** les livrables écrits et publiés. À distance, ils sont même plus importants : c'est ce qui empêche la session vidéo de devenir de la fumée.

### Variante V3 : legacy lourd (produit ancien, peu de tests, documentation obsolète)

**Ce qui change :** le point de départ. Vous ne spécifiez pas le comportement existant — vous le découvrez en spécifiant.

- La semaine 2 s'étend sur deux semaines si nécessaire : la première spécification porte sur un comportement existant à clarifier (pas sur une nouvelle demande). Écrire la spécification de ce que le système fait *aujourd'hui* est l'exercice le plus rentable du parcours sur un legacy lourd.
- Les cas de validation existants sont rares : commencez par des tests de caractérisation (le test qui enregistre le comportement actuel sans juger s'il est bon). Ils rendent les refactorisations futures possibles.
- La carte du SDLC (semaine 4) mettra en évidence le sentiment de « personne ne comprend le système » : c'est normal, c'est le point de départ. Le livrable est la carte de ce qu'on ne sait pas.
- Attendez-vous à un point mort plus tôt et plus rude : le legacy résiste. La semaine 5 peut arriver en semaine 4. C'est correct.

**Ce qui ne change pas :** l'honnêteté du constat. Sur legacy lourd, la tentation de maquiller la situation est maximale — et le coût du maquillage aussi.

### Variante V4 : organisation réglementée (processus formels, traçabilité obligatoire)

**Ce qui change :** le surplus de formalisme existe déjà — le risque n'est pas le désordre, c'est le formalisme mort.

- Les gabarits de TOTALISATION doivent être mappés sur les exigences réglementaires dès la semaine 1 : montrez que la spécification IF-THEN *est* votre exigence de conception documentée, que le Go/No-Go *est* votre revue formelle. TOTALISATION ne remplace pas la conformité : il la rend vivante.
- Le lexique officiel devient un document réglementaire : les définitions ont un poids d'audit. Choisissez-les avec encore plus de soin.
- La dérogation écrite est un outil précieux dans ce contexte : elle est souvent le seul moyen légitime de documenter un écart acceptable.
- Les rituels existent déjà sous forme de revues formelles : TOTALISATION les rend utiles au lieu d'ajouter des rituels.

**Ce qui ne change pas :** la règle du livrable vivant. La conformité mort-vive (documents écrits pour l'auditeur, jamais lus) est précisément ce que le parcours combat : un document qui sert à décider satisfait l'auditeur gratuitement.

### Variante V5 : le sponsor sceptique

**Ce qui change :** la source d'énergie du parcours. Sans sponsor enthousiaste, le carburant vient de la preuve.

- La semaine 1 se termine par une micro-démonstration : pas une présentation, un artefact (la carte des irritants, le lexique). Le scepticisme se traite par l'artefact, pas par l'argument.
- Chaque fin de semaine produit un « fait de la semaine » : une phrase, mesurable, envoyée au sponsor. Pas un rapport : une phrase. (« Cette semaine : 4 spécifications écrites avant le code, 2 reprises évitées. »)
- Le remontage de la semaine 5 devient crucial : le sponsor sceptique qui reçoit des demandes avec preuves à la semaine 5 devient souvent le sponsor le plus engagé de la suite — s'il a reçu des faits toutes les semaines avant.
- Le test de réussite du sponsor sceptique : il cite spontanément un de vos faits dans une réunion où vous n'êtes pas. C'est le moment où le scepticisme a changé de camp.

**Ce qui ne change pas :** l'honnêteté des chiffres. Le sponsor sceptique cherche une raison de vous croire ; un seul chiffre gonflé lui donne sa raison de ne plus jamais le faire.

### Variante V6 : reprise après un échec précédent

**Ce qui change :** la mémoire du terrain. Une tentative précédente a échoué, et tout le monde s'en souvient.

- La semaine 1 commence par une rétrospective honnête de l'échec précédent : qu'est-ce qui a été tenté, où ça a cassé, qu'est-ce qui est différent cette fois ? Sans cette rétrospective, chaque participant teste silencieusement si « c'est encore une mode qui va passer ».
- Le premier livrable doit être visible rapidement : la crédibilité se construit sur la première preuve, pas sur le plan.
- Les personnes les plus sceptiques sont vos meilleurs capteurs : elles détectent la dérive du programme avant tout le monde. Invitez-les à le dire explicitement — « dis-nous quand tu vois le pattern de l'échec précédent ».
- Ne reniez pas l'échec précédent : la pratique qui a survécu à l'échec précédent est probablement bonne. La reprise qui part de ce qui a survécu est plus solide que celle qui part de zéro.

**Ce qui ne change pas :** la règle du livrable. Après un échec, c'est la seule promesse crédible.

---

## Comment utiliser cette partie

- **Avant de commencer le parcours** : lisez les variantes qui correspondent à votre contexte (V1-V6). Elles ajustent vos attentes.
- **Pendant le parcours** : quand un atelier bloque, cherchez le cas vécu correspondant — le miroir des situations réelles donne des pistes que le descriptif d'atelier ne contient pas.
- **À la semaine 8** : comparez vos gabarits remplis avec les exemples. Si les vôtres sont moins spécifiques, ce n'est pas un échec : c'est la mesure du chemin restant.

Les gabarits vides sont dans les annexes A4 à A7. Cette partie vous montre ce qu'ils donnent une fois remplis — par une vraie équipe, dans un vrai contexte, avec les vraies difficultés. C'est tout ce qu'un livre peut faire de plus.
