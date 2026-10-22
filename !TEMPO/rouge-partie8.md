
---

# Partie 8 : Exercices avancés, FAQ et anti-patterns du niveau 1

## 1. Exercices d'entraînement supplémentaires (E7 à E12)

### Exercice E7 : La spécification à trois relecteurs

**Durée :** 90 minutes. **Prérequis :** une spécification récente, trois relecteurs de rôles différents.

**Consigne :** donnez la spécification à trois relecteurs (développeur, testeur, demandeur) séparément. Chacun écrit : ce qu'il comprend qu'il doit faire/livrer/vérifier. Confrontez les trois lectures à froid.

**Ce que l'exercice révèle :** le niveau réel d'ambiguïté. Là où les trois lectures divergent, la spécification a un trou — et ce trou est exactement là où le malentendu se transformera en reprise. Trois lectures divergentes = trois bugs en attente.

**Grille de correction :** chaque divergence trouvée est classée — ambiguity de comportement (le plus grave), de priorité, de vocabulaire. Les ambiguïtés de comportement sont corrigées le jour même ; les autres rejoignent le lexique. Spécification réussie : divergences ≤ 1.

### Exercice E8 : Le chiffrage du flou

**Durée :** 60 minutes, en équipe. **Prérequis :** les reprises des trois derniers mois.

**Consigne :** pour chaque reprise récente, déterminez sa cause racine : spécification absente, spécification floue, changement de demande légitime, erreur technique pure. Calculez le coût de chaque catégorie (heures perdues × taux horaire ou simplement jours-homme).

**Ce que l'exercice révèle :** la proportion du flou dans le coût réel. Les équipes découvrent typiquement que 40 à 60 % de leurs reprises proviennent de spécifications absentes ou floues — c'est-à-dire de la partie que le niveau 1 corrige. Ce chiffre est votre meilleur argument pour continuer.

**Grille de correction :** le tableau de causes est publié au centre d'excellence avec son coût total. La catégorie « spécification absente/floue » devient la cible chiffrée du trimestre : réduire de X à Y.

### Exercice E9 : Le lexique à l'épreuve des nouveaux

**Durée :** 45 minutes. **Prérequis :** le lexique officiel, un volontaire ignorant du domaine.

**Consigne :** donnez le lexique à quelqu'un qui ne connaît pas votre produit. Il relit chaque définition et pose les questions que la définition n'empêche pas : « "Livraison" — vous voulez dire mise en production ou mise à disposition ? » Chaque question est un défaut de définition.

**Ce que l'exercice révèle :** les définitions écrites par les initiés sont toujours partielles — elles oublient les distinctions évidentes pour elles. Le regard neuf est le révélateur le moins cher du lexique.

**Grille de correction :** chaque question notée devient une amélioration de définition le jour même. Un lexique qui survit à un regard neuf sans une seule question est suspect : soit il est parfait (rare), soit le lecteur n'a pas assez cherché.

### Exercice E10 : Le Go/No-Go en aveugle

**Durée :** 45 minutes. **Prérequis :** les preuves d'une livraison récente, masquées (le décideur ne voit que les conclusions, pas les données).

**Consigne :** présentez au décideur seulement les conclusions de chaque critère (« les tests passent », « la doc est à jour ») sans les preuves. S'il a un doute sur un critère, il demande la preuve. Comptez les demandes : chacune est un critère dont la présentation doit être plus factuelle.

**Ce que l'exercice révèle :** la différence entre affirmer et prouver. Un Go/No-Go où le décideur doit faire confiance sans données n'est pas un rituel de décision : c'est une cérémonie de légitimation. Les demandes de preuve sont les endroits où la confiance remplace la vérification.

**Grille de correction :** chaque demande de preuve est transformée en exigence de présentation : le critère sera présenté avec sa donnée, pas avec sa conclusion. Après deux itérations, le nombre de demandes tend vers zéro — le format de preuve est appris.

### Exercice E11 : La confirmation inversée

**Durée :** 60 minutes. **Prérequis :** une livraison récente, les utilisateurs réels accessibles.

**Consigne :** au lieu de demander « êtes-vous satisfaits ? » (question qui produit des politesses), demandez : « montrez-moi comment vous l'utilisez vraiment ». Observez. Notez chaque usage imprévu, chaque contournement, chaque frustration non verbalisée.

**Ce que l'exercice révèle :** l'écart entre ce qui a été spécifié et ce qui est utilisé. Les contournements observés sont des besoins non élicités — les meilleurs indices pour la prochaine élicitation. C'est la grande boucle en mode observation.

**Grille de correction :** chaque usage imprévu noté devient une question pour la cérémonie d'élicitation suivante. Trois usages imprévu documentés = trois élicitations futures améliorées.

### Exercice E12 : L'audit des cérémonies

**Durée :** 90 minutes, en fin de parcours. **Prérequis :** les cérémonies installées (Partie 6).

