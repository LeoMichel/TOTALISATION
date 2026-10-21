
---

# Partie 9 : Les situations difficiles du niveau 2

Cette partie traite les situations qui font échouer le niveau 2, avec les réponses qui ont fonctionné dans les missions réelles. Elle est destinée au lecteur qui rencontre déjà le problème — pas à celui qui veut l'éviter par la théorie.

## 1. L'équipe qui modélise mais ne converse jamais

**Symptôme.** Les modèles existent, sont propres, à jour — et personne ne les utilise. Les décisions se prennent en réunion comme avant. La confrontation n'a lieu que lorsque le coach l'anime.

**Diagnostic.** Le modèle a été présenté comme un livrable (« il faut des modèles ») et non comme un instrument (« les modèles servent à se comprendre »). Une équipe qui modélise pour satisfaire une attente produit des artefacts ; une équipe qui modélise pour résoudre un problème réel produit des outils.

**Ce qui a fonctionné.**
- Arrêter toute production de nouveaux modèles pendant deux semaines, et ne conserver que la confrontation du modèle existant. La pénurie forcée oblige à utiliser ce qui existe.
- Faire entrer la confrontation dans un moment déjà existant : la revue hebdomadaire, le stand-up du lundi. Un rituel nouveau meurt ; un rituel greffé survit.
- Mesurer ce qui compte : non pas « le modèle est à jour » mais « la dernière divergence trouvée ». Zéro divergence en un mois signifie que la confrontation ne se fait pas — c'est le signal d'alarme, pas la preuve de qualité.

**Ce qui n'a pas fonctionné.** Rendre la confrontation obligatoire par décret. Elle s'est faite pendant trois semaines, puis a disparu avec le décret. La confrontation ne se décrète pas : elle se déclenche par un problème réel (« mais tu testes avant ou après ? ») que le modèle rend visible.

## 2. Le modèle que le nouveau venu ne comprend pas

**Symptôme.** Le modèle est précis, complet — et chaque nouveau arrivant doit le faire expliquer par un senior. Le modèle ne remplit pas sa fonction d'onboarding.

**Diagnostic.** Le modèle a été écrit par ceux qui connaissent déjà, pour ceux qui connaissent déjà. Les conventions implicites (ce que signifie « traiter », où commence le processus, qui décide quoi) ne sont pas dans le modèle — elles sont dans la tête des anciens.

**Ce qui a fonctionné.**
- Faire relire le modèle par le dernier arrivé, et noter chaque question comme un défaut du modèle. Dix questions typiques = dix corrections : le modèle s'améliore exactement là où il échoue.
- Ajouter un glossaire du modèle : chaque terme ambigu défini en une phrase. Le lexique du niveau 1 est la base — le glossaire du modèle est sa spécialisation.
- Faire dessiner par le nouveau la version simplifiée (« le modèle en une page ») : celui qui dessine comprend. La version une page devient aussi l'entrée de tous.

**Ce qui n'a pas fonctionné.** Organiser une formation au modèle. Les slides ont été regardées, puis le modèle est resté aussi opaque. La compréhension vient de l'usage (relire, questionner, redessiner), pas de l'exposé.

## 3. La documentation générée que personne ne lit

**Symptôme.** Le pipeline de documentation fonctionne, les pages se régénèrent — et les statistiques de lecture sont proches de zéro. L'équipe continue de poser ses questions en direct.

**Diagnostic.** La documentation répond aux questions que personne ne se pose, ou ne répond pas aux questions que tout le monde se pose. Une documentation générée n'est pas utile parce qu'elle est à jour : elle est utile parce qu'elle répond aux vraies questions, au bon endroit, au bon niveau de détail.

**Ce qui a fonctionné.**
- Inventorier les questions réellement posées pendant un mois (support, internes, nouveaux) et vérifier lesquelles la documentation répond. Les questions non couvertes sont le plan de travail de la documentation — pas les sujets que l'équipe croit utiles.
- Placer la documentation là où les questions se posent : le message d'erreur qui renvoie à la page, le code qui commente la page, la réunion qui l'affiche. Une documentation qu'on ne trouve pas au moment du besoin est une documentation morte.
- Supprimer sans pitié les pages non lues. Chaque page morte noie les pages vivantes : la documentation utile se distingue par sa rareté, pas par son volume.

**Ce qui n'a pas fonctionné.** Améliorer le générateur (plus de pages, plus de détails, plus de formats). Le problème n'était jamais la génération : c'était l'adéquation aux questions réelles.

## 4. Le MBT qui coûte plus qu'il ne rapporte

**Symptôme.** Le pipeline de génération est en place, les tests s'exécutent — et le bilan est négatif : plus de temps à maintenir le pipeline et trier les tests qu'à écrire des tests utiles à la main.

**Diagnostic.** Le domaine n'a pas l'explosion combinatoire qui justifie le MBT, ou le modèle n'est pas assez stable pour servir de base de génération. Le MBT amplifie la qualité du modèle : un modèle mouvant produit des tests mouvants, et le coût de suivi dépasse la valeur.

