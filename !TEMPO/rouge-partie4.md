
---

# Partie 4 : Formation, exercices et évaluation (niveau 1)

Les huit semaines du ROUGE construisent l'implémentation minimale. Cette partie la rend transmissible : former de nouveaux membres, exercer les gestes de base, évaluer honnêtement ce qui est acquis. Au niveau 1, la transmission n'est pas encore une priorité stratégique — mais elle est déjà un garde-fou : une équipe qui ne peut pas expliquer ce qu'elle fait ne comprend pas ce qu'elle fait.

## Le principe du niveau 1 : former par le geste, évaluer par la preuve

La formation du niveau 1 est minimale par design : trois modules courts, six exercices, deux grilles. L'équipe est en train d'apprendre elle-même ; la formation sert surtout à intégrer un nouveau membre sans casser le rythme des huit semaines, et à vérifier que les fondations sont comprises, pas seulement pratiquées.

La règle du niveau 1 : **on n'explique jamais un geste sans le faire faire, et on n'évalue jamais un acquis sans demander la preuve.**

---

## Modules de formation niveau 1

### Module F1 : Écrire une spécification avant le code

**Durée :** 90 minutes. **Public :** tout nouveau membre de l'équipe pilote.

**Objectif :** à la fin de la session, le participant a écrit une spécification pour une demande réelle, avant que le code existe, et elle a survécu à la revue.

**Matériel :** une demande réelle du backlog (petite mais significative), le gabarit de spécification de l'équipe, la spécification exemplaire de la semaine 2.

**Déroulé :**