**Consigne :** pour chaque cérémonie installée, répondez aux trois questions du test : a-t-elle des entrées obligatoires ? un livrable daté ? tient-elle sans le facilitateur ? Pour chaque échec, écrivez la correction et son propriétaire.

**Ce que l'exercice révèle :** l'état réel des rituels. Les cérémonies qui échouent à la question 3 (sans facilitateur) sont les plus importantes à corriger : ce sont celles qui disparaîtront au départ du coach.

**Grille de correction :** le tableau d'audit est publié : cérémonie / entrées / livrable / sans facilitateur. Chaque « non » a une action datée. Les cérémonies qui échouent à deux questions sur trois sont candidates à la refonte complète — pas au rafistolage.

## 2. FAQ du niveau 1

**Q : Combien de temps avant de voir des résultats mesurables ?**
R : Les premiers signes apparaissent en deux semaines (les reprises baissent dès que les spécifications précèdent le code). Les résultats mesurables et défendables arrivent au bout de huit semaines — le tableau de mouvement de la semaine 8. Au-delà de trois mois sans signe mesurable, vérifiez que les rituels tiennent sans le coach : le problème est presque toujours là, pas dans la méthode.

**Q : On n'a pas de QA dédié. Peut-on quand même faire le niveau 1 ?**
R : Oui — le niveau 1 exige des rôles, pas des titres. Le testeur peut être un développeur qui porte le chapeau, le demandeur peut être le product owner. Ce qui n'est pas négociable : les trois rôles existent dans les rituels (spécification revue par trois lectures, Go/No-Go avec un décideur réel). Voir le cas Sherweb (Partie 7) : la qualité déléguée disparaît avec les gardiens ; la qualité distribuée survit à tout.

**Q : Le développeur senior refuse d'écrire des spécifications (« je code mieux que je n'écris »).**
R : Ne le convainquez pas — mesurez. Demandez-lui de compter ses propres reprises des trois derniers mois et leur cause (exercice E8). Puis demandez-lui de spécifier une seule demande avant de coder, et de compter les questions qu'on lui pose pendant l'implémentation. Les données font le travail que l'argument ne fait pas. Et acceptez sa forme : un senior peut écrire ses spécifications sous la forme qu'il préfère (tableau, pseudo-code, liste) tant que les critères de validation y sont.

**Q : Le client change d'avis en milieu d'itération. La spécification ne sert-elle pas à rien ?**
R : La spécification sert précisément à ça : rendre le changement *visible et chiffrable*. Sans spécification, un changement d'avis est invisible — il se paie en reprises surprises. Avec, il se paie en décision explicite : la spec est modifiée, le contrat d'itération est ajusté, le Go/No-Go jugera la nouvelle version. Le niveau 1 ne rend pas les changements impossibles ; il les rend honnêtes.

**Q : Faut-il un outil pour les rituels ?**
R : Non — le niveau 1 fonctionne avec du texte, des tableaux et de la discipline. L'outil arrive au niveau 2, quand les rituels tiennent et qu'il faut les scaler. Un rituel qui ne tient qu'avec son outil ne tient pas : il est délégué à l'outil.

**Q : Comment défendre ce temps devant la direction ?**
R : Par le coût du flou, chiffré (exercice E8). Les équipes typiques découvrent que 40 à 60 % de leurs reprises proviennent de spécifications absentes — un coût direct, mesurable, imputable. Le niveau 1 attaque exactement cette part. La question à retourner n'est pas « comment nous payer ce temps ? » mais « combien vous coûte le flou aujourd'hui ? ».

**Q : À quel moment passe-t-on au niveau 2 ?**
R : Quand les cérémonies du niveau 1 passent le test des trois questions (Partie 6) : entrées obligatoires, livrable daté, tenue sans le facilitateur. Une cérémonie qui ne tient pas seule sera modélisée en vain au niveau 2 : le modèle mourra avec le rituel. Le test de maturité est l'audit E12, pas le calendrier.

## 3. Les anti-patterns du niveau 1

### Anti-pattern 1 : La spécification théâtrale

**Le symptôme :** les spécifications existent, sont rédigées après coup (le code est déjà écrit), et servent à documenter ce qui a été fait plutôt qu'à décider ce qui sera fait.

**Pourquoi ça arrive :** l'exigence « il faut des spécifications » arrive sans la pratique « la spécification précède le code ». L'équipe produit le document pour l'auditoire, après le fait.

**Le remède :** la règle du flux inversé : une demande ne passe en développement que si sa spécification existe et est datée avant le premier commit. Vérifiable en une minute sur n'importe quel historique Git : date de la spécification vs date du premier commit. Si la règle ne tient pas, la spécification théâtrale est confirmée — et c'est le flux qu'il faut corriger, pas les documents.

### Anti-pattern 2 : Le Go/No-Go toujours vert

