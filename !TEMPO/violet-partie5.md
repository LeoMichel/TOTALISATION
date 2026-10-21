
---

# Partie 5 : Cas réels, gabarits remplis et variantes contextuelles (niveau 7)

Les gabarits remplis, les situations vécues, et l'adaptation du niveau 7 (philosophie, culture, transmission) aux contextes réels. Le niveau 7 est le plus difficile à illustrer par des gabarits : ses preuves sont des récits, ses artefacts sont des comportements. Les gabarits ci-dessous montrent comment documenter l'invisible.

## 1. Les gabarits remplis d'exemples réels

### 1.1 La vision commune — exemple rempli

> La vision d'une organisation réelle au niveau 7, avec ses reformulations par métier. La vision tient en une phrase ; les reformulations en font un outil.

**La vision (une phrase) : « Nous construisons des produits que nous serions fiers d'administrer nous-mêmes, dix ans plus tard. »**

**Les reformulations par métier (validées en atelier 8.3) :**

| Fonction | Reformulation | Observable |
|---|---|---|
| Développement | « J'écris le code que je voudrais trouver en reprenant ce produit dans 10 ans, pas celui qui passe le sprint » | Le code des fonctionnalités critiques relisible sans explication de son auteur |
| QA | « Je teste ce qui cassera dans 10 ans, pas seulement ce qui casse aujourd'hui » | Les cas limites de vieillissement (données accumulées, volume, évolution) dans chaque plan de test |
| Support | « Je documente ce que je voudrais lire quand j'aurai oublié ce que je sais » | Les pages de support relues et complétées sans demande |
| Vente | « Je promets ce que le produit sera, pas ce qu'il pourrait être » | Aucune promesse sans fonctionnalité livrée ou engagement daté |
| Direction | « Je choisis la décision que nous n'aurons pas à défaire » | Chaque décision majeure documentée avec l'option non retenue et pourquoi |

**Ce qui fait la qualité de cette vision :** elle est testable dans chaque métier, et elle est contraignante (elle défend des choix coûteux). Une vision qui ne coûte rien n'est pas une vision : c'une devise.

### 1.2 La jurisprudence des dilemmes — exemple rempli

> Trois entrées réelles de la jurisprudence. C'est le document le plus précieux du niveau 7 : la mémoire des dilemmes résolus.

**Jurisprudence — dilemmes de valeurs (version 4, mise à jour trimestrielle)**

**Dilemma #1 (2024-03) : La fonctionnalité rentable qui n'aurait pas de propriétaire**

Les valeurs en tension : *fierté du produit* vs *santé financière*. Un client important a demandé une fonctionnalité d'export personnalisé. Le travail était rentable (facturable immédiatement). Mais aucune équipe ne voulait la maintenir : le client voulait sa version, non réutilisable.

**La décision :** refuser la version personnalisée, proposer une version paramétrable standard (3 mois de plus, non facturée). Le client a accepté après discussion ; la version standard sert aujourd'hui à 4 clients.

**La rationale :** « dix ans plus tard » — un export personnalisé non maintenu serait une dette pour l'équipe qui héritera. Le coût de la décision a été réel (3 mois sans facturation) ; le retour a été 4 clients sur un investissement au lieu de 1.

**Dilemma #2 (2024-09) : La transparence sur un retard embarrassant**

Les valeurs en tension : *transparence* vs *confiance des parties prenantes*. Un retard de 6 semaines sur une livraison importante. La tentation : communiquer « un ajustement de calendrier » au lieu du vrai motif (une refonte de la sécurité, décidée tardivement, prioritaire).

**La décision :** transparence complète — le motif, le pourquoi du retard, la date révisée. Deux clients ont réagi négativement au motif (sécurité = problème ?). La réponse : présenter la refonte comme ce qu'elle était (une anticipation d'une exigence à venir), avec le bénéfice pour le client.

**La rationale :** « nous n'aurons pas à défaire » — une demi-vérité se défera inévitablement. Le coût a été une conversation inconfortable ; le retour, une crédibilité intacte quand un deuxième retard (justifié différemment) a été annoncé six mois plus tard.

**Dilemma #3 (2025-01) : Le départ d'une personne clé incompatible avec la culture**

Les valeurs en tension : *respect des personnes* vs *respect du produit*. Une personne brillante, critique pour une livraison, mais dont les pratiques (déployer en contournant les tests, mépriser la revue) sont contraires à la philosophie. La livraison était dans 3 semaines.

**La décision :** un dialogue direct d'abord (la personne a ajusté, partiellement), puis l'organisation a accepté le scénario le plus coûteux : la personne est partie pendant la préparation de la livraison. La livraison a pris 2 semaines de plus.

**La rationale :** « fiers d'administrer nous-mêmes » — une équipe qui voit les contournements récompensés apprend que la philosophie est décorative. Le coût a été 2 semaines ; le retour, une équipe qui croit que les règles sont réelles.

