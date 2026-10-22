
---

# Partie 13 : Le glossaire du praticien N2 et les fiches-outils

## 1. Le glossaire du niveau 2, étendu

**Modèle BPMN (Business Process Model and Notation)** — la représentation standard des processus : événements, tâches, passerelles, flux. À ne pas confondre avec la documentation (qui décrit) : le modèle est discutable (confronté), la documentation est lue. Le modèle vit ; la documentation rapporte.

**Confrontation** — l'acte central du niveau 2 : deux rôles décrivent le processus de l'autre à partir des modèles, et les écarts sont nommés. À ne pas confondre avec la revue (qui vérifie un artefact) : la confrontation révèle ce que personne ne savait — les malentendus entre vivants du processus.

**Divergence** — l'écart détecté entre deux descriptions, deux modèles, ou un modèle et le réel. La devise du niveau 2 : la divergence est une information, pas une faute. La question n'est jamais « qui a tort » mais « qu'est-ce que le réel fait, et que doit-on corriger — le modèle, le code, ou les deux ».

**MBT (Model-Based Testing, test basé sur le modèle)** — la génération de tests à partir du modèle. À ne pas confondre avec l'automatisation de tests (qui scripte des cas connus) : le MBT découvre des combinaisons que personne n'aurait écrites. Le ratio honnête : beaucoup produits, peu sélectionnés, rarement un utile — et cet un vaut la campagne.

**Gabarit de génération** — le moule qui transforme les chemins du modèle en tests exécutables. À ne pas confondre avec le modèle (qui décrit) : le gabarit produit. Un gabarit trop productif génère du bruit ; le tri corrige, mais le gabarit s'améliore à chaque campagne (l'exercice E8 le mesure).

