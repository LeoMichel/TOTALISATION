
---

# Partie 11 : Le vécu étendu du niveau 2 — les histoires derrière les modèles

Le niveau 2 transforme les rituels du niveau 1 en système modélisé. Les histoires qui suivent racontent ce que ce passage a coûté et rapporté sur le terrain — avec les échecs qui ont forgé la méthode.

## Sherweb, l'héritage technique : quand la documentation sauve le legacy

**L'épisode étendu.** Chez Sherweb, après le retrait des QA, l'équipe a reconstruit sa qualité — mais le produit restait un legacy documenté de manière légendaire : des wiki de cinq révisions en arrière, des commentaires de code contradictoires, et un savoir oral fragile. Le tournant du niveau 2 a été un choix simple : ne plus écrire de documentation à côté du système, mais la faire dériver du système lui-même.

**La première documentation vivante.** Le modèle du processus de déploiement a été confronté (deux malentendus trouvés), et la première page de documentation en a dérivé. Elle a été relue par le support — qui a signalé deux informations manquantes. Ces deux informations ont rejoint le modèle (pas seulement la page) : la documentation et le modèle ont appris ensemble.

**Ce que cet épisode enseigne au niveau 2 :**
- La documentation vivante est la porte d'entrée la plus rentable du niveau 2 sur un legacy : elle rapporte immédiatement (le support lit), elle enrichit le modèle (les trous sont trouvés par les lecteurs), et elle prouve la valeur sans attendre l'automatisation complète.
- Le support est le premier client de la documentation vivante — et son meilleur capteur de trous. Invitez-le dès la première page.
- Ne demandez pas la documentation parfaite : demandez la documentation datée et sourcée. Une page qui cite son modèle peut être vérifiée ; une page non sourcée ne peut qu'être crue.

**Pour l'atelier :** la semaine 2 (documentation vivante) peut s'ouvrir sur cet épisode. La question aux équipes : « qui lit votre documentation aujourd'hui ? » Si la réponse est « personne », l'épisode de Sherweb donne la route : partir de ce que le support demande réellement.

## Genius Solution, la modélisation à grande échelle : trois QA, quarante développeurs, un modèle

**L'épisode étendu.** Le ratio trois pour quarante rendait impossible la qualification unitaire de chaque demande. La solution du niveau 2 a été radicale : modéliser les flux critiques de l'ERP (facturation, inventaire, taxes) et faire des modèles la source de vérité. Les développeurs ont codé contre les modèles ; les trois QA ont revu les modèles (pas les 40 flux de code) ; les tests générés ont couvert les combinaisons.

**La résistance initiale.** « Nous n'avons pas le temps de modéliser un ERP de 20 ans » — exact. L'équipe n'a pas modélisé l'ERP : elle a modélisé les trois flux où les bugs coûtaient le plus cher. Le reste du système vivait comme avant. La règle apprise : le modèle ne se déploie pas, il se choisit — là où le coût du malentendu est le plus élevé.

**Le résultat chiffré.** Sur les six mois suivant la modélisation des trois flux : les bugs de facturation ont baissé de moitié, et le temps d'onboarding d'un nouveau développeur sur ces flux est passé de six semaines à deux (le modèle était son cours).

**Ce que cet épisode enseigne au niveau 2 :**
- La modélisation est un investissement ciblé, pas un baptême général. Trois flux bien modélisés valent mieux que trente flux esquissés.
- Le modèle est aussi un outil d'onboarding : c'est le cours que les nouveaux peuvent lire. Sa valeur pédagogique rejoint sa valeur de conformité.
- Les QA deviennent des architectes de la qualité : ils modélisent, génèrent, arbitrent. Leur rareté cesse d'être un handicap quand leur rôle change.

**Pour l'atelier :** la semaine 1 (modélisation BPMN) peut utiliser ce cas pour la règle de choix des processus : « quel flux coûte le plus cher en malentendus ? Commencez par lui. »

## Opal-RT, l'automatisation en mission : le modèle qui a survécu à la production