**Ce qui fait la qualité de cette jurisprudence :** les coûts assumés et chiffrés. Une jurisprudence qui ne raconte que des décisions gratuites est une publicité, pas une mémoire.

### 1.3 La carte des récits fondateurs — exemple rempli

> Le plan des récits que les nouveaux entendront, avec leurs moments. Le parcours de transmission (atelier 8.3) s'appuie sur cette carte.

**Les récits que chaque nouveau devrait entendre (dans les 3 premiers mois) :**

| Récit | Raconté par | Moment | Ce qu'il enseigne |
|---|---|---|---|
| « Le bug que personne ne voulait croire » | Le fondateur | Le premier mois, pendant une session d'équipe | Les signaux sont réels même quand ils sont dérangeants ; le premier bug ignoré a fondé la philosophie |
| « L'incident à 400 000 $ que nous avions documenté » | Le responsable qualité | Après le premier trimestre | Le savoir sans l'action est une négligence documentée ; l'humilité organisationnelle |
| « Le départ de [prénom] pendant la livraison » | Un membre de l'équipe d'alors | Quand le nouveau demande « pourquoi tant de process ? » | Les règles sont réelles, même quand elles coûtent |
| « La fois où nous avons dit non au plus gros client » | La direction | Après le premier trimestre | La vision guide les décisions commerciales, pas seulement techniques |
| « L'échec de la première tentative de transformation » | Un ancien de l'équipe pilote | À la demande du nouveau, ou après le premier échec vécu | L'échec fait partie du chemin ; ce qui a survécu vaut la peine |

**La règle du récit :** chaque récit contient son échec ou son coût. Un récit sans coût n'est pas un récit fondateur, c'est un pamphlet.

## 2. Cas vécus étendus : le niveau 7

### Cas de la semaine 2 : le dilemme que la jurisprudence a failli manquer

**Situation.** L'atelier du dilemme (module F2) a présenté un cas réel : un développeur senior avait contourné la revue « juste cette fois » pour respecter une échéance client, et son correctif a causé un incident mineur. La question : que fait-on — la philosophie (les règles sont réelles) ou le contexte (l'échéance était réelle) ?

**La découverte.** En discussion, la moitié de la salle a proposé de « rappeler les règles », l'autre moitié de « comprendre la pression ». Le débat a tourné en rond jusqu'à ce qu'une personne demande : « Est-ce que ce cas est déjà dans la jurisprudence ? » Il n'y était pas — et il ressemblait au dilemme #3 (le départ pendant la livraison), sauf sur un point : ici, la personne avait reconnu son erreur et l'incident était mineur.

**La décision.** Le cas a été traité par analogie au dilemme #3, avec la différence documentée : dialogue direct, pas de sanction, mais le cas est ajouté à la jurisprudence comme variante « erreur reconnue ». La jurisprudence a gagné sa première entrée « gradation » : toutes les violations ne méritent pas la même réponse.

**Ce que ce cas enseigne.**
- La jurisprudence n'est pas un code pénal : c'est une mémoire d'analogies. Le premier réflexe face à un nouveau dilemme est « est-ce que nous avons déjà vu quelque chose de semblable ? ».
- Les gradations existent et doivent être documentées : l'erreur reconnue, la répétition, le mépris assumé ne sont pas la même chose. Une jurisprudence sans gradation produit soit des réponses uniformément dures, soit des excuses systématiques.
- L'atelier du dilemme alimente la jurisprudence à chaque session : c'est son mécanisme de croissance. Une jurisprudence qui ne s'enrichit pas est un musée.

### Cas de la semaine 3 : la mission impossible qui a révélé le vrai problème

**Situation.** L'exercice des missions personnelles (module F3) a produit 24 missions, dont 7 marquées « impossibles » par leurs auteurs. La direction a dû répondre à chacune. Six ont été résolues (moyens, permissions). La septième était dérangeante : « Je ne peux pas faire ma mission tant que l'évaluation annuelle de mon équipe récompense le contraire. »

**La découverte.** La mission impossible n'était pas une demande de moyen : c'était une contradiction structurelle. L'organisation demandait la philosophie dans les missions et récompensait le contraire dans les évaluations. Toutes les autres missions impossibles étaient des symptômes de celle-ci.

**La décision.** La direction a révisé les critères d'évaluation annuelle pour inclure les observables des missions personnelles (2 critères sur 8). La révision a pris un trimestre et une négociation RH — et elle a été la décision la plus importante du niveau 7 de cette organisation.

