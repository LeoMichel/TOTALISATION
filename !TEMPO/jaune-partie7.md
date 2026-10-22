
---

# Partie 7 : Les cérémonies du niveau 3

Cette partie adapte les sept cérémonies de TOTALISATION au niveau 3 : les cérémonies du niveau 2 deviennent des processus forgés à cadence constante — mêmes objectifs, mêmes participants, mais avec un rythme, des seuils, et une autonomie prouvée. Le niveau 3 ne transforme pas les cérémonies : il les cadence.

**La règle du niveau 3 :** une cérémonie n'est forgée que si sa version du niveau 2 tient sans le coach pendant quatre semaines consécutives. On ne forge pas sur du sable.

## Cérémonie 1 : L'ÉLICITATION cadencée

**Ce que le niveau 3 ajoute :** l'élicitation n'est plus un événement déclenché par une demande ; elle est un rendez-vous de flux — les demandes entrent en file, sont élicitées à cadence fixe, et la file est visible.

**Le déroulé du niveau 3 (60 minutes, à heure fixe) :**

1. **La revue de la file d'entrée** (10 min) : les demandes en attente d'élicitation sont relues — aucune ne dépasse 5 jours ouvrables sans élicitation. Le temps d'attente est un signal du tableau de bord N3.
2. **L'élicitation des demandes du jour** (40 min) : le format du niveau 2 (modèle en support, questions structurées), à cadence fixe. Les demandes simples (30 min) et complexes (60 min) sont planifiées différemment — la variété est assumée.
3. **La sortie cadencée** (10 min) : chaque demande élicitée entre en spécification avec son rendez-vous daté. La file de spécification est visible — c'est le deuxième signal.

**Les entrées obligatoires :** la demande brute avec sa source, le demandeur identifié, le modèle du domaine à jour.

**Les sorties attendues :** le besoin reformulé, le modèle enrichi, le rendez-vous de spécification daté.

**Le piège du niveau 3 :** la file invisible. Une demande qui attend 5 jours sans signal est une demande perdue. Le tableau de bord N3 compte les demandes en attente — et le seuil (5 jours) existe parce qu'une demande qui attend trop arrive avec un demandeur frustré, ce qui dégrade l'élicitation elle-même.

**Le lien avec le niveau 2 :** le modèle reste le support. Ce qui change : le rythme. La demande n'attend plus le bon moment ; le bon moment est fixe, et la demande le trouve.

## Cérémonie 2 : LA DÉFINITION forgée

**Ce que le niveau 3 ajoute :** la spécification a un SLA (délai de service) : écrite dans les X jours de l'élicitation, revue dans les Y jours de son écriture. La spécification N3 est cadencée, pas seulement dérivée.

**Le déroulé du niveau 3 (90 minutes, à cadence fixe) :**

1. **La génération des règles à partir du modèle** (30 min) : comme au niveau 2, avec la contrainte de cadence — la spécification est écrite pour la date prévue, pas pour « quand on aura le temps ».
2. **La revue à trois rôles** (30 min) : comme au niveau 2, avec un ajout N3 — la revue vérifie aussi la testabilité automatique : chaque règle peut-elle devenir un test générable ? Si non, pourquoi ? (La réponse légitime existe ; elle est documentée.)
3. **La sortie vers la planification** (30 min) : la spécification prête entre en file de planification avec son rendez-vous daté. La DoR du niveau 3 inclut le SLA.

**Les entrées obligatoires :** le modèle enrichi (cérémonie 1), la capacité de revue réelle, les gabarits de spécification à jour.

**Les sorties attendues :** la spécification complète avec SLA respecté, les critères de validation, les tests candidats identifiés (générables ou non, avec raison).

**Le piège du niveau 3 :** le SLA qui tue la qualité. Un SLA de 3 jours sur des demandes complexes produit des spécifications bâclées — le niveau 3 exige des SLA différenciés (simples : 2 jours ; complexes : 5 jours ; exploratoires : traitées comme des spikes). Le SLA unique est le piège ; le SLA par classe est la forge.

**Le lien avec le niveau 2 :** la revue à trois rôles reste intangible. Ce qui change : les dates. Une revue sans date n'existe pas au niveau 3 — c'est un vœu.

## Cérémonie 3 : LA PLANIFICATION cadencée

**Ce que le niveau 3 ajoute :** la planification devient un métronome : même heure, même durée, même format. L'itération est cadencée — les engagements sont mesurés contre la cadence, pas contre l'humeur.

