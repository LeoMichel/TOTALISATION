
---

# Partie 12 : Exercices avancés, FAQ et anti-patterns du niveau 2

## 1. Exercices avancés (E7 à E12 du niveau 2)

### Exercice E7 : La génération à l'aveugle

**Durée :** 90 minutes. **Prérequis :** un modèle confronté, un outil de génération.

**Consigne :** deux binômes génèrent indépendamment les tests du même modèle (sans se consulter). Comparez les sorties : combien de tests identiques ? Différents ? Les différences révèlent soit des options de configuration divergentes, soit des interprétations différentes du modèle.

**Ce que l'exercice révèle :** l'ambiguïté de la configuration de génération. Les tests différents sur le même modèle ne sont pas un problème : ils sont une richesse (couverture élargie). Mais ils doivent être compris — sinon le pipeline produit des sorties dont personne ne maîtrise le périmètre.

**Grille de correction :** chaque divergence de génération est documentée (option en cause, effet). La configuration standard est mise à jour avec les options recommandées. Référence pour les futurs binômes.

### Exercice E8 : Le ratio de tri à rebours

**Durée :** 60 minutes. **Prérequis :** trois campagnes de génération.

**Consigne :** reprenez les tests supprimés des trois campagnes. Pour chacun : la raison de la suppression était-elle prévisible à la génération (option de gabarit) ou inhérente au système (bruit inévitable) ? Classez.

**Ce que l'exercice révèle :** les suppressions prévisibles sont des corrections de gabarit à faire — le tri devient moins nécessaire à chaque itération. Si 80 % des suppressions sont prévisibles, vos gabarits produisent beaucoup de déchets : c'est un signal de reprise du gabarit. Si elles sont inhérentes, le tri est une étape normale du processus — pas un échec.

**Grille de correction :** les corrections de gabarit issues de l'exercice sont datées et testées sur la campagne suivante. L'indicateur de santé : le ratio de suppression doit baisser campagne après campagne — sinon les gabarits ne s'améliorent pas.

### Exercice E9 : Le modèle face au nouveau

**Durée :** 45 minutes. **Prérequis :** un nouveau dans l'équipe (même externe).

**Consigne :** le nouveau décrit votre processus de release à partir du modèle seul, en trois phrases. Comparez avec le réel. Chaque écart est un défaut du modèle (ou du processus).

**Ce que l'exercice révèle :** les trous du modèle que les habitués ne voient plus. Les habitués ont le contexte oral ; le nouveau n'a que le modèle. Ce que le nouveau ne comprend pas est ce que le modèle ne dit pas.

**Grille de correction :** chaque écart devient une mise à jour du modèle (ou une entrée au glossaire du modèle). Le test de qualité d'un modèle : un nouveau peut le décrire sans poser de question — sinon, il n'est pas autonome.

### Exercice E10 : La documentation au test du support

**Durée :** 45 minutes. **Prérequis :** trois pages de documentation vivante, une question réelle du support.

**Consigne :** donnez au support une question réelle et les pages de documentation. Peut-il répondre sans revenir vers l'équipe ? Chaque retour vers l'équipe est un défaut de documentation — trou, jargon, mauvais niveau de détail.

**Ce que l'exercice révèle :** le niveau réel de la documentation. Une documentation que le support ne peut pas utiliser n'est pas vivante — elle est interne aux développeurs qui savent déjà.

**Grille de correction :** chaque retour vers l'équipe devient une amélioration de page (et souvent une entrée de glossaire). Le test à refaire chaque mois : la documentation qui survit à trois questions du support sans retour est vivante.

### Exercice E11 : Le stress-test du plan lié

**Durée :** 60 minutes. **Prérequis :** le plan du trimestre, avec ses références de modèles.

**Consigne :** vérifiez chaque référence du plan : le modèle existe-t-il ? Sa dernière confrontation date-t-elle de moins d'un mois ? La spécification dérivée est-elle à jour ? Chaque référence cassée est un élément de plan décoré — pas planifié.