**Le symptôme :** tous les Go/No-Go se terminent par un Go. Personne ne se souvient du dernier No-Go.

**Pourquoi ça arrive :** soit les critères sont trop laxistes (la grille ne filtre rien), soit la décision est prise avant la cérémonie (en couloir), soit le décideur n'a pas le pouvoir réel de dire non.

**Le remède :** l'exercice E10 (l'aveugle) révèle si les conclusions sont vérifiées ou affirmées. Et le test de la grille : si aucun critère n'a jamais été rouge, les seuils sont décoratifs — ils doivent être resserrés jusqu'à ce que la grille ait du pouvoir. Un Go/No-Go qui ne dit jamais non est une réunion de plus.

### Anti-pattern 3 : Le lexique musée

**Le symptôme :** le lexique a été écrit en semaine 1, publié, et n'a plus changé depuis. Les malentendus continuent, mais personne ne les documente plus.

**Pourquoi ça arrive :** le lexique a été traité comme un livrable (à produire) au lieu d'un registre (à tenir). La production a un moment de fin ; le registre n'en a pas.

**Le remède :** la règle du registre vivant : chaque malentendu constaté dans la semaine produit une entrée (ou une correction) au lexique. L'exercice E9 (le regard neuf) révèle les définitions mortes. Et la métrique saine : le lexique qui ne bouge plus est le signal d'alarme, pas la preuve de stabilité.

### Anti-pattern 4 : La confirmation qui ne confirme rien

**Le symptôme :** la cérémonie de Confirmation a lieu, tout le monde est « content », et aucune information n'en sort.

**Pourquoi ça arrive :** la question posée est « êtes-vous satisfaits ? » — qui produit des politesses. La confirmation TOTALISATION confronte les critères de succès élicités au réel observé : c'est une collecte de données, pas une enquête de satisfaction.

**Le remède :** relire les critères de succès de la cérémonie d'Élicitation avant chaque confirmation, et demander chacun explicitement : « le critère était X, est-il rempli, comment le savez-vous ? ». Et pratiquer la confirmation inversée (E11) : observer l'usage réel plutôt que demander l'opinion.

### Anti-pattern 5 : Le coach qui ne part jamais

**Le symptôme :** huit semaines sont passées, l'équipe fonctionne — et le coach est toujours là, « pour la transition ». Six mois plus tard, il est toujours là.

**Pourquoi ça arrive :** le coach est devenu le garant de la qualité. Son départ semble le retirer — alors que son maintien empêche l'équipe de devenir son propre garant.

**Le remède :** la règle du mandat daté : le coach rend son mandat à la semaine 8 (le rapport de maturité le formalise). S'il reste, c'est pour un nouveau mandat distinct (par exemple former l'équipe voisine) — jamais pour « s'assurer que ça tient ». La qualité qui a besoin d'un garant permanent n'est pas acquise.

### Anti-pattern 6 : Le sponsor qui délègue son engagement

**Le symptôme :** le sponsor a signé la charte en semaine 1 et n'a plus reparlé à l'équipe. Les demandes de la semaine 5 restent sans réponse.

**Pourquoi ça arrive :** l'engagement du sponsor a été traité comme un événement (la signature) au lieu d'un régime (la disponibilité). Un sponsor qui ne répond pas n'est pas occupé : il est absent.

**Le remède :** le contrat de disponibilité : le sponsor s'engage à répondre aux demandes écrites sous cinq jours ouvrables (voir BLEU, cas du sponsor qui ne vient plus). La présence continue n'est pas nécessaire ; la réponse garantie l'est. Un sponsor qui ne peut pas s'engager à répondre doit le savoir : il n'est pas un sponsor, il est une signature.

## 4. Le test final du niveau 1

Avant de passer au niveau 2, l'équipe répond par écrit à ces cinq questions, publiées au centre d'excellence :

1. **Quel pourcentage de nos demandes sont aujourd'hui spécifiées avant le code ?** (Un chiffre. En dessous de 80 %, le flux inversé n'est pas acquis.)
2. **Quand a eu lieu notre dernier No-Go, et que s'est-il passé ensuite ?** (Un No-Go qui n'a jamais eu lieu ou qui n'a rien changé sont deux alarmes.)
3. **Combien d'entrées notre lexique a-t-il gagnées depuis la semaine 1 ?** (Zéro = lexique musée.)
4. **Quel est notre délai de confirmation après livraison, et que nous a-t-il appris ?** (La confirmation qui n'apprend rien n'existe pas.)
5. **Qui, dans l'équipe, défendrait la spécification avant le code si le coach disparaissait demain ?** (Si personne ne se lève, le niveau 1 n'est pas terminé — il est abandonné en douceur.)

Ces cinq réponses sont le passeport du niveau 2 : ce que l'équipe revendique, le niveau suivant le demandera en preuve.
