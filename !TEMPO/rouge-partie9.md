
---

# Partie 9 : Former l'équipe et nourrir l'année

## 1. Le plan de formation interne du niveau 1

Quand le niveau 1 tient, l'équipe devient capable d'intégrer de nouveaux membres sans coach. Ce plan est le programme d'intégration : il transforme l'arrivée d'un nouveau en événement d'apprentissage pour tous.

### Le parcours du nouveau en 30 jours

**Semaine 1 : observer.** Le nouveau assiste à toutes les cérémonies sans rôle : il observe l'élicitation, la spécification, le point de qualité. Sa seule consigne : noter ce qu'il ne comprend pas. Ces notes sont le plan de formation individualisé — elles indiquent ce que l'équipe doit expliquer.

**Semaine 2 : lire.** Il lit le lexique (en le critiquant — exercice E9), une spécification exemplaire, le compte rendu du dernier Go/No-Go. Il écrit une page : « ce que je crois avoir compris ». Cette page est relue par le mentor et les malentendus sont corrigés — les siens ET ceux du lexique.

**Semaine 3 : faire accompagné.** Il écrit sa première spécification (module F1), avec un binôme. Il participe au Go/No-Go en jouant le rôle du décideur sur une livraison mineure. Il pose sa première question gênante en cérémonie — et l'équipe la traite comme légitime (c'est le test de la culture : un nouveau qui n'ose pas poser de questions est un nouveau mal accueilli).

**Semaine 4 : faire seul.** Il spécifie sa première demande en autonomie. Il anime son premier point de qualité (module F2). Son bilan d'intégration est écrit : ce qu'il comprend, ce qui reste flou, ce qu'il propose d'améliorer dans le parcours d'accueil lui-même.

**Le mentor :** un membre de l'équipe, pas le plus senior (les seniors expliquent mal ce qui est devenu évident pour eux), mais celui qui a le mieux intériorisé les rituels. Le mentorat dure 30 jours ; après, le nouveau est un pair.

### La formation du reste de l'organisation

Le niveau 1 ne se limite pas à l'équipe pilote : les équipes voisines finiront par poser des questions. Le plan minimal :

- **La séance de 45 minutes** (à offrir aux équipes curieuses) : le principe de la spécification avant le code, le déroulé d'un Go/No-Go, une capsule du vécu. Sans vente : une démonstration.
- **La porte ouverte** : les rituels de l'équipe pilote sont ouverts aux observateurs (avec préavis). Un observateur qui comprend en voyant vaut mieux qu'un convaincu par slides.
- **Les artefacts publics** : le lexique et les critères de bugs sont consultables par tous. La première adoption externe commence toujours par le vol d'artefacts : quelqu'un d'une autre équipe copie les critères pour son usage. C'est le signe que la diffusion a commencé.

## 2. Le calendrier de lecture annuel

Un livre de guidance se pratique sur un an. Voici le calendrier de relecture — ce que le lecteur relit, et quand, pour que le contenu reste vivant :

| Période | Relecture | Pourquoi |
|---|---|---|
| Semaines 1-8 (parcours) | Les parties dans l'ordre, avant chaque semaine | Préparer les ateliers |
| Mois 3 | Les capsules du vécu (Partie 7) + les checklists de fin de semaine | Raviver les leçons quand l'enthousiasme retombe |
| Mois 4 | Les situations difficiles (Partie 8) | Le moment où les difficultés réelles arrivent |
| Mois 5 | Les exercices non faits (E7-E12) | Les exercices reportés pendant le parcours |
| Mois 6 | L'audit des cérémonies (E12) + le test final (Partie 8 §4) | Le point de contrôle semestriel |
| Mois 7-9 | Une capsule par semaine, en rotation (répétition espacée) | L'entretien : une leçon par semaine, pas un marathon |
| Mois 10-12 | Les gabarits remplis (Partie 5) en comparaison avec les siens | Mesurer sa propre progression ; préparer la transmission |

**La règle de la répétition espacée :** une leçon relue après un usage réel ancre mieux que dix leçons relues d'affilée sans usage. Le calendrier est conçu pour que chaque relecture arrive après une expérience qui lui donne du sens.

**Le marqueur de progression du lecteur :** en mois 1, le livre est une instruction. En mois 6, c'est un miroir. En mois 12, c'est un témoin — et le lecteur qui passe au niveau 2 découvrira que le livre du niveau 1 est devenu sa référence des fondations.

## 3. Les gabarits d'annexe remplis supplémentaires

### 3.1 Contrat qualité v2.0 — exemple entièrement rempli

**Contrat qualité de l'équipe plateforme — version 2.0 (semaine 8)**

