
---

# Partie 16 : L'entretien du système : la routine permanente

Les huit semaines construisent le système. La vie le maintient — ou le laisse mourir. Cette partie est le guide d'entretien : la routine permanente qui fait vivre les modèles, les tests, la documentation, la planification et la confirmation après le départ du coach. Elle tient sur une page, parce que la complexité est l'ennemie de la constance.

## La routine hebdomadaire (60 minutes au total)

**La revue des modèles (15 minutes, en équipe, dans le rituel existant).** Relire les modèles actifs : la dernière confrontation, les divergences ouvertes, les mises à jour pendantes. Question standard : « le modèle dit-il encore le vrai ? ». Une divergence plus vieille que deux semaines devient un chantier — pas une discussion.

**La lecture du tableau de bord N2 (5 minutes).** Les six signaux N2 (divergences doc/modèle, tests flaky, ratio de tri, temps de pipeline, usage IA, modèles confrontés). Un signal rouge sans décision depuis deux semaines est une alarme double : le signal, et la non-décision.

**La revue de la documentation vivante (10 minutes).** Les pages les plus consultées cette semaine : à jour ? Les pages non consultées depuis un mois : à tailler ? Le support a-t-il signalé des trous ? La documentation se taille chaque semaine — les pages mortes sont archivées, pas laissées.

**La préparation du prochain Go/No-Go (15 minutes).** Les preuves automatisées collectées, les réserves précédentes vérifiées (levées ?), les informatifs consultés. Le Go/No-Go du jeudi ne doit jamais commencer par la collecte : la collecte est faite avant.

**Le tour des nouveaux (15 minutes, informel).** Comment vont les derniers arrivés ? Qu'est-ce qu'ils ne comprennent pas ? Leurs confusions sont les trous du lexique, du modèle, ou de la documentation — traités comme des livrables, pas comme des questions.

## La routine mensuelle (2 heures au total)

**La revue des fiches de tri (30 minutes).** Les rapports de tri des campagnes du mois : les ratios s'améliorent-ils ? Les questions ouvertes (les « question au PO ») ont-elles trouvé réponse ? Les gabarits produisent-ils moins de déchets ?

