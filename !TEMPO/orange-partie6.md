
---

# Partie 6 : Formation, exercices et évaluation du niveau 2

Cette partie est l'équivalent, pour le niveau 2, de la Partie 4 de ROUGE : les capsules formatées pour un lecteur qui n'a pas vécu la mission, les exercices avec corrigés, et les évaluations d'acquisition des compétences du niveau 2.

## 1. Les capsules du niveau 2

Chaque capsule suit le format de ROUGE : description, raison, exemple, piège, exercice. Le lecteur de ROUGE connaît le format ; voici les huit capsules du niveau 2.

### Capsule 2.1 — Le modèle BPMN des processus réels

**Description.** Un modèle BPMN décrit un processus en événements, tâches, passerelles et flux. Le niveau 2 modélise les processus réels de l'équipe — pas les processus idéaux du manuel.

**Raison.** Les malentendus entre rôles vivent dans les processus réels, rarement écrits. Le modèle rend le processus discutable : chacun peut pointer ce qui n'est pas ce qu'il fait.

**Exemple.** Le processus de correction de bug modélisé avec trois sources de détection, une passerelle de criticité, une tâche de spécification de correction, et la mise à jour du modèle lui-même.

**Piège.** Modéliser le processus idéal (« ce que nous devrions faire »). Le modèle de l'idéal ne révèle aucun malentendu, car tout le monde est d'accord sur l'idéal. Le modèle du réel, lui, provoque les « attends, toi tu fais ça ? ».

**Exercice.** Modélisez votre processus de correction de bug tel qu'il se passe vraiment, y compris les contournements. Comptez les divergences trouvées lors de la confrontation. Objectif : au moins deux.

### Capsule 2.2 — La confrontation des modèles entre rôles

**Description.** Chaque binôme de rôles différents décrit le modèle de l'autre à partir de ce qu'il croit, puis compare avec le modèle réel. Les écarts sont les malentendus.

**Raison.** On ne découvre pas ses propres malentendus en regardant son propre modèle. La confrontation croisée est le mécanisme de découverte — c'est l'atelier le plus rentable du niveau 2.

**Exemple.** Le développeur décrit le modèle du QA : « tu testes avant la correction ». Le modèle réel dit le contraire. Quarante ans de confusion réglés en quarante minutes.

**Piège.** Transformer la confrontation en procès (« tu fais mal »). La règle du jeu : on décrit, on compare, on corrige le processus ensemble — jamais on ne juge la personne. Le ton est celui d'une découverte, pas d'un procès.

**Exercice.** Binôme développeur/QA : chacun décrit le modèle de l'autre en trois phrases. Comparez avec le modèle réel. Notez les écarts — ce sont vos sujets d'atelier suivants.

### Capsule 2.3 — La spécification à partir du modèle

**Description.** Toute fonctionnalité ou correction commence par une spécification dérivée du modèle BPMN : comportements, règles de validation, cas limites.

**Raison.** La spécification du niveau 2 n'est pas une page libre : elle hérite de la structure du modèle. C'est ce qui la rend complète par construction — les passerelles du modèle deviennent les cas limites de la spécification.

**Exemple.** La spécification du correctif BUG-1247 : une page, trois règles de validation numérotées, un cas limite métier explicite.

**Piège.** Écrire la spécification à partir de la demande client directement, en sautant le modèle. C'est le niveau 1 déguisé. La valeur du niveau 2 vient précisément du passage par le modèle.

**Exercice.** Prenez la prochaine demande. Modélisez-la d'abord (même grossièrement, 20 minutes). Puis écrivez la spécification à partir du modèle. Comparez avec ce que vous auriez écrit sans modèle : le cas limite oublié est la preuve de valeur.

### Capsule 2.4 — La documentation liée au modèle

**Description.** La documentation produit est liée au modèle : chaque page cite sa source (modèle, révision) et se met à jour à chaque révision du modèle.

**Raison.** La documentation orpheline devient fausse en silence. La documentation liée devient fausse de manière visible — la référence permet de la vérifier.

**Exemple.** La page « Comportement du filtre du rapport X » avec sa référence BPM-004, révision 3, et sa synchronisation automatique.

