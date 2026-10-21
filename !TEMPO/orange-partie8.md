
---

# Partie 8 : Approfondissements techniques du niveau 2

Cette partie traite en profondeur les sujets que les capsules ne font qu'effleurer : la granularité du BPMN, les pièges du MBT en pratique, la versioning des modèles, et les questions que les équipes posent toujours.

## 1. La granularité du BPMN : où s'arrêter

La question la plus fréquente du niveau 2 : « Jusqu'où détailler le modèle ? » Trop grossier, le modèle ne révèle rien ; trop fin, il devient une charge de maintenance et meurt en trois mois.

### Le critère de granularité

Un élément du modèle mérite d'exister si l'un de ces trois critères est rempli :

1. **Il porte un malentendu potentiel.** Si deux rôles peuvent diverger sur ce qui se passe à cette étape, elle mérite d'être un élément explicite. C'est le critère principal : le modèle existe pour rendre discutable ce qui ne l'était pas.
2. **Il conditionne le flux.** Une passerelle (décision) est toujours explicite — c'est là que les processus divergent réellement. Une passerelle implicite dans la description orale est presque toujours un malentendu en attente.
3. **Il produit ou consomme un artefact vérifiable.** Une étape qui produit une spécification, un test, une preuve mérite d'être visible : elle est le point d'attache de la traçabilité.

Tout le reste se résume dans le nom de la tâche. Une tâche « Traiter la demande » qui cache quatre sous-étapes sans malentendu ni artefact reste une tâche.

### Le test de la mauvaise granularité

Trois symptômes d'un modèle trop fin :
- Le modèle n'a pas changé depuis un mois alors que le processus a évolué. La maintenance ne suit plus : le modèle est déjà en train de mourir.
- Personne ne sait lire le modèle sans son auteur. Un modèle illisible sauf par son créateur est un piège, pas un actif.
- Les discussions sur le modèle portent sur la notation, pas sur le processus. Quand l'équipe dispute des symboles, le modèle est devenu un sujet au lieu d'être un instrument.

Trois symptômes d'un modèle trop grossier :
- La confrontation des rôles ne trouve jamais rien. Si trois sessions consécutives ne révèlent aucun écart, le modèle est trop grossier — les malentendus se cachent dans les tâches-résumés.
- Le modèle ne mentionne aucun artefact. Si aucune tâche ne produit ou ne consomme quelque chose de vérifiable, la traçabilité n'a pas de point d'attache.
- Les nouveaux arrivants posent des questions que le modèle devrait répondre. Si l'onboarding pose les mêmes questions chaque mois, le modèle est trop superficiel pour servir de référence.

### La règle pratique

Commencez grossier, puis affine seulement là où un malentendu apparaît. Le modèle du premier mois est volontairement superficiel : il est le squelette. Chaque malentendu détecté est l'occasion d'affiner l'élément concerné. Ainsi, la granularité suit la valeur découverte — le modèle se développe exactement là où il rapporte, jamais ailleurs. C'est la seule façon dont un modèle reste vivant dans une équipe qui a autre chose à faire.

## 2. Le MBT en pratique : ce que les tutoriels ne disent pas

La génération de tests à partir de modèles (Model-Based Testing) est présentée dans les tutoriels comme un pipeline magique : modèle → tests → exécution. La pratique est plus nuancée. Voici ce que l'expérience enseigne.

### Ce que le MBT fait bien

- **Les combinaisons.** Le modèle énumère systématiquement les combinaisons de passerelles que l'expérience humaine ne pense pas à tester. C'est sa valeur principale, et elle est réelle : le cas T-042 en est la preuve type.
- **Les chemins rares.** Les flux qui n'arrivent que dans 5 % des cas sont précisément ceux que les tests manuels oublient. Le modèle les traite comme les autres.
- **La régression structurelle.** Quand le modèle change, les tests régénérés couvrent le nouveau comportement sans réécriture manuelle. C'est le lien entre le modèle vivant et la suite de tests vivante.

### Ce que le MBT ne fait pas

