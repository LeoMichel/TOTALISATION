
---

# Partie 14 : La trousse de premiers secours et le bilan de vitalité

## La trousse de premiers secours du niveau 3

Les urgences qui menacent la cadence — et les réponses à appliquer dans les 48 heures.

### Urgence 1 : le coach ou le porteur part en plein forgeage

**Situation.** Le porteur principal d'un rituel (souvent le chargé de livraison) part avant la fin du forgeage. Le rituel est à moitié forgé : il tient avec lui, il ne tiendra pas sans lui.

**La réponse dans les 48 heures :** (1) documenter ce que le partant savait faire (son protocole implicite devient explicite — c'est la première fois que le gabarit est vraiment testé) ; (2) nommer deux personnes qui reprennent en binôme (pas une : la rotation est le remède) ; (3) ralentir le forgeage plutôt que le précipiter. Le rituel à moitié forgé qui est précipité meurt au premier obstacle — le rituel à moitié forgé qui est ralenti survit.

### Urgence 2 : trois rituels reportés la même semaine

**Situation.** Une semaine de crise (incident de production, deadline client) : trois rituels reportés en trois jours. La cadence est menacée.

**La réponse dans les 48 heures :** (1) vérifier que les reports sont écrits (raison, date de reprise) — si non, les écrire maintenant ; (2) tenir au moins UN rituel en version réduite (5 minutes) pour maintenir le battement — le rituel maintenu empêche l'abandon généralisé ; (3) planifier le rattrapage des trois reports en une seule cérémonie de rattrapage (pas trois cérémonies séparées).

### Urgence 3 : le SLA est contourné par la moitié de l'équipe

**Situation.** La moitié des demandes re-classées après leur classement initial, ou classées « complexes » pour prendre plus de temps, ou classées « simples » pour paraître efficaces.

**La réponse dans les 48 heures :** (1) compter les re-classifications et les afficher sans nom (le pattern, pas les coupables) ; (2) demander à l'équipe : « le classement est-il mal forgé, ou le respect du classement est-il mal partagé ? » ; (3) si le classement est mal forgé (les définitions sont floues), le réviser avec les données ; si le respect est mal partagé, la réunion de clarification sur la règle du report écrit est le prochain rituel.

### Urgence 4 : la grille de Go/No-Go bloque tout

**Situation.** La grille est si stricte que les livraisons s'accumulent : trois semaines de livraisons en attente, le client s'impatiente, la pression monte.

**La réponse dans les 48 heures :** (1) re-classifier les critères : sont-ils tous bloquants ? S'il y a 12 critères bloquants, la grille n'a pas de soupape ; (2) activer la dérogation écrite comme soupape : chaque livraison en attente reçoit sa dérogation (critère rouge, risque assumé, condition de levée) ou son Go propre ; (3) si plus de 3 dérogations actives, le problème n'est pas la grille — c'est en amont (la qualité des tests, la documentation). Traitez la cause, pas la conséquence.

### Urgence 5 : le chargé de livraison en épuisement

**Situation.** Le chargé de livraison depuis 3 mois commence à dériver : les rituels sont tenus mais sans énergie, les décisions sont reportées, les preuves sont « en retard ».

**La réponse dans les 48 heures :** (1) activer le binôme immédiatement (pas « quand quelqu'un sera prêt ») ; (2) donner au binôme les 15 minutes de préparation du gabarit (le protocole remplace la compétence) ; (3) parler au sponsor : la charge du chargé de livraison doit être reconnue (3-5 heures par semaine dans la planification). Un rôle qui n'est pas reconnu dans la charge est une surcouche qui épuise.

### Urgence 6 : le sponsor conteste un No-Go en public

**Situation.** Le sponsor conteste la décision en réunion, devant l'équipe. Le chargé de livraison est isolé, et le message reçu par tous est : la grille ne protège pas contre la hiérarchie.

**La réponse dans les 48 heures :** (1) le chargé de livraison ne débat pas en séance — il lit la grille, énonce les critères rouges, propose le chemin de rattrapage avec sa date. La formule : « pas aujourd'hui, voici pourquoi, voici quand » ; (2) après la séance, le praticien parle au sponsor en privé : la grille n'est pas une défiance envers lui, c'est une protection pour lui (les livraisons sans preuve sont les sources d'incidents qui coûtent le plus cher) ; (3) la dérogation est proposée comme voie de sortie honnête : si le sponsor veut livrer malgré le critère rouge, la dérogation écrite assume le risque avec lui — et il en est responsable.

## Le bilan de vitalité du niveau 3

Le rituel trimestriel de vérification de la forge : les piliers sont-ils vivants ?

**Les quatre piliers à vérifier :**

1. **Les critères vivants** : la grille Go/No-Go, les SLA par classe, les seuils du tableau. Test : ont-ils survécu à une urgence réelle ? La relève existe-t-elle ? Un critère jamais utilisé depuis trois mois est suspect.

2. **Le pipeline à trois vitesses** : les tests bloquants au commit, les tests bloquants au merge, les informatifs la nuit. Test : les bloquants tournent-ils réellement à chaque commit ? Les informatifs nocturnes trouvent-ils des bugs ? Un pipeline dont la vitesse rapide ne tourne pas est un pipeline mort.

3. **La confirmation systématique** : chaque défaut résolu a un statut explicite. Test : le taux de statuts explicites est-il au-dessus de 80 % ? Une confirmation qui n'existe que pour les défauts critiques est une confirmation partielle.

4. **La veille et les seuils** : les lettres de veille sont-elles envoyées ? Les seuils sont-ils relus ? La veille qui n'a jamais envoyé de lettre est une veille morte — elle a peut-être raison (rien à signaler), mais elle doit le prouver.

**La sortie du bilan :** la carte de fragilité (les piliers qui échouent, avec leurs chantiers), et la reconnaissance de ce qui est solide. Un bilan qui ne trouve aucune fragilité n'a pas été honnête — et la fragilité la plus dangereuse est celle du pilier qui a toujours réussi.

## Le connecteur : ce que le niveau 3 transmet au niveau 4

Le niveau 4 (VERT) prend le relais avec la mesure : les rituels cadencés deviennent mesurés, les preuves deviennent des données, les décisions deviennent des tendances. Mais le niveau 4 ne remplace pas le niveau 3 : il le mesure.

Le praticien du niveau 3 transmet au niveau 4 : la cadence (le niveau 4 la mesure), le SLA par classe (le niveau 4 en mesure le taux de respect), les réserves avec levée (le niveau 4 en mesure le taux de levée à date). Ce que le niveau 3 construit, le niveau 4 le voit — et ce que le niveau 4 découvre, le niveau 3 le corrige.

Le test de transition : les huit questions du test des cérémonies du niveau 3 réussies sans le coach pendant un trimestre complet. Si oui, le niveau 4 est raisonnable. Si non, consolidez — la mesure ne construit pas sur du sable.
