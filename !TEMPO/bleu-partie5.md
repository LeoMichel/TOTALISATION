
---

# Partie 5 : Cas réels, gabarits remplis et variantes contextuelles (niveau 5)

Les gabarits remplis, les situations vécues, et l'adaptation du niveau 5 (gouvernance inter-équipes) aux contextes réels.

## 1. Les gabarits remplis d'exemples réels

### 1.1 La charte du comité qualité — exemple rempli

> La charte réelle du comité qualité d'une organisation de 5 équipes après le niveau 5. Notez le périmètre écrit : ce que le comité ne décide PAS est aussi important que ce qu'il décide.

**Charte du comité qualité — version 2 (adoptée le 03/09)**

**Membres :** un représentant par équipe adoptante (5), le responsable du centre d'excellence, le sponsor. Présidence tournante trimestrielle.

**Réunion :** mardi, 45 minutes, toutes les deux semaines. Quorum : 4 membres dont 1 président.

**Le comité décide :**
- Les seuils partagés (couverture, divergences, flaky) — avec preuve à l'appui
- Les règles communes des gabarits — modifications votées
- Les dérogations inter-équipes — demande écrite préalable
- Les escalades qu'aucune équipe ne peut trancher seule

**Le comité ne décide pas :**
- Les priorités produit des équipes
- Le contenu des backlogs
- L'organisation interne des équipes
- Les choix d'architecture (sauf s'ils affectent la chaîne partagée)

**Standard de preuve :** toute décision est appuyée par une donnée mesurée (rapport, métrique, incident documenté). Une demande sans preuve est renvoyée sans débat.

**Registre :** chaque décision est notée au registre (date, décision, preuve, opposants, condition de révision). Le registre est public dans l'organisation.

**Procédure de contestation :** toute décision peut être contestée dans les 10 jours ouables, par écrit, avec une preuve nouvelle. La contestation est traitée au comité suivant.

**Ce qui fait la qualité de cette charte :** la section « ne décide pas » et la procédure de contestation. Un comité sans limite de périmètre devient un organigramme parallèle ; un comité sans voie de contestation attend son conflit fatal.

### 1.2 Le registre des décisions — exemple rempli

> Six mois de décisions réelles, échantillon représentatif. Notez la colonne « opposants » : une décision sans opposant est suspecte (personne ne la lisait).

| Date | Décision | Preuve | Pour | Contre | Révision |
|---|---|---|---|---|---|
| 12/09 | Abaisser le seuil de couverture de 80 à 75 % pour l'équipe C (legacy, données partielles) | Rapport de couverture équipe C, incident du 02/09 | 5 | 0 | T1 prochain |
| 26/09 | Refuser la dérogation de l'équipe B (exemption de tri des tests de migration) | Registre de tri équipe B absent, incident Migration-2019 cité | 3 | 2 | Sur nouvelle preuve |
| 10/10 | Faire évoluer le gabarit « standard » (gestion des valeurs nulles) | 4 dérogations identiques des équipes A, C, D en 2 mois | 6 | 0 | — |
| 24/10 | Escalader au sponsor le conflit de fenêtre de génération nocturne (équipes B et E) | 2 arbitrages infructueux en comité (12/10, 19/10) | 6 | 0 | Décision sponsor |
| 07/11 | Marquer le modèle BPM-011 « non fiable » (pas de mise à jour depuis 3 mois) | Historique du modèle, relance sans réponse | 5 | 1 | Au retour du propriétaire |

**Ce que ce registre montre :** des décisions contre (26/09 : 2 contre), des escalades (24/10), des sanctions techniques (07/11). Un registre où tout est unanime et où rien ne remonte n'est pas un organe de gouvernance : c'est un tampon.

### 1.3 Le bilan de qualité à l'échelle — exemple rempli

> Le bilan trimestriel présenté au comité (atelier 7.2), rempli avec des données réelles.

**Bilan de qualité de génération — T3**

| Équipe | Modèles | Couverture | Ratio de tri (gardés/produits) | Tests utiles (défauts) | État |
|---|---|---|---|---|---|
| A | 4 | 81 % | 89/247 (36 %) | 6 | ✅ conforme |
| B | 3 | 77 % | 62/140 (44 %) | 4 | ⚠️ seuil sous 80 |
| C | 5 | 74 % | 51/180 (28 %) | 2 | ⚠️ héritage, plan spécial |
| D | 3 | 83 % | 44/98 (45 %) | 3 | ✅ conforme |
| E | 2 | 79 % | 30/110 (27 %) | 1 | ✅ conforme (équipe récente) |

