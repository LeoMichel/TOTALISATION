
---

# Partie 6 : Le vécu du niveau 4 : les histoires qui ont fait le VERT

Le VERT est le niveau de la mesure — et la mesure n'est pas un instrument neutre : elle révèle, déplace, et parfois détruit. Les quatre histoires de cette partie sont celles d'équipes qui ont appris que le passage du JAUNE (la cadence) au VERT (la mesure) est le plus traître des passages : tout ce qui était invisible devient visible, et tout ce qui devient visible demande une réponse.

## 1. L'histoire de K.L. : le tableau qui a tué la confiance

K.L. était le praticien VERT d'une équipe de support de niveau 2 dans une entreprise de services financiers. Son équipe avait une cadence solide (les rituels tenaient), et il a introduit le premier tableau de mesure VERT : les délais de traitement par type de demande, mis à jour en temps réel, visible de tous.

La première semaine, le tableau a fait ce qu'on attendait : les délais ont été vus, les goulets ont été identifiés, la conversation a commencé. La deuxième semaine, le tableau a fait ce qu'on craignait : les gens ont commencé à optimiser pour le tableau. Les demandes complexes ont été classées « simples » (pour préserver leur délai affiché), les demandes longues ont été découpées artificiellement (pour faire apparaître des traitements rapides), et le délai médian a chuté de 30 % — sans qu'aucun traitement réel ne soit plus rapide.

K.L. a découvert le piège le plus classique de la mesure : **quand une mesure devient une cible, elle cesse de mesurer** (la loi de Goodhart). Son tableau était beau, précis, et mensonger.

**La correction :** K.L. a remplacé son tableau unique (avec cible affichée) par trois mesures sans cible affichée (délai médian, taux de re-classification, satisfaction des demandeurs), avec la règle : les mesures sont discutées au rituel, jamais affichées en continu. L'affichage continu crée la pression ; la discussion cadencée crée la conversation. Et il a ajouté la mesure-miroir : le taux de re-classification, qui révèle exactement le comportement de contournement — quand les demandes complexes sont reclassées « simples » pour préserver un délai, ce taux monte, et la triche devient visible.

**La leçon :** la mesure du VERT n'est pas affichée — elle est discutée. Le tableau de bord du praticien VERT est un support de rituel, pas un affichage de couloir.

## 2. L'histoire de l'équipe qui a mesuré les mauvaises choses

Une équipe de développement (8 personnes) au niveau 3 solide a passé son trimestre VERT à mesurer : les lignes de code produites, le nombre de commits, le taux d'utilisation des développeurs, la vélocité par personne. Les quatre mesures ont été choisies en une réunion de 30 minutes, parce qu'elles étaient faciles à extraire des outils.

Le trimestre suivant, les quatre mesures ont toutes progressé : plus de lignes, plus de commits, plus d'utilisation, plus de vélocité individuelle. Et la qualité a chuté : plus de bugs, plus de reprises, plus de frictions en intégration. Le praticien VERT a découvert que son équipe avait optimisé exactement ce qu'on lui avait demandé — et que ce qu'on lui avait demandé ne mesurait pas la valeur, mais l'activité.

