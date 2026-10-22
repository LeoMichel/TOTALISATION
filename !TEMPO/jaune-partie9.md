
---

# Partie 9 : Les exercices avancés E7-E12, la FAQ, les anti-patterns et la situation difficile du niveau 3

## Les exercices avancés E7-E12

Le niveau 3 forge la cadence. Les six exercices qui suivent sont conçus pour les équipes qui ont déjà les critères (niveau 2) et qui apprennent maintenant à tenir le rythme.

### E7 — La micro-cadence en situation de crise

**Durée :** 30 minutes + la crise réelle. **Format :** exercice déclencheur.

Scénario : l'équipe apprend que la mise en production de demain a une régression critique, à 17h, alors que le rituel de qualimétrie du mardi est à 9h. Le groupe décide : report, réduction, ou maintien ? Trois options sont chiffrées (coût en signaux perdus, risque de dérive, message envoyé à l'équipe). Le débrief oppose la réponse réflexe (« on reporte, c'est la crise ») à la règle du niveau 3 (« jamais reporté, parfois réduit »).

Le vrai test arrive à la crise suivante : l'équipe a-t-elle tenu la micro-cadence ? Le registre tranche — et le pattern de reports est le thermomètre de la forge.

### E8 — Le SLA par classe : classer 15 demandes réelles

**Durée :** 45 minutes. **Format :** atelier en binômes avec les demandes réelles de l'équipe.

Chaque binôme reçoit 15 demandes réelles (ou pseudo-réelles issues du vécu) et les classe : simple / complexe / exploratoire. Puis chaque binôme propose un SLA par classe (ex. : simple = 2 jours, complexe = 5 jours avec revue, exploratoire = 1 sprint avec jalon). La mise en commun fait ressortir les désaccords de classement — et chaque désaccord est une spécification manquante (définition floue) ou un cas limite à trancher collectivement.

La règle de sortie : chaque classe a un SLA, chaque demande est classée à l'entrée, et le SLA est mesuré (respecté / dépassé) au registre. Le SLA qui n'est pas mesuré n'existe pas.

### E9 — Le pipeline des preuves hiérarchisées

**Durée :** 60 minutes. **Format :** atelier technique avec le contexte réel du pipeline.

L'équipe cartographie son pipeline actuel (quels tests tournent où, quand, avec quels délais), puis applique la grille du niveau 3 : quels tests doivent être **bloquants au commit** (fiables, rapides, détectent les régressions immédiates), **bloquants au merge** (fiables, moyennement rapides, détectent les conflits), **informatifs la nuit** (lents, exploratoires, détectent les dérives lentes)? La contrainte du niveau 3 : aucun test fiable ne peut être purement informatif, aucun test fragile ne peut être bloquant.

Le débrief examine les signaux : les tests bloquants tombent-ils trop souvent à tort (fragiles mal placés) ? Les tests informatifs trouvent-ils des bugs tard (preuves mal hiérarchisées) ? La sortie est une grille de migration — pas un refonte (le niveau 3 migre progressivement).

### E10 — La confirmation systématique des défauts résolus

**Durée :** 45 minutes en atelier, puis 2 semaines réelles. **Format :** drill sur données réelles.

L'équipe extrait les 10 derniers défauts résolus et applique le protocole de confirmation systématique : le défaut est-il reproductible dans les conditions d'origine ? La correction est-elle vérifiée par un test qui la couvre ? Le test est-il au bon niveau du pipeline (bloquant si régression, informatif si couverture) ? Le scoring N3 donne le pourcentage de confirmations réelles — la moyenne du secteur est basse, et le chiffre brut est souvent un choc.

Les 2 semaines réelles appliquent le protocole à tous les nouveaux défauts résolus, et le registre suit la courbe. L'objectif du niveau 3 n'est pas 100 % (il y a des défauts exploratoires) : c'est que 100 % des défauts aient un statut de confirmation explicite (confirmé / non-confirmable / à suivre).

### E11 — La lettre de pré-retraite d'une dérive

**Durée :** 30 minutes. **Format :** écriture individuelle puis partage.

Chaque participant écrit la lettre qu'il recevrait (ou recevrait avec soulagement) s'il était le porteur d'une dérive que le système de veille a détectée : qui la signe, quels sont les signaux chiffrés, quelles sont les options proposées, quel est le délai de réponse. L'exercice inverse la perspective du porteur de dérive (niveau 2) : ici, c'est le receveur qui définit ce qu'une lettre utile contient.

La mise en commun fait émerger le gabarit collectif de la lettre de veille : signaux datés, pattern visible, options chiffrées, deadline de réponse. Ce gabarit devient le standard de la veille N3 — et chaque lettre reçue qui ne respecte pas le gabarit est une dérive de la veille elle-même.

### E12 — L'audit de cadence : notre rythme tiendra-t-il 6 mois ?

**Durée :** 90 minutes. **Format :** atelier de fin de cycle, le rituel le plus exigeant du niveau 3.

L'équipe reprend les 4 piliers de la forge (critères vivants, pipeline cadencé, confirmation systématique, veille+seuils) et pose pour chacun la question du niveau 3 : « tiendra-t-il sans le coach, pendant les urgences, après le départ des porteurs initiaux ? ». Pour chaque pilère, trois tests : le test de la urgence (tiendra-t-il à 120 % de charge ?), le test de la relève (qui l'anime quand le porteur actuel part ?), le test de la transmission (les nouveaux l'apprennent-ils par la pratique ?).

La sortie est une carte de fragilité : les piliers qui échouent à un test sont les chantiers de la forge suivante. L'audit de cadence est le rituel de fin de cycle du niveau 3 — et il se répète chaque trimestre, car une cadence qui tient aujourd'hui peut lâcher demain.

## La FAQ du niveau 3

**Q : la cadence fixe n'est-elle pas de la rigidité bureaucratique ?**
R : La rigidité est l'application de règles sans contexte ; la cadence est le maintien d'un rythme avec contexte. La cadence réduit, s'adapte, évolue — mais ne disparaît pas en silence. Un rituel reporté trois fois est une bureaucratie déguisée en flexibilité ; un rituel de 10 minutes tenu 26 semaines est de la rigueur vivante.

**Q : que faire quand un rituel tombe en plein incident de production ?**
R : La règle « jamais reporté, parfois réduit » s'applique : le rituel devient 5 minutes de signaux bruts (statuts de production, porteurs notifiés), tenu par n'importe qui — et l'incident est l'occasion de vérifier si la cadence survit à ce qu'elle est censée gérer. Si elle ne survit pas, c'est le sujet du prochain audit de cadence.

**Q : le SLA par classe ne va-t-il pas créer des incitations à mal classer les demandes ?**
R : Oui, si le classement est auto-déclaré sans vérification. La protection du niveau 3 : le classement est fait à l'entrée par le demandeur, vérifié par le porteur, et les re-classifications sont notées au registre. Un pattern de re-classifications (ex. : tout devient « complexe ») est un signal de dérive — et il se traite comme tel.

**Q : comment tenir la cadence quand les porteurs changent constamment ?**
R : Le rituel du niveau 3 est conçu pour être animé par n'importe quel porteur: il a un gabarit (3 signaux, une question, une décision), il est documenté, et il se transmet par la pratique. Si un rituel exige un porteur unique pour tenir, il n'est pas forgé — il est escorté. La rotation est le test : si elle tue le rituel, le rituel était décoratif.

**Q : la confirmation systématique n'est-elle pas trop coûteuse pour les petits défauts ?**
R : Le niveau 3 ne demande pas une confirmation lourde pour chaque défaut : il demande un statut explicite (confirmé / non-confirmable / à suivre) et un test de couverture pour les défauts classés « régression ». Les défauts exploratoires et les défauts mineurs ont un protocole allégé. Le coût réel du niveau 3 n'est pas la confirmation : c'est l'absence de statut.

**Q : les seuils de veille, comment les choisir sans se tromper ?**
R : On ne les choisit pas au début : on les forge. Le niveau 3 commence par collecter les signaux (sans seuil), forge les patterns sur 2-3 semaines, puis pose les seuils sur les données réelles. Un seuil posé avant les données est une supposition ; un seuil forgé sur les données est une décision. Et chaque seuil a son histoire — l'incident qui l'a fait naître.

## Les anti-patterns du niveau 3

### AP-N3-1 : La cadence décorative
Les rituels existent dans le calendrier, ont des noms sérieux, mais sont systématiquement reportés, réduits à zéro, ou tenus sans contenu. **Signal :** un rituel reporté 3 fois de suite sans raison écrite. **Contre-mesure :** la règle du report écrit + l'audit de cadence trimestriel qui confronte le calendrier réel au calendrier prévu.

### AP-N3-2 : Le SLA uniforme
Un délai unique pour toutes les demandes, « pour être équitable ». Résultat : sur-traitement des simples, bâclage des complexes, et le SLA n'est respecté par personne. **Signal :** le taux de respect du SLA oscille entre 20 % et 95 % selon les semaines. **Contre-mesure :** le SLA par classe (E8), avec les re-classifications notées au registre.

### AP-N3-3 : Le pipeline-boucher
Tous les tests sont bloquants, tout échec bloque tout, et l'équipe finit par ignorer les échecs (ou par désactiver les tests). **Signal :** les commits sont désactivés en période de rush, les tests « skipés » systématiquement. **Contre-mesure :** la grille bloquant/informatif (E9), la migration progressive, et la règle : un test bloquant doit être fiable, sinon il ne protège rien.

### AP-N3-4 : La confirmation en creux
Les défauts sont résolus, mais personne ne vérifie qu'ils le sont vraiment. Le statut passe à « fermé » par défaut (le ticket est ancien, le développeur est parti, personne ne veut rouvrir). **Signal :** le taux de ré-ouverture des défauts « fermés » est anormalement bas (personne ne vérifie) ou anormalement haut (personne ne confirmait). **Contre-mesure :** le protocole E10, le statut explicite, et la règle : un défaut sans statut de confirmation n'est pas fermé.

### AP-N3-5 : La veille-qu'on-oublie
Le système de veille existe, les seuils sont posés, mais les alertes s'accumulent sans traitement (ou sont désactivées après le premier faux positif). **Signal :** les alertes de veille n'ont pas de statut de traitement, ou les seuils n'ont jamais été ajustés. **Contre-mesure :** la lettre de veille (E11) avec deadline de réponse, et le rituel : chaque alerte a un propriétaire daté.

### AP-N3-6 : La forge fantôme
L'équipe croit avoir forgé (les rituels ont tenu un mois, le pipeline a tourné une fois), mais au premier départ de porteur, tout s'effondre. **Signal :** aucun rituel n'a survécu à une rotation. **Contre-mesure :** l'audit de cadence (E12) et ses trois tests : urgence, relève, transmission. La forge n'est terminée que quand elle survit au départ.

## La situation difficile du niveau 3 : le rituel que personne ne veut animer

**La situation.** Le point de qualimétrie hebdomadaire existe, il est dans le calendrier, il a un gabarit — mais personne ne veut l'animer. Chaque semaine, la question « qui anime ? » flotte, la réunion démarre en retard, quelqu'un finit par le faire à contrecœur, et la qualité s'en ressent. L'équipe a la méthode ; elle n'a pas le porteur.

**Pourquoi c'est difficile.** C'est le nœud du niveau 3 : la cadence exige un porteur, mais le porteur est une charge — et personne ne veut la porter en permanence. Les réponses classiques échouent toutes : désigner un responsable (le responsable finit par tout porter seul et lâcher), tourner la charge (chaque rotation réapprend, la qualité chute), automatiser (les signaux sont automatiques, l'animation est humaine).

**Le chemin du niveau 3.** La forge commence par nommer le problème : le rituel n'a pas de porteur, il a des occupants. La sortie est double :
1. **Le gabarit d'animation** : un document de 1 page (3 signaux à lire, 1 question à poser, 1 décision à noter) qui permet à n'importe qui d'animer en 5 minutes de préparation. L'animation n'est plus une compétence : c'est un protocole.
2. **La rotation outillée** : la charge tourne, mais chaque rotation est outillée (le gabarit, les données prêtes, le précédent animé en binôme avec le sortant). Le coût de la rotation tombe à ~15 minutes.

**La règle apprise :** un rituel qui exige un porteur héroïque n'est pas forgé. La forge du niveau 3 consiste à rendre l'animation suffisamment protocole pour que la charge devienne tournante — et suffisamment courte pour que personne ne la refuse. Le test de réussite : le rituel tient 6 semaines avec 6 animateurs différents, et personne ne peut dire qui est le « responsable ».