**Ce que l'exercice révèle :** l'écart entre le plan décoré (qui affiche des références) et le plan lié (dont les références sont vivantes). Les éléments décorés sont les zones où le niveau 1 s'est arrêté : ils doivent être retraités ou déclassés honnêtement.

**Grille de correction :** les éléments avec références cassées sont déclassés ou reliés (avec dates). Le test à refaire chaque semaine de planification : le plan lié est un plan qui se vérifie, pas un plan qui s'affiche.

### Exercice E12 : L'audit des cérémonies N2

**Durée :** 90 minutes. **Prérequis :** les cérémonies N2 installées (Partie 10).

**Consigne :** chaque cérémonie est évaluée sur les six questions (3 du niveau 1 + 3 du niveau 2 : reliée aux modèles, preuves automatisées, livrables enrichissant les modèles). Chaque échec a sa correction.

**Ce que l'exercice révèle :** le niveau réel de maturité. Les cérémonies qui échouent à la question 4 (reliée aux modèles) sont encore au niveau 1 avec des outils posés à côté. Les cérémonies qui réussissent les six questions sont prêtes pour le niveau 3.

**Grille de correction :** le tableau d'audit est publié et relu chaque mois. Une cérémonie qui régresse (réussissait la question 5, échoue maintenant) est un signal d'alarme plus fort qu'une cérémonie qui n'a jamais réussi : elle indique une dérive du système.

## 2. FAQ du niveau 2

**Q : Combien de modèles faut-il au minimum ?**
R : Un. Le premier modèle (le processus le plus coûteux en malentendus) est l'investissement le plus rentable. Deux valent mieux qu'un, cinq valent mieux que deux — mais un modèle vivant bat zéro modèle et dix modèles décoratifs. La question n'est jamais « combien » mais « lesquels » : là où le malentendu coûte.

**Q : BPMN ou un autre format ?**
R : Le format importe moins que la confrontation. BPMN est le standard le plus répandu, lisible par les métiers ; mais un diagramme de séquence, un flowchart ou même des boîtes et flèches sur un tableau blanc fonctionnent si la confrontation se fait. Le test : deux rôles différents peuvent-ils le lire sans formation de deux heures ? Le BPMN passe ce test pour la plupart des équipes ; le formalisme de votre choix peut le passer aussi.

**Q : L'IA peut-elle générer le modèle ?**
R : L'IA peut proposer un premier jet de modèle à partir d'une description — utile comme point de départ. Mais le modèle qui sera confronté doit être écrit par ceux qui vivent le processus : c'est la confrontation qui crée le modèle, et elle ne peut pas être déléguée. L'IA assistant du niveau 2 : oui, pour les premiers jets, les reformulations, les vérifications de cohérence. L'IA auteure du modèle : non — le modèle est l'accord des gens qui vivent le processus, pas une synthèse optimisée.

**Q : Nos modèles divergent du code en deux semaines. À quoi bon ?**
R : La divergence n'est pas un échec du modèle : c'est sa fonction. Une divergence détectée est une information (le modèle est périmé OU le code a dévié OU le réel a changé). Le niveau 2 transforme la divergence en routine : chaque détection est traitée dans la semaine. L'alternative (ne pas modéliser pour ne pas diverger) revient à ne pas se peser pour ne pas grossir : l'information disparaît, pas le problème.

**Q : Comment justifier le temps de modélisation devant l'équipe ?**
R : Par la confrontation, pas par la théorie. La première confrontation qui trouve une divergence réelle (« attends, toi tu testes après ? ») vaut tous les arguments. Et le cas Genius (Partie 11) : le modèle d'onboarding qui a fait passer la montée en compétence de six semaines à deux — la justification la plus concrète pour une équipe qui forme.

**Q : Peut-on modéliser un projet en démarrage ?**
R : C'est le meilleur moment : le modèle se construit en même temps que le système, et chaque décision d'architecture se prend sur le modèle (visible, discutable) plutôt que dans le code (invisible jusqu'à l'implémentation). Le modèle d'un projet neuf est un outil de design ; le modèle d'un projet existant est un outil de découverte. Les deux sont valides.