**Ce que ce cas enseigne.**
- Les missions impossibles ne sont pas des plaintes : elles sont le diagnostic le plus honnête de l'écart entre la philosophie affichée et l'organisation réelle.
- La contradiction structurelle (les systèmes de l'organisation qui récompensent le contraire de la philosophie) est le vrai adversaire du niveau 7. Les affiches et les ateliers ne la corrigent pas : seuls les changements de système le font.
- La réponse de la direction aux missions impossibles est le test de sérieux du niveau 7 : des réponses écrites et datées (même « non, parce que ») valent mieux que l'absence de réponse.

### Cas de la semaine 5 : le test du volontaire qui a fait mieux que les experts

**Situation.** Le parcours de l'héritier (module F5) a été testé par un volontaire : un développeur de 6 mois d'ancienneté. L'attendu : il découvrirait les récits et pourrait reformuler la vision. Le réel : sa reformulation de la vision a été retenue comme meilleure que les versions précédentes.

**Sa reformulation :** « On construit pour le type qui aura notre boulot dans 10 ans, sauf qu'on ne le connaît pas encore — alors on construit pour qu'il puisse nous maudire poliment. »

**Pourquoi sa version est meilleure :** elle dit la même chose, mais en langage d'équipe. Les versions précédentes étaient écrites par la direction (langage de direction). La sienne est le langage dans lequel les développeurs se parlent. Elle a été adoptée comme version « de l'équipe » de la vision, à côté de la version officielle.

**Ce que ce cas enseigne.**
- Le test du volontaire n'est pas une validation : c'est une co-création. Le nouveau voit ce que les anciens ne voient plus.
- La vision a besoin de ses versions par public — la version officielle (pour l'extérieur, la direction) et les versions vécues (pour chaque équipe). Une seule version officielle dans tous les contextes produit de la traduction forcée.
- L'héritier qui reformule mieux que les fondateurs est le signe que la transmission fonctionne : la philosophie devient de plus en plus vraie à mesure qu'elle passe par plus de gens.

### Cas de la semaine 7 : le départ des fondateurs (la vraie transmission)

**Situation.** Le fondateur de la culture (celui qui racontait « le bug que personne ne voulait croire ») a pris sa retraite 6 mois après le niveau 7. La transmission avait été préparée : les récits étaient racontés par 4 personnes différentes, la jurisprudence était tenue par le comité, les dilemmes se traitaient sans lui.

**Le test réel.** Trois mois après le départ, un dilemme nouveau est survenu (une demande client contraire à la vision). La décision a été prise en suivant la jurisprudence — et la rationale citée était celle du dilemme #1, écrite par le fondateur. La décision a été la même qu'il l'aurait prise, sans lui.

**Ce que ce cas enseigne.**
- La transmission réussie se mesure 6 mois après le départ, pas à la cérémonie. Le test : une décision nouvelle prise selon la philosophie, sans les fondateurs.
- Les artefacts écrits (jurisprudence, vision, récits multiples) sont ce qui survit. Les personnes sont irremplaçables ; leurs raisonnements, transmissibles.
- Le moment le plus important de la transmission n'est pas la cérémonie : c'est le premier dilemme post-départ. Préparez-le mentalement — il arrive toujours.

### Cas de la semaine 8 : la carte que le nouveau a écrite

**Situation.** À la cérémonie de clôture, chaque participant a écrit sa carte (une chose qu'il fera différemment, une chose à ne jamais abandonner). Un développeur de 8 mois d'ancienneté a écrit : « Je ferai différemment : je poserai les questions gênantes, parce que j'ai vu que ça se fait ici. À ne jamais abandonner : le droit de dire non à un client important. »

**La signification.** Cette carte résume le niveau 7 vu par un nouveau : ce qu'il a appris (les questions gênantes sont normales ici) et ce qu'il a observé (le non au client, dilemme #1). Il n'a pas vécu le dilemme — il l'a entendu, et cela a suffi à faire de lui un porteur.

**Ce que ce cas enseigne.**
- Les cartes de la cérémonie sont le baromètre le plus honnête de la culture : ce que les gens écrivent spontanément est ce qu'ils ont réellement intériorisé.
- Un nouveau qui cite un dilemme qu'il n'a pas vécu prouve la valeur des récits : la transmission par le récit fonctionne. C'est l'argument le plus fort pour l'investissement dans les récits fondateurs.
- Relire les cartes un an après (comme promis dans l'atelier 8.4) est le rituel d'évaluation le plus honnête : les cartes tenues sont la culture réelle ; les cartes oubliées sont le diagnostic de ce qui a dérivé.

## 3. Variantes contextuelles du niveau 7

### V1 : petite organisation (moins de 30 personnes)

- La jurisprudence peut être tenue à voix haute (les dilemmes se racontent en réunion d'équipe) avec une trace écrite minimale : dans une petite organisation, la mémoire orale fonctionne si les personnes restent. La trace écrite devient critique au moment du premier départ important.
- La vision tient en une phrase dans les deux sens : elle se reformule plus facilement dans une petite organisation (tout le monde se connaît), et se dérive plus facilement aussi (un seul décideur peut la faire dériver). Le garde-fou : la jurisprudence écrite.
- Les récits fondateurs sont portés par peu de personnes : le risque de mort du récit au départ est élevé. Multipliez les porteurs dès le début (chaque récit raconté par au moins 2 personnes).
- Les missions personnelles sont plus faciles : chacun peut les discuter directement avec la direction. Le risque : la direction qui répond oralement et oublie. Écrivez les réponses quand même.

### V2 : organisation distribuée

- La transmission des récits par visio fonctionne moins bien qu'en personne : prévoyez des enregistrements des récits fondateurs (avec l'accord des raconteurs), et des sessions en personne régulières pour les moments clés (la première semaine, le premier trimestre).
- La jurisprudence écrite est l'actif central de la distribution : elle remplace les conversations de couloir qui n'existent pas. Elle doit être plus riche que dans une organisation co-localisée.
- Les dilemmes se traitent par écrit d'abord (chaque partie écrit sa position), se discutent ensuite : le croisement écrit est plus honnête et plus durable.
- Le test des cartes (semaine 8) est encore plus révélateur à distance : ce que les gens écrivent spontanément en l'absence de toute pression sociale directe est ce qu'ils ont vraiment intériorisé.

### V3 : organisation en croissance rapide

**Contexte.** L'organisation grandit vite : 20 % de nouvelles têtes par an. La culture est mise à l'épreuve par le renouvellement.

- Le parcours de transmission est le mécanisme le plus critique : il doit être systématique (chaque nouveau, sans exception) et mesuré (combien de nouveaux ont complété le parcours par trimestre). Dans une organisation qui grandit, la culture se dilue par défaut : le parcours est ce qui la maintient.
- Les récits fondateurs doivent être enregistrés tôt : les fondateurs partent ou s'éloignent plus vite que prévu. Un récit non enregistré est un récit perdu.
- La jurisprudence grandit plus vite : chaque trimestre apporte ses dilemmes nouveaux (les dilemmes de la croissance : promettre pour croître, embaucher pour la pression, etc.). Prévoyez une revue trimestrielle de la jurisprudence.
- La reformulation de la vision par les nouveaux est un instrument de détection : si les nouveaux reformulent la vision différemment des anciens, la culture est en train de se déplacer. Ce n'est pas toujours mauvais — mais c'est toujours un événement à nommer.

### V4 : organisation avec une culture forte préexistante

**Contexte.** L'organisation avait déjà une culture (souvent : une culture de performance, ou une culture familiale). Le niveau 7 ne part pas de zéro.

**Ce qui a fonctionné :** commencer par l'inventaire des récits existants : quels récits la culture actuelle raconte-t-elle ? Quels sont les dilemmes déjà résolus, et selon quelles valeurs ? La philosophie TOTALISATION se greffe sur la culture existante en réconciliant, pas en remplaçant : les valeurs existantes sont citées dans la jurisprudence, réconciliées avec les nouvelles. Une culture attaquée se défend ; une culture réconciliée s'enrichit.

**Ce qui n'a pas fonctionné :** présenter le niveau 7 comme une « nouvelle culture ». Les équipes qui ont vécu des changements de culture successifs (rebranding, nouveaux slogans) les ont identifiés immédiatement comme de l'habillage. La continuité explicite (ce qui reste, ce qui change, pourquoi) est la seule entrée qui fonctionne.

### V5 : l'organisation qui doute (après des années difficiles)

**Contexte.** Des années de réductions, de départs, de promesses non tenues. La confiance est basse, le cynisme élevé. « Encore un programme de culture. »

**Ce qui a fonctionné :** le niveau 7 se construit ici sur une seule monnaie : les décisions coûteuses visibles. Pas de vision, pas d'ateliers, pas de récits avant la première décision qui coûte quelque chose à la direction (une promesse tenue contre l'intérêt immédiat, un aveu d'erreur, un changement de système réclamé depuis des années). La première décision honnête fait plus que dix ateliers. Ensuite — et seulement ensuite — les ateliers prennent sens.

**Ce qui n'a pas fonctionné :** commencer par les ateliers. Dans une organisation cynique, les ateliers d'abord sont lus comme du théâtre, et le cynisme est renforcé. L'ordre inverse (décisions coûteuses d'abord, ateliers ensuite) est la seule voie.

---

## Comment utiliser cette partie

- **Au démarrage** : la vision reformulée (§1.1) et le cas du fondateur parti (semaine 7) — le test ultime du niveau 7 arrive après le niveau 7.
- **Pendant le parcours** : le cas de la mission impossible (semaine 3) — la contradiction structurelle est le vrai adversaire.
- **Pour la transmission** : la carte des récits (§1.3) et la jurisprudence (§1.2) sont les deux actifs qui survivent aux personnes.
