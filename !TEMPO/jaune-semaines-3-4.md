---

## Semaine 3 : La qualimétrie N3 et les signaux de décision

**Objectif de la semaine :** installer la qualimétrie de niveau 3 : des métriques qui déclenchent des décisions, pas des tableaux décoratifs. Répondre à la question : « quels signaux nous disent que le niveau 3 tient, et lesquels nous disent qu'il casse ? »

**Résultat attendu à la fin de la semaine :** un tableau de bord N3 minimal (5 à 7 signaux), des seuils par signal avec la décision associée, un premier point de qualimétrie tenu, et un registre des décisions déclenchées par les signaux.

### Atelier 3.1 : Inventaire des signaux disponibles

**Objectif :** faire l'inventaire honnête de ce que l'équipe peut mesurer aujourd'hui, sans rêver d'outillage idéal. Une métrique qui n'existe pas encore est une promesse ; une métrique qui existe mais n'est pas regardée est un gaspillage.

**Durée :** 2 heures. **Participants :** équipe pilote, coach TOTALISATION, lead technique.

**Étapes :**
1. Recensement des données déjà produites par l'équipe : rapports de tests automatisés, couverture, incidents, temps de cycle, taux de réouverture, dérogations, usages de l'IA (traçabilité), revues de livraison.
2. Classer chaque donnée : vivante (produite et regardée), dormante (produite mais jamais regardée), fantôme (réclamée mais jamais produite).
3. Identifier les données manquantes les plus critiques pour le niveau 3, et le coût réel de leur production.
4. Choisir les 5 à 7 signaux du tableau de bord N3 : suffisamment peu pour être lus, suffisamment juste pour être utiles.

**Livrable :** inventaire des signaux N3 (vivants, dormants, fantômes), short-list des 5 à 7 signaux du tableau de bord.

### Atelier 3.2 : Seuils et décisions associées

**Objectif :** pour chaque signal, définir un seuil et la décision qu'il déclenche. La règle du niveau 3 : un signal sans décision associée est de la décoration. Un seuil sans plan d'action est de la décoration aussi.

**Durée :** 2 heures. **Participants :** équipe pilote, coach TOTALISATION, lead technique, product owner.

**Étapes :**
1. Pour chaque signal retenu, définir : la valeur actuelle (mesurée, pas estimée), le seuil vert, le seuil rouge, et la période de référence.
2. Pour chaque seuil rouge : la décision associée (arrêter une diffusion, re-prioriser, allouer un temps de remédiation, remonter au sponsor) et la personne qui la prend.
3. Pour chaque signal au vert stable depuis deux semaines : la décision d'allègement (réduire la fréquence de lecture, automatiser davantage) pour éviter la sur-mesure.
4. Écrire la règle de lecture : le tableau de bord se lit en réunion, ensemble, en 15 minutes, avec les décisions notées dans le registre.

**Livrable :** tableau de bord N3 avec seuils et décisions associées, règle de lecture écrite, registre des décisions ouvert.

### Atelier 3.3 : Premier point de qualimétrie tenu

**Objectif :** tenir le premier point de qualimétrie N3 avec le tableau de bord réel, et alimenter le registre des décisions. C'est l'atelier où la qualimétrie devient un outil vivant, pas un document.

**Durée :** 30 minutes + 30 minutes de débrief. **Participants :** équipe pilote, chargé de livraison, coach (observateur).