**Engagements de l'équipe :**
1. Aucune demande ne passe en implémentation sans spécification écrite et revue par trois rôles. *(Preuve mesurable : 92 % des demandes du trimestre. Objectif : 100 % au T+2.)*
2. Les bugs sont priorisés selon les critères du 18 juin ; toute dérogation est écrite avec sa condition de levée. *(3 dérogations ce trimestre, toutes levées à date.)*
3. Chaque diffusion passe par le rituel Go/No-Go, avec compte rendu publié le jour même. *(7 Go, 1 No-Go levé en 2 jours.)*
4. Le point de qualimétrie a lieu chaque vendredi, 15 minutes ; chaque signal rouge reçoit une décision avec décideur et levée. *(Métrique de reprise : 31 % → 12 %.)*
5. Les apprentissages de CONFIRMATION alimentent l'élicitation suivante. *(4 confirmations faites, 7 entrées de lexique issues des confirmations.)*

**Engagements de l'organisation (sponsor) :**
6. Le sponsor répond aux demandes écrites sous 5 jours ouvrables. *(3 demandes ce trimestre, délai moyen 2,4 jours.)*
7. La capacité dédiée aux rituels (4 h/semaine) est protégée dans la planification.
8. Le champion du centre d'excellence dispose de 4 h/semaine reconnues.

**Règle des dérogations :** s'écarter du contrat si nécessaire, mais écrire la dérogation : qui décide / pourquoi / jusqu'à quand / ce qu'on apprend. Une dérogation sans levée datée est une règle cassée en silence.

**Révision :** le contrat est relu à chaque trimestre. Toute version modifie la précédente, jamais ne la remplace en silence. Historique : v0.1 (semaine 1), v0.2 (semaine 3), v2.0 (semaine 8).

**Signatures :** équipe (8 signatures) — sponsor — décideur de livraison. Date : [semaine 8].

**Ce qui distingue ce contrat d'un contrat de vitrine :** chaque engagement a sa preuve mesurable entre parenthèses. Un engagement sans mesure est une intention. C'est le format qui permet à la revue trimestrielle de dire « tenu » ou « non tenu » sans débat.

### 3.2 Note de fin de phase pour la direction — exemple entièrement rempli

**À : [VP produit] — De : équipe pilote — Objet : bilan des 8 semaines — niveau 1**

**Où nous étions :** en juin, les demandes étaient codées sans spécification, les bugs priorisés à l'appel, les problèmes découverts en production. Coût du flou sur le trimestre précédent : 19 jours-homme de reprises (mesure E8).

**Ce que nous avons construit :** spécification avant code (92 % des demandes), critères de bugs partagés (fin des priorités à l'appel), rituel Go/No-Go (7 livraisons passées par la grille, 1 No-Go documenté), métrique hebdomadaire regardée, lexique vivant (23 entrées), centre d'excellence avec 23 artefacts.

**Les chiffres du mouvement :** reprises 31 % → 12 % ; temps de cycle stable (+3 %) malgré les rituels ; 1 incident de production en 8 semaines (contre 3 sur les 8 semaines précédentes) ; satisfaction du demandeur pilote : de « je ne sais jamais où j'en suis » à « je sais toujours où j'en suis, même quand c'est non ».

**Ce qui reste fragile :** la métrique de cycle est collectée à la main (3 interruptions en 8 semaines) ; la confirmation des livraisons n'atteint que 60 % des demandes (les clients pas toujours accessibles).

**Ce que nous demandons :** (1) pérenniser 4 h/semaine pour les rituels ; (2) financer l'automatisation de la métrique (3 jours de travail) ; (3) autoriser le passage au niveau 2 avec cette équipe. Refuser ces demandes est légitime — mais voici ce que chacune protège.

**Signature :** l'équipe au complet.

**Ce qui fait la qualité de cette note :** une page, des chiffres, une demande explicite. La direction lit une page ; elle ne lit jamais un rapport de 12 pages. Et la phrase du demandeur (« je sais toujours où j'en suis, même quand c'est non ») est la preuve qualitative qui accompagne les chiffres.

## 4. La transition vers le niveau 2

Le niveau 1 a fait exister les rituels. Le niveau 2 (ORANGE) les rend modélisables : les processus deviennent des diagrammes, les spécifications deviennent des modèles exécutables, la documentation se relie à la vérité.

**Le readiness test du niveau 2** — quatre conditions, toutes mesurables :

1. Les cérémonies passent le test des trois questions (E12).
2. La spécification avant le code atteint 90 %+ sans surveillance.
3. La métrique de qualimétrie est regardée spontanément (l'équipe la consulte sans rappel).
4. Un membre de l'équipe peut expliquer chaque rituel à un nouveau sans le coach (test F1 inversé).

Si les quatre conditions sont remplies, le niveau 2 est une extension naturelle. Si une condition manque, la consolider d'abord : le niveau 2 construit sur le niveau 1 exactement comme le niveau 1 construit sur rien. Les fondations ne se rattrapent jamais en montant.

**Le lecteur qui a parcouru les neuf parties de ce livre a maintenant :** la méthode (Parties 1-3), la transmission (Partie 4), les preuves (Parties 5-7), les garde-fous (Partie 8), et le plan de l'année (Partie 9). Il ne lui manque qu'une chose, que aucun livre ne donne : la première semaine réelle avec son équipe. Elle commence lundi.
