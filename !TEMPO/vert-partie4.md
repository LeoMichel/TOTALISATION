
---

# Partie 4 : Formation, exercices et évaluation (niveau 4)

Le niveau 4 rend l'automatisation infrastructurelle. Cette partie la rend transmissible : former à BEASTEST sans en faire un mystère, exercer la génération critique, évaluer la qualité de la génération — pas seulement sa vitesse. Un outil qui ne se transmet pas génère une dépendance ; un outil qui se transmet génère une capacité.

## Le principe du niveau 4 : former à l'outil, éduquer au jugement

BEASTEST génère des tests à partir des modèles. Mais la génération sans jugement produit des tests qui ne testent rien : verts, rapides, vides. La formation du niveau 4 a donc deux volets indissociables :

1. **Le volet outil** : configurer, lancer, lire les sorties, maintenir les gabarits. C'est technique, c'est transmissible en quelques sessions.
2. **Le volet jugement** : reconnaître un test généré qui ne vérifie rien, repérer une couverture apparente, savoir quand ne pas faire confiance à la génération. C'est le volet qui distingue un utilisateur d'un praticien — et c'est lui qui demande le plus d'exercices.

Chaque module ci-dessous combine les deux volets. La règle : **aucune session de formation BEASTEST sans au moins un exercice de critique de sortie générée.**

---

## Modules de formation niveau 4

### Module F1 : Configurer et lancer une première génération

**Durée :** 90 minutes. **Public :** tout nouveau membre de l'équipe, ou l'équipe voisine qui prépare son niveau 4.

**Objectif :** à la fin de la session, le participant a généré une première série de tests à partir d'un modèle réel, et sait où sont les résultats.

**Matériel :** un modèle BPMN/MBT stable de l'équipe, un environnement BEASTEST configuré (ou l'outil de génération en place), le guide de configuration de l'équipe.

**Déroulé :**

| Temps | Séquence | Contenu |
|---|---|---|
| 0-15 min | Le principe avant le clic | Pourquoi générer à partir d'un modèle : le modèle est la source de vérité, les tests en sont des projections. Générer sans modèle, c'est projeter sans source. Rappel des règles du niveau 2. |
| 15-40 min | Configuration guidée | Le participant configure son environnement en suivant le guide réel de l'équipe. Chaque choix de configuration est expliqué (profondeur de génération, filtres, exclusions). |
| 40-65 min | Première génération | Génération sur le modèle réel. Lecture des résultats : combien de tests générés, quels chemins couverts, quels chemins ignorés. |
| 65-80 min | Première critique | Chaque participant choisit trois tests générés et tente d'expliquer ce que chacun vérifie réellement. Ceux qui n'y arrivent pas découvrent le volet jugement. |
| 80-90 min | Consolidation | Où sont les résultats, comment les relancer, qui contacter en cas d'échec. Ces trois réponses sont écrites dans le guide de l'équipe. |

**Critère de réussite :** le participant relance une génération seul, une semaine plus tard, et retrouve ses résultats.

**Piège classique :** la session démo où tout fonctionne du premier coup parce que l'environnement était pré-configuré. Corriger : faire configurer réellement, y compris les erreurs de configuration. C'est en corrigeant une erreur de gabarit qu'on apprend ce que l'outil fait vraiment.

### Module F2 : Critiquer une sortie générée

**Durée :** 90 minutes. **Public :** tous ceux qui consomment des tests générés (QA, devs, PO).

**Objectif :** rendre chaque participant capable d'évaluer un test généré : que vérifie-t-il ? Que manque-t-il ? Vaut-il la maintenance ?

**Matériel :** 10 tests générés par BEASTEST sur un modèle réel, dont 3 volontairement faibles (assertions absentes, chemins redondants, données triviales).

**Déroulé :**

