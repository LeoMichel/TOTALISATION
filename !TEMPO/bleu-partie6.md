
---

# Partie 6 : Le vécu étendu du niveau 5 — les histoires de la gouvernance inter-équipes

Le niveau 5 gouverne l'échelle. Les histoires qui suivent racontent ce que la gouvernance inter-équipes coûte et rapporte — avec les échecs qui ont forgé ses règles.

## 1. L'histoire du comité qui est devenu un organe de pouvoir

Une organisation de 12 équipes au niveau 4 a créé son comité qualité avec enthousiasme. Trois mois plus tard, le comité avait 20 membres (un représentant par équipe + les managers + les architectes + les sponsors), traitait 30 sujets par réunion, et prenait des décisions que les équipes contournaient systématiquement — parce qu'elles étaient prises trop loin du terrain.

Le praticien du niveau 5 (le président du comité) a fait le diagnostic : le comité était devenu un organe de pouvoir par accumulation. Chaque sujet traité hors périmètre augmentait son empire apparent et diminuait sa légitimité réelle. Les équipes qui contournent ne sont pas rebelles : elles constatent que le comité décide sans connaître — et elles ont raison.

**La correction :** la charte a été réécrite avec la section « ne décide pas » (déjà dans le livre), le nombre de membres est revenu à 8 (un représentant actif par équipe — pas les managers), et la règle de quorum a été durcie : 4 représentants actifs minimum, un manager ne peut pas représenter une équipe sans y travailler. Six mois plus tard : 5 sujets par réunion, des décisions appliquées, et les équipes viennent chercher le comité au lieu de le contourner.

**La leçon :** le comité de gouvernance se juge par la fidélité d'application de ses décisions, pas par leur nombre. Un comité dont les décisions sont contournées est un organe décoratif qui consomme la crédibilité du système tout entier — et chaque décision hors périmètre achète cette décrédibilisation.

## 2. L'histoire du registre qui a sauvé deux équipes d'un conflit de trois ans

Deux équipes (une équipe produit et une équipe plateforme) étaient en conflit ouvert sur les délais d'intégration depuis presque trois ans : chacune avait ses exemples, ses dates, ses historiques de courriels — et aucune n'acceptait les données de l'autre. Les réunions de résolution tournaient en rond : chaque partie recomptait ses faits.

Le praticien du niveau 5 a proposé la seule chose qu'aucune des deux ne pouvait contester : un registre commun, tenu à chaque passage de demande, avec trois données simples (date de réception, date de livraison acceptée, nombre d'allers-retours). Pas une mesure de performance — un journal partagé. Les deux équipes y ont inscrit leurs passages pendant deux mois, avec l'accord préalable : les données ne serviraient pas d'évaluation, seulement de conversation.

Le résultat a transformé le conflit : les données ont montré que 80 % des allers-retours venaient de demandes avec des prérequis manquants (le gabarit de demande était incomplet), et que le délai médian était de 6 jours — dont 4 d'attente de clarification. Le conflit « ils sont lents » / « ils demandent mal » est devenu un chantier commun : le gabarit de demande a été réécrit ensemble, et les allers-retours ont chuté de 60 %.

**La leçon :** le registre de gouvernance n'est pas un instrument de jugement — c'est un instrument d'objectivation. Deux équipes en conflit ont chacune leurs anecdotes ; deux équipes qui tiennent un registre ensemble ont des faits communs. Et la règle préalable (les données ne servent pas d'évaluation) est ce qui a permis la coopération : une registre tenu pour évaluer sera rempli de maquillage.

## 3. L'histoire du seuil qui a divisé l'organisation

