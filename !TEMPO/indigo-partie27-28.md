
---

# Partie 27 : Le guide du nouveau praticien du niveau 6

Le praticien du niveau 6 n'arrive pas de nulle part : il arrive du niveau 5 (BLEU), où il a appris à synchroniser, à documenter, à transmettre. Mais le niveau 6 est un changement de posture : il ne s'agit plus de synchroniser ce qui existe, mais d'anticiper ce qui n'existe pas encore. Ce guide est destiné au praticien qui commence son niveau 6 — il lui donne la carte du territoire, les premiers pas, et les pièges.

## Les trois changements de posture

**Changement 1 — De la synchronisation à l'anticipation.**
Au niveau 5, vous répondiez à la question : *est-ce que l'équipe et le client voient la même chose ?* Au niveau 6, vous répondez à une question différente : *est-ce que l'équipe voit ce qui va arriver avant que cela n'arrive ?* Le niveau 5 regarde le présent. Le niveau 6 regarde l'avenir. Ce n'est pas une différence de technique : c'est une différence d'horizon.

**Changement 2 — De la réactivité à la prévention.**
Au niveau 5, vous réagissiez aux signaux (une divergence, un décalage, une attente). Au niveau 6, vous prévenez les incidents avant qu'ils ne se produisent. Le niveau 5 répare la communication. Le niveau 6 empêche la panne. Ce n'est pas une différence d'outils : c'est une différence d'intention.

**Changement 3 — De l'équipe à l'organisation.**
Au niveau 5, votre unité de travail était l'équipe. Au niveau 6, votre unité de travail est l'organisation : les chantiers de prévention touchent le build, les dépendances, les documents, les fournisseurs — des éléments qui dépassent l'équipe. Ce n'est pas une différence de périmètre : c'est une différence de responsabilité.

## Les premiers pas (les 4 premières semaines)

**Semaine 1 — Observer sans agir.**
Votre première semaine au niveau 6 ne produit rien : elle observe. Notez chaque signal faible que vous croisez — une remarque en passant, une lenteur qui s'installe, une documentation qui traîne, une réunion qui dérive. Ne classifiez pas encore : collectez. À la fin de la semaine, vous aurez 10 à 20 signaux bruts.

**Semaine 2 — Classer les signaux.**
Reprenez vos signaux et classez-les selon la grille du niveau 6 : signal technique (le build monte), signal humain (une personne évite un sujet), signal organisationnel (une dépendance se crispe), signal documentaire (une doc diverge). Chaque signal reçoit une note de gravité (1 à 5) et une note de confiance (1 à 5). Les signaux qui dépassent gravité 3 ET confiance 3 sont vos candidats-chantiers.

**Semaine 3 — Poser votre premier chantier.**
Choisissez UN candidat — le plus simple, le plus local, le plus rapide à confirmer. Écrivez le chantier avec le gabarit standard : signal, hypothèse, coût si rien n'est fait, coût de la prévention, action proposée, porteur. Ne cherchez pas le chantier parfait : cherchez le chantier livrable en une semaine.

