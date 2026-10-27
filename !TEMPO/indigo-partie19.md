
---

# Partie 19 : Les questions d'entretien du niveau 6

Ce jeu de questions sert à sélectionner ou évaluer un praticien TOTALISATION au niveau 6 (prévention). Chaque question porte une posture, un gabarit, ou une discipline du niveau 6 — et une réponse trahit soit la maîtrise, soit l'imitation.

## Bloc 1 : Le signal faible et l'élicitation

**Q1 — Un membre de l'équipe dit : « Je trouve que le déploiement prend plus de temps qu'avant, mais je ne sais pas si c'est vrai. » Que faites-vous ?**

Réponse de maîtrise : je note l'observation sans l'interpréter (quoi, quand, combien de fois), je demande les données (le temps de déploiement des 8 dernières semaines), et je cherche une confirmation indépendante. Si la tendance est confirmée, je déclenche l'élicitation — et je laisse le membre nommer ce qu'il a vu, pas moi.

Réponse d'imitation : je dis « oui, c'est probablement vrai » et je pose un chantier de correction tout de suite.

**Q2 — Trois personnes ont signalé la même observation. Que faites-vous ?**

Réponse de maîtrise : la règle des trois confirmations est déclenchée — j'ouvre l'élicitation proactive avec le demandeur pressenti (celui qui a vu le signal en premier, pas celui qui a le plus de légitimité). Je documente la chaîne de confirmations dans le registre.

Réponse d'imitation : j'attends que ça devienne un incident.

**Q3 — Quelle est la différence entre un signal faible et une plainte ?**

Réponse de maîtrise : le signal faible est une observation factuelle (répétée, contextualisée) — la plainte est une émotion sur un événement. Le signal faible déclenche une élicitation ; la plainte déclenche une écoute. Les deux sont légitimes, mais elles ne mènent pas au même chantier.

Réponse d'imitation : je les traite pareil — toutes les deux comme des problèmes à résoudre.

## Bloc 2 : Le chantier de prévention

**Q4 — Formulez un chantier de prévention à partir de : « le build prend 42 minutes au lieu de 28 ».**

Réponse de maîtrise : « SI rien n'est fait, ALORS le build dépasse la fenêtre d'intégration continue dans ~4 semaines (à +2 min/semaine) — ALORS chaque déploiement bloque l'équipe 20 minutes. PRÉVENTION : investiguer la régression du temps de build. PREUVE ATTENDUE : le temps retourne sous 30 minutes. PORTEUR : nommé avec 4 heures réservées. ÉCHÉANCE : 2 semaines. »

Réponse d'imitation : « le build est trop lent, on va le corriger ».

**Q5 — Qui porte un chantier de prévention ?**

Réponse de maîtrise : le porteur est celui qui a vu le signal ou qui maîtrise le domaine — jamais le praticien par défaut. Le porteur a un temps réservé (capacité préventive), pas un temps restant. Si le porteur n'a pas de temps, le chantier est une fiction.

Réponse d'imitation : le praticien porte tout — c'est plus rapide.

**Q6 — Comment mesurez-vous qu'une prévention a fonctionné ?**

Réponse de maîtrise : par la morsure — ce qui a été évité, chiffré (l'incident évité, le temps épargné, la tendance corrigée). La morsure est documentée dans la mémoire (entrée MEM-nnn) avec le chiffrage (ex. : 2 heures de correction vs 40 personnes-jours évités). Une prévention sans morsure mesurée est une dépense, pas un investissement.

Réponse d'imitation : « on a corrigé le build, ça marche mieux ».

## Bloc 3 : La mémoire et la veille

**Q7 — Que mettez-vous dans la mémoire de l'équipe ?**

Réponse de maîtrise : trois types d'entrées — les règles actives (l'apprentissage qui devient une pratique : « toute modification d'infrastructure est suivie d'une semaine de surveillance »), les cas limites (ce qui a failli arriver et comment ça a été évité), les patterns confirmés (ce qui se répète). Chaque entrée est documentée avec l'origine (le chantier), le chiffrage (la morsure), et les liens vers les entrées reliées.