**Ce qui a fonctionné.**
- Réduire le MBT à une seule zone à haute valeur combinatoire (typiquement une machine à états ou un ensemble de règles de combinaison), et faire le reste à la main. Le MBT partiel est presque toujours le bon équilibre.
- Mesurer honnêtement le ratio : tests produits / sélectionnés / utiles. Un ratio qui ne s'améliore pas sur trois campagnes est le signal d'arrêt.
- Conserver le modèle pour sa valeur première (rendre le processus discutable) même si la génération est abandonnée. L'abandon du MBT n'est pas un échec du modèle.

**Ce qui n'a pas fonctionné.** Persévérer « parce que l'investissement est fait ». Le coût irrécupérable n'est pas une raison de continuer à perdre : l'arrêt documenté est une décision mature.

## 5. Le sponsor qui demande des modèles sans savoir pourquoi

**Symptôme.** Le sponsor a entendu parler du BPMN (conférence, article, concurrent) et exige des modèles. Il ne sait pas ce qu'il en attend — mais il les veut.

**Diagnostic.** La demande est réelle même si sa motivation est floue. Le risque est de produire des modèles de vitrine : propres, inutiles, et la déception du sponsor quand il découvre qu'ils ne changent rien.

**Ce qui a fonctionné.**
- Faire préciser la question à laquelle le sponsor veut une réponse : « Quand vous regardez un modèle, que voulez-vous y apprendre ? » Les réponses typiques : « qui fait quoi », « où est le risque », « pourquoi c'est lent ». Chaque réponse oriente un modèle différent — et les modèles de vitrine disparaissent.
- Livrer le premier modèle avec sa première divergence trouvée : « ce modèle nous a fait découvrir que le QA teste après, pas avant ». Le sponsor comprend alors la valeur par l'exemple, pas par la théorie.
- Faire figurer dans le rapport mensuel les preuves d'usage : divergences trouvées, questions résolues par les modèles. Le sponsor qui voit l'usage cesse de demander le volume.

**Ce qui n'a pas fonctionné.** Livrer les modèles demandés sans clarifier l'usage. Dix modèles propres ont été produits, regardés une fois, et le sponsor a conclu que « ça ne sert à rien » — conclusion correcte pour des modèles de vitrine, tragique pour la suite de l'initiative.

## 6. L'équipe qui veut sauter à l'automatisation

**Symptôme.** Dès la semaine 2, l'équipe propose d'automatiser : génération de documentation, exécution de tests, intégration continue des modèles. Le niveau 2 la lasse — elle veut du niveau 3.

**Diagnostic.** L'enthousiasme pour l'outil est réel et précieux — mais l'automatisation prématurée fige les modèles dans leur état embryonnaire. Un générateur construit sur un modèle non confronté produit de la documentation fausse en masse.

**Ce qui a fonctionné.**
- Canalyser l'enthousiasme vers la confrontation : « automatisez la détection des divergences entre les deux descriptions du processus ». C'est de l'automatisation utile, qui renforce le niveau 2 au lieu de le court-circuiter.
- Poser la règle des trois usages : un modèle doit avoir été confronté trois fois avec des divergences trouvées avant d'être automatisé. La règle est simple, vérifiable, et elle protège l'investissement.
- Laisser l'équipe construire un prototype d'automatisation sur un seul modèle — comme pilote. Le pilote révèle les coûts réels avant l'engagement.

**Ce qui n'a pas fonctionné.** Interdire l'automatisation jusqu'à la fin du niveau 2. L'interdiction a tué l'enthousiasme, qui ne revenait plus. La canalisation vaut mieux que l'interdiction.

## 7. La fin de mission qui sonne comme un abandon

**Symptôme.** Au départ du coach, les modèles continuent d'exister mais le rythme s'arrête : plus de confrontations, plus de mises à jour documentées. Trois mois plus tard, les modèles sont des reliques.

**Diagnostic.** Le niveau 2 dépendait du coach plus que le niveau 1 : la confrontation est un acte social plus coûteux qu'une relecture. Sans animateur, l'acte ne se fait plus — sauf si l'équipe a trouvé son propre déclencheur.

**Ce qui a fonctionné.**
- Transférer le déclencheur, pas la tâche : identifier le moment où les divergences se révèlent naturellement (le bug de production, la question du nouveau, la réunion tendue) et greffer la confrontation dessus. Un déclencheur naturel survit ; une tâche planifiée meurt.
- Nommer un duo de gardiens (deux rôles différents, jamais deux personnes du même rôle) avec la responsabilité de la confrontation — pas de la mise à jour. La mise à jour suit la confrontation ; sans confrontation, la mise à jour est du ritualisme.
- Prévoir la règle de deuil : si un modèle n'a pas été confronté depuis deux mois, il est marqué « dormant » publiquement. Un modèle dormant est honnête ; un modèle prétendument vivant est un piège.

**Ce qui n'a pas fonctionné.** Laisser « l'équipe saura faire seule ». Certaines équipes oui ; la plupart non. Le transfert explicite du déclencheur est la différence entre la survivance et la relique.

---

## Comment utiliser cette partie

- **Au symptôme** : chaque section est un symptôme. Allez à la section qui décrit votre situation, pas à celle qui semble la plus sage.
- **Pour le diagnostic** : chaque section distingue le symptôme de sa cause réelle — la cause est presque toujours un usage absent, pas un outil manquant.
- **Pour l'action** : chaque section donne « ce qui a fonctionné » et « ce qui n'a pas fonctionné ». La seconde liste est aussi précieuse que la première : elle évite les erreurs déjà payées par d'autres.
