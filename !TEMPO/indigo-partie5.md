
---

# Partie 5 : Cas réels, gabarits remplis et variantes contextuelles (niveau 6)

Les gabarits remplis, les situations vécues, et l'adaptation du niveau 6 (prévention, anticipation, intelligence organisationnelle) aux contextes réels.

## 1. Les gabarits remplis d'exemples réels

### 1.1 Le registre des risques — exemple rempli

> Le registre réel de l'organisation, avec des risques dans chaque état. Notez que les états sont assumés : un registre où tout est « actif » est un registre décoratif.

| ID | Risque (scénario concret) | Probabilité | Impact | Chantier de prévention | Propriétaire | Échéance | État |
|---|---|---|---|
| R-001 | Le mainteneur du pipeline de génération part, la chaîne s'arrête | Moyenne | Élevé | Binôme + guide testé par 2 personnes | L.T. | En cours | 🟢 actif |
| R-004 | Croissance du volume de données rend la suite nocturne trop lente (>2h) | Élevée | Moyen | Analyse de partitionnement, prototype sur 2 suites | Équipe D | 15/12 | 🟢 actif |
| R-007 | Migration du framework X rend obsolètes 30 % des gabarits | Moyenne | Élevé | Inventaire des gabarits affectés, plan de migration | Centre d'excellence | Q2 | 🟢 actif |
| R-011 | Dépendance au fournisseur de l'outil de génération (écart de licence) | Faible | Critique | Étude des alternatives, POC d'un outil open source | Sponsor | Annulée — licence renouvelée 3 ans | ⚪ purgé |
| R-014 | La documentation vivante dérive du modèle (dérive lente) | Moyenne | Moyen | *(aucun — dormant depuis 8 mois)* | — | — | 🟡 dormant |
| R-017 | Le canal des signaux faibles devient un dépotoir de plaintes | Moyenne | Faible | Rappel des règles + tri mensuel par le gardien | Gardien canal | 30/11 | 🟢 actif |

**Lecture du registre :** le risque R-014 est dormant depuis 8 mois — il a reçu un sort au dernier trimestre : activé avec un chantier minimal (audit de dérive automatisé), ou purgé. Un dormant n'y reste jamais : le trimestre décide. Le purgé (R-011) est resté dans l'historique : on ne réinvente pas un risque déjà traité.

### 1.2 Le registre des signaux faibles — exemple rempli

> Le canal des signaux faibles sur un mois réel. Les signaux sont factuels (ce qui a été observé), pas interprétatifs.

| Date | Signal (observation factuelle) | Qui | Conséquence |
|---|---|
| 04/11 | « Troisième ticket ce mois sur le filtre X avec la même confusion (valeurs nulles) » | Support | → signal existant confirmé, la page doc du filtre X est révisée |
| 07/11 | « Le build nocturne a duré 2h15, contre 1h30 le mois dernier » | L.T. équipe D | → relié au risque R-004 (en cours), accélération de l'analyse |
| 12/11 | « Un nouveau venu a demandé pourquoi le processus Y existe — personne n'a su répondre » | QA | → question au centre d'excellence : le processus Y a un modèle ? Son pourquoi est documenté ? |
| 18/11 | « Deux retours clients mentionnent la lenteur du rapport Z dans le même cas » | Support | → signal faible cumulé : à 3, ça devient un ticket de performance prioritaire |
| 25/11 | « Le pipeline de l'équipe C a échoué 3 fois cette semaine sur le même test flaky » | Équipe C | → relié au signal « flaky » du niveau 3, déjà traité par l'équipe |

**La revue mensuelle des signaux (extrait) :** 5 signaux du mois, 2 confirmés comme tendances (filtre X, lenteur Z), 1 relié à un risque actif (R-004), 1 transféré (processus Y), 1 doublon. Aucun signal sans sort : un signal qui reste en liste sans traitement est un signal ignoré.

**Ce qui fait la qualité du canal :** les signaux sont factuels (observation, pas interprétation) et chaque signal a un sort. Le dépotoir de plaintes (« tout le monde se plaint de tout ») est le symptôme de signaux interprétatifs.

### 1.3 Le compte rendu de la revue de prévention — exemple rempli

> La revue mensuelle (45 minutes), remplie. C'est le battement de cœur du niveau 6.

**Revue de prévention — 28/11, 45 minutes. Présents :** responsable prévention, 3 propriétaires de chantiers, gardien du canal, centre d'excellence.