**Étapes :**
1. Le chargé de livraison anime le point : chaque signal est lu, sa tendance est nommée, sa décision (aucune, action, escalade) est énoncée à voix haute.
2. Chaque décision est notée dans le registre : signal, valeur, décision, responsable, échéance.
3. Le débrief (30 min) : le point a-t-il déclenché des décisions ? Sinon, le tableau est mal conçu (signaux sans pouvoir d'action). Ajuster.
4. Fixer la cadence : le point de qualimétrie N3 a lieu [jour], à [heure], animé par le chargé de livraison, même en l'absence du coach.

**Livrable :** premier point de qualimétrie tenu et débriefé, registre des décisions initialisé, cadence fixée.

### Atelier 3.4 : Livrable de la semaine

**Objectif :** consolider la semaine : tableau de bord publié, registre actif, cadence fixée.

**Durée :** 1 heure. **Participants :** équipe pilote, sponsor.

**Étapes :**
1. Revue du tableau de bord N3 : les signaux sont-ils lisibles ? Les seuils sont-ils justes ? Une décision a-t-elle déjà été déclenchée ?
2. Vérifier que chaque signal a une décision associée (ou est retiré).
3. Checklist de fin de semaine (voir ci-dessous).
4. Annoncer la semaine 4 : la documentation vivante N3.

**Livrable :** tableau de bord N3 publié, registre des décisions actif, cadence de qualimétrie fixée.

### Capsule du vécu — Mission Faucon, Opal-RT

Dans la mission Faucon, l'équipe produisait des rapports de tests, mais personne ne les regardait : ils étaient produits « pour la trace », pas pour décider. Quand l'équipe a réduit le tableau de bord à six signaux — chacun avec une décision associée — le point de qualimétrie est devenu la réunion la plus courte et la plus utile de la semaine. Le jour où un signal rouge a déclenché un No-Go argumenté par la preuve, l'équipe a compris que la qualimétrie ne décrit pas la qualité : elle déclenche des décisions.

### Points de vigilance

- Un signal sans décision associée est une décoration. Retirez-le ou donnez-lui une décision.
- Les seuils ne sont pas définitifs : ils s'ajustent avec la pratique. Documentez chaque ajustement (qui, quand, pourquoi).
- La cadence tient même en semaine occupée : un point de qualimétrie sauté est un signal rouge lui-même.

### Checklist de fin de semaine 3

- [ ] Inventaire des signaux (vivants, dormants, fantômes) fait
- [ ] Tableau de bord N3 : 5 à 7 signaux avec seuils et décisions associées
- [ ] Premier point de qualimétrie tenu, débriefé, cadence fixée
- [ ] Registre des décisions initialisé

---

## Semaine 4 : La documentation vivante N3 et la première consolidation

**Objectif de la semaine :** rendre la documentation produit et processus vivante au niveau 3 : reliée aux modèles, mise à jour par la pratique, lisible par un nouvel arrivant. Répondre à la question : « si un nouveau arrive lundi, peut-il comprendre notre processus de livraison N3 en lisant la documentation seule ? »

**Résultat attendu à la fin de la semaine :** la documentation N3 reliée aux artefacts vivants (modèles, grille Go/No-Go, tableau de bord, règles IA), un test du nouvel arrivant (une personne qui lit et réussit la navigation), et la première consolidation de la partie 1 : le niveau 3 en forge est opérationnel.

### Atelier 4.1 : Cartographier la documentation existante

**Objectif :** cartographier honnêtement la documentation N3 : ce qui existe, ce qui est relié, ce qui est orphelin. La documentation orpheline (personne ne la maintient, personne ne la lit) est un passif, pas un actif.

**Durée :** 2 heures. **Participants :** équipe pilote, coach TOTALISATION.

**Étapes :**
1. Inventaire de la documentation existante : pages wiki, gabarits, modèles, grilles, règles, chronologies. Pour chaque item : vivante (reliée à la pratique, lue), dormante (existe mais jamais lue), orpheline (non maintenue).
2. Identifier les reliages manquants : la grille Go/No-Go pointe-t-elle vers les preuves attendues ? Le tableau de bord vers le registre des décisions ? Les règles IA vers les usages tracés ?
3. Classer les reliages : N1 (document isolé), N2 (document relié à un autre document), N3 (document relié à la pratique : un rituel le lit, un rituel le met à jour).
4. Prioriser : quels reliages installer cette semaine pour que la documentation soit vivante ?

**Livrable :** cartographie de la documentation N3 avec état vivant/dormant/orphelin, reliages prioritaires choisis.

### Atelier 4.2 : Le test du nouvel arrivant

**Objectif :** vérifier que la documentation N3 est vivante en la faisant lire par quelqu'un qui n'a pas participé à sa rédaction. Ce test est simple et sans pitié : une documentation qui ne guide pas un nouvel arrivant n'est pas vivante.

**Durée :** 2 heures. **Participants :** lecteur test (un collègue d'une autre équipe ou un nouvel arrivant), équipe pilote, coach.

**Étapes :**
1. Donner au lecteur test une mission : « À partir de la documentation seule, décris notre processus de livraison N3 et dis où tu bloques. »
2. Observer le parcours de lecture : où le lecteur hésite, où il rebrousse chemin, où il revient en arrière.
3. Noter les points de rupture : lien manquant, jargon non défini, seuil non expliqué, référence obsolète.
4. Corriger les points de rupture immédiatement (20 minutes), puis refaire le test si des ruptures majeures ont été corrigées.

**Livrable :** test du nouvel arrivant fait, points de rupture corrigés, documentation N3 plus navigable.

### Atelier 4.3 : La consolidation de la partie 1 (semaines 1-4)

**Objectif :** consolider le niveau 3 en forge : processus de planification, rituels d'implémentation, qualimétrie, documentation vivante. Ce n'est pas un bilan de fin de mission : c'est un contrôle technique de mi-parcours.

**Durée :** 2 heures. **Participants :** équipe pilote, coach, sponsor (15 dernières minutes).

**Étapes :**
1. Inventaire des quatre fondations de la partie 1 : processus de planification N3, rituels d'implémentation, qualimétrie N3, documentation vivante. Pour chacune : stabilisée, fragile, ou dépendante d'un blocage externe.
2. Pour chaque fondation fragile : la cause (pratique trop lourde, responsabilité floue, blocage organisationnel) et l'action correctrice datée.
3. Preuves de fonctionnement : un Go/No-Go argumenté par preuves, un rituel tenu sans coach, un signal rouge déclenché une décision, une documentation navigable par un lecteur test.
4. Présentation de 15 minutes au sponsor : les fondations, les fragilités, les actions correctrices, la demande (rien, ou un déblocage précis).

**Livrable :** bilan de mi-parcours N3 : fondations classées, actions correctrices datées, présentation au sponsor faite.

### Capsule du vécu — Mission Faucon, Opal-RT

Dans la mission Faucon, la documentation était riche et morte. Les pages existaient, mais personne ne les lisait, parce que personne ne les utilisait dans un rituel. Le tournant est venu du test du nouvel arrivant : un collègue d'une autre équipe a essayé de comprendre le processus de livraison en lisant la documentation seule, et il s'est perdu. Les points de rupture qu'il a signalés ont été corrigés en une après-midi — et la documentation est devenue vivante, parce qu'un rituel la lisait désormais chaque semaine. La leçon du niveau 3 : la documentation vivante n'est pas « à jour » ; elle est *utilisée*.

### Points de vigilance

- Le test du nouvel arrivant est sans pitié, et c'est sa valeur. Un lecteur qui dit « tout est clair » n'a pas lu assez longtemps.
- La consolidation de mi-parcours n'est pas une cérémonie : c'est un contrôle technique. Les fragilités sont nommées, datées, avec action correctrice.
- Ne pas confondre « documentation reliée » (liens entre documents) et « documentation vivante » (un rituel la lit et la met à jour). Le niveau 3 exige la seconde.

### Checklist de fin de semaine 4

- [ ] Cartographie de la documentation N3 (vivante/dormante/orpheline) faite
- [ ] Reliages prioritaires installés (document ↔ rituel)
- [ ] Un lecteur test a navigué la documentation seule et ses ruptures ont été corrigées
- [ ] Bilan de mi-parcours : fondations classées (stabilisée/fragile), actions correctrices datées
- [ ] Présentation de 15 minutes au sponsor faite

---

## Notes de facilitation — Semaines 3 et 4

**Erreurs fréquentes (S3)**
- Faire du tableau de bord un objet d'exposition. S'il n'est pas lu en réunion, il n'existe pas.
- Collecter des signaux « au cas où ». Un signal non lu depuis trois semaines sort du tableau.
- Confondre seuil et décision : le seuil dit où on en est, la décision dit ce qu'on fait.

**Erreurs fréquentes (S4)**
- Corriger la documentation en la relisant entre experts : ils savent déjà tout, ils ne voient plus les ruptures. Seul un lecteur test révèle les ruptures réelles.
- Traiter la consolidation comme un bilan de fin : elle est un contrôle technique de mi-parcours, avec actions correctrices datées, pas des discours.
- Laisser le sponsor voir uniquement les succès : il doit voir les fragilités aussi, sinon sa confiance sera trahie au point mort de la semaine 5.

**Variantes**
- *Équipe sans coach au quotidien :* l'atelier 3.3 peut être animé par le chargé de livraison seul, avec le coach lu les notes de facilitation à distance.
- *Documentation déjà très mûre :* le test du nouvel arrivant se fait alors sur une demande réelle : le lecteur doit non seulement comprendre le processus, mais aussi y trouver le gabarit et les preuves attendues.
- *Fondations très fragiles au bilan de mi-parcours :* ne pas forcer le virage en semaine 6. Décalez le virage d'une semaine, corrigez les fragilités, puis traversez le point mort avec des fondations tenables.

**Tests de réussite**
- S3 : un signal rouge a déclenché une décision enregistrée dans le registre.
- S4 : un lecteur test a navigué la documentation seule, ses ruptures ont été corrigées, et la documentation est reliée à un rituel hebdomadaire qui la lit.