**L'épisode étendu.** Pendant la mission Faucon, le niveau 2 a été installé en temps réel sur un produit en production active. Le modèle du processus de release a été construit, confronté, et — moment décisif — utilisé pour générer les tests de la mise en production suivante. Un test généré a détecté une configuration de déploiement que personne n'avait signalée : le chemin « déploiement avec historique de version incomplet » existait dans le modèle, pas dans les checklists manuelles.

**La discussion qui a suivi.** Le test a-t-il trouvé un bug ? Non : il a trouvé une divergence entre le modèle et la réalité — la checklist manuelle était incomplète. Le modèle a corrigé la checklist, pas le code. C'est le signe le plus sain du niveau 2 : la divergence trouve son vrai propriétaire.

**Ce que cet épisode enseigne au niveau 2 :**
- Le test généré ne trouve pas que des bugs de code : il trouve des trous de processus. Sa valeur dépasse la qualité logicielle — il audite la façon de travailler elle-même.
- La mise en production est le processus le plus rentable à modéliser : c'est là que les omissions coûtent le plus cher, et là que les checklists manuelles montrent leurs limites.
- La divergence doit être rendue à son vrai propriétaire : un test qui échoue peut signifier un bug (le code suit le modèle), un modèle périmé (le modèle suit le code), ou un processus incomplet (les deux suivent le réel). L'arbitrage est la vraie compétence du niveau 2.

**Pour l'atelier :** la semaine 3 (MBT) peut s'ouvrir sur ce cas. La question : « que ferait votre checklist de déploiement si un test généré la relisait ? »

## Le pedigree de la méthode : les épisodes qui l'ont précédée

Trois épisodes plus anciens éclairent pourquoi le niveau 2 est construit comme il l'est.

### L'échec fondateur : la documentation à côté du système

Avant TOTALISATION, la documentation était le cimetière habituel : écrite avec enthousiasme, morte en six mois. L'analyse de cet échec répété a produit le principe fondateur du niveau 2 : **la documentation qui ne dérive pas du système meurt ; la documentation dérivée survit avec lui.** Ce n'est pas une question de discipline (les gens n'ont jamais manqué de bonne volonté) : c'est une question de structure — maintenir deux sources de vérité est un travail en double qui finit toujours par être abandonné.

### La leçon du modèle manuel : le dessin qui ne servait à rien

Les premiers essais de modélisation (bien avant le niveau 2) ont produit de beaux diagrammes que personne n'utilisait — parce qu'ils décrivaient l'idéal, n'étaient jamais confrontés, et n'entraînaient rien. L'échec a forgé les règles actuelles : le modèle du réel (pas de l'idéal), la confrontation obligatoire, la mise à jour datée. Un modèle sans ces trois ingrédients est de la décoration — et l'équipe avait raison de l'ignorer.

### La découverte du langage commun : le jour où le QA a dessiné ce que le dev faisait

Le moment originel du niveau 2 est banal : un QA a dessiné, sur un coin de tableau, ce qu'il croyait que le développeur faisait. Le développeur a corrigé. Puis a dessiné ce qu'il croyait que le QA faisait. Le QA a corrigé. Quatre malentendus sont morts en quinze minutes — et aucun n'était un bug : tous étaient des divergences de mental model. Le modèle BPMN a généralisé ce coin de tableau. L'idée n'a jamais changé depuis : **faire dessiner l'un ce qu'il croit de l'autre est l'outil de réconciliation le plus rapide jamais trouvé.**

## Comment ces histoires se racontent

Chaque histoire fonctionne en ouverture d'atelier (2 minutes, désarme la résistance), en réponse à un doute spécifique (la bonne histoire au bon doute), ou en formation des nouveaux (la culture se transmet par les récits avant les règles).

Et la règle qui les gouverne : **chaque histoire raconte un coût payé.** La méthode qui en est sortie n'a pas de magie : elle a des cicatrices utiles. Le lecteur qui comprend les cicatrices comprend pourquoi chaque règle existe — et il défendra mieux une règle dont il connaît la blessure fondatrice.