**Ordre du jour et décisions :**

1. **Régressions du mois** (10 min) : 2 régressions détectées, 2 actions de prévention consignées dans les délais. Aucun dépassement de délai. *(Information, pas de décision.)*
2. **Chantiers en cours** (15 min) :
   - R-004 (suite nocturne trop lente) : l'analyse de partitionnement a identifié 3 suites à scinder. Prototype prévu la semaine du 02/12. **Sur la bonne voie.**
   - R-007 (migration framework) : l'inventaire des gabarits affectés est terminé : 14 gabarits, dont 6 critiques. Plan de migration rédigé, estimation 3 semaines. **Sur la bonne voie.**
   - R-014 (dérive documentation) : **dormant depuis 8 mois — décision du jour** : activation avec un audit de dérive automatisé (script qui compare doc et modèle chaque semaine). Propriétaire : centre d'excellence. Échéance : 20/12.
3. **Signaux du mois** (10 min) : le signal « lenteur rapport Z » atteint 3 occurrences cumulées → **décision** : ouvrir un ticket de performance prioritaire (il quitte le canal des signaux, il devient un chantier).
4. **Horizon** (5 min) : point sur la préparation semestrielle — l'exercice de l'horizon aura lieu mi-décembre, les fonctions sont avisées.
5. **Nouveau risque** (5 min) : le départ annoncé de S.M. (mainteneur pipeline) confirmé pour janvier → R-001 monte en priorité : le binôme est confirmé, le guide sera re-testé par la relève avant le départ.

**Le registre est mis à jour en séance.** Trois décisions datées, une activation de dormant, une priorisation. 45 minutes.

**Ce qui fait la qualité de ce compte rendu :** les décisions en séance (pas « on va y réfléchir »), le dormant traité (pas repoussé), et le signal qui monte en chantier quand il atteint son seuil. Le compte rendu de 45 minutes qui décide vaut mieux que 3 heures qui constatent.

## 2. Cas vécus étendus : le niveau 6

### Cas de la semaine 1 : la régression qui a pris 6 semaines à être détectée

**Situation.** La première analyse des régressions (module F1) a révélé une médiane choquante : 6 semaines entre l'introduction d'un défaut et sa détection. L'équipe croyait que « la détection était immédiate, le pipeline tourne à chaque commit ».

**Le diagnostic.** Le défaut avait été introduit dans une branche longue (refonte de module, 5 semaines de développement), et le pipeline ne tournait que sur les commits de la branche principale. Les tests rapides tournaient, mais pas les tests de régression standard — la régression n'était détectée qu'au merge.

**La correction.** La règle « les tests de régression standard tournent sur les branches longues aussi (au moins 2 fois par semaine, en nocturne de branche) ». Le délai médian est passé à 3 jours sur le trimestre suivant.

**Ce que ce cas enseigne.**
- Le délai de détection n'est pas une propriété du pipeline : c'est une propriété du workflow. Un pipeline impeccable sur la branche principale laisse les branches longues aveugles.
- La mesure du délai (module F1) est l'exercice qui révèle ces angles morts : sans la médiane mesurée, l'équipe croyait sa détection immédiate depuis des années.
- La correction est une règle de workflow, pas une optimisation de pipeline. Cherchez toujours : où le défaut peut-il vivre sans être vu ?

### Cas de la semaine 2 : le canal qui est devenu un dépotoir (et comment il en est sorti)

**Situation.** Le canal des signaux faibles, ouvert avec enthousiasme, a reçu 40 « signaux » le premier mois : des plaintes, des opinions, des frustrations, des interprétations. La revue mensuelle a duré 2 heures et n'a rien décidé. Trois semaines plus tard, personne ne postait plus : le canal était mort.

**Le diagnostic.** Les signaux interprétatifs (« le process X est mauvais », « tout le monde déteste le nouvel outil ») ne sont pas des signaux : ce sont des opinions. Un canal qui les accepte devient un dépotoir, et la revue devient un tribunal impossible à arbitrer.

**La correction.** La règle du factuel : un signal décrit une observation, pas une interprétation. « Troisième ticket ce mois sur le filtre X » est un signal. « Le filtre X est mal conçu » est une opinion. La reformulation a été enseignée par l'exemple : le gardien a reformulé les 10 premiers signaux d'opinion en signaux factuels, publiquement, dans le canal. Après un mois, l'équipe écrivait factuel d'elle-même.