**Piège.** Générer de la documentation sans qu'elle soit lue. Le test d'une documentation vivante : quelqu'un la cite. Si personne ne la cite en trois mois, elle est morte — réduisez-la plutôt que de l'automatiser davantage.

**Exercice.** Prenez la page de documentation la plus consultée de votre wiki. Vérifiez si elle cite sa source. Sinon : trouvez le modèle correspondant, ajoutez la référence, et vérifiez la page contre le modèle. Les divergences trouvées sont vos premières preuves.

### Capsule 2.5 — Le plan lié aux modèles

**Description.** Chaque élément du plan de livraison est lié à son modèle et à son état de preuve : modélisé, spécifié, prouvé. Les éléments non modélisés sont catégorisés comme tels.

**Raison.** Le plan lié répond factuellement à « où on en est ? ». La catégorie « non modélisé » rend l'incertitude visible au lieu de la maquiller.

**Exemple.** Le plan du trimestre avec quatre éléments ferme et deux en investigation de modèle, avec dates de résolution.

**Piège.** Le plan à trois états (vert/orange/rouge) sans critères. Chaque état du niveau 2 a un critère : « modélisé » signifie « le modèle existe et a été confronté », pas « quelqu'un a l'intention de le modéliser ».

**Exercice.** Prenez votre plan actuel. Pour chaque élément, demandez : le modèle existe-t-il ? A-t-il été confronté ? Classez. Comptez les « non modélisés » — ce sont vos zones d'incertitude réelles.

### Capsule 2.6 — Les tests générés par le modèle (MBT)

**Description.** La matrice de couverture inclut les tests générés par le modèle : les chemins et combinaisons que le modèle contient deviennent des tests exécutables.

**Raison.** Le modèle raisonne plus systématiquement que les humains. Les tests générés couvrent les combinaisons que l'expérience ne pense pas à écrire.

**Exemple.** Le test généré T-042, combinaison de filtres non écrite manuellement, qui a détecté le défaut de comportement combiné.

**Piège.** Générer des centaines de tests sans prioriser. Le générateur produit beaucoup ; la valeur vient de la sélection. Le ratio honnête est celui du cas T-042 : un test utile pour quarante produits.

**Exercice.** Générez les tests d'une passerelle de votre modèle. Sélectionnez-en trois à garder (les combinaisons rares). Documentez le ratio. Ce document devient votre première preuve MBT.

### Capsule 2.7 — La maintenance du modèle

**Description.** Le modèle est maintenu : à chaque divergence processus réel/modèle, le processus ou le modèle est corrigé, et la correction est datée.

**Raison.** Un modèle non maintenu devient faux en silence — pire qu'un modèle absent, car il inspire une confiance imméritée. La maintenance est la condition de vie du modèle.

**Exemple.** Trois corrections de modèle datées dans un mois, chacune provenant d'une divergence détectée en production ou en confrontation.

**Piège.** Laisser le modèle se dégrader parce que « personne n'a le temps ». La règle : une divergence détectée est corrigée dans la semaine, sinon le modèle est marqué « non fiable à partir du [date] ». Un modèle marqué non fiable est honnête ; un modèle faux mais non marqué est un piège.

**Exercice.** Comptez les corrections de modèle des trois derniers mois. Zéro signifie que le modèle n'est pas utilisé (pas que le processus est parfait). Cherchez la divergence la plus récente : elle devrait exister.

### Capsule 2.8 — Le rapport de maturité du niveau 2

**Description.** À la fin du niveau 2, l'équipe produit son rapport : les modèles vivants, les malentendus trouvés et corrigés, la documentation citée, les tests générés utiles, et les métriques honnêtes.

**Raison.** Le rapport du niveau 2 est la preuve que la modélisation vit au-delà de la mission. Sa structure est celle du rapport du niveau 1, avec les catégories du niveau 2.

**Exemple.** Le rapport de la mission Faucon : deux modèles vivants, onze malentendus corrigés, trois pages de documentation citées, un test généré utile, un modèle marqué non fiable et restauré.

**Piège.** Le rapport de succès sans les métriques honnêtes. Le rapport qui ne dit pas « 40 tests produits, 1 utile » n'est pas un rapport de maturité : c'est une brochure.