**La revue des confirmations (45 minutes).** Les confirmations du mois : les usages observés, les enrichissements du modèle, les apprentissages destinés. Une confirmation sans apprentissage est suspecte (elle n'a pas cherché).

**La revue du plan lié (30 minutes).** Chaque ligne du plan : sa référence est-elle vivante ? Les éléments « non modélisés » ont-ils progressé ? Les dates promises sont-elles encore fondées sur des preuves ?

**La revue du registre IA (15 minutes).** Les usages consignés, les ratios de validation, les règles à affiner. Un usage IA qui n'a pas été validé humainement est une dérogation — traitée comme telle.

## La routine trimestrielle (3 heures au total)

**L'audit des cérémonies (60 minutes).** Les six questions du test N2 (entrées obligatoires, livrables, tenue sans le coach, reliée aux modèles, preuves automatisées, enrichissement). Chaque échec a sa correction.

**La revue des gabarits de génération (60 minutes).** Les gabarits évoluent-ils ? Les tour de garde tourne-t-il ? Les signaux de dérive sont-ils actifs ? Les gabarits qui ne changent jamais sont des gabarits morts.

**La revue des variantes contextuelles (60 minutes).** Ce qui a changé dans le contexte (nouvelle équipe, nouveau legacy, nouveau client) ? Les variantes du parcours doivent-elles être ajustées ? Un parcours qui ne s'ajuste pas à son contexte se dérègle en silence.

## La routine annuelle (une journée au total)

**Le bilan d'ancrage complet (2 heures).** Ce qui tourne sans effort, ce qui tourne avec effort, ce qui ne tourne plus — photographié, comparé au bilan précédent, et publié.

**L'audit de la chaîne complète (2 heures).** De la demande à la confirmation : chaque maillon fonctionne-t-il ? Où sont les goulots ? Où sont les roues qui grincent ? La chaîne complète est visitée une fois par an — même si rien ne semble cassé.

**La transmission (2 heures).** L'équipe voisine : qui a été démontré ? Qui a été accompagné ? Qu'est-ce qui a été repris ? L'extension est le test de vitalité du niveau 2 — et elle se planifie, elle ne se décrète pas.

## Le test de l'entretien

Une seule question, à se poser chaque mois : **si le praticien partait demain, quel élément de la routine s'arrêterait ?** Chaque élément qui dépend d'une personne (et pas d'un protocole) est une fragilité — et chaque fragilité est un chantier de rotation : le gabarit existe-t-il ? La rotation est-elle documentée ? Deux personnes savent-elles le faire ?

L'entretien qui survit au praticien est l'entretien forgé. C'est la seule mesure qui compte.

---

# Partie 17 : La FAQ de fin de parcours — les questions que les équipes posent au bout

Ces questions arrivent toujours, généralement entre la semaine 6 et le mois 3. Les réponses sont celles qui ont fonctionné.

**« On a tout fait, pourquoi ça ne change rien dans nos livraisons ? »**
Vérifier trois choses : les engagements contractuels (les SI/ALORS) sont-ils réellement testables, ou reformulés en vœux ? Les Go/No-Go disent-ils parfois non (un Go/No-Go qui dit toujours oui est un rituel décoratif) ? Les confirmations trouvent-elles des usages imprévus (une confirmation qui ne découvre rien n'a pas cherché) ? Si les trois sont sains, le changement est probablement réel mais invisible à court terme — la courbe des bénéfices du niveau 2 est décalée : elle commence à payer au mois 3-6.

**« Le modèle est derrière, le code est devant. Qui suit qui ? »**
Le modèle suit le code quand le code révèle une meilleure solution (l'implémentation a découvert ce que le modèle ne prévoyait pas). Le code suit le modèle quand le code dévie sans raison (l'implémentation a contourné la spécification). La règle d'arbitrage : chaque divergence a un propriétaire — soit le modèle est corrigé (légitimate), soit le code est corrigé (conformité), soit la divergence est documentée comme un choix assumé. Ce qui est interdit : la divergence silencieuse.

**« Le MBT ne fonctionne pas chez nous, on abandonne ? »**
D'abord diagnostiquer : est-ce le modèle (pas confronté, trop flou), les gabarits (trop productifs, tests vides), ou le domaine (pas de combinatoire réelle) ? Si le domaine n'a pas de combinatoire (un processus linéaire), le MBT n'est pas l'outil — et l'abandon est légitime, documenté comme tel. Si c'est le modèle ou les gabarits, corriger d'abord. L'abandon du MBT après correction n'est pas un échec : c'est une décision éclairée.

**« Nos clients ne lisent pas la documentation. À quoi elle sert ? »**
À trois choses que les clients ne voient pas : elle oblige l'équipe à comprendre ce qu'elle construit (l'écrire révèle les trous), elle sert au support et aux nouveaux (les lecteurs invisibles de la documentation), et elle sert au niveau 3 (les tests générés partent de la documentation vivante). Une documentation qui ne sert qu'aux clients rate les deux tiers de sa valeur.

**« Combien de temps pour le niveau 3 ? »**
Huit semaines, comme les autres — mais avec une condition d'entrée stricte : les six questions du test N2 réussies. Si elles ne le sont pas, le niveau 3 construit sur du sable : la cadence du niveau 3 amplifie ce qui existe (vivant ou mort). La règle du praticien : ne jamais monter pour échapper au travail de consolidation.

**« Et si on arrêtait tout ? »**
La question de la semaine 5, revenue au mois 3. La réponse est la même que pour la semaine 5 : ce n'est pas une faute de la demander — c'est une faute de ne pas y répondre par les chiffres. Refaites l'exercice E2 de ROUGE (le bilan d'activité, chiffré) et comparez : qu'est-ce qui a été gagné, chiffré ? Qu'est-ce qui serait perdu, chiffré ? La décision qui suit les chiffres est honnête, quelle qu'elle soit.

## Le dernier mot : le niveau 2 en une page

Si tout ce livre devait tenir en une page, ce serait celle-ci :

**Le niveau 2, c'est la spécification qui vit.** Un processus modélisé (discutable par tous), une spécification dérivée (héritant des décisions), des tests générés (couvrant les combinaisons), une documentation vivante (reliée à la source), un plan lié (vérifiable à chaque ligne), et une confirmation qui enrichit le modèle.

**Le niveau 2, c'est l'anti-divergence.** Tout ce qui vit est relié : la doc au modèle, le modèle au code, le code aux tests, le plan aux preuves. Les divergences ne disparaissent pas — elles deviennent visibles, datées, et traitées dans la semaine.

**Le niveau 2, c'est l'anti-dépendance.** Chaque artefact a un gabarit, chaque gabarit a deux utilisateurs, chaque pratique a deux détenteurs. L'outillage existe pour être partagé, et le partage est ce qui rend le niveau réel.

Le niveau 3 (JAUNE) vous attend avec la cadence — mais le niveau 2 est un accomplissement, pas un palier provisoire. Une équipe qui modélise, dérive, génère, tri et confirme est une équipe qui sait ce qu'elle construit. Peu de choses sont plus rares.