**Semaine 4 — Livrer et documenter.**
Livrez le chantier (l'action préventive), documentez-le dans la mémoire organisationnelle, et écrivez votre première lettre de veille. À la fin de la semaine 4, vous avez bouclé le cycle complet : signal → chantier → prévention → mémoire → veille. Ce cycle, répété, devient votre pratique.

## Les trois pièges du débutant

**Piège 1 — Vouloir tout prévenir.**
Le débutant voit 20 signaux et veut poser 20 chantiers. Erreur : la capacité préventive est de 10 % — soit environ un demi-jour par semaine. Un chantier par cycle de deux semaines, c'est déjà ambitieux. La discipline du niveau 6 est de choisir, pas de tout faire.

**Piège 2 — Prévenir seul.**
Le débutant pose les chantiers, les porte, les livre — seul. Erreur : un praticien seul est un point de défaillance. Dès le premier chantier, cherchez un binôme. Dès le troisième, formez un relève. La prévention qui dépend d'une seule personne n'est pas de la prévention : c'est un report de risque.

**Piège 3 — Confondre prévention et perfectionnisme.**
Le débutant confond « prévenir » et « tout nettoyer ». Erreur : la prévention cible les incidents à fort coût évitable, pas les imperfections esthétiques. Un refactoring cosmétique n'est pas un chantier de prévention. Un test qui empêche une régression de données en production, si.

## La première auto-évaluation

À la fin de votre premier mois, évaluez-vous honnêtement :

| Capacité | Question | Oui / Non |
|---|---|---|
| Observation | Ai-je collecté des signaux chaque semaine ? | |
| Classification | Mes signaux sont-ils classés et notés ? | |
| Chantier | Ai-je posé au moins un chantier documenté ? | |
| Livraison | Ai-je livré au moins une prévention ? | |
| Mémoire | Mes apprentissages sont-ils dans la mémoire ? | |
| Veille | Ai-je écrit ma première lettre de veille ? | |
| Binôme | Ai-je un binôme ou un relève en vue ? | |

Si 5 réponses sur 7 sont « oui », vous êtes en route. Si moins de 5, ralentissez : reprenez les semaines 1 à 3 — la base doit être solide avant de monter en cadence.

## Le mot du guide

Le niveau 6 n'est pas un niveau de plus : c'est un changement de métier. Vous passiez pour celui qui synchronise ; vous devenez celui qui anticipe. Cette transition prend un mois — et se confirme en un an. Soyez patient avec vous-même, exigeant avec votre méthode, et généreux avec vos binômes.

Le niveau 6 vous attend. Commencez par observer.

---

# Partie 28 : La FAQ du niveau 6 — les questions de la direction

La direction pose des questions différentes de celles de l'équipe. Voici les huit questions que les directions posent le plus souvent au praticien du niveau 6 — et les réponses qui tiennent en une réunion de quinze minutes.

**Q1 — « Combien coûte la prévention ? »**
Réponse : 10 % de la capacité de l'équipe, soit environ un demi-jour par semaine et par personne. Sur une année, cela représente six semaines-personnes pour une équipe de dix. En regard : notre bilan de l'année montre 55 jours-personnes d'incidents évités pour 9 heures investies. Le ROI observé est de 60:1 — et les deux incidents survenus cette année (6 jours de dommage) étaient tous deux des chantiers abandonnés ou jamais posés.

**Q2 — « Que se passe-t-il si l'équipe est en crisis et que nous devons prendre les 10 % ? »**
Réponse : la règle de capacité préventive prévoit une clause de suspension — en cas de crise, la capacité préventive peut être réaffectée, mais pour une durée maximale de deux semaines, avec un retour obligatoire et un chantier de rattrapage. Au-delà, la dette de prévention s'accumule comme une dette technique : elle se paiera avec intérêts.

**Q3 — « Comment mesurez-vous ce que vous évitez ? »**
Réponse : par le contrepoint. Chaque chantier documente le coût estimé de l'incident évité (en jours-personnes) et le coût de la prévention (en heures). Le registre des chantiers tient le compte. Ce n'est pas une mesure exacte — c'est une estimation conservatrice, revue rétroactivement au bilan annuel. Nos estimations sont systématiquement prudentes : nous comptons les incidents évités à leur coût minimum.

**Q4 — « Que se passe-t-il quand vous vous trompez ? »**
Réponse : deux cas. Un chantier posé sur un signal qui ne se confirme pas : le coût est le temps investi (généralement 2 à 8 heures), et l'apprentissage est documenté dans la mémoire — les faux positifs affinent la grille de classification. Un incident qui survient malgré un chantier : c'est un échec de prévention, analysé comme un incident de plus — le bilan annuel le documente, et la mémoire en tire une règle.

**Q5 — « Qui porte la prévention quand le praticien part ? »**
Réponse : d'abord le binôme (chaque chantier a un porteur et un binôme), ensuite la relève formée (le praticien du niveau 6 forme au moins un successeur par an), enfin la mémoire organisationnelle (50+ entrées documentées : les règles survivent aux personnes). Notre test de solidité est le congé de deux semaines : si les rituels tiennent sans le praticien, la prévention est organisationnelle, pas personnelle.

**Q6 — « La prévention ne ralentit-elle pas la livraison ? »**
Réponse : elle la sécurise. Nos métriques de livraison sur l'année : aucune panne de build majeure, aucune régression de données, deux incidents mineurs (6 jours au total). Comparez avec l'année précédant le niveau 6 : quatre pannes majeures, deux régressions, 55 jours de debug et de reprise. La prévention ne ralentit pas la livraison — elle supprime les arrêts.

**Q7 — « Quelle est la différence avec la gestion des risques classique ? »**
Réponse : trois différences. La gestion des risques identifie les risques connus ; le niveau 6 observe les signaux faibles, y compris ceux qu'aucun registre ne prévoyait. La gestion des risques produit des matrices ; le niveau 6 pose des chantiers livrés par l'équipe. La gestion des risques est un exercice annuel ; le niveau 6 est une pratique hebdomadaire. Les deux approches se complètent — mais seule la seconde est vivante.

**Q8 — « Quand saurons-nous que nous n'en avons plus besoin ? »**
Réponse : jamais — et c'est le signe que cela fonctionne. Une organisation qui n'a plus besoin de prévention est une organisation qui ne voit plus ce qui monte. L'objectif n'est pas d'arrêter la prévention : c'est de la rendre si naturelle qu'elle ne se voit plus. Quand vos équipes préviennent sans y penser, vous avez réussi — pas terminé.

---

*Fin de la FAQ direction. Ces huit réponses tiennent sur une page — gardez-les à portée de main pour votre prochaine revue de direction.*