**Ce que ce cas enseigne.**
- Le canal des signaux faibles vit ou meurt sur la distinction factuel/interprétatif. Elle ne s'impose pas : elle s'enseigne par l'exemple (la reformulation publique).
- Le volume n'est pas la santé du canal : 5 signaux factuels traités valent mieux que 40 opinions ignorées.
- La mort du canal (personne ne postait plus) n'était pas un manque d'engagement : c'était un système d'incitation cassé (les opinions restaient sans réponse). Corrigez le système, pas les gens.

### Cas de la semaine 3 : le risque qui a coûté 400 000 $ (et qui était documenté depuis 2 ans)

**Situation.** L'incident majeur (dépendance au fournisseur, écart de licence, arrêt de l'outil de génération pendant 3 semaines) est arrivé. En analysant, l'équipe a retrouvé le risque dans le registre : documenté depuis 2 ans, probabilité « faible », jamais traité. Le registre contenait le scénario exact de ce qui s'est passé.

**Le constat brutal.** Le registre avait raison depuis 2 ans. Personne ne l'avait lu. Le risque était documenté, non traité — ce qui est pire que non documenté : l'organisation savait et n'a rien fait.

**La correction.** Trois mesures : (1) le registre des risques est relu en revue mensuelle (il ne suffisait pas d'exister) ; (2) tout risque à impact critique a un plan minimal même en probabilité faible (une étude, un POC, une échéance — pas une solution complète) ; (3) la revue trimestrielle présente les risques à impact critique même en probabilité faible, à chaque fois, sans exception.

**Ce que ce cas enseigne.**
- Un registre non relu est pire qu'aucun registre : il donne l'illusion d'une gestion des risques. Le risque documenté et non traité est un aveu documenté de négligence.
- La probabilité faible n'annule pas l'impact critique : les risques à impact critique ont toujours un plan minimal, quelle que soit la probabilité. C'est la règle qui aurait coûté une étude de 2 semaines au lieu d'un incident de 3 semaines.
- Cet incident est le meilleur argument de financement du niveau 6 que vous aurez jamais : « nous avions documenté le risque depuis 2 ans ». Il se raconte — avec la honte assumée, qui est ce qui le rend crédible.

### Cas de la semaine 5 : le départ du mainteneur (et la succession qui a tenu)

**Situation.** Le départ annoncé de S.M., mainteneur principal du pipeline, était le scénario du risque R-001. La préparation a suivi le plan : binôme confirmé, guide re-testé par la relève, transmission sur 4 semaines.

**Le test réel.** Le départ a eu lieu. La semaine suivante, le pipeline a eu 2 incidents (une erreur E217, un timeout). La relève les a résolus en utilisant le guide — sans appel. Le canal `#gen-support` a documenté les deux résolutions.

**Ce que ce cas enseigne.**
- La succession prévée par le niveau 6 fonctionne quand elle est testée avant le départ — pas pendant. Le binôme et le guide re-testé sont ce qui a tenu.
- Les 2 incidents de la semaine suivante sont la preuve de la réussite, pas de l'échec : la relève a résolu seule, avec les artefacts. Une transition sans aucun incident est suspecte (rien n'a été testé).
- Le risque R-001 a été purgé après le départ réussi : il reste dans l'historique. La purge d'un risque traité est un moment de satisfaction rare et réel.

### Cas de la semaine 6 : l'horizon qui a prédit le vrai problème

**Situation.** L'exercice de l'horizon (semestriel) a fait dire à l'équipe de support : « dans 18 mois, la croissance du volume de données rendra les rapports X inutilisables en l'état ». L'équipe de développement a évalué : plausible, mais « on verra dans 18 mois ».

**La suite.** Le thème a été consigné au registre avec date de relecture (12 mois). À la relecture : les rapports X étaient déjà à la limite, la croissance était en avance sur la prédiction. Le chantier a été ouvert avec 12 mois d'avance sur la crise — au lieu de 3 mois après.

**Ce que ce cas enseigne.**
- L'horizon ne produit pas des vérités : il produit des hypothèses datées. La relecture programmée est ce qui transforme l'hypothèse en anticipation réelle.
- La fonction support voit souvent l'avenir avant le développement : elle vit le volume croissant au quotidien. L'exercice de l'horizon qui inclut toutes les fonctions capte ces signaux.
- Le chantier ouvert 12 mois d'avance coûte une fraction de ce que coûte le chantier ouvert 3 mois après la crise. C'est le ROI de l'anticipation — et il se raconte : « nous avons vu venir ce problème 15 mois avant ».