**Le déroulé du niveau 3 (60 minutes, métronome) :**

1. **La revue de la capacité réelle** (10 min) : comme au niveau 2, avec les données du dernier cycle (temps réel vs temps estimé). La capacité est apprise, pas espérée.
2. **La sélection par la file** (20 min) : les spécifications prêtes (SLA respecté) entrent en ordre de priorité documentée. La règle N3 : pas de négociation de dernière minute — les exceptions sont des décisions de sponsor documentées, pas des débats de rituel.
3. **Le contrat d'itération cadencé** (20 min) : les engagements avec leurs preuves attendues et leurs dates de preuve. Le contrat du niveau 3 inclut le calendrier des preuves (quand chaque preuve sera disponible).
4. **Les risques en revue** (10 min) : les risques du cycle précédent sont relus d'abord — leurs levées sont vérifiées. Un risque qui se répète sans traitement est un signal du tableau N3.

**Les entrées obligatoires :** les spécifications prêtes (SLA), les données de capacité du dernier cycle, le registre des risques à jour.

**Les sorties attendues :** le contrat d'itération avec calendrier de preuves, la file de planification à jour, les risques traités ou escaladés.

**Le piège du niveau 3 :** la planification qui devient un rituel de vœux. Le métronome sans les données réelles de capacité produit des itérations uniformément en retard — la cadence sans honnêteté. La mesure de la capacité réelle est la condition de la cadence crédible.

**Le lien avec le niveau 2 :** le plan lié aux modèles reste la base. Ce qui change : le plan est relu à chaque cycle avec ses données de performance — le plan N3 apprend de ses erreurs, chiffrées.

## Cérémonie 4 : L'IMPLÉMENTATION en cadence

**Ce que le niveau 3 ajoute :** l'implémentation devient mesurable : le temps de cycle (de la spécification à la mise en production) est un signal premier. Les revues de code, les tests générés, et les mises à jour de modèle tournent à cadence fixe.

**Le déroulé du niveau 3 (30 minutes par revue, à cadence fixe) :**

1. **La conformité au modèle** (10 min) : comme au niveau 2 — avec un ajout : la revue vérifie aussi la vitesse (« ce chemin a-t-il pris le temps prévu ? » — la divergence de vitesse est un signal, pas une faute).
2. **Les tests générés** (10 min) : les tests tournent à cadence fixe (pipeline) — l'échec ouvre un ticket daté, pas une discussion. Le flaky est quarantené avec règle.
3. **La mise à jour du modèle** (10 min) : à cadence fixe (hebdomadaire au minimum). Une divergence code/modèle plus vieille que 5 jours est un signal rouge du tableau N3.

**Les entrées obligatoires :** le code, le modèle à jour (5 jours max), les tests générés en pipeline.

**Les sorties attendues :** le code approuvé, les tests passés ou quarantenés, le modèle synchronisé dans les 5 jours.

**Le piège du niveau 3 :** la cadence qui cache la dérive. Un rituel à heure fixe qui ne traite pas les divergences n'est pas une cadence : c'est une répétition. La mesure de la cadence réussie est le délai de traitement des divergences — pas la présence aux rendez-vous.

**Le lien avec le niveau 2 :** l'outillage N2 reste la base. Le niveau 3 ajoute les échéances : chaque automatisme a son rythme, chaque rythme a son seuil, chaque seuil a son décideur.

## Cérémonie 5 : LA DIFFUSION — le Go/No-Go N3

**Ce que le niveau 3 ajoute :** le Go/No-Go devient prévisible : la grille N3 avec ses 5 bloquants et ses informatifs, les preuves automatisées, la décision en 30 minutes — et la preuve de la décision suivie (les réserves levées).

**Le déroulé du niveau 3 (30 minutes, au métronome) :**

1. **Les 5 bloquants** (10 min) : la grille N3 ne présente que les bloquants en séance — les informatifs sont consultables avant. Le temps de séance est investi sur les vraies décisions.
2. **Les réserves** (10 min) : chaque réserve est formulée avec sa condition de levée et son décideur. Les réserves sans levée datée sont refusées par l'animateur — c'est la règle forgée du niveau 3.
3. **La décision et son suivi** (10 min) : le Go/No-Go de la fois précédente est relus d'abord — les réserves levées ? Les dérogations respectées ? La grille apprend de ses décisions passées.

