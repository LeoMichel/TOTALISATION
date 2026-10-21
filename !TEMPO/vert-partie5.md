
---

# Partie 5 : Cas réels, gabarits remplis et variantes contextuelles (niveau 4)

Les gabarits remplis par une équipe réelle, les situations vécues derrière les capsules, et l'adaptation du parcours aux contextes non standards.

## 1. Les gabarits remplis d'exemples réels

### 1.1 Le guide de configuration de la chaîne — exemple rempli

> Le guide réel de l'équipe, tel qu'il est fourni à un nouveau mainteneur. C'est ce document qui fait passer la chaîne de « la machine de quelqu'un » à « l'infrastructure de l'équipe ».

**Configuration de la chaîne de génération — version 3 (maintenance : binôme S.M./L.T., rotation mensuelle)**

**1. Ce qu'il faut pour travailler :**
- Accès au dépôt `pipeline-gen` (demander à l'admin, mentionner le groupe `gen-maintainers`)
- L'outil de génération, version ≥ 4.2 (le vérifier : `gen --version`)
- Le fichier de config `config.yaml` (dans le dépôt, ne jamais le modifier en local sans commit)

**2. Générer pour la première fois :**
```
gen run --model BPM-004 --profile standard
```
Le résultat va dans `out/BPM-004/<date>/`. Trois fichiers : le rapport de génération (combien de tests, quels chemins), la liste des tests, les erreurs éventuelles.

**3. Les erreurs typiques et leur signification :**
- `E104 : modèle non conforme au schéma` → le modèle a été édité à la main hors de l'outil. Re-exporter depuis l'outil, ne jamais éditer le XML à la main.
- `E217 : gabarit introuvable` → vérifier le chemin dans `config.yaml`, section `templates`. Erreur fréquente après un déplacement de dossier.
- `E330 : timeout de génération` → le modèle est trop gros pour le profil standard. Utiliser `--profile deep` en nocturne, ou découper le modèle.

**4. Après chaque génération : la checklist de tri (obligatoire, voir critères de tri §3).**

**5. Qui contacter :** erreurs de gabarit → S.M. ; erreurs d'environnement → L.T. ; tout le reste → le canal `#gen-support`.

**Ce qui fait la qualité de ce guide :** les codes d'erreur réels avec leur signification. Un guide qui dit « si ça ne marche pas, contactez-nous » n'est pas un guide : c'est une carte de visite.

### 1.2 Les critères de tri — exemple rempli

> Les critères réels de l'équipe, issus du module F2. Ils sont appliqués à chaque génération.

**Critères de tri des tests générés (version 2, adoptés le 18/07)**

**À garder :**
- Le test couvre une combinaison de passerelles absente des tests manuels (vérification par couverture croisée).
- Le test peut échouer pour une raison nommable en une phrase (« échoue si la commande X est soumise deux fois dans la même seconde »).
- Le test couvre un chemin marqué critique dans le modèle ( passerelles de sécurité, de facturation, de migration).

**À modifier avant de garder :**
- Le test est valide mais dépend d'une donnée non garantie : réécrire le setup de données.
- Le test est redondant avec un test manuel mais plus rapide : remplacer le manuel, documenter le remplacement.

**À supprimer (avec justification obligatoire) :**
- Le test ne peut pas échouer (assertion tautologique ou vérification vide).
- Le test duplique un chemin déjà couvert, sans valeur additive.
- Le test dépend d'un ordre d'exécution non garanti (test flaky par conception).

**La consignation :** chaque décision de tri (garder/modifier/supprimer) est notée dans `out/<model>/tri.md` avec sa raison en une ligne. Le fichier de tri fait partie du livrable de génération.

**Les nombres de la dernière campagne (exigés dans le rapport) :** produits 247 / gardés 89 / modifiés 31 / supprimés 127. Utiles à ce jour (défauts trouvés) : 6.

**Ce qui fait la qualité de ces critères :** la justification obligatoire des suppressions. Un test supprimé sans raison est une information perdue ; avec raison, c'est une donnée sur la génération qui améliore les gabarits.

### 1.3 Le rapport de tri — exemple rempli

> Le fichier `tri.md` d'une vraie campagne. C'est le document qui transforme le tri en apprentissage.

```
# Tri de la campagne BPM-004 du 12/08
Produits : 247 | Gardés : 89 | Modifiés : 31 | Supprimés : 127

## Supprimés (échantillon justifié)
- T-014 : assertion vide (le test vérifie que le retour n'est pas null, rien d'autre)
- T-038 à T-041 : même chemin que T-037 avec des données différentes non significatives
- T-102 : dépend de l'ordre (échoue si T-099 n'a pas tourné avant)
- T-155 à T-201 : tests de la branche « migration » (47 tests) — la branche est
  marquée deprecated dans le modèle, à confirmer avec le PO avant toute réactivation

## Modifiés (échantillon)
- T-023 : setup de données réécrit (les données du gabarit n'existaient pas dans env-test)
- T-055 : ralenti volontairement (flaky à cause d'un async non attendu)

## Utiles à ce jour
- T-062 : a trouvé BUG-1247 (combinaison de filtres) — voir ticket
- T-091 : a trouvé une régression de la migration (données historiques)

## Question ouverte
Les 47 tests de la branche migration : le modèle est-il à jour ? La branche
deprecated doit-elle rester dans le modèle ? → question au PO, ticket MOD-15.
```

**Ce qui fait la qualité de ce rapport :** la question ouverte à la fin. Le tri ne se contente pas de classer : il détecte les incohérences du modèle lui-même. C'est le tri qui entretient le modèle, pas l'inverse.

## 2. Cas vécus étendus : le niveau 4

### Cas de la semaine 1 : la génération qui a échoué en beauté

**Situation.** La première génération réelle a produit une erreur `E104` : le modèle avait été édité à la main par un développeur pressé (ajout d'une passerelle en XML direct). La génération a échoué ; l'outil n'a produit aucun test.

**La réaction contre-productive (évitée).** Corriger le XML à la main pour que ça passe. C'est le début de la fin : une fois qu'on édite le XML à la main, le modèle et l'outil divergent pour toujours.

**Ce qui a été fait.** Le développeur a réimporté le modèle dans l'outil, refait sa modification dans l'interface, re-exporté. La génération a passé. La règle a été écrite au guide (voir §1.1, erreur E104) : « ne jamais éditer le XML à la main ».

**Ce que ce cas enseigne.**
- La première erreur de génération est un moment fondateur : elle fixe la culture de la chaîne. La corriger « à l'arrache » fixe la culture inverse.
- Le bon réflexe (réimporter via l'outil) a coûté 20 minutes ; le mauvais (édition directe) aurait coûté des semaines de divergence invisible.
- Les codes d'erreur documentés dans le guide viennent de ces moments. Chaque erreur rencontrée et comprise devient une ligne du guide — c'est ainsi qu'un guide devient utile.

### Cas de la semaine 2 : le test qui ne pouvait pas échouer

**Situation.** En triant la première campagne, un test nommé `T-014_check_order_total` est passé en revue. Il vérifiait que le total de la commande n'était pas `null`. Le développeur a protesté : « C'est un test utile, il vérifie le total ! »

**La démonstration.** Le QA a posé la question du module F2 : « ce test échoue si... quoi ? » Le développeur a répondu : « si le total est null. » — « Et quand est-ce que le total serait null ? » — « ...en théorie jamais. » — « Donc le test échoue jamais ? » — « ...ben, si le code est complètement cassé. » — « C'est-à-dire si le système ne tourne pas du tout. Ce test ne vérifie pas le total : il vérifie que le programme tourne. »

Le test a été supprimé, remplacé par un test manuel vérifiant le calcul réel du total (avec des cas nommables : remise, TVA multi-taux, total négatif interdit).

**Ce que ce cas enseigne.**
- La question « ce test échoue si... ? » est l'outil de tri le plus puissant. Elle transforme un débat d'opinion (« il est utile ! » / « non ! ») en une analyse factuelle.
- Les tests qui ne peuvent pas échouer sont nombreux dans les générations : ils vérifient des invariants triviaux. Leur coût (temps d'exécution, bruit dans les rapports) dépasse largement leur valeur.
- La suppression n'est pas une humiliation : le développeur de cet exemple a écrit le test de remplacement, bien meilleur. La critique du test n'est jamais la critique de la personne — c'est une règle de tri, pas un procès.

### Cas de la semaine 4 : le pipeline devenu mutex

**Situation.** Après l'ajout des tests générés au pipeline, le temps de build est passé de 8 à 34 minutes. Les développeurs ont commencé à repousser leurs commits en fin de journée pour éviter le pipeline — exactement l'effet inverse de la protection visée.

**Le diagnostic.** Les 127 tests générés de la campagne tournaient à chaque commit. Or la plupart (les tests lents de charge, de migration, les E2E complets) n'ont pas besoin de tourner à chaque commit.

**La correction.** La répartition en trois vitesses : les tests rapides et critiques (2 min) au commit ; les tests de régression standard (8 min) au merge sur la branche principale ; les tests lourds (E2E, charge, migration) en nocturne. Le pipeline est redescendu à 11 minutes. La protection n'a pas baissé : les tests nocturnes ont attrapé 2 régressions la première semaine.

**Ce que ce cas enseigne.**
- Le pipeline est un bien commun : quand il ralentit, les développeurs l'évitent, et la protection s'effondre. La vitesse du pipeline est une condition de la couverture, pas un luxe.
- La répartition en vitesses est la réponse standard. Elle demande une classification des tests (rapide/critique, standard, lourd) qui se fait naturellement lors du tri.
- Le test de validation de la répartition : les développeurs poussent-ils leurs commits en confiance ? Si un développeur attend 17h pour pousser, le pipeline est déjà trop lent.

### Cas de la semaine 6 : la transmission qui a révélé le guide creux

**Situation.** L'équipe voisine a suivi le guide de configuration pour sa première génération. Elle a buté sur une étape que le guide ne mentionnait pas : la configuration du profil de génération (`config.yaml` devait être copié depuis un modèle, ce que l'équipe pilote faisait de mémoire).

**La correction.** Trois questions notées, trois corrections du guide le jour même. Le guide est passé de version 2 à version 3. La transmission a repris le lendemain, et l'équipe voisine a généré sans aide.

**Ce que ce cas enseigne.**
- Le test à l'aveugle (exercice E5) n'est pas optionnel : un guide écrit par ceux qui savent est toujours creux. Les trous ne se voient que par un lecteur qui ne sait pas.
- Les questions de l'équipe voisine sont des corrections gratuites du guide : chaque question notée est une ligne évitée à toutes les équipes suivantes.
- La transmission est un service mutuel : l'équipe voisine apprend la chaîne, l'équipe pilote reçoit l'audit de son guide. Ne transmettez jamais « à sens unique ».

### Cas de la semaine 7 : l'incident que la génération n'aurait jamais attrapé

**Situation.** Un incident de production (corruption de données dans un cas de concurrence extrême) a été analysé avec l'exercice E3 : un test généré aurait-il pu le détecter ? Réponse honnête : non. Le modèle décrit les flux logiques, pas la concurrence. Aucun test généré n'aurait vu ce bug.

**La conclusion de l'équipe.** Plutôt que de blâmer la génération, l'équipe a documenté : « cette famille de bugs (concurrence) est hors de portée de la génération basée modèle. Elle relève des tests de charge et de stress, manuels, dans la passe nocturne. » La matrice de couverture a été mise à jour avec cette limite explicite.

**Ce que ce cas enseigne.**
- L'honnêteté sur les limites de la génération est plus précieuse que la promesse de sa toute-puissance. Une équipe qui dit « la génération ne couvre pas X » est crue quand elle dit « la génération couvre Y ».
- L'exercice E3 sur chaque incident entretient la carte des limites : c'est ainsi que la matrice de couverture devient un document de vérité et non un affichage de victoire.
- La matrice de couverture qui liste aussi ce qu'elle ne couvre pas est l'outil de communication le plus honnête avec les parties prenantes — et le plus rare.

## 3. Variantes contextuelles du niveau 4

### V1 : petite équipe (2-4 personnes)

- Le binôme de maintenance devient la rotation de deux personnes sur trois mois, avec le guide comme filet : dans une petite équipe, le guide doit être encore meilleur, car personne n'est disponible pour dépanner.
- La répartition en vitesses se simplifie : deux vitesses suffisent (commit rapide / nocturne complet).
- Le tri des tests se fait en binôme obligatoire (une personne seule triera trop indulgemment ses propres tests).
- La transmission à l'équipe voisine peut se faire en une session de deux heures si le guide est bon — investissez le temps sur le guide plutôt que sur les sessions.

### V2 : équipe distribuée

- Le tri asynchrone : chaque personne trie sa portion et remplit le `tri.md` ; une revue hebdo synchrone règle les cas contestés. La contestation asynchrone (commentaires écrits) fonctionne bien et laisse une trace.
- Le guide est l'actif central de la distribution : il doit être testé par au moins deux fuseaux avant publication (les hypothèses de disponibilité diffèrent).
- La passe nocturne « nocturne pour qui ? » : avec des fuseaux multiples, la fenêtre de nuit n'existe pas. Définissez la fenêtre de faible activité réelle (données d'usage, pas de intuition).
- Le canal `#gen-support` devient le lieu principal de dépannage : sa tenue (questions/réponses archivées et consultables) remplace partiellement la conversation informelle.

### V3 : legacy lourd

- La première génération sur un legacy produit souvent des tests sur des comportements surprenants du système actuel. Ne les supprimez pas d'office : chacun est une découverte du comportement réel. Classez-les « à qualifier » avant le tri standard.
- Les gabarits de génération doivent gérer les zones d'ombre du legacy : des données partielles, des états historiques, des règles implicites. Prévoyez un profil « legacy » avec plus de tolérance et moins d'assertions fortes.
- Le ratio utile sera plus bas au début (le modèle du legacy est approximatif) : c'est normal. La courbe de progression est le bon indicateur, pas le ratio absolu.
- Le tour de garde des gabarits est critique : les gabarits legacy évoluent souvent (on découvre les règles implicites). Sans rotation, le savoir reste chez celui qui a écrit le gabarit.

### V4 : organisation réglementée

- Le tri des tests devient une trace réglementaire : la justification des suppressions satisfait souvent une exigence de justification de la couverture. Le `tri.md` est un document d'audit.
- Les tests générés peuvent constituer la preuve de couverture exigée par le référentiel : la matrice de couverture avec les exécutions liées est le document à présenter.
- La répartition en vitesses doit être validée contre les exigences de fréquence de test du référentiel (certains exigent une exécution par build ; adaptez la vitesse rapide en conséquence).
- La transmission à une équipe voisine peut exiger une validation qualité formelle du guide : prévoyez-le dans le planning, ça prend deux semaines.

### V5 : le sponsor sceptique

- Le niveau 4 a l'argument le plus concret de tous : le test généré qui a trouvé le bug. Le « fait de la semaine » : « cette semaine, la génération a produit 247 tests, nous en avons gardé 89, et l'un d'eux a trouvé un bug que 6 mois de tests manuels n'avaient pas vu ».
- Le sponsor sceptique va demander le ROI de l'infrastructure (vs les tests manuels). Le ratio honnête en trois colonnes (gagné mesuré, coût mesuré, pas encore mesurable) est la seule réponse qui tient.
- Le moment de bascule : la première régression attrapée par la passe nocturne. Elle doit être documentée et racontée : c'est la preuve que la chaîne protège pendant que personne ne regarde.

### V6 : reprise après échec

- Si une tentative de génération a déjà échoué, le guide existant (s'il existe) est probablement creux ou faux : le test à l'aveugle est le premier acte de la reprise.
- La reprise commence par un profil minimal : un seul modèle, un seul gabarit, un seul tri. La chaîne complète est reconstruite après ce premier succès — pas avant.
- L'erreur passée (souvent : generation too big too fast) est nommée explicitement en ouverture de reprise : « la dernière fois, on a généré 2000 tests et le pipeline est mort. Cette fois : un modèle, une campagne, on évalue. »

---

## Comment utiliser cette partie

- **Au démarrage** : la variante de votre contexte, et le cas de la semaine 1 (la génération qui a échoué) — il fixe la culture de la chaîne.
- **Pendant le parcours** : le cas du pipeline mutex (semaine 4) est le plus fréquent des blocages du niveau 4.
- **À la semaine 8** : comparez votre guide et vos critères de tri avec les exemples. Le test de qualité : un nouveau mainteneur peut-il suivre votre guide seul ?
