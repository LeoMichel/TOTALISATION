
---

# Partie 14 : Le lexique du praticien — les entrées types

Le lexique de l'équipe (semaine 1) se remplit au fil des malentendus. Cette partie fournit les entrées types que presque toutes les équipes finissent par écrire — avec les définitions qui fonctionnent et celles qui n'ont pas tenu. C'est le lexique préfabriqué : à adapter, pas à copier.

## Les entrées qui reviennent toujours

**Terminé (done)**
La définition qui fonctionne : « code mergé + tests passés + spécification vérifiée conforme + documentation à jour ». La définition qui ne tient pas : « ça marche sur ma machine ». La nuance qui fait tout : *terminé pour qui ?* — pour le développeur, pour le testeur, pour l'utilisateur. Le niveau 1 tranche : terminé pour le critère de validation, point.

**Bug critique**
Fonctionne : « rend une fonctionnalité promettable inutilisable pour un client réel, ou corrompt des données ». Ne tient pas : « urgent » (l'urgence est un contexte, pas une catégorie). La nuance : *chez nous* n'est pas un client réel — la gravité se mesure chez l'utilisateur, pas dans le bureau.

**Livraison**
Fonctionne : « à disposition des utilisateurs réels ». Ne tient pas : « mergé sur main ». La nuance : la livraison est un événement extérieur ; le merge est un événement intérieur. Les équipes qui confondent les deux découvrent leur confusion à chaque incident de production.

**Spécification**
Fonctionne : « document court (≤ 2 pages) : contexte, besoin, comportements SI/ALORS, critères de validation, cas limites ». Ne tient pas : « document qui décrit ce qu'on va faire » (trop vague pour être testable). La nuance : la longueur suit la complexité — une demi-page pour un correctif simple, deux pages pour une fonctionnalité, jamais une encyclopédie.

**Revue**
Fonctionne : « lecture par trois rôles avec trois questions différentes : implémentabilité, testabilité, fidélité ». Ne tient pas : « relecture de code » (trop étroite : le code n'est qu'un des objets). La nuance : la revue critique un artefact contre un autre (code vs spécification) — jamais une personne contre une norme.

**Priorité**
Fonctionne : « fréquence × impact × coût de report, mesurés ». Ne tient pas : « ce qui crie le plus ». La nuance : la priorité est un calcul visible ; si l'un des trois termes est absent, c'est une opinion avec un label.

**Rituel**
Fonctionne : « rendez-vous formel avec entrées obligatoires, livrable daté, format fixe ». Ne tient pas : « réunion régulière ». La nuance : la réunion discute et peut ne rien produire ; le rituel produit, ou n'a pas lieu.

**Dérogation**
Fonctionne : « écart écrit : qui décide, pourquoi, jusqu'à quand, ce qu'on apprend ». Ne tient pas : « exception accordée ». La nuance : la dérogation est un document qui préserve la règle ; l'exception accordée est un aveu que la règle est négociable — donc décorative.

**Confirmation**
Fonctionne : « vérification structurée des critères de succès auprès de l'usage réel, 1 à 4 semaines après livraison ». Ne tient pas : « feedback client ». La nuance : le feedback est spontané et non structuré ; la confirmation confronte des critères élicités — c'est une donnée, pas une impression.

**Vitesse / Vitesse durable**
Fonctionne : « le rythme qui peut être maintenu sans accumulation de dette invisible ». Ne tient pas : « rapidité ». La nuance : la vitesse mesurée en un trimestre ment ; la vitesse durable se lit sur l'année — c'est celle que la qualimétrie protège.

## Les entrées spécifiques aux équipes (exemples de terrain)

Les équipes finissent par écrire des entrées propres à leur contexte. Trois exemples réels, à titre d'inspiration :

**« Environnement de préparation » (équipe plateforme)** — « l'environnement où les tests de régression tournent avant le Go/No-Go. Il n'est PAS l'environnement de production, et un test qui passe en préparation ne garantit rien en production — c'est pourquoi la grille exige aussi la vérification post-diffusion. » Cette entrée est née d'un incident : un test vert en préparation, un bug en production, et un débat stérile. L'entrée a tué le débat.

**« Donnée historique » (équipe avec legacy)** — « les enregistrements créés avant la mise en place des règles actuelles. Ils peuvent violer les règles d'aujourd'hui sans être des bugs : les règles de validation doivent préciser s'ils s'appliquent rétroactivement. » Cette entrée a mis fin à un débat récurrent : les données historiques sont un cas limite par défaut, pas une anomalie.

**« Urgence réelle vs urgence déclarée » (équipe avec support client pressé)** — « une urgence réelle perd de l'argent chaque heure (production arrêtée, client bloqué). Une urgence déclarée est inconfortable mais supportable. Les urgences réelles court-circuitent la file ; les urgences déclarées y entrent avec leur priorité calculée. » Cette entrée a réduit les « urgences » de 70 % — parce qu'elles devaient être prouvées.

## Le format d'entrée qui tient

Chaque entrée du lexique suit ce gabarit en quatre parties :

```
TERME : ____________________
DÉFINITION (une phrase testable) : ____________________
LA NUANCE (la confusion que l'entrée tue) : ____________________
SOURCE (qui a tranché, quand) : ____________________
```

La partie « nuance » est la plus importante : une définition sans nuance est un dictionnaire ; une définition avec nuance est un accord d'équipe. Et la « source » protège la définition du rejet : elle rappelle que l'équipe a tranché — pas que le coach a imposé.

## L'entretien du lexique

Trois rituels d'entretien, légers mais réguliers :

1. **La revue mensuelle** (15 minutes) : relire les entrées du mois, vérifier qu'elles sont utilisées, marquer les mortes-nées.
2. **Le test du nouveau** : chaque arrivant relit le lexique et pose ses questions (exercice E9). Les questions améliorent les entrées ; les entrées accélèrent les suivants.
3. **La purge annuelle** : les entrées jamais citées depuis un an sont archivées (pas supprimées — archivées, avec leur histoire). Un lexique qui grossit sans purge devient un dictionnaire que plus personne ne lit.

## Les mots qui manquent toujours

Il existe une famille de mots que les équipes n'écrivent jamais et qui causent pourtant les pires malentendus. Le praticien les cherche délibérément en semaine 1 :

- **« Rapidement »** — combien de temps exactement ? (Heures ? Jours ? La réponse change la solution.)
- **« Simple »** — simple pour qui ? (Pour le développeur, simple = peu de code ; pour l'utilisateur, simple = peu d'étapes ; les deux se contredisent souvent.)
- **« Améliorer »** — selon quelle mesure ? (Vitesse ? Moins de bugs ? Satisfaction ? Les trois se disputent.)
- **« Bientôt »** — quelle date ? (Bientôt n'est pas un engagement ; c'est un anesthésiant.)
- **« La plupart des cas »** — quel pourcentage ? (90 % et 60 % se traitent différemment.)

Ces cinq mots sont des amortisseurs de conversation : ils semblent communiquer et cachent des écarts énormes. Le lexique qui les définit évite des mois de malentendus — et l'exercice du jeu des trois questions (S2, approfondissement) les révèle naturellement.

---

# Partie 15 : Les réponses aux questions de direction

Le praticien finit toujours par s'asseoir devant un décideur. Cette partie prépare ces conversations — avec les questions typiques de la direction et les réponses qui ont fonctionné.

## « Combien ça coûte ? »

La réponse honnête en trois blocs : le coût mesuré (les rituels : 4 heures par semaine pour 8 semaines, plus 4 heures d'entretien hebdomadaire — c'est 10 % de la capacité d'une équipe), le coût évité (le chiffrage E8 : le flou coûtait X, il coûte maintenant Y, l'écart est le premier retour), et le coût non encore mesurable (l'effet sur les livraisons suivantes, avec échéance de mesure). Ne promettez jamais le troisième bloc : la promesse non mesurée est la matière première du scepticisme.

## « Prouvez-moi que ça marche »

Le praticien ne prouve pas par l'argument : il prouve par le pilote. « Nous allons le faire sur une équipe, pendant huit semaines, avec des mesures avant/après que VOUS choisirez. Si les mesures ne bougent pas, nous arrêterons — par écrit. » L'offre du pilote mesuré est irréfutable : celui qui la refuse ne cherche pas la preuve, il cherche le refus.

Et le pilote se choisit bien : une équipe réelle qui livre (pas une équipe laboratoire), un irritant réel (pas un cas d'école), un sponsor même sceptique (le scepticisme rend la mesure crédible).

## « On a déjà des processus » / « On a déjà essayé »

Deux réponses différentes. À « on a déjà des processus » : « montrez-moi le processus qui décide si cette livraison part. » Le processus existant est souvent un document vivant dans l'oubli — le niveau 1 ne remplace pas, il rend exécutable. À « on a déjà essayé » : la rétrospective de l'échec (variante V6) — « racontez-moi ce qui s'est passé, où ça a cassé, et ce qui est différent cette fois ». La connaissance de l'échec précédent est la plus grande richesse d'une reprise : elle est gratuite, elle est là.

## « Combien de temps avant que mon problème [précis] soit résolu ? »

La réponse structurée : « Votre problème est probablement une des catégories suivantes — spécifications absentes, priorités floues, découvertes tardives. Les trois sont traitées aux semaines 2 et 3. Si votre problème est ailleurs, dites-le moi maintenant, et je vous dis honnêtement si le niveau 1 le traite — et sinon, ce qui le traitera. » L'honnêteté sur les limites de la méthode est l'argument le plus puissant en sa faveur : le praticien qui prétend tout résoudre est décrédibilisé par sa première promesse non tenue.

## « Pourquoi huit semaines ? Pourquoi pas deux ? »

Parce que les rituels ne sont pas des connaissances : ils sont des habitudes. Une habitude se forme par répétition en contexte réel — et le contexte réel produit environ un cycle complet en deux semaines. Huit semaines = quatre cycles complets, dont un traversé sous pression (semaine 5). Deux semaines produiraient des rituels de vitrine : compréhensibles, démontrés, jamais vécus sous tension.

## « L'équipe résistera »

Probablement — et la résistance est de l'information, pas un obstacle. Trois formes typiques : le scepticisme chiffré (le traiter par les données : E8), le cynisme d'échec précédent (le traiter par la rétrospective honnête : variante V6), la protection territoriale (le traiter par l'écriture : les rôles et critères clarifient qui garde quoi). La résistance qui persiste après le traitement de sa cause n'est plus de la résistance : c'est un refus — et il se documente, comme tout le reste.

## Le tableau de bord de la direction

La direction finit toujours par demander un tableau à elle. Le praticien le prépare dès la semaine 1 — trois lignes, une par page de direction :

1. **La vitesse durable** : le temps de cycle, mesuré (pas estimé), avec sa tendance.
2. **La fiabilité** : les incidents de production par mois, et les reprises.
3. **La confiance** : le pourcentage de livraisons passées par la grille avec toutes les preuves — et le nombre de No-Go assumés (un No-Go est un signe de santé : il prouve que le système protège).

Ce tableau de bord de direction est alimenté par la qualimétrie de l'équipe — c'est le même flux de données, traduit en langage de direction. Un seul tableau, deux lectures : l'équipe lit les signaux, la direction lit les tendances. Le pont entre les deux est la preuve écrite.

---

## La carte de sortie du niveau 1

Le lecteur arrive au bout de ce livre avec un inventaire complet :

**Ce qu'il sait faire :** éliciter avec des questions structurées, spécifier en IF…THEN, planifier avec un DoR, revoir en conformité, décider avec une grille, confirmer avec des critères, mesurer avec des décisions.

**Ce qu'il possède :** six fiches-outils, un lexique vivant, un registre des décisions, un centre d'excellence, un contrat signé, un calendrier annuel.

**Ce qu'il a traversé :** un point mort, un No-Go, un cycle complet, une démonstration aux voisins, un bilan chiffré.

**Ce qu'il devient :** l'équipe qui n'a plus besoin de demander la permission d'être rigoureuse. C'est tout le niveau 1 — et c'est déjà énorme.

Le niveau 2 (ORANGE) prend le relais : les modèles rendront les processus visibles, l'automatisation rendra les preuves systématiques, la documentation reliée rendra le savoir transmissible. Mais le niveau 2 construira sur ce que ce livre a installé — et ce qu'il n'installe pas, le niveau 2 ne pourra pas le simuler.

À lundi, semaine 1. Le sous-sol de Rayduf attend.