**Exercice.** Écrivez la première page de votre rapport de maturité du niveau 2 : le fait le plus marquant, puis les métriques honnêtes, y compris celles qui ne flattent pas.

## 2. Les exercices du niveau 2 avec corrigés

### Exercice A : le modèle du réel (capsules 2.1 et 2.2)

**Consigne.** En binôme de rôles différents, modélisez votre processus de correction de bug tel qu'il se passe vraiment. Puis chacun décrit le modèle de l'autre. Comptez les écarts.

**Corrigé (exemple de l'équipe Faucon).**

Modèle réel obtenu (extrait) :
- Détection : 3 sources (test auto, client via support, interne).
- Qualification : critères écrits, mais une exception orale (« les bugs du client VIP passent la file ») — pas dans les critères écrits. **Divergence 1 : le processus réel contient une exception orale.**
- Après qualification : les deux rôles avaient modélisé la correction directement. Le processus réel contient une étape de spécification courte dans 60 % des cas (quand le correctif touche un comportement documenté), et pas dans les autres. **Divergence 2 : le modèle binaire (spécification toujours / jamais) était faux ; le réel est conditionnel.**
- Vérification : le modèle du QA plaçait la vérification avant la mise en production ; le réel la place après, sous forme de CONFIRMATION client dans 30 % des cas. **Divergence 3.**

Résultat : 3 divergences, dont une exception orale qui aurait dû être un critère écrit depuis longtemps.

**Ce que le corrigé enseigne.** Les divergences les plus précieuses sont les exceptions orales et les comportements conditionnels — les endroits où le modèle binaire simplifie le réel. Cherchez-les délibérément.

### Exercice B : la spécification dérivée du modèle (capsule 2.3)

**Consigne.** Prenez une demande en attente. Modélisez-la en 20 minutes. Écrivez la spécification à partir du modèle. Identifiez ce que la spécification contient que la demande ne disait pas.

**Corrigé (exemple).**

Demande : « Ajouter un filtre par statut au rapport Y. »

Modèle obtenu : passerelle « statut unique ou combiné ? », passerelle « valeur vide = tout ou rien ? », événement « filtre sauvegardé avec la vue ? ».

Spécification dérivée (extrait) :
1. Le filtre s'applique à la colonne statut ; une valeur vide dans le filtre signifie « tous les statuts ».
2. Le filtre se combine aux filtres existants par ET logique.
3. Le filtre choisi est sauvegardé avec la vue (comportement du rapport X, cohérence).
4. Cas limite : les statuts archivés n'apparaissent pas dans le filtre, mais les lignes archivées déjà filtrées restent visibles.

Ce que la spécification contient que la demande ne disait pas : les points 1, 3 et 4. Le point 3 vient de la cohérence avec le modèle du rapport X — c'est la valeur du passage par le modèle : il hérite des décisions déjà prises.

### Exercice C : la documentation vivante (capsule 2.4)

**Consigne.** Vérifiez trois pages de documentation contre leurs sources. Comptez les divergences. Corrigez ou marquez.

**Corrigé (exemple de l'équipe Faucon).**

| Page | Vérifiée contre | Divergences |
|---|---|---|
| « Comportement du filtre X » | BPM-004 rév. 3 | 2 (la règle des valeurs nulles n'était pas documentée ; la règle de combinaison était fausse) |
| « Processus de livraison » | BPM-002 rév. 5 | 1 (l'étape de revue QA avait changé de place dans le réel) |
| « Guide du nouveau arrivant » | aucune source | orpheline — marquée « à lier à un modèle » |

Résultat : 3 divergences dans 2 pages vérifiables, 1 page orpheline. Les divergences sont corrigées ; la page orpheline est marquée.

### Exercice D : le plan lié (capsule 2.5)

**Consigne.** Classez les éléments de votre plan actuel : modélisé et confronté / modélisé non confronté / non modélisé. Présentez la répartition à votre sponsor.

**Corrigé (exemple).**

Répartition de l'équipe Faucon au début de la semaine 3 : 4 ferme (modélisés et confrontés), 1 modélisé non confronté, 2 non modélisés. Le sponsor a vu la répartition et a demandé : « Pourquoi les deux ne sont pas modélisés ? » Réponse : « Ils dépendent d'une décision métier pas encore prise. Voici la décision et la date. » Le plan a été validé avec cette transparence.

## 3. Les évaluations d'acquisition du niveau 2

Les évaluations du niveau 2 vérifient que les compétences sont acquises, pas que les artefacts existent.

### Évaluation 1 : modélisation (capsule 2.1)

**Tâche.** Modélisez un processus réel de votre équipe en 45 minutes.

**Critères de réussite.**
- Le modèle décrit le réel, y compris une exception ou un comportement conditionnel (pas le processus idéal).
- Les éléments BPMN sont corrects (événements, tâches, passerelles, flux).
- Un lecteur du modèle peut décrire le processus sans demander.

**Échec type.** Un modèle propre qui décrit l'idéal. Il est sans valeur pour la découverte des malentendus.

### Évaluation 2 : confrontation (capsule 2.2)

**Tâche.** En binôme, décrivez le modèle de l'autre en trois phrases, puis comparez.

**Critères de réussite.**
- La description est formulée à partir du modèle de l'autre, pas du sien.
- Les écarts trouvés sont notés comme sujets d'atelier, sans jugement de personne.
- Au moins un écart réel est identifié.

**Échec type.** Décrire son propre modèle au lieu de celui de l'autre. C'est l'erreur la plus fréquente — la consigne est d'y veiller explicitement.

### Évaluation 3 : spécification dérivée (capsule 2.3)

**Tâche.** Écrivez la spécification d'une demande à partir de son modèle.

**Critères de réussite.**
- La spécification hérite de la structure du modèle (chaque passerelle devient un cas).
- Elle contient au moins un élément que la demande ne disait pas.
- Un développeur peut la coder sans poser de question.

**Échec type.** Une spécification écrite à partir de la demande, le modèle étant décoratif. La valeur du niveau 2 est alors absente.

### Évaluation 4 : maintenance (capsule 2.7)

**Tâche.** Montrez la dernière divergence processus/modèle et sa correction.

**Critères de réussite.**
- La divergence est réelle, datée, et sa résolution est documentée.
- La correction a été faite dans la semaine de la détection.
- Le modèle est fiable à la date du jour (ou marqué non fiable, ce qui est aussi une réponse correcte).

**Échec type.** Un modèle jamais corrigé depuis des mois, présenté comme à jour. Il inspire une confiance imméritée — c'est pire qu'absent.

## 4. Le gabarit de rapport de maturité du niveau 2

```
# Rapport de maturité — niveau 2
Équipe : [nom]     Mission : [nom]     Période : [dates]

## Le fait le plus marquant
[Une phrase : la découverte ou l'événement qui a le plus changé la façon de travailler]

## Les modèles vivants
| Modèle | Révision | Dernière correction | Confrontée ? |
|---|---|---|---|
| BPM-00x | rév. n | date | oui/non |

## Les malentendus trouvés et corrigés
[Nombre et 2-3 exemples, dont le plus surprenant]

## La documentation liée
| Page | Source | Synchronisée ? |
|---|---|---|

## Les tests générés
Produits : [n]   Sélectionnés : [n]   Utiles (défauts trouvés) : [n]

## Les métriques honnêtes
- Ce que le niveau 2 a coûté : [heures, points durs]
- Ce qu'il a rapporté : [les preuves, y compris les signes externes]
- Ce qui n'a pas marché : [honnêteté obligatoire]

## Ce qui continue sans le coach
[Qui maintient quoi, à quelle cadence, avec quel critère]
```

---

## Comment utiliser cette partie

- **Pour animer** : les capsules 2.1 à 2.8 se donnent en 20 minutes chacune, au début des semaines correspondantes.
- **Pour exercer** : les exercices A à D se font dans les ateliers correspondants.
- **Pour évaluer** : les évaluations 1 à 4 se passent aux semaines 2, 4, 6 et 8.
- **Pour conclure** : le gabarit de rapport se remplit à la semaine 8, avec le sponsor présent.