**Q : Le niveau 2 remplace-t-il les rituels du niveau 1 ?**
R : Non — il les outille. L'élicitation reste une conversation (avec un modèle en support), la spécification reste une rédaction humaine (dérivée du modèle), le Go/No-Go reste une décision (avec plus de preuves automatisées). Si une cérémonie du niveau 2 a éliminé la conversation humaine de sa correspondante du niveau 1, elle a dérivé : corrigez-la.

## 3. Les anti-patterns du niveau 2

### Anti-pattern 1 : Le modèle musée

**Symptôme :** les modèles sont beaux, encadrés, à jour — et jamais confrontés. Ils décrivent avec précision un processus que personne ne discute.

**Pourquoi ça arrive :** la modélisation a été traitée comme un livrable (à produire) et non comme un instrument (pour révéler). L'auto-complaisance du document propre tue la confrontation.

**Le remède :** la règle du mouvement : un modèle qui n'a pas produit de divergence en trois confrontations est suspect (soit le processus est parfait — rare ; soit les confrontations ne sont pas réelles). La métrique inversée : chercher les divergences est le but ; ne pas en trouver est l'alarme.

### Anti-pattern 2 : Le modèle majestueux

**Symptôme :** le modèle couvre tout le processus de l'entreprise, en 40 pages, avec tous les détails. Il est complet — et personne ne le lit sans guide.

**Pourquoi ça arrive :** la modélisation exhaustive semble rigoureuse. Elle est en fait une reconstruction de la complexité, sans le bénéfice de la simplicité qui rend discutable.

**Le remède :** le modèle du niveau 2 se choisit (les 3-5 processus les plus coûteux en malentendus) et se limite (une page par processus). La compléxité résiduelle reste dans le code et le réel — le modèle en capture ce qui doit être discuté, pas ce qui doit être catalogué.

### Anti-pattern 3 : La génération sans tri

**Symptôme :** les tests générés s'accumulent dans le pipeline : des centaines de tests verts, un pipeline de 45 minutes, et personne ne sait ce que chaque test vérifie.

**Pourquoi ça arrive :** la génération a été adoptée pour son volume (« plus de tests = mieux »). Le tri (la sélection critique) a été sauté comme une tâche optionnelle.

**Le remède :** la règle du tri obligatoire : chaque campagne passe par les critères de tri écrits, avec le rapport trié (produits / gardés / supprimés, avec justifications). Le tri est ce qui transforme le volume en couverture utile. Un pipeline sans tri est un pipeline qui ralentit sans protéger.

### Anti-pattern 4 : La documentation générée orpheline

**Symptôme :** la documentation est générée du modèle, à jour — mais personne ne la lit (compteurs de consultation à zéro).

**Pourquoi ça arrive :** la documentation a été écrite pour le modèle, pas pour un lecteur. Elle répond à « qu'est-ce que le système fait ? » — personne ne pose cette question. Les vraies questions (« comment je fais X ? », « pourquoi ça échoue quand Y ? ») ne sont pas couvertes.

**Le remède :** orienter la documentation par les questions réelles (exercice E10 : le test du support). La documentation vivante commence par les questions que les gens posent — dérivée du modèle, oui, mais organisée par l'usage. Une page non lue depuis trois mois est coupée : la documentation se taille, elle ne s'accumule.

### Anti-pattern 5 : Le Go/No-Go audit de conformité

**Symptôme :** le Go/No-Go dure deux heures : on relit les modèles, les rapports de génération, les documentations. La décision devient une inspection.

**Pourquoi ça arrive :** l'enrichissement des critères N2 a été pris pour un allongement du rituel. Les preuves N2 sont automatisées — si elles sont collectées manuellement en séance, l'outillage est défaillant.

**Le remède :** les preuves N2 sont préparées avant (rapports liés, dates vérifiables) ; la séance porte sur les décisions. Si la collecte dépasse 5 minutes, corrigez l'automatisation — pas le format. Le Go/No-Go du niveau 2 dure toujours 30 minutes : c'est ce qui prouve que l'outillage fonctionne.

### Anti-pattern 6 : La confirmation qui ne modifie jamais le modèle