**Tri** — la sélection des tests générés selon les critères écrits : garder, modifier, supprimer, avec justification. À ne pas confondre avec la revue de code (qui juge l'implémentation) : le tri juge la pertinence de la couverture. Le ratio de tri qui baisse campagne après campagne est l'indicateur d'amélioration du gabarit.

**Spécification dérivée** — la spécification dont la structure vient du modèle : chaque passerelle devient un cas, chaque chemin une règle. À ne pas confondre avec la spécification libre du niveau 1 (qui part de la demande) : la dérivée hérite de la structure et des décisions passées. Son avantage mesurable : elle contient ce que la demande ne disait pas.

**Documentation vivante** — la documentation liée au modèle : datée, sourcée, synchronisée. À ne pas confondre avec la documentation générée (automatique) : générée ne suffit pas — la vivante répond aux questions réelles des lecteurs réels (le test du support, E10). La vivante se taille ; l'orpheline s'accumule.

**Plan lié** — le plan de livraison dont chaque élément pointe vers son modèle et son état de preuve. À ne pas confondre avec le plan décoré (qui affiche des références mortes) : le plan lié se vérifie à chaque planification (E11). La catégorie « non modélisé » est une catégorie honnête du plan lié — pas un aveu.

**Versioning du modèle** — la mémoire des changements : quoi, pourquoi, qui. À ne pas confondre avec l'historique d'outil (qui garde les instantanés) : le versioning garde le pourquoi — la divergence qui a motivé le changement. Sans le pourquoi, le ping-pong des décisions revient.

**Chemin non couvert** — un chemin du modèle pour lequel aucun test n'existe (généré ou manuel). À ne pas confondre avec le bug (comportement faux) : le chemin non couvert est une zone d'ombre documentée. La matrice de couverture du niveau 2 liste les deux : les chemins couverts ET les zones d'ombre assumées.

**Usage imprévu** — un usage du produit observé en confirmation que le modèle ne prévoyait pas. À ne pas confondre avec le bug (comportement faux) : l'usage imprévu est un chemin réel que le modèle ignorait. C'est la grande boucle au niveau 2 : le réel enrichit le modèle.

## 2. Les fiches-outils du niveau 2

### Fiche 7 : La fiche de modèle (carte d'identité du BPMN)

**Usage :** chaque modèle a sa fiche — la mémoire de son état, sa dernière confrontation, son propriétaire.

```
MODÈLE — BPM-004                              Révision : 3
Titre : Processus de correction de bug
Propriétaire : L.T. (QA) / S.M. (dev) — binôme

DERNIÈRE CONFRONTATION : 12/07 — dev/QA — 2 divergences trouvées
CORRIGÉES LE : 14/07 (révision 3)

DIVERGENCES CUMULÉES TROUVÉES : 11 depuis la création
EXTENSIONS CANDIDATES (depuis confirmations) : 2

ZONE D'OMBRE assumée : le traitement des bugs historiques
(pas modélisé — décision du 14/07, revisitée au T+1)

LISTE DES RÉVISIONS :
r3 (14/07) : passerelle criticité avant qualification (le modèle mentait)
r2 (28/06) : tâche spécification ajoutée (conditionnelle)
r1 (12/06) : création
```

**Le test de la fiche :** un nouveau peut comprendre l'état du modèle sans poser de question. La fiche est le passeport du modèle — sans elle, le modèle est une image sans historique.

### Fiche 8 : Le gabarit de confrontation

**Usage :** à chaque confrontation — le format qui transforme la discussion en livrable.

```
CONFRONTATION — [Modèle] [Révision]          Date : ____
Participants (rôles différents) : __________ / __________

CE QUE A CROIT DE B :
_______________________________________________________

CE QUE B CROIT DE A :
_______________________________________________________

DIVERGENCES TROUVÉES :
1. A croyait ______ ; B fait ______ → correction : ______
2. ___________________________________________________
3. ___________________________________________________

ACTIONS : modèle modifié (oui/non — si non, pourquoi) :
_______________________________________________________
```

**Exemple rempli (extrait réel) :**

```
CONFRONTATION — BPM-002 (processus de release)  Date : 03/07
Participants : S.M. (dev) / M.C. (ops)

CE QUE S.M. CROIT DE M.C. : M.C. exécute le rollback manuellement
si la vérification post-déploiement échoue.

CE QUE M.C. CROIT DE S.M. : S.M. surveille le déploiement jusqu'à
la fin de la fenêtre de vérification.

DIVERGENCES :
1. S.M. croyait que la vérification post-déploiement était de sa
   responsabilité pendant 24h ; M.C. la fait pendant 2h seulement
   → correction : le modèle précise la fenêtre (2h) et le transfert
   (après 2h, alerte automatique vers l'équipe).
2. Aucun des deux ne savait qui décidait d'un rollback partiel
   → correction : le modèle ajoute la passerelle de décision
   (décideur : M.C., en lien avec le demandeur).

ACTIONS : modèle modifié (oui — révision 4, le 03/07)
```

### Fiche 9 : Le gabarit de spécification dérivée

**Usage :** la spécification du niveau 2, dont la structure vient du modèle.

```
SPÉCIFICATION — [ID]              Modèle : BPM-00x rév. n
Titre : ____________________

PÉRIMÈTRE SUR LE MODÈLE : (quels chemins sont affectés)
_______________________________________________________

RÈGLES (une par chemin actif du périmètre) :
1. SI _______________ ALORS _______________________
2. SI _______________ ALORS _______________________
3. SI _______________ ALORS _______________________

CAS LIMITES (issus des passerelles non couvertes) :
- ___________________________________________________
- ___________________________________________________

TESTS ATTENDUS (générés et/ou manuels, par chemin) :
_______________________________________________________

DOC À SYNCHRONISER : [page(s)] — vérifiée le : ____

Revue : dev ___ test ___ demandeur ___ (date ___)
```

**Ce que la dérivation apporte (mesurable) :** le nombre de règles est déterminé par le modèle (les chemins actifs), pas par l'imagination de l'auteur. Les cas limites sont systématiques (chaque passerelle non couverte). Et la doc à synchroniser est identifiée AVANT l'implémentation — pas après.

### Fiche 10 : Le gabarit de rapport de tri

**Usage :** à chaque campagne de génération. Voir l'exemple complet en Partie 5 (§1.3).

**Le format condensé :**

```
TRI — Campagne [Modèle] du [date]
Produits : ___ | Gardés : ___ | Modifiés : ___ | Supprimés : ___
Utiles à ce jour (défauts trouvés) : ___

SUPPRESSIONS (justifiées, échantillon) :
- T-___ : ___________________________________
- T-___ : ___________________________________

QUESTION OUVERTE pour le modèle : _____________________
```

**La ligne « question ouverte » est la plus précieuse :** elle transforme le tri en audit du modèle. Les gabarits produisent des tests dans les zones où le modèle est flou — le tri le détecte.

### Fiche 11 : Le gabarit de confirmation N2

**Usage :** la confirmation du niveau 2 enrichit le modèle.

```
CONFIRMATION — [Version]                  Date : ____
Demandeur : ______  Élicitation : [ID]  Modèle : BPM-00x rév. n

CRITÈRES DE SUCCÈS (de l'élicitation) :
1. ______ → atteint ? oui/partiel/non
2. ______ → atteint ? oui/partiel/non

USAGES OBSERVÉS :
- Comme prévu : _______________________________
- Autrement : _________________________________ ← extensions candidates
- Non utilisé : _______________________________

MODÈLE À ENRICHIR :
- Chemin manquant : ___________________________
- Passerelle incomplète : _____________________

Révision du modèle : oui/non — si oui, nouvelle révision : ___
```

**La dernière ligne est le test de la grande boucle N2 :** une confirmation sans mise à jour du modèle est une confirmation morte. Les usages imprévus sont le cadeau de la confirmation — le modèle qui ne reçoit pas ce cadeau ne vivra pas.

### Fiche 12 : Le tableau de bord N2

**Usage :** le système de signaux du niveau 2. Six lignes, pas plus.

| Signal | Valeur | Seuil | Décideur | Dernière décision |
|---|---|---|
| Divergences doc/modèle | | | | |
| Tests flaky | | | | |
| Ratio de tri (dernière campagne) | | | | |
| Temps de pipeline | | | | |
| Usage IA conforme au registre | | | | |
| Modèles confrontés < 30 jours | | | | |

**La règle de rotation :** un signal qui reste vert pendant trois mois est soit une réussite, soit un seuil trop lâche. Chaque trimestre, un signal sort (ou son seuil se resserre) — le tableau reste vivant par la rotation, pas par l'ajout.

## 3. Le connecteur vers le niveau 3

Le niveau 3 (JAUNE) forge la cadence : les rituels N2 deviennent des processus à rythme constant, les livraisons se cadencent, l'autonomie se prouve par le temps. Le niveau 2 prépare trois choses que le niveau 3 exigera :

1. **Des modèles vivants** — le niveau 3 les maintiendra en cadence, pas en effort.
2. **Des preuves automatisées** — le niveau 3 les intégrera au pipeline de livraison régulier.
3. **Une équipe qui confronte sans le coach** — le niveau 3 l'officialisera (le bilan d'autonomie).

Le test de transition : les six questions du test des cérémonies N2 (Partie 12, E12). Quatre réussies sur six = le niveau 3 est raisonnable. Moins de quatre : consolidez — le JAUNE est un forgeage, et on ne forge pas du sable.