| Temps | Séquence | Contenu |
|---|---|---|
| 0-15 min | Pourquoi avant le code | Le geste qui définit le niveau 1 : comprendre avant de construire. Le coût réel du malentendu : une heure de clarification évite une journée de reprise. Le participant raconte son propre pire malentendu — tout le monde en a un. |
| 15-45 min | Écriture guidée | Le participant écrit la spécification de la demande réelle avec le gabarit : contexte, besoin, comportement attendu, règles de validation, cas limites. Le mentor est disponible mais n'écrit pas. |
| 45-70 min | La revue à trois rôles | Le groupe joue les trois rôles de la revue (l'utilisateur pressé, l'intégrateur qui cherche la faille, l'exploitant qui devra maintenir). Chaque rôle attaque la spécification. Les trous trouvés sont corrigés immédiatement. |
| 70-85 min | Le lien au code | Le participant (ou un développeur) commence l'implémentation avec la spécification ouverte à côté. Première divergence constatée : soit la spécification était floue (on la corrige, on la re-versionne), soit le code dévie (on corrige le code). |
| 85-90 min | Critère de réussite | Le participant écrit seul une spécification complète pour sa prochaine demande, sans mentor. |

**Critère de réussite :** la prochaine spécification du participant est écrite avant le code, revue, et tenue.

**Piège classique :** la spécification encyclopédique (« on ne sait jamais, écrivons tout »). Corriger : une spécification de deux pages qui prévient le malentendu vaut mieux qu'un mémoire de vingt pages que personne ne lit. Le test : le développeur la lit-il avant de coder ?

### Module F2 : Tenir son premier point de qualité

**Durée :** 60 minutes. **Public :** tout nouveau membre, en particulier le futur responsable du point de qualité.

**Objectif :** le participant sait lire la métrique de l'équipe, la présenter en une minute, et proposer une décision.

**Matériel :** la métrique de l'équipe avec deux semaines de données, le compte rendu du dernier point de qualité.

**Déroulé :**

| Temps | Séquence | Contenu |
|---|---|---|
| 0-10 min | La métrique et son histoire | Pourquoi cette métrique a été choisie (semaine 1), ce qu'elle raconte, ce qu'elle ne raconte pas. Une métrique qui ne raconte rien est changée — c'est prévu. |
| 10-25 min | Lecture guidée | Le participant lit la métrique à voix haute : valeur, tendance, surprise éventuelle. Le groupe réagit : qu'est-ce que ça nous dit ? |
| 25-45 min | Simulation du point | Le participant anime un point de qualité simulé en cinq minutes : la métrique, ce qu'elle suggère, la décision proposée. Le groupe joue l'équipe, avec ses vraies objections (« on n'a pas le temps », « c'est la faute des autres »). |
| 45-55 min | Le point réel | Le participant anime le point de qualité réel de la semaine (le mentor observe). |
| 55-60 min | Critère de réussite | Le participant peut animer le prochain point sans préparation particulière. |

**Critère de réussite :** le prochain point de qualité est animé par le nouveau membre, avec une décision notée.

**Piège classique :** le nouveau membre qui présente la métrique comme un devoir (« voici le chiffre ») sans la commenter. Corriger : la règle du point — chaque métrique présentée est suivie d'une phrase qui commence par « et donc... ».

### Module F3 : Participer à un Go/No-Go

**Durée :** 60 minutes. **Public :** tout nouveau membre.

**Objectif :** le participant connaît les critères de Go, sait où trouver les preuves, et ose exprimer un doute.

**Matériel :** la grille de Go/No-Go de l'équipe, le compte rendu du dernier Go/No-Go réel.

**Déroulé :**

| Temps | Séquence | Contenu |
|---|---|---|
| 0-15 min | Les critères et leur histoire | Chaque critère est relu avec l'incident (ou le presque-incident) qui l'a fait naître. Un critère sans histoire est un critère décoratif — le vérifier et le retirer s'il ne sert à rien. |
| 15-35 min | Le Go/No-Go rejoué | Le dernier Go/No-Go réel est rejoué : le participant joue le décideur, le groupe joue l'équipe. Le participant doit demander les preuves lui-même, sans qu'on les lui tende. |
| 35-50 min | Le droit au doute | Exercice clé : chacun raconte une fois où il a eu un doute sur une livraison et ne l'a pas exprimé. Pourquoi ? (Souvent : crainte de déplaire, sentiment de ne pas être légitime.) La règle est posée : au Go/No-Go, un doute exprimé est un service rendu, jamais une faute. |
| 50-60 min | Critère de réussite | Le participant participe au prochain Go/No-Go réel et pose au moins une question de preuve. |

**Critère de réussite :** le participant pose une question de preuve au prochain Go/No-Go, et la question est traitée comme légitime.

**Piège classique :** le nouveau membre qui « ne veut pas déranger ». Corriger : le droit au doute est exercé dès la première session, sinon il ne le sera jamais. Un Go/No-Go où le nouveau membre reste silencieux trois fois de suite est un échec d'intégration.

---

## Exercices d'approfondissement

### Exercice E1 : Le malentendu chiffré

**Durée :** 45 minutes. **Prérequis :** une spécification récente et le code correspondant.

**Consigne :** comparez la spécification et le code livré : trouvez trois différences de comportement (même mineures). Pour chaque différence, déterminez : la spécification était-elle floue, ou le code a-t-il dévié ?

**Grille de correction :** spécification floue → corriger la spécification et noter le mot ou la phrase responsable (c'est un mot dangereux à bannir). Code dévié → l'écart devient un cas de test pour la prochaine fois. Trois différences analysées : exercice réussi.

**Ce que l'exercice révèle :** le malentendu n'est presque jamais un problème de compétence : c'est un problème de mot flou ou de contexte non écrit. Chaque analyse produit du vocabulaire commun.

### Exercice E2 : La métrique du vendredi

**Durée :** 30 minutes par semaine, pendant quatre semaines. **Prérequis :** la métrique de l'équipe en collecte.

**Consigne :** chaque vendredi, avant le point de qualité, écrivez votre prédiction de la valeur de la métrique. Puis comparez avec la valeur réelle. Après quatre semaines : calculez votre taux de réussite et examinez vos erreurs systématiques (toujours trop optimiste ? toujours sur la mauvaise tendance ?).

**Grille de correction :** taux de prédiction > 60 % : l'équipe connaît réellement son système. < 40 % : la métrique raconte quelque chose que l'équipe ne voit pas — c'est excellent, c'est exactement pour ça qu'elle existe. Les erreurs systématiques sont discutées au point de qualité.

**Ce que l'exercice révèle :** la distance entre ce qu'on croit et ce qu'on mesure. Une équipe qui prédit bien sa métrique a intériorisé son système ; une équipe qui se trompe toujours dans le même sens a un biais collectif à nommer.

### Exercice E3 : Le Go/No-Go à l'envers

**Durée :** 45 minutes en groupe. **Prérequis :** un No-Go récent (ou un Go qui a mal tourné).

**Consigne :** prenez un No-Go réel (ou un Go suivi d'un incident) et rejouez-le à l'envers : supposons que la décision ait été l'inverse. Écrivez ce qui se serait passé, avec autant de précision que possible. Comparez avec ce qui s'est réellement passé.

**Grille de correction :** l'exercice produit deux leçons : (1) les critères qui ont fait la différence sont-ils bien dans la grille ? (2) le coût réel de la décision alternative est-il chiffrable ? Si l'alternative aurait été moins coûteuse, la grille doit être ajustée honnêtement — un No-Go systématique est aussi un problème qu'un Go systématique.

**Ce que l'exercice révèle :** les décisions se jugent au moment où elles sont prises avec les informations disponibles — pas après coup. L'exercice distingue la mauvaise décision (mal prise) de la décision malheureuse (bien prise, mal tournée). La première se corrige par la grille, la seconde par le hasard — et il ne faut pas les confondre.

### Exercice E4 : Le lexique vivant

**Durée :** 30 minutes par semaine, pendant quatre semaines. **Prérequis :** le lexique officiel v0.1.

**Consigne :** chaque semaine, ajoutez au lexique un terme que vous avez vu mal compris cette semaine. La règle : le terme doit avoir causé une confusion réelle (une question, une reprise, un débat). Pas de terme théorique ajouté « au cas où ».

**Grille de correction :** quatre termes ajoutés en quatre semaines avec leurs histoires : le lexique est vivant. Zéro terme : soit l'équipe n'a plus de malentendus (suspect), soit personne ne regarde le lexique (probable). Le lexique est relu au point de qualité de fin de mois.

**Ce que l'exercice révèle :** le lexique n'est pas un projet documentaire, c'est un registre des malentendus résolus. Sa croissance est le pouls du vocabulaire commun.

### Exercice E5 : Le journal des blocages

**Durée :** 10 minutes par jour, pendant une semaine. **Prérequis :** rien.

**Consigne :** pendant une semaine, notez chaque blocage : ce qui vous a fait perdre du temps ou du moral. La règle : on note le système (« l'environnement de test est en panne »), jamais la personne (« untel a cassé l'environnement »). À la fin de la semaine, classez : ce qui dépend de l'équipe, ce qui dépend de l'organisation.

**Grille de correction :** les blocages dépendant de l'organisation sont remontés au sponsor avec preuve et impact (format de la semaine 5). Les blocages dépendant de l'équipe deviennent des items de rétrospective. Zéro blocage noté : la semaine était parfaite (suspect) ou le journal n'a pas été tenu (probable).

**Ce que l'exercice révèle :** le journal des blocages est l'entraînement du diagnostic de la semaine 5. Une équipe qui a le réflexe du journal arrive au point mort avec des preuves déjàcollectées.

### Exercice E6 : Le bilan des huit semaines en une page

**Durée :** 60 minutes. **Prérequis :** les checklists des huit semaines.

**Consigne :** écrivez le bilan des huit semaines en une page maximum, en répondant à trois questions : qu'est-ce qui a changé dans ma façon de travailler ? qu'est-ce qui a résisté ? qu'est-ce que je recommande à l'équipe qui commence ? La page est signée et partagée.

**Grille de correction :** la page est honnête si elle contient au moins un élément négatif. Un bilan tout positif n'a pas été écrit par quelqu'un qui a traversé la semaine 5. Les pages sont conservées dans le centre d'excellence — elles serviront à la prochaine équipe pilote.

**Ce que l'exercice révèle :** le bilan personnel vaut plus que le bilan collectif pour la transmission : c'est le seul qui raconte l'expérience vécue plutôt que le résultat obtenu.

---

## Les grilles d'évaluation du niveau 1

### Grille de maturité de l'équipe pilote (fin de semaine 8, puis trimestrielle)

| Élément | Absent | Fragile | Acquis | Preuve requise |
|---|---|---|---|---|
| Spécification avant le code | Jamais | Parfois, sans revue | Systématique, avec revue | Une demande codée après clarification |
| Métrique de qualité | Non collectée | Collectée, non regardée | Regardée et commentée | Point de qualité tenu avec décision |
| Go/No-Go | Absent | Théâtral (toujours Go) | Critères réels, décisions honnêtes | Un No-Go documenté ou un Go avec réserves |
| Lexique | Absent | Créé, jamais consulté | Consulté spontanément | Une consultation spontanée observée |
| Centre d'excellence | Vide | Créé, jamais alimenté | Alimenté chaque semaine | Artefacts datés des huit semaines |
| Blocages | Subis en silence | Mentionnés sans preuve | Remontés avec preuve et impact | Une remontée au sponsor avec réponse |
| Rôles | Flous | Nominaux | Tenus (chargé de livraison actif) | Un rituel animé sans le coach |

**Règle de remplissage :** la colonne « preuve requise » n'est pas décorative : un « acquis » sans preuve est un « fragile » déguisé.

### Le test des trois questions de fin de niveau 1

À la fin des huit semaines, chaque membre répond par écrit (publié au centre d'excellence) :

1. **Quel geste de TOTALISATION ai-je adopté naturellement, sans qu'on me le demande ?** (Le geste spontané est le seul acquis réel.)
2. **Qu'est-ce qui a le plus résisté chez moi, et qu'est-ce que je vais en faire ?** (La résistance nommée est le début de l'adhésion.)
3. **Qu'est-ce que je dirais à quelqu'un qui commence les huit semaines la semaine prochaine ?** (Le conseil honnête est la première forme de transmission.)

Ces trois réponses sont le certificat de sortie du niveau 1 : ce qui est acquis, ce qui résiste, ce qui se transmet.

---

## Le bilan de la partie formation du niveau 1

Le niveau 1 réussit quand une phrase est vraie : **l'équipe fait les gestes sans qu'on le lui rappelle.** La spécification avant le code, la métrique regardée le vendredi, le doute exprimé au Go/No-Go, le lexique consulté spontanément.

Si la phrase n'est pas encore vraie, ce n'est pas un échec : c'est le calendrier normal. Les gestes deviennent naturels des semaines après avoir été appris. Le niveau 2 (ORANGE) donnera à ces gestes leurs outils définitifs ; ce que le niveau 1 demande, c'est seulement qu'ils existent — imparfaits, tenus, à vous.