## 3. Variantes contextuelles du niveau 6

### V1 : petite organisation (2-3 équipes)

- La revue de prévention peut être fusionnée avec le point de gouvernance (niveau 5) : un rituel enrichi vaut mieux que deux rituels pauvres, dans une petite organisation.
- Le registre des risques peut être réduit à 5-10 risques réels : un registre de 40 risques dans une organisation de 15 personnes est un exercice de style. Le nombre n'est pas la gestion.
- Le canal des signaux faibles peut être un simple canal de discussion avec la règle du factuel : l'outillage n'est pas ce qui fait le canal.
- L'horizon peut être réduit à 3 fonctions clés (dev, support, direction) : l'essentiel est le croisement des regards, pas l'exhaustivité.

### V2 : organisation distribuée

- Les quatre battements doivent survivre aux fuseaux : chaque battement a un journal écrit (pas seulement des réunions), et les décisions urgentes passent par le registre asynchrone avec délai d'objection.
- La revue de prévention est enregistrée (ou son compte rendu est complet) : les absents de fuseau lisent, et peuvent contester par écrit sous 48h.
- Le canal des signaux faibles est l'outil de distribution le plus précieux du niveau 6 : il capte les observations de tous les fuseaux, y compris ceux qui ne sont jamais dans les réunions.
- L'exercice de l'horizon est écrit d'abord (chaque fonction écrit ses réponses), croisé ensuite en visio : le croisement écrit est plus honnête que le tour de table en direct.

### V3 : organisation réglementée

- Le registre des risques satisfait souvent une exigence de gestion des risques : mappez-le sur le référentiel dès le départ, et faites valider le mapping. La prévention réglementaire et le registre sont la même chose, bien faite.
- La revue de prévention peut couvrir une exigence de revue périodique : documentez-la comme telle (compte rendu formel, décisions tracées).
- Les incidents exigés d'analyse causale (root cause) : l'exercice E3 (l'incident que la génération n'aurait pas attrapé) est souvent exactement l'analyse exigée — un seul exercice, deux objectifs.
- La prévention documentée mais non traitée (le cas du risque à 400 000 $) est une non-conformité dans certains référentiels : c'est un argument réglementaire de plus pour la revue effective.

### V4 : l'organisation qui a eu son incident majeur récemment

**Contexte.** Le niveau 6 est souvent initié après un incident majeur. C'est le meilleur moment et le pire : l'énergie est là, mais la tentation de la sur-correction aussi.

**Ce qui a fonctionné :** canaliser l'énergie de l'incident vers le système (registre, revue, canal) plutôt que vers des mesures ponctuelles. L'incident est le premier cas d'école du registre : il y entre comme risque rétroactivement analysé. La question structurante : « quel système aurait évité cet incident ? » — la réponse est le plan du niveau 6.

**Ce qui n'a pas fonctionné :** la sur-correction (7 nouvelles procédures, 3 comités, une checklist de 40 points) qui a créé plus de dette que l'incident. Le système minimal (un registre relu, un canal factuel, une revue qui décide) évite plus qu'une bureaucratie complète.

### V5 : l'équipe qui croit que la prévention est du pessimisme

**Symptôme.** « On passe notre temps à imaginer des catastrophes. On n'avance plus. »

**Ce qui a fonctionné :** le ratio assumé : la prévention du niveau 6 prend 5-10 % de la capacité. C'est un coût mesurable, présenté tel quel. La question au sceptique : « quel pourcentage de ton temps as-tu perdu l'an dernier à éteindre des incendies qui auraient pu être prévus ? » La réponse (souvent 20-30 %) est le vrai chiffre à comparer au 5-10 % de la prévention. La prévention n'est pas du pessimisme : c'est de l'arbitrage, chiffré.

**Ce qui n'a pas fonctionné :** défendre la prévention par la morale (« c'est mieux de prévenir »). L'arbitrage chiffré convainc les sceptiques ; la morale les confirme.

---

## Comment utiliser cette partie

- **Au démarrage** : le registre des risques (§1.1) avec ses états assumés — un registre où tout est actif est un registre qui ment.
- **Pendant le parcours** : le cas du risque à 400 000 $ (semaine 3) est le meilleur argument de financement — à utiliser avec la honte assumée, qui le rend crédible.
- **En continu** : le compte rendu de revue (§1.3) est le modèle du battement mensuel : 45 minutes, décisions en séance, dormants traités.