**Lecture du bilan :** le ratio de tri de C (28 %) est le plus bas — investigation : son modèle hérité est imprécis, ce qui produit des tests peu pertinents. Le plan spécial : refonte du modèle C avec le binôme du centre d'excellence (daté). Les tests utiles au total : 16 défauts trouvés par la génération ce trimestre, contre 9 au T2 — la courbe monte.

**Action corrective (exemple de la qualité attendue) :** « Équipe C : refonte du modèle BPM-021 avec le binôme du centre d'excellence, séances des 14 et 21/11. Critère de levée : ratio de tri > 40 % au prochain bilan. Propriétaire : L.T. (équipe C) + centre d'excellence. »

## 2. Cas vécus étendus : le niveau 5

### Cas de la semaine 1 : le comité qui voulait tout décider

**Situation.** Le premier comité qualité a duré 2 heures 40 et a traité 14 sujets, dont la priorisation du backlog de l'équipe C et un choix d'architecture de l'équipe B. Les représentants sont sortis épuisés — et deux équipes ont commencé à contourner le comité dès la semaine suivante.

**Le diagnostic.** Le comité avait rempli le vide : sans périmètre écrit, tout sujet inter-équipes semblait de sa compétence. Et chaque sujet traité hors périmètre réduisait la légitimité du comité sur son vrai périmètre.

**La correction.** L'atelier « le comité ne décide pas » (module F1) a été rejoué en séance spéciale. La charte a gagné sa section « ne décide pas ». Les 14 sujets ont été retriés : 5 relevaient du comité, 9 ont été retournés à leurs équipes avec une phrase : « ce sujet vous appartient ; le comité s'attend à ce que sa décision respecte les seuils partagés ».

**Ce que ce cas enseigne.**
- Le périmètre d'un comité se définit autant par ses refus que par ses décisions. La section « ne décide pas » est le garde-fou qui empêche le comité de devenir un organigramme parallèle.
- Le contournement est le symptôme du dépassement de périmètre : quand les équipes arrêtent de venir, ce n'est pas de l'insubordination, c'est de l'information.
- Le retrait des sujets hors périmètre doit être explicite et respectueux : « ce sujet vous appartient » préserve l'autonomie gagnée au niveau 3.

### Cas de la semaine 2 : le premier arbitrage contre la plus grosse équipe

**Situation.** L'équipe A (la plus grande, la plus ancienne, celle qui a porté le niveau 4) a demandé une dérogation : exemption du tri pour ses tests de migration, « parce qu'elle a toujours géré sa migration seule ». L'équipe D (la plus récente) a contesté : les règles sont pour tous, sinon elles ne servent à rien.

**Le dilemme fondateur.** Ce premier arbitrage définit la gouvernance pour des années : le comité applique-t-il les règles à tout le monde, ou protège-t-il ceux qui ont construit ?

**La décision.** Le comité a refusé la dérogation (3 pour, 2 contre), avec une citation du registre de tri : l'équipe A n'avait pas de registre de tri du tout, et l'incident Migration-2019 (cité par D) avait précisément pour cause des tests de migration non triés. La décision a été motivée par la preuve, pas par l'égalité abstraite.

**La suite.** L'équipe A a fourni son registre de tri le mois suivant, et a trouvé 3 tests dangereux dans ses migrations. Son représentant l'a dit au comité : « On avait raison de nous refuser la dérogation. »

**Ce que ce cas enseigne.**
- Le premier arbitrage contre le plus fort est le moment où la gouvernance devient réelle. S'il est perdu (la plus grosse équipe obtient son exemption), le comité devient le comité des faibles.
- La preuve tranche les conflits que le statut ne devrait pas trancher. L'incident Migration-2019 a fait ce que l'argument « les règles sont pour tous » seul n'aurait pas fait.
- L'issue la plus fréquente et la plus saine : l'équipe perdante applique la règle, y trouve un bénéfice, et devient parfois sa meilleure défenseuse. Ne prenez pas la décision à sa place — laissez-la découvrir.

### Cas de la semaine 4 : l'adoptante qui n'a jamais présenté au comité