**La correction :** l'équipe a remplacé les quatre mesures d'activité par quatre mesures de résultat : le délai de traitement des demandes (du reçu au livré), le taux de retour (demandes rouvertes ou réassignées), la stabilité post-livraison (incidents par livraison), et la disponibilité de la prochaine capacité (le pourcentage de semaines où l'équipe a de la capacité pour les demandes entrantes). Les mesures d'activité ont été supprimées — pas gardées « pour information » : supprimées, parce qu'elles créent le comportement qu'elles mesurent.

**La leçon :** le praticien VERT mesure des résultats (délai, retour, stabilité, disponibilité), pas des activités (lignes, commits, utilisation, vélocité individuelle). L'activité est le symptôme ; le résultat est la santé.

## 3. L'histoire de S.B. : la mesure qui a réconcilié deux équipes

S.B. était le praticien VERT d'une équipe, et son voisin immédiat (une autre équipe, qui livrait les demandes que la sienne recevait) était en conflit ouvert avec elle : « ils livrent n'importe quoi », « ils demandent n'importe quoi ». Les réunions inter-équipes tournaient au procès : chaque partie avait ses anecdotes, ses preuves, sa liste de griefs.

S.B. a proposé la mesure réconciliante : pendant un mois, les deux équipes ont noté ensemble, pour chaque demande passée d'une équipe à l'autre, trois données : le délai total (réception à livraison), le nombre d'allers-retours (combien de fois la demande est revenue pour clarification), et le verdict final (accepté tel quel, modifié, rejeté). Pas un tableau de bord : une liste, tenue ensemble, revue ensemble à la fin du mois.

Le résultat a surpris les deux équipes : 70 % des demandes passaient en un aller-retour maximum, le délai médian était de 4 jours, et les rejets étaient concentrés sur 3 types de demandes (les mêmes, toujours). Le conflit « ils/nous » est devenu une conversation « ces trois types de demandes » — et les trois types ont été retravaillés ensemble (leurs gabarits de demande ont été corrigés), ce qui a fait passer les rejets de 30 % à 8 %.

**La leçon :** la mesure du VERT n'est pas là pour attribuer — elle est là pour objectiver. Deux équipes en conflit ont chacune leurs anecdotes ; deux équipes qui mesurent ensemble ont des données communes. La mesure est un instrument de paix quand elle est tenue ensemble, et une arme quand elle est tenue contre.

## 4. L'histoire de l'équipe qui a renoncé à mesurer (et pourquoi c'était la bonne décision)

Une équipe de maintenance (5 personnes, support applicatif legacy) au niveau 3 a tenté le passage au VERT. Le praticien a déployé les mesures standard (délai, retour, stabilité, disponibilité). Le résultat a été inhabituel : les mesures étaient stables, les conversations étaient stériles, et l'équipe s'est ennuyée.

Le diagnostic du praticien : l'équipe ne produisait pas de demandes — elle gérait des incidents récurrents sur un système en fin de vie, avec un cycle court et prévisible. Les mesures VERT (conçues pour des flux de demandes) ne mesuraient rien d'intéressant ici : le délai était constant (le même chaque semaine), le retour était nul (les incidents ne revenaient pas), la stabilité était inchangée (le système ne pouvait pas être plus stable).

**La décision du praticien :** renoncer au VERT — et l'assumer. L'équipe est restée au niveau 3, avec une mesure unique (le nombre d'incidents récurrents, la seule chose qui pouvait régresser) et un rituel de maintenance. Le praticien a documenté le renoncement : « le VERT mesure des flux de transformation ; notre flux n'est pas transformable (le système legacy est en fin de vie, le coût d'une amélioration dépasse son bénéfice). Les mesures seraient stables par construction — les tenir serait du théâtre. »

**La leçon :** le praticien VERT sait quand ne pas mesurer. La mesure est un investissement (collecte, revue, correction) — et elle n'est justifiée que si quelque chose peut régresser et être corrigé. Une équipe dont tout est stable et inchangeable n'a pas besoin de mesures : elle a besoin de paix. Le renoncement argumenté est une décision de praticien, pas un échec.

## 5. La synthèse des quatre histoires

| Histoire | Piège du VERT | Correction |
|---|---|---|
| K.L. | La mesure devenue cible (Goodhart) | Mesures sans cible affichée, discutées au rituel, mesure-miroir |
| L'équipe de dev | Mesurer l'activité au lieu du résultat | Quatre mesures de résultat, activités supprimées |
| S.B. | La mesure tenue contre l'autre équipe | La mesure tenue ensemble (liste commune, revue commune) |
| L'équipe legacy | Mesurer ce qui ne peut pas changer | Le renoncement argumenté, documenté |

Le praticien VERT apprend de ces quatre histoires que la mesure est un acte social autant que technique : elle crée des comportements (K.L.), des orientations (l'équipe de dev), des paix ou des guerres (S.B.), et parfois des évidences de renoncement (l'équipe legacy). La mesure n'est jamais neutre — et le praticien qui l'ignore produit de la triche, de l'activité, du conflit ou du théâtre.