**Symptôme :** les confirmations ont lieu, les retours sont notés — et le modèle n'a jamais bougé après une confirmation.

**Pourquoi ça arrive :** la confirmation est traitée comme une validation de fin (le modèle était bon, la confirmation le prouve) au lieu d'un apprentissage (les usages imprévus révèlent les chemins absents).

**Le remède :** la règle de l'enrichissement : chaque confirmation qui n'a rien ajouté au modèle est suspecte (les usages imprévus existent toujours). La grande boucle du niveau 2 passe par le modèle : CONFIRMER → MODÈLE → ÉLICITER. Une confirmation sans enrichissement est une confirmation morte.

## 4. Le plan de formation du niveau 2

### Le parcours du nouveau au niveau 2 (30 jours, au-dessus du niveau 1)

**Semaine 1 : le premier modèle.** Le nouveau lit le modèle du domaine principal, le décrit en trois phrases (exercice E9), et note chaque confusion. Ses confusions sont les premiers trous du modèle à corriger — avec lui.

**Semaine 2 : sa première confrontation.** Il participe à une confrontation du modèle (observe, puis participe). Son regard neuf est l'atout : les habitués ne voient plus certaines divergences.

**Semaine 3 : sa première spécification dérivée.** Il écrit une spécification à partir du modèle (avec binôme), découvrant que la structure du modèle structure la spécification — les passerelles deviennent les cas.

**Semaine 4 : sa première génération critiquée.** Il génère les tests du modèle (ou assiste à la génération), les trie selon les critères, et écrit son rapport de tri. Il découvre le ratio réel — la leçon d'honnêteté fondamentale du niveau 2.

### Le plan de formation de l'équipe voisine

Quand une équipe voisine demande le niveau 2, le parcours est plus long — et plus important. Le format recommandé :

1. **La démonstration** (1 heure) : le premier modèle, une confrontation rejouée, une divergence réelle trouvée. Pas de slides.
2. **Le premier modèle de l'équipe voisine** (2 semaines) : elles modélisent leur processus le plus coûteux, avec un binôme de votre équipe en observateur. Leur modèle, leur confrontation, leurs divergences.
3. **La première spécification dérivée** (1 semaine) : leur première spécification issue de leur modèle, relue par votre binôme (c'est un service mutuel : vous voyez comment la méthode s'adapte).
4. **Le point de bascule** : leur première confrontation qui trouve une divergence qu'ils ne connaissaient pas. À partir de là, ils n'ont plus besoin de vous — la méthode est auto-portante.

**La règle de transmission du niveau 2 :** on ne transmet pas le modèle (il appartient à ceux qui vivent le processus) ; on transmet la méthode de confrontation — c'est elle qui crée les modèles. Une équipe qui a appris à confronter peut modéliser n'importe quel processus ; une équipe qui a reçu des modèles dépend pour toujours.

## 5. Le calendrier de lecture annuel du niveau 2

| Période | Relecture | Pourquoi |
|---|---|---|
| Semaines 1-8 | Les parties dans l'ordre | Préparer les ateliers |
| Mois 3 | Les capsules N2 (Partie 6) + les gabarits remplis (Partie 7) | Raviver le format vivant |
| Mois 4 | Les approfondissements techniques (Partie 8) | La granularité, le MBT, le versioning |
| Mois 5 | Les situations difficiles (Partie 9) | Le moment des vraies difficultés |
| Mois 6 | L'audit des cérémonies (E12) + les 6 questions du test | Le point de contrôle semestriel |
| Mois 7-9 | Une capsule par semaine en rotation | L'entretien par répétition espacée |
| Mois 10-12 | Le vécu étendu (Partie 11) + préparation de la transmission | Devenir la référence de l'équipe voisine |

Le calendrier du niveau 2 ajoute une dimension à celui du niveau 1 : **le lecteur devient porteur de méthode** pour l'équipe voisine. Les mois 10-12 le préparent à transmettre — et la transmission est le test ultime du niveau 2 : une méthode qui ne se transmet pas est une méthode qui meurt avec son coach.