- **Il ne trouve pas les bugs de données.** Un modèle décrit des flux logiques, pas des valeurs. Les bugs de données (format, encodage, bornes) restent du domaine des tests écrits à la main. Le MBT les ignore silencieusement — ne comptez pas sur lui pour cette famille.
- **Il ne remplace pas les tests d'expérience utilisateur.** Un flux correct logiquement peut être une catastrophe à utiliser. Le MBT valide le modèle, pas l'expérience.
- **Il ne valide pas la pertinence du modèle.** Si le modèle est faux, les tests générés sont faux de la même façon — et ils passeront, donnant une confiance imméritée. C'est le piège majeur : le MBT amplifie la qualité du modèle, bonne ou mauvaise. D'où la règle : la confrontation du modèle (capsule 2.2) précède toujours la génération.

### Le ratio honnête à présenter

Chaque campagne de génération doit documenter trois nombres : tests produits, tests sélectionnés, tests utiles (ceux qui ont trouvé un défaut). Le ratio de la mission Faucon — 40 produits, 12 sélectionnés, 1 utile — est représentatif d'une première campagne. Il est honnête et il suffit : un bug trouvé par une combinaison que personne n'aurait écrite est une valeur réelle, et le rapport qui le dit tel quel est crédible. Les campagnes suivantes s'améliorent (le ratio monte vers 1 utile pour 10 sélectionnés) — mais c'est la courbe qui convainc, pas le nombre absolu.

### Quand ne PAS faire du MBT

Le MBT a un coût d'installation. Il ne vaut la peine que si :
- Le modèle existe déjà et est vivant (confronté, maintenu). Faire du MBT pour justifier le modèle est un sophisme — le modèle se justifie par les malentendus qu'il révèle, pas par les tests qu'il génère.
- Le domaine a une vraie explosion combinatoire. Si le processus a 3 passerelles et 5 chemins, écrire les tests à la main est plus rapide que monter le pipeline.
- L'équipe maintiendra. Un pipeline de génération non maintenu produit des tests obsolètes en silence — le même poison que le modèle non maintenu, en pire.

Dans les autres cas : écrivez les tests à la main, gardez le modèle pour ce qu'il fait de mieux — rendre le processus discutable.

## 3. Le versioning des modèles : la mémoire du processus

Un modèle vivant change. La question n'est pas de l'empêcher de changer, mais de garder la mémoire de ce qui a changé et pourquoi. Sans mémoire, le modèle perd sa valeur d'actif organisationnel : on ne sait plus pourquoi le processus est ce qu'il est.

### Ce qu'il faut versionner

Trois informations par changement :

1. **Le quoi** : l'élément modifié, l'ancienne et la nouvelle forme. C'est le minimum technique — tout outil de versioning le fait.
2. **Le pourquoi** : la divergence détectée qui a motivé le changement. C'est l'information que les outils ne capturent pas, et c'est la plus précieuse : six mois plus tard, « pourquoi cette étape a-t-elle bougé ? » a une réponse.
3. **Le qui** : pas pour blâmer — pour savoir qui interroger. La personne qui a fait le changement est celle qui connaît le contexte.

### La pratique légère

Pas besoin d'outils sophistiqués : un fichier de changements à côté du modèle suffit.

```
# Changements — BPM-004 (processus de correction de bug)
## 2025-07-12 — révision 3
Quoi : la passerelle « criticité » passe avant la qualification (avant : après)
Pourquoi : les bugs critiques étaient traités après les non-critiques en pratique ;
          le modèle mentait. Aligné sur le réel, discuté en atelier du 09/07.
Qui : S.M. (dev), validation L.T. (QA)

## 2025-06-28 — révision 2
Quoi : ajout de la tâche « spécification courte » (conditionnelle : seulement
       si le correctif touche un comportement documenté)
Pourquoi : divergence trouvée en confrontation dev/QA — le modèle binaire
           (toujours/jamais) ne reflétait pas le réel conditionnel.
Qui : L.T. (QA)
```