Réponse d'imitation : « les décisions importantes ».

**Q8 — Comment une équipe consulte-t-elle sa mémoire ?**

Réponse de maîtrise : avant toute décision de chantier, pas après. Par thèmes (2–4 mots-clés), avec un tri explicite : applicables directement / applicables avec adaptation / inapplicables (le tri est de l'information). Ce que la consultation a révélé (le trou, le pattern nouveau) devient une nouvelle entrée.

Réponse d'imitation : la mémoire est un dépôt — on y va quand on se souvient qu'elle existe.

**Q9 — Qu'est-ce qu'une lettre de veille ?**

Réponse de maîtrise : un rituel périodique (hebdomadaire) qui compare les valeurs observées aux seuils, montre les marges (la distance au seuil), et les évolutions (la tendance). Chaque alerte est accompagnée d'une action formulée. Sans action, une alerte n'est qu'une inquiétude.

Réponse d'imitation : un dashboard qui montre les valeurs actuelles.

**Q10 — Quelle est la différence entre veille et surveillance ?**

Réponse de maîtrise : la surveillance regarde le présent (les valeurs actuelles vs les seuils). La veille regarde le futur (les tendances, les projections : « dans 4 semaines, la valeur sera X SI la tendance continue »). La surveillance détecte les dépassements ; la veille détecte les montées avant qu'elles ne deviennent des dépassements.

Réponse d'imitation : « c'est pareil — on regarde les chiffres ».

## Bloc 4 : La projection

**Q11 — Comment faites-vous une projection ?**

Réponse de maîtrise : je collecte la tendance (8 semaines de données minimum), je projette avec l'hypothèse explicite (« SI la tendance continue »), je définis la zone d'alerte, et je documente. À l'échéance, je valide rétroactivement : valeur réelle, écart, verdict (fiable / partiellement fiable / non fiable). La projection est conservée même si elle est non fiable — c'est l'hypothèse qui est testée, pas la personne.

Réponse d'imitation : je devine d'après mon expérience.

**Q12 — Une projection s'est révélée fausse. Que faites-vous ?**

Réponse de maîtrise : je documente le verdict (non fiable, avec l'écart), je cherche pourquoi (l'hypothèse était fausse ? les données étaient incomplètes ? la tendance a changé ?), et je documente ce que la projection a révélé. Une projection fausse est une information — elle a testé une hypothèse.

Réponse d'imitation : je la supprime du registre — elle ne sert plus.

## Bloc 5 : La transmission

**Q13 — Comment passez-vous du niveau 5 au niveau 6 ?**

Réponse de maîtrise : je ne change pas de contenu — je change de relation au temps. Au niveau 5, j'opère le présent (ce qui se voit, ce qui se mesure). Au niveau 6, j'opère le futur (ce qui vient, ce qui se prévient). Je passe de la réponse à l'anticipation, de l'incident au chantier de prévention, de la mesure à la veille, de l'individu à l'équipe.

Réponse d'imitation : « j'ajoute les gabarits de prévention à ma boîte à outils ».

**Q14 — Comment transmettez-vous le niveau 6 à un nouveau praticien ?**

Réponse de maîtrise : je ne le décris pas — je le fais vivre. Le nouveau praticien écoute les signaux (semaine 1), les trie (semaine 2), pose son premier chantier (semaine 3), consulte sa mémoire (semaine 4). Je ne fais jamais à sa place — je l'accompagne. Le niveau 6 se transmet par la pratique, pas par la documentation.

Réponse d'imitation : « je lui donne le manuel de terrain ».

## Comment lire les réponses

Les réponses de maîtrise partagent trois traits : elles sont **chiffrées** (la morsure, le délai, la marge), elles sont **documentées** (le registre, la mémoire, la lettre), et elles **appartiennent à l'équipe** (le porteur, l'expression, la pratique). Les réponses d'imitation partagent les trois traits inverses : elles sont floues, elles sont orales, et elles appartiennent au praticien.

---

*Fin des questions d'entretien du niveau 6.*