**Les entrées obligatoires :** les preuves automatisées (5 bloquants), les réserves précédentes et leur état, le décideur réel.

**Les sorties attendues :** la décision datée, les réserves avec conditions de levée, la mise à jour du registre.

**Le piège du niveau 3 :** la grille qui n'apprend pas. Une grille identique depuis six mois est suspecte : soit le produit est immuable (rare), soit la grille n'a pas été confrontée à ses échecs. La revue trimestrielle de la grille (quels critères ont servi ? lesquels ont été contournés ?) est la forge permanente.

**Le lien avec le niveau 2 :** les critères N2 restent. Le niveau 3 les hiérarchise (bloquants/informatifs) et les fait vivre (revue trimestrielle, réserves suivies).

## Cérémonie 6 : LA CONFIRMATION systématique

**Ce que le niveau 3 ajoute :** la confirmation devient systématique : chaque livraison est confirmée dans les 10 jours ouvrables — le taux de confirmation est un signal du tableau. Les confirmations ratées (client inaccessible) sont documentées avec une relance datée.

**Le déroulé du niveau 3 (45 minutes, systématique) :**

1. **Les critères de succès** (10 min) : confrontation au réel, comme au niveau 2.
2. **Les usages observés** (20 min) : la confirmation N3 inclut l'observation (pas seulement l'entretien) : les usages réels sont documentés, les imprévus enrichissent le modèle — la grande boucle N3 est systématique.
3. **Le traitement des apprentissages** (15 min) : chaque apprentissage a sa destination : le modèle (extension candidate), la spécification (correction), l'élicitation (question nouvelle). Un apprentissage sans destination est un apprentissage perdu — et le tableau N3 le compte.

**Les entrées obligatoires :** les critères de succès, le modèle livré, l'accès aux utilisateurs (ou le refus documenté avec relance).

**Les sorties attendues :** les critères confirmés, les extensions du modèle, les apprentissages destinés.

**Le piège du niveau 3 :** la confirmation de complaisance systématique. Un taux de confirmation de 100 % avec 100 % de critères atteints est suspect : la confirmation qui ne découvre jamais rien ne cherche rien. La métrique honnête : les apprentissages par confirmation (0 apprentissage = confirmation morte).

**Le lien avec le niveau 2 :** l'enrichissement du modèle reste la règle. Le niveau 3 ajoute la systématisation : chaque livraison est confirmée, chaque confirmation alimente le système, et le taux de confirmation est un signal public.

## Cérémonie 7 : LA QUALIMÉTRIE N3

**Ce que le niveau 3 ajoute :** le tableau de bord N3 (6 signaux avec décideurs) devient le battement principal — et chaque signal est relié à un risque nommé (pourquoi ce signal existe : quel incident, quelle crainte).

**Le déroulé du niveau 3 (20 minutes, métronome) :**

1. **La lecture** (10 min) : les signaux avec leurs valeurs, tendances, et leurs références de risque (« ce signal existe depuis l'incident de mars »).
2. **Les décisions** (10 min) : chaque décision avec décideur et levée — et la revue des décisions passées (les levées sont vérifiées).

**Les entrées obligatoires :** le tableau alimenté automatiquement, le registre ouvert, les décisions passées.

**Les sorties attendues :** les décisions notées, les levées vérifiées, les escalades documentées.

**Le piège du niveau 3 :** le tableau devenu rituel de lecture sans pouvoir. La test : la dernière décision du tableau — quand ? Qu'a-t-elle changé ? Un tableau sans décision depuis 4 semaines est un mort en marche : resserrer les seuils ou réviser les signaux.

**Le lien avec le niveau 2 :** les signaux N2 restent. Le niveau 3 les ancre dans les risques (chaque signal a son pourquoi) et les fait vivre (levées vérifiées, rotations assumées).

## Le test des cérémonies du niveau 3

Le test à six questions du niveau 2 gagne une dimension — la cadence :

7. **Tient-elle à cadence fixe ?** (Même heure, même durée, même format — indépendamment des urgences.)
8. **Ses SLA sont-ils respectés et classés ?** (Le niveau 3 forge des délais différenciés et tenus.)

Ces huit questions sont le test de passage au niveau 4 : une cérémonie qui les réussit toutes est une infrastructure de processus — prête à être automatisée, rendue systématique, et transformée en chaîne. Une cérémonie qui échoue encore aux questions 1-3 doit retourner au niveau 1 — la forge ne construit pas sur du sable.