Ce fichier est la mémoire vivante du processus. Sa valeur apparaît dans trois situations : l'arrivée d'un nouveau (qui lit l'historique au lieu de poser des questions), le retour d'un ancien (qui voit ce qui a changé depuis son départ), et l'audit (qui trouve la traçabilité déjà faite).

### L'anti-pattern : le versioning sans mémoire

Un modèle versionné par l'outil (v1, v2, v3...) sans fichier de changements est une collection d'instantanés sans explication. La question « pourquoi la révision 3 a-t-elle bougé la passerelle ? » n'a pas de réponse — et sans réponse, la tentation est de revenir en arrière « parce que c'était mieux avant », sans savoir pourquoi c'avait changé. La mémoire du pourquoi est ce qui empêche le ping-pong des décisions.

## 4. Les questions que tout le monde pose

Ces questions reviennent dans presque chaque mission du niveau 2. Voici les réponses qui ont fonctionné.

### « On modélise tout le processus de l'entreprise ? »

Non. On modélise les processus où les malentendus coûtent cher — typiquement les processus inter-équipes (dev/QA/support, dev/ops), les processus où les nouveaux posent toujours les mêmes questions, et les processus qui produisent des artefacts vérifiables. Un processus que une seule personne fait de bout en bout, sans artefact ni malentendu, n'a pas besoin de modèle — le modéliser est du rituel, pas de l'ingénierie.

Le test de sélection : « Quel processus nous a coûté le plus cher en malentendus l'an dernier ? » C'est lui, le premier modèle. Le deuxième suit la même règle.

### « Le modèle devient obsolète dès qu'on le finit »

C'est le symptôme d'un modèle sans propriétaire ni moment de maintenance. Le modèle vit dans le cycle : chaque divergence détectée est corrigée dans la semaine (capsule 2.7). Si personne n'a ce rôle, le modèle meurt — et il vaut mieux le savoir tôt : un modèle mort est pire qu'aucun modèle, car il inspire une confiance imméritée.

La prévention : le modèle a un propriétaire nommé, un moment de maintenance hebdomadaire (même 15 minutes), et la règle de la semaine. Un modèle sans ces trois éléments est un document mort en attente de déclassification.

### « Le client ne veut pas voir nos modèles »

Le client n'a pas à voir les modèles internes — il voit leurs effets : la documentation claire, les réponses factuelles, les plans honnêtes. Si le client veut voir le modèle (certains veulent, surtout en réglementé), c'est un bonus — mais ce n'est jamais le but. Le but du modèle est interne : rendre le processus discutable entre les rôles qui le vivent.

L'exception : le processus inter-organisations (vous et le client faites ensemble un processus) — là, le modèle partagé est l'outil de coordination, et sa valeur est directe.

### « On a déjà de la documentation, on repart de zéro ? »

Non. La documentation existante est l'inventaire de départ. Le premier atelier du niveau 2 peut être : prenez votre documentation la plus consultée, trouvez son modèle (s'il existe), vérifiez-la contre le modèle. Les divergences trouvées justifient la suite. Si la documentation est orpheline (sans modèle), elle est marquée « à lier » — et la priorisation des liens suit la même règle : ce qui est le plus consulté d'abord.

### « Combien de temps pour le niveau 2 ? »

Huit semaines à raison d'une demi-journée par semaine, comme le niveau 1 — mais avec plus de profondeur par session. Le facteur limitant n'est pas le temps des sessions : c'est la discipline de maintenance entre les sessions. Une équipe qui fait les sessions mais ne maintient pas entre elles termine avec des modèles morts à la semaine 8, quelle que soit la qualité des ateliers.

L'indicateur d'avancement honnête n'est pas « la semaine n est faite » : c'est « le modèle est toujours vivant à la semaine n ». Un modèle vivant à la semaine 8 vaut mieux que quatre modèles morts.

### « On saute directement au niveau 3 ? »

Le niveau 3 (intégration continue, automatisation avancée) présume le niveau 2 : des modèles vivants, maintenus, avec génération fonctionnelle. Monter au niveau 3 sur des modèles morts est construire sur du sable : l'automatisation amplifie exactement ce que le modèle est, vivant ou mort.

Le test d'éligibilité au niveau 3 : le modèle a-t-il survécu trois mois sans le coach ? Si oui, le niveau 3 est raisonnable. Si non, consolidez d'abord — la consolidation est toujours moins chère que la reconstruction.

---

## Comment utiliser cette partie

- **Au démarrage** : la section 1 (granularité) prévient l'erreur la plus coûteuse du niveau 2.
- **À la semaine 5-7** : la section 2 (MBT) aide à décider si le MBT vaut la peine — et à le présenter honnêtement sinon.
- **En continu** : la section 3 (versioning) est la pratique qui maintient les modèles vivants au-delà de la mission.
- **Quand une question bloque** : la section 4 contient les réponses aux questions que tout le monde pose.