| Temps | Séquence | Contenu |
|---|---|---|
| 0-10 min | Les trois défauts types | (1) Le test vert vide : il passe mais ne vérifie rien. (2) Le test redondant : il répète un chemin déjà couvert. (3) Le test fragile : il dépend d'une donnée ou d'un ordre non garanti. |
| 10-40 min | Chasse aux défauts | Par binôme, trier les 10 tests : valables / faibles / à supprimer, avec justification. Les binômes divergent presque toujours sur 2 ou 3 tests : c'est le matériel du débrief. |
| 40-60 min | Débrief des divergences | Pour chaque test contesté : qu'est-ce qui rend le jugement difficile ? Souvent : la différence entre « le test passe » et « le test prouve ». |
| 60-80 min | Rédaction des critères de tri | L'équipe écrit ses propres critères de tri des tests générés (3 à 5 critères max). Ces critères rejoignent les règles d'usage de l'outil. |
| 80-90 min | Application réelle | Tri réel des derniers tests générés par l'équipe, avec les nouveaux critères. Les tests supprimés sont documentés (pourquoi). |

**Critère de réussite :** les critères de tri écrits sont appliqués à la génération suivante, et le ratio tests conservés/supprimés est consigné.

**Piège classique :** jeter tous les tests faibles sans consigner pourquoi. La consignation est ce qui transforme la critique en connaissance : la prochaine génération sera meilleure si l'on sait ce qui a été rejeté et pourquoi.

### Module F3 : Maintenir les gabarits et les modèles

**Durée :** 75 minutes. **Public :** les responsables de modèles et les mainteneurs de la chaîne de génération.

**Objectif :** transmettre la maintenance de la chaîne modèle → gabarit → génération : qui met à jour quoi, comment, et comment détecter qu'un gabarit dérive.

**Matériel :** la chaîne de génération réelle, l'historique des dernières modifications de modèles, le journal des échecs de génération.

**Déroulé :**

| Temps | Séquence | Contenu |
|---|---|---|
| 0-15 min | La chaîne et ses gardiens | Cartographie : qui maintient les modèles (niveau 2), qui maintient les gabarits (niveau 4), qui consomme les sorties. Les goulots sont là où un nom revient trop souvent. |
| 15-35 min | Cas réel de dérive | Un gabarit qui a dérivé est analysé : comment l'équipe s'en est-elle aperçue (ou pas) ? Quel a été le coût de la non-détection ? Quel signal aurait permis de la détecter plus tôt ? |
| 35-55 min | Exercice : le signal de dérive | L'équipe définit deux signaux de dérive de gabarit (ex. : taux d'échec de génération, ratio de tests rejetés par la critique) et les ajoute au tableau de bord N4. |
| 55-70 min | Le tour de garde | Définition du tour de garde des gabarits : qui surveille, à quelle fréquence, avec quel droit de correction. Un mainteneur unique est un goulot ; une rotation documentée est une infrastructure. |
| 70-75 min | Consolidation | Le guide de maintenance est mis à jour avec les signaux et le tour de garde. |

**Critère de réussite :** les signaux de dérive sont actifs au tableau de bord, et le tour de garde est documenté avec au moins deux noms.

**Piège classique :** le mainteneur unique et héroïque. Corriger : la rotation. Une infrastructure qui dépend d'une seule personne n'est pas une infrastructure, c'est une personne avec un titre.

### Module F4 : La couverture systématique sans sur-test

**Durée :** 90 minutes. **Public :** QA, devs, PO.

**Objectif :** utiliser la génération pour atteindre la couverture systématique (semaine 7) sans générer des milliers de tests qui ralentissent le pipeline sans le protéger.

**Matériel :** la matrice de couverture N4, le temps d'exécution actuel du pipeline, les rapports des trois dernières générations.

**Déroulé :**