**Situation.** L'équipe E, adoptante depuis 6 semaines, ne s'était jamais présentée au comité (l'atelier 3.3 prévoit la présentation dans les 30 jours). Relancée deux fois, elle répondait : « on attend que ça soit stabilisé ».

**Le diagnostic.** L'absence de présentation n'était pas de la timidité : l'équipe E craignait d'être jugée sur ses chiffres (ratio de tri bas, 27 %). La relance par courriel ne règle pas la peur du jugement.

**Ce qui a fonctionné.** Le président du comité a changé le cadre : au lieu de « présentez vos résultats », il a proposé « venez présenter ce qui vous bloque ». L'équipe E est venue avec ses vrais problèmes (modèle hérité imprécis, gabarits inadaptés) — et le comité a fait ce qu'il était fait pour faire : l'équipe D a partagé son gabarit adapté aux données partielles, et un binôme s'est formé.

**Ce que ce cas enseigne.**
- L'adoption n'est complète que lorsque l'adoptante participe à la gouvernance. Une adoptante qui ne vient pas au comité est une adoptante qui utilise l'outil sans la communauté — et elle repartira aussi facilement.
- Le format de la première présentation détermine la relation à long terme : « présentez vos résultats » produit du maquillage ; « présentez ce qui vous bloque » produit de l'entraide.
- Les chiffres bas d'une équipe récente sont normaux — le comité qui les juge sans contexte tue la transparence future. La question utile : « où en es-tu par rapport à ton propre mois dernier ? »

### Cas de la semaine 6 : l'arbitrage que le comité a refusé de trancher

**Situation.** Le conflit de fenêtre nocturne entre les équipes B et E (toutes deux voulaient la même plage) est venu au comité. Après 40 minutes de discussion, le comité n'a pas tranché : les preuves des deux équipes étaient incomparables (des métriques de différents systèmes, des périodes différentes).

**La décision de refuser de décider.** Le comité a rendu une décision de non-décision documentée : « Le comité ne statue pas : les preuves des deux parties sont incomparables. Demande aux équipes : produire, d'ici deux semaines, une mesure d'occupation de la fenêtre sur la même période et le même système. Le comité tranchera sur ces données. »

**Le dénouement.** Les mesures ont révélé que les deux équipes se chevauchaient sur 20 minutes seulement, et qu'une plage adjacente était libre. Les équipes ont trouvé une solution avant le comité suivant. L'escalade au sponsor prévue n'a pas été nécessaire.

**Ce que ce cas enseigne.**
- Le refus d'arbitrer sans preuve comparable est une décision forte, pas une faiblesse. Un comité qui tranche sur des preuves incomparables établit le précédent que l'arbitrage est un combat de rhétorique.
- La demande de mesure commune est le mécanisme clé : elle transforme le conflit d'opinions en un problème de données. Souvent, les données réglent le conflit avant le comité suivant.
- L'escalade au sponsor est une réserve, pas un objectif : le comité qui escalade chaque conflit qu'il ne peut pas trancher rapidement perd sa raison d'être. La mesure commune est souvent la troisième voie.

### Cas de la semaine 7 : le bilan qui a révélé le modèle mort

**Situation.** Le bilan de qualité à l'échelle a montré un signal inquiétant : le ratio de tri de l'équipe C avait baissé de 44 % à 28 % en un trimestre. L'investigation a trouvé la cause : le modèle BPM-021 de l'équipe C n'avait pas été mis à jour depuis 3 mois — le propriétaire était parti, sans succession.

**La décision.** Le comité a appliqué la procédure du niveau 2 : le modèle a été marqué « non fiable » publiquement (décision du 07/11 au registre), un binôme a été formé pour la refonte, et le centre d'excellence a ajouté la question « qui maintient ce modèle ? » à sa checklist d'adoption.

**Ce que ce cas enseigne.**
- Un niveau 5 sans surveillance du niveau 2 régresse en silence : la gouvernance inter-équipes doit vérifier les fondations, pas seulement les étages. Le bilan trimestriel est ce contrôle.
- Le départ d'une personne est le test de vérité de la maintenance : si le modèle meurt avec elle, la maintenance n'était pas une pratique, c'était une habitude personnelle.
- La sanction technique (marquer le modèle non fiable) n'est pas punitive : elle protège les autres équipes de la confiance imméritée. Le marquage public est un service rendu.

## 3. Variantes contextuelles du niveau 5

### V1 : petite organisation (2-3 équipes)

- Le comité peut être l'équipe complète de deux personnes par équipe — mais le quorum et le périmètre écrit restent indispensables : à 6 personnes, le dépassement de périmètre est encore plus facile.
- La fréquence peut être hebdomadaire (30 minutes) : plus léger et plus réactif que bihebdomadaire à 45 minutes.
- Le registre des décisions est l'actif le plus important : dans une petite organisation, les décisions non écrites se contredisent encore plus vite (tout le monde se parle à tous).
- La procédure de contestation est essentielle : dans une petite organisation, une décision contestée en silence empoisonne plus vite (tout le monde croise tout le monde tous les jours).

### V2 : organisation distribuée

- Le comité se tient en visio avec une règle d'or : les preuves sont partagées à l'avance (24h), jamais présentées en live de mémoire. La preuve lue avant la réunion change la nature du débat.
- Le registre asynchrone : entre les réunions, les décisions urgentes se prennent par écrit sur le registre (avec un délai d'objection de 48h avant application). C'est la gouvernance asynchrone.
- Les fuseaux : le tour de présidence tient compte des fuseaux (le président de chaque trimestre héberge l'heure). Aucun fuseau ne devrait porter 100 % de l'inconvénient.
- Le bilan trimestriel est écrit d'abord, discuté ensuite : les données partagées par écrit réduisent le temps de réunion de moitié.

### V3 : organisation réglementée

- Le comité qualité satisfait souvent une exigence de revue inter-projets : mappez la charte du comité sur l'exigence réglementaire dès la première réunion, et faites valider le mapping par votre qualité réglementaire.
- Le registre des décisions est un document d'audit : sa tenue (preuves, opposants, révisions) couvre souvent la traçabilité des décisions qualité exigée.
- Les dérogations réglementées (écarts aux référentiels) passent par le comité avec un formalisme supérieur : le format de dérogation est un document réglementaire.
- La transmission inter-équipes peut exiger une qualification des formateurs : le programme « catalyseur qualifié » (formation + test à l'aveugle du guide + validation qualité) est souvent demandé.

### V4 : le sponsor qui ne vient plus au comité

**Symptôme.** Le sponsor était présent aux premiers comités, puis a délégué, puis a disparu. Les escalades restent sans réponse.

**Ce qui a fonctionné :** remplacer la présence par le contrat : le sponsor répond aux escalades écrites sous 5 jours ouvrables (engagement pris une fois, écrit dans la charte). La présence continue n'est pas nécessaire ; la réponse garantie l'est. Un sponsor qui répond par écrit aux escalades en 5 jours est plus utile qu'un sponsor présent qui ne décide jamais.

**Ce qui n'a pas fonctionné :** exiger sa présence. Elle a été obtenue deux fois par la contrainte, puis a disparu. L'engagement de réponse est plus solide que la présence forcée.

### V5 : l'équipe qui refuse la gouvernance

**Symptôme.** Une équipe adoptante utilise la chaîne mais refuse les règles : pas de registre de tri, pas de présentation au comité, dérogations demandées systématiquement.

**Ce qui a fonctionné :** le dialogue en trois temps : (1) écouter — le refus a souvent une raison légitime (une règle mal écrite, un contexte différent) ; (2) ajuster la règle si elle est fautive (les règles vivent) ; (3) si le refus persiste après ajustement, la décision devient binaire : utiliser la chaîne avec les règles, ou ne pas l'utiliser. Un tiers d'utilisateur qui contourne les règles est pire pour la communauté qu'un non-adoptant : il consomme l'infrastructure sans en respecter la gouvernance.

**Ce qui n'a pas fonctionné :** tolérer l'exception « parce qu'ils sont importants ». Une exception visible détruit la gouvernance pour toutes les autres équipes — et l'équipe exceptionnelle elle-même (elle n'apprend jamais la discipline qui fait la valeur).

---

## Comment utiliser cette partie

- **Au démarrage** : la charte du comité (§1.1) et le cas du comité qui voulait tout décider — le périmètre est la survie du comité.
- **Pendant le parcours** : le premier arbitrage contre la plus grosse équipe (semaine 2) arrive presque toujours — préparez-le avec le cas.
- **En continu** : le registre (§1.2) et le bilan (§1.3) sont les deux documents qui font vivre la gouvernance entre les réunions.