Une organisation de 6 équipes au niveau 4 a voulu standardiser le seuil de couverture de tests à 80 % pour toutes. Trois équipes étaient déjà à 75-85 % (le seuil était raisonnable) ; une équipe de maintenance legacy était à 45 % (impossible d'atteindre 80 % sans réécrire des modules) ; deux équipes de nouvelles fonctionnalités étaient à 90 %+ (le seuil était déjà dépassé).

Le débat a duré six semaines. Les équipes hautes défendaient le 80 % (« c'est le standard »), l'équipe legacy défendait son exemption (« notre code ne peut pas être testé à ce niveau sans refonte »), et les managers cherchaient un compromis (70 % ?) qui ne satisfaisait personne.

**La résolution du niveau 5 :** le comité a distingué le seuil par contexte, avec une règle de transition : le seuil standard de 80 % pour les nouvelles fonctionnalités (toutes les équipes, dès la prochaine fonctionnalité), un seuil de maintenance de 60 % pour le code legacy existant (sans régression du niveau actuel), et un plan de migration par équipe (le seuil de chaque équipe monte de 5 points par trimestre, avec les moyens associés). Le plan a été accepté par toutes les équipes — parce qu'il reconnaissait les contextes réels tout en fixant une direction commune.

**La leçon :** un seuil d'organisation n'est pas un nombre unique — c'est un système (standard / contexte / transition). Un seuil unique sur des contextes hétérogènes produit soit du maquillage (les équipes trichent), soit de la révolte (les équipes refusent), soit du théâtre (les seuils ne sont pas vérifiés). Le système à trois niveaux est plus complexe à décrire et beaucoup plus simple à tenir.

## 4. L'histoire de l'escalade qui n'a jamais eu lieu (et qui aurait dû)

Une équipe (l'équipe B) contournait systématiquement les règles de tri des tests générés : les tests étaient produits, mais jamais triés — et le pipeline de l'organisation s'alourdissait de tests vides. Le praticien du niveau 5 avait envoyé deux lettres de veille, sans réponse. Le comité avait discuté du cas trois fois. Mais l'équipe B était dirigée par un manager influent, et personne ne voulait l'escalade formelle.

Trois mois plus tard, le coût était là : le pipeline de l'organisation avait doublé de temps, trois équipes avaient rejeté la gouvernance (« pourquoi nous, et pas l'équipe B ? »), et le comité avait perdu sa crédibilité sur son sujet principal.

**L'autopsie du praticien :** l'escalade formelle (au sponsor, avec les données) aurait dû arriver après la première lettre sans réponse — le protocole du niveau 5 (la lettre avec deadline, puis l'escalade) existait, et il n'a pas été appliqué par peur politique. La peur a coûté trois mois et la crédibilité du comité.

**La correction :** la règle de l'escalade automatique : une lettre de veille sans réponse dans le délai déclenche l'escalade automatique (le registre du comité la note, le sponsor la reçoit) — sans décision humaine supplémentaire. L'escalade n'est pas une punition : elle est le mécanisme qui rend la gouvernance réelle. Un comité qui n'escalade pas quand il doit n'est pas prudent : il est démissionnaire.

**La leçon :** la gouvernance qui a peur de son propre pouvoir n'a pas de pouvoir. L'escalade automatique est ce qui protège le comité de sa propre politesse — et protège les équipes qui respectent les règles de voir les autres les respecter aussi.

## 5. L'histoire du bilan à l'échelle qui a révélé l'invisible

Le premier bilan de qualité à l'échelle (atelier 7.2 du BLEU) d'une organisation de 8 équipes a produit une surprise : deux équipes (F et G) avaient des ratios de tri excellents (50 %+ gardés, beaucoup de défauts trouvés) — et personne ne le savait, y compris elles-mêmes. Leurs pratiques n'étaient pas partagées : elles avaient développé leurs gabarits en silence, sans compte au comité.

**La découverte :** deux des meilleures pratiques de l'organisation étaient invisibles — parce que le bilan à l'échelle n'existait pas avant. Le comité a invité les équipes F et G à présenter leurs gabarits (atelier partagé), les gabarits ont été adoptés par quatre autres équipes, et le ratio moyen de l'organisation a monté de 12 points en un trimestre.

**La leçon :** le bilan à l'échelle ne sert pas qu'à détecter les problèmes : il sert à découvrir les réussites invisibles. Une organisation qui ne fait pas de bilan à l'échelle a probablement de bonnes pratiques cachées dans ses coins — et les ignorer est un gaspillage autant que d'ignorer ses dérives.

**Le corollaire :** la règle de partage des pratiques : toute pratique à ratio exceptionnel (au-dessus de la moyenne + 20 %) est présentée au comité dans le trimestre — pas pour être copiée (les contextes diffèrent), mais pour être documentée et discutée. Les meilleures pratiques se propagent par l'histoire, pas par la consigne.

## 6. La synthèse des histoires du niveau 5

| Histoire | Piège du niveau 5 | Correction |
|---|---|---|
| Le comité-pouvoir | L'accumulation de périmètre | La charte « ne décide pas », le quorum actif |
| Le registre réconciliant | Le conflit d'anecdotes | Le registre partagé, la règle non-évaluative |
| Le seuil divisant | Le seuil unique sur contextes hétérogènes | Le système standard/contexte/transition |
| L'escalade manquée | La peur politique de la gouvernance | L'escalade automatique après délai |
| Le bilan révélateur | Les bonnes pratiques invisibles | La règle de partage des pratiques exceptionnelles |

Le praticien du niveau 5 apprend de ces cinq histoires que la gouvernance n'est pas une structure : c'est un équilibre — entre le pouvoir et le terrain, entre les anecdotes et les données, entre l'uniformité et les contextes, entre la politesse et l'action. L'équilibre se tient par des règles écrites (charte, registre, escalade) et se nourrit de bilans qui révèlent à la fois les dérives et les trésors.