| Temps | Séquence | Contenu |
|---|---|---|
| 0-15 min | Le paradoxe de la génération | Générer est peu coûteux, exécuter coûte cher. Une couverture systématique mal pilotée transforme le pipeline en mutex : tout le monde attend. |
| 15-40 min | Exercice : le tri par valeur | Pour une fonctionnalité critique : quels tests générés appartiennent au pipeline de chaque livraison (rapides, critiques), et quels tests appartiennent à la passe nocturne ou hebdomadaire ? Le groupe remplit la répartition. |
| 40-60 min | Mesure d'impact | Le temps actuel du pipeline est comparé à la projection avec la répartition proposée. Objectif : la couverture monte sans que le pipeline ralentisse. |
| 60-80 min | Les seuils de suppression | Définir quand un test généré quitte la suite : obsolète, redondant après refactorisation, jamais échoué en X mois (test suspect d'inutilité). Ces seuils sont écrits. |
| 80-90 min | Consolidation | La politique de répartition est documentée et ajoutée au guide de l'équipe. |

**Critère de réussite :** la répartition pipeline/passe nocturne est active, et le temps du pipeline est resté stable (ou a baissé) pendant que la couverture montait.

**Piège classique :** la couverture comme nombre à maximiser. Corriger : la couverture comme risque à piloter. Un test qui ne peut jamais échouer ne couvre rien ; un pipeline qui met 40 minutes à cause de tests redondants protège moins qu'un pipeline de 12 minutes ciblé.

### Module F5 : Transmettre la chaîne de génération à une équipe voisine

**Durée :** 120 minutes. **Public :** les catalyseurs N4, l'équipe voisine.

**Objectif :** transmettre la chaîne complète (modèle → gabarit → génération → critique → pipeline) à une équipe voisine, avec les artefacts réels et les erreurs déjà commises.

**Matériel :** les modules F1 à F4, le journal des échecs de génération de l'équipe pilote, un modèle de l'équipe voisine.

**Déroulé :**

| Temps | Séquence | Contenu |
|---|---|---|
| 0-20 min | Le format de transmission | Règle établie au niveau 3 : on n'apporte pas de slide, on apporte la chaîne. L'équipe voisine repartira avec : le guide de configuration, les gabarits, les critères de tri, les seuils de suppression. |
| 20-60 min | Première génération sur le modèle de l'équipe voisine | L'équipe voisine génère sur son propre modèle (pas celui de l'équipe pilote). Les premiers échecs sont l'occasion d'enseigner la lecture des erreurs. |
| 60-90 min | La critique des sorties | Les sorties sont triées avec les critères de l'équipe pilote. L'équipe voisine adapte les critères à son contexte (et documente ses adaptations). |
| 90-110 min | Le tour de garde de l'équipe voisine | Qui maintient quoi chez eux ? Les goulots sont identifiés avant qu'ils ne deviennent des dépendances. |
| 110-120 min | Le suivi | Date de revue commune à 30 jours : ce qui a tenu, ce qui a dérivé, ce qui a été abandonné (et pourquoi). |

**Critère de réussite :** l'équipe voisine a généré, critéré et intégré des tests dans son pipeline dans les 30 jours, sans intervention continue de l'équipe pilote.

**Piège classique :** transmettre l'outil et pas la chaîne. L'équipe voisine qui a l'outil sans les critères de tri générera vite des tests vides en masse — et en tirera la conclusion que la génération ne marche pas. La critique transmise vaut plus que l'outil.

---

## Exercices d'approfondissement

### Exercice E1 : La chasse au test vert vide

**Durée :** 60 minutes, en binôme. **Prérequis :** la dernière génération BEASTEST.

**Consigne :** prenez 20 tests générés récemment. Pour chacun, répondez en une phrase : « ce test échoue si… ». Si vous ne pouvez pas compléter la phrase (ou si la réponse est « si le serveur est en panne », ce qui n'est pas un test), le test est vide.

**Grille de correction :** moins de 3 tests vides sur 20 : chaîne saine. Plus de 10 : la génération produit du volume, pas de la protection — revoir les gabarits avant de générer à nouveau. Chaque test vide est supprimé ou corrigé, avec la raison consignée.

**Ce que l'exercice révèle :** le ratio réel de protection de la génération. C'est la métrique que la qualimétrie N4 devrait suivre : pas le nombre de tests générés, mais le nombre de tests qui *peuvent échouer pour une bonne raison*.

### Exercice E2 : Le modèle menteur

**Durée :** 75 minutes en groupe. **Prérequis :** un modèle BPMN réel, sa dernière génération.

**Consigne :** modifiez volontairement une passerelle du modèle pour qu'il contienne une erreur (une condition impossible, une séquence illégale). Régénérez. Question : les tests générés détectent-ils l'absurdité, ou la reproduisent-ils fidèlement ?

**Grille de correction :** si les tests reproduisent l'absurdité (cas attendu), la leçon est en place : la génération est fidèle au modèle, donc elle hérite de ses erreurs. L'équipe écrit alors la règle : « la revue du modèle précède la génération, toujours » — et définit qui fait la revue.

**Ce que l'exercice révèle :** la génération n'ajoute pas de vérité, elle multiplie celle du modèle. Un modèle faux à 90 % produit des tests faux à 90 %, plus vite. C'est l'argument le plus fort pour les règles du niveau 2, revisité au niveau 4.

### Exercice E3 : L'incident de la nuit

**Durée :** 90 minutes. **Prérequis :** un incident réel de production des trois derniers mois.

**Consigne :** reprenez l'incident et demandez-vous : un test généré aurait-il pu le détecter ? Si oui, pourquoi n'existait-il pas (modèle incomplet ? gabarit trop étroit ? critère de tri l'ayant éliminé ?). Si non, quel type de test l'aurait détecté, et pourquoi la génération n'en produit pas ?

**Grille de correction :** pour chaque incident, une réponse écrite en trois lignes : le test qui l'aurait attrapé, ce qui l'a empêché d'exister, l'action concrète pour la prochaine génération. Ces réponses alimentent la revue des gabarits.

**Ce que l'exercice révèle :** la génération protège ce que les modèles décrivent. Les incidents vivent souvent dans les zones que les modèles ne décrivent pas : données réelles, concurrence, dégradation progressive. L'exercice fait remonter ces zones vers les modèles.

### Exercice E4 : Le coût réel de la suite

**Durée :** 60 minutes, seul puis en groupe. **Prérequis :** accès aux temps d'exécution du pipeline sur un mois.

**Consigne :** calculez le coût réel de la suite de tests générés : temps total d'exécution × fréquence × nombre de développeurs en attente. Comparez au temps que les échecs attrapés ont économisé (incidents évités, reprises évitées). Le ratio vous dit si la suite protège ou consomme.

**Grille de correction :** ratio > 1 (protège plus qu'elle ne consomme) : la suite est saine. Ratio < 1 : soit la suite est trop lourde (voir module F4), soit elle attrape trop peu (revoir les gabarits). Dans les deux cas, l'action est consignée avec une date.

**Ce que l'exercice révèle :** la suite de tests est un investissement, pas un poste de coûts moral. La mesurer en langage business est ce qui permet de défendre la couverture devant la direction — et de couper ce qui ne protège pas.

### Exercice E5 : La transmission à l'aveugle

**Durée :** 45 minutes. **Prérequis :** le guide de configuration de l'équipe.

**Consigne :** donnez le guide à un collègue d'une autre équipe. Il configure son environnement en suivant le guide seul, sans poser de question (les questions sont notées, pas répondues). Chaque question notée est une faille du guide.

**Grille de correction :** moins de 3 questions sur l'installation complète : guide conforme. Chaque question est transformée en correction du guide le jour même. Le guide est re-versionné.

**Ce que l'exercice révèle :** les guides écrits par ceux qui savent déjà sont des guides troués. Le test à l'aveugle est le seul qui révèle les trous avant qu'ils ne coûtent une journée à l'équipe voisine.

### Exercice E6 : Le trimestre de la génération

**Durée :** 120 minutes, à la fin de chaque trimestre. **Prérequis :** les registres du trimestre (générations, tris, incidents, dérives).

**Consigne :** l'équipe relit les registres du trimestre et répond par écrit : (1) quel gabarit a le plus dérivé, et pourquoi ? (2) quel type de test a attrapé le plus de défauts réels ? (3) quel type n'a rien attrapé — le garder, et pourquoi ? (4) la chaîne est-elle plus rapide ou plus lente qu'il y a trois mois, et est-ce mieux ?

**Grille de correction :** les quatre réponses sont écrites, datées, publiées au centre d'excellence. Les actions qui en découlent (modifier un gabarit, retirer un type, doubler le tour de garde) ont un propriétaire et une date. Sans action datée, la revue trimestrielle est un rituel de consolation.

**Ce que l'exercice révèle :** l'infrastructure vit. Ce qui était optimal il y a trois mois ne l'est plus. La revue trimestrielle est le mécanisme qui empêche l'infrastructure de devenir un musée.

---

## Les grilles d'évaluation du niveau 4

### Grille de maturité de la chaîne de génération (fin de semaine 8, puis trimestrielle)

| Élément | Niveau 3 (départ) | Niveau 4 (acquis) | Niveau 5 (en vue) | Preuve requise |
|---|---|---|---|---|
| Génération à partir du modèle | Manuelle ou pilote | Systématique, relancée à chaque évolution du modèle | Optimisée par apprentissage des tris | Historique de générations lié aux versions du modèle |
| Qualité des sorties | Non évaluée | Critères de tri écrits et appliqués | Ratio de protection mesuré | Registre des tris avec justifications |
| Intégration pipeline | Tests générés hors pipeline | Répartition pipeline/passe nocturne active | Temps de pipeline optimisé | Temps de pipeline stable avec couverture croissante |
| Maintenance des gabarits | Un mainteneur | Tour de garde documenté, signaux de dérive actifs | Gabarits versionnés et revus | Signaux au tableau de bord, rotation nominative |
| Transmission | Non entamée | Un module répété, artefacts préparés | Une équipe voisine opérationnelle | Guide re-versionné après test à l'aveugle |
| Retour d'incident | Non structuré | Exercice E3 fait sur chaque incident | Gabarits enrichis par les incidents | Registre des incidents avec action de génération |

**Règle de remplissage :** comme au niveau 3 — aucun niveau sans preuve nommée. La colonne « preuve requise » est le garde-fou contre l'auto-satisfaction.

### Le test des cinq questions de fin de niveau 4

À la fin des huit semaines, l'équipe répond par écrit, publie au centre d'excellence :

1. **Quelle proportion de nos tests de régression sont générés, et quelle proportion devrait l'être ?** (Un chiffre, avec l'écart assumé.)
2. **Quel test généré a attrapé un défaut réel ce trimestre ?** (S'il n'y en a aucun, la génération protège-t-elle ou décore-t-elle ?)
3. **Où notre modèle est-il le plus mensonger, et qui le sait ?** (L'exercice E2 appliqué honnêtement.)
4. **Si le mainteneur des gabarits part demain, qui prend le relais, et en combien de temps ?** (Une réponse nominative, avec un délai crédible.)
5. **Qu'est-ce que l'équipe voisine a réussi à faire seule avec notre chaîne ?** (Le test réel de la transmission.)

Ces cinq réponses sont le contrat d'entrée du niveau 5 (BLEU), où la chaîne s'industrialise au-delà de l'équipe pilote. Ce qui n'est pas répondu ici sera demandé là — mieux vaut le savoir maintenant.

---

## Le bilan de la partie formation du niveau 4

Le niveau 4 réussit quand trois phrases sont vraies en même temps :

- **La génération est systématique** : chaque évolution de modèle déclenche une régénération, sans décision humaine d'« on a le temps cette semaine ».
- **La critique est institutionnalisée** : les tests générés sont triés par des critères écrits, pas par l'habitude.
- **La chaîne est transmissible** : une équipe voisine peut l'adopter avec les artefacts seuls, sans l'équipe pilote à ses côtés.

Si l'une des trois phrases n'est pas vraie, le niveau 4 est à moitié fait — et c'est une information utile, pas une honte. Le niveau 5 (BLEU) traitera l'industrialisation ; il vaut mieux lui transmettre une chaîne complète qu'une chaîne rapide.
