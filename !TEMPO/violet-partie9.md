
---

# Partie 9 : Les fiches-outils du niveau 7

## Fiche 31 : Le gabarit du récit de transmission

**Usage :** raconter un épisode fondateur ou significatif — le format qui préserve les détails, les erreurs et les apprentissages.

```
RÉCIT — [titre]                       Raconté le : [date]
Par : [nom — et le nom de qui l'a transmis, le cas échéant]

QUAND (la période, le contexte de l'organisation à ce moment) :
________________________________________________________

CE QUI S'EST PASSÉ (les faits, chronologiques, y compris
les erreurs et les doutes) :
1. ______________________________________________
2. ______________________________________________
3. ______________________________________________

CE QUE ÇA A COÛTÉ (le temps, l'argent, l'énergie, la réputation) :
________________________________________________________

CE QU'ON A APPRIS (l'apprentissage toujours actif, si possible
relié à un MEM du niveau 6) :
________________________________________________________

POURQUOI CE RÉCIT EST RA CONTÉ (sa fonction dans la transmission :
un moment fondateur ? un précédent de décision ? un échec instructif ?)
________________________________________________________
```

**Exemple rempli (tiré du cas NationalProperty, dilemme 1) :**

```
RÉCIT — La fonctionnalité sans propriétaire
Raconté le : premier lundi de chaque trimestre (rituel 1)
Par : le praticien (qui l'a reçu de l'ancien praticien)

QUAND : automne 2023, après la refonte du site. L'équipe était
en croissance (de 6 à 11 personnes), et la pression commerciale
avec elle.

CE QUI S'EST PASSÉ :
1. Un agent d'affaires a demandé une fonctionnalité « simple » :
   une carte par quartier, avec zonage dessiné, budget et
   revenus. Sans Wireframe, il était impossible de viser
   correctement.
2. J'ai passé le wireframe au modèle, convaincu qu'il était
   bon. Il ne l'était pas : les zones pouvaient se chevaucher,
   le calcul était faux, le budget n'était jamais vérifié.
3. Le développeur a implémenté le modèle fidèlement — c'était
   son travail, et il l'a bien fait. Le bug est arrivé en
   production.
4. Nous avons discuté en rétrospective. La décision a été
   de nous blâmer collectivement : le développeur avait fait
   son travail ; c'était l'organisation qui avait échoué à
   empêcher le bug d'arriver.

CE QUE ÇA A COÛTÉ : une semaine de correction en urgence,
deux clients mécontents, et la confiance du développeur (qu'il
nous a fallu regagner).

CE QU'ON A APPRIS : « si une affirmation n'est pas testable,
elle n'est pas spécifiée. » Cet apprentissage est devenu la
règle active MEM-001 — elle est citée dans presque toutes les
spécifications depuis.

POURQUOI CE RÉCIT EST RA CONTÉ : c'est l'histoire de notre
règle d'or. Chaque développeur qui l'entend comprend pourquoi
les affirmations non testables ne passent pas. Et chaque
manager qui l'entend comprend pourquoi nous ne blâmons pas
les individus : nous réparons l'organisation.
```

## Fiche 32 : Le gabarit d'entrée de jurisprudence

**Usage :** documenter une décision ou un dilemme résolu — la jurisprudence de la philosophie.

```
JURISPRUDENCE — J-[n]                 Cré le : [date]
CONSOLIDÉE : [dates des épisodes similaires]

LE DILEMME (deux valeurs ou exigences en tension) :
D'un côté : ______________________________ (valeur A)
De l'autre : ______________________________ (valeur B)

L'ÉPISODE INITIAL (l'histoire courte, avec le lien au récit
fondateur s'il existe) :
________________________________________________________

LA DÉCISION PRISE :
________________________________________________________

LA PRÉCEDENT QU'ELLE ÉTABLIT (la règle pour les dilemmes
similaires à venir) :
« Quand [situation], nous faisons [décision], parce que
[valeur]. »

LES ÉPISODES DE CONSOLIDATION (chaque fois que le précédent
a été appliqué) :
- [date] : [rappel bref]
- [date] : [rappel bref]

LA CONFORTATION (ce qui confirme la règle aujourd'hui) :
________________________________________________________
```

**Exemple rempli (tiré du vécu de l'ORANGE, activité contre résultat) :**

```
JURISPRUDENCE — J-3                   Cré le : 2024
CONSOLIDÉE : 2024, 2025 (3 épisodes)

LE DILEMME : la confiance dans les personnes (faut-il croire
le report d'activité ?) contre la robustesse de la mesure
(les données ne mentent pas).

L'ÉPISODE INITIAL : les nouvelles arrivantes déclaraient des
heures « réelles » ; une personne a signalé 10h pour une tâche
de 40h. Le spécialiste métier est intervenu : « les heures
déclarées ne sont pas des heures réelles, elles mesurent le
sentiment de difficulté ». On a gardé les données pour ce
qu'elles sont, pas pour ce qu'on aurait voulu qu'elles soient.

LA DÉCISION PRISE : ne jamais transformer une déclaration en
mesure de vérité, et ne jamais sanctionner sur un écart
d'activité. L'activité indique un signal ; l'entretien
l'interprète.

LE PRÉCÉDENT : « Quand une donnée déclarée entre en tension
avec une mesure, nous cherchons ce que chaque source mesure
réellement, et nous ne transformons jamais l'une en l'autre. »

LES ÉPISODES DE CONSOLIDATION :
- 2024 : l'écart d'activité entre deux personnes identiques
  (1h vs 40h) a été interprété en entretien, pas sanctionné.
- 2025 : les données d'entraînement des nouveaux (artificielle-
  ment rapides) n'ont jamais été utilisées pour les évaluer.
- 2025 : le renoncement à l'API de suivi (vécu N6) : les
  données étaient tentantes, mais elles auraient transformé
  la surveillance en mesure.

LA CONFORTATION : chaque tentative de réconciliation (faire
des heures déclarées des heures réelles) a échoué et a créé
des comportements de couverture. Le précédent est conforté
par ses échecs d'infraction autant que par ses succès.
```

## Fiche 33 : Le gabarit du bilan de vitalité culturelle

**Usage :** le bilan annuel du niveau 7 — le pouls de la culture.

```
BILAN DE VITALITÉ — [année]          Fait le : [date]

1. LES RITUELS
| Rituel | Fréquence prévue | Fréquence réelle | Vivant ? |
|--------|-----------------|------------------|----------|
| Récit du lundi | hebdo | __/52 | oui/partiel/non |
| Conversation valeurs | mensuelle | __/12 | |
| Revue horizon | trimestrielle | __/4 | |
| Pèlerinage | annuel | __/1 | |
| Célébration échecs | semestrielle | __/2 | |
| Révision philosophie | annuelle | __/1 | |

2. LES RÉCITS
- Racontés cette année : __
- Cités dans des décisions : __ (lesquels)
- Les nouveaux peuvent en raconter : __/__

3. LA JURISPRUDENCE
- Entrées nouvelles : __
- Consultées pour des décisions : __ fois
- Entrées devenues obsolètes : __ (lesquelles, pourquoi)

4. LA TRANSMISSION
- Nouveaux arrivés : __ ; accompagnés par un porteur : __/__
- Peuvent raconter les récits fondateurs : __/__
- Réussite : __/__
- Réussite des nouveaux : __/__

5. LE RENONCEMENT
- Ce qu'on a abandonné cette année : __
- Ce que ça nous a appris : __

6. LES DÉCISIONS (pour l'année prochaine)
- Rituels à raviver : __
- Récits à re-raconter : __
- Transmissions à rattraper : __
```

**La valeur du bilan :** il transforme la vitalité culturelle d'une impression en une mesure. Les rituels notés « partiel » ne sont pas condamnés : ils sont diagnostiqués (pourquoi la fréquence réelle est-elle plus basse ? le rituel est-il mal placé, mal conçu, mal compris ?). Un bilan honnête est plus précieux qu'un bilan parfait.

## Fiche 34 : Le gabarit de l'apprentissage réconcilié

**Usage :** quand deux apprentissages (souvent de deux personnes, de deux équipes, de deux cultures) semblent contradictoires — le format de la réconciliation.

```
RÉCONCILIATION D'APPRENTISSAGE — [n]  Cré le : [date]

APPRENTISSAGE A : « [formulation] »
Source : [personne/équipe/récit]

APPRENTISSAGE B : « [formulation] »
Source : [personne/équipe/récit]

LA TENSION (pourquoi ils semblent contradictoires) :
________________________________________________________

L'INVESTIGATION (ce que chaque apprentissage mesure vraiment :
dans quel contexte A a-t-il été appris ? dans quel contexte B ?)
- A a été appris dans : [contexte]
- B a été appris dans : [contexte]

LA RÉCONCILIATION (l'apprentissage qui subsume les deux, ou
la règle de bascule entre les deux) :
________________________________________________________

LE NOUVEL APPRENTISSAGE (relié aux deux sources) :
→ MEM-[n]
```

**Exemple rempli (tiré du vécu de l'ORANGE, les heures qui ne se réconciliaient pas) :**

```
RÉCONCILIATION D'APPRENTISSAGE — R-1  Cré le : 2025

APPRENTISSAGE A : « il faut 40 heures pour ajouter un modèle »
Source : le formateur vétéran, formé sur l'ancien pipeline

APPRENTISSAGE B : « il faut 1 heure pour ajouter un modèle »
Source : les nouveaux, formés sur le nouveau pipeline

LA TENSION : 40 heures contre 1 heure pour la même tâche —
quelqu'un se trompe, ou l'un des deux pipelines est mauvais.

L'INVESTIGATION :
- A a été appris dans : l'ancien pipeline (saisie manuelle
  des données, montage manuel des paramètres, vérification
  visuelle).
- B a été appris dans : le nouveau pipeline (saisie guidée,
  presets, vérification automatisée).

LA RÉCONCILIATION : les deux disent vrai — ils ne parlent pas
du même travail. A mesure l'effort de l'artisanat complet ;
B mesure l'effort de l'utilisation de l'outil. La tâche n'est
pas la même, parce que le pipeline a changé le travail.

LE NOUVEL APPRENTISSAGE : « quand deux mesures du même intitulé
divergent, chercher si le travail sous-jacent a changé — la
divergence peut révéler une transformation, pas une erreur. »
→ MEM-055, relié à J-3 (les heures déclarées).
```

**La valeur de la fiche :** la réconciliation d'apprentissages contradictoires est l'un des gestes les plus puissants du niveau 7 — elle transforme une dispute en découverte. Les divergences de mesure sont souvent des révélations de transformation, pas des erreurs.

## Le glossaire du niveau 7

**Philosophie** — l'ensemble vivant des valeurs, de la vision, des rituels et de la jurisprudence qui oriente les décisions. Sa règle : elle vit dans les décisions, pas sur les murs — l'écriture est sa trace, pas son corps.

**Valeurs** — les trois à cinq principes qui tranchent les dilemmes. Sa règle : une valeur se reconnaît à son prix — une valeur qui n'a jamais coûté rien n'a jamais rien décidé.

**Vision** — l'image du futur que la philosophie sert. Sa règle : elle se révisionne annuellement avec les valeurs — une vision figée devient une nostalgie.

**Rituel** — une pratique régulière qui vitifie la philosophie (récit, conversation, revue, pèlerinage, célébration, révision, transmission). Sa règle : un rituel sans trace n'a pas eu lieu.

**Récit de transmission** — l'histoire d'un épisode significatif, racontée avec ses erreurs et ses coûts. Sa règle : le récit qui ment fabrique des croyants, pas des porteurs.

**Jurisprudence** — l'ensemble des précédents de décision documentés (dilemmes résolus, règles établies, consolidations). Sa règle : une jurisprudence qui ne guide aucune décision est un historique.

**Précédent** — la règle établie par une décision de dilemme, applicable aux situations similaires. Sa règle : il se consolide par les épisodes similaires — un précédent appliqué une fois est une opinion, appliqué trois fois est une jurisprudence.

**Pèlerinage** — la transmission annuelle des origines, avec ses erreurs fondatrices. Sa règle : les erreurs font partie du récit — souvent la partie la plus utile.

**Célébration des échecs** — le rituel semestriel qui reconnaît l'échec assumé comme honorable. Sa règle : au moins un échec par célébration doit avoir coûté quelque chose.

**Révision** — la mise à jour annuelle de la philosophie (valeurs, vision), argumentée. Sa règle : au plus une révision substantielle par an, argumentée par trois épisodes vécus.

**Compagnonnage** — la transmission de personne à personne : un porteur, un nouveau, un trimestre. Sa règle : la philosophie se transmet par le contact, pas par décret.

**Bilan de vitalité** — la mesure annuelle de la culture (rituels, récits, jurisprudence, transmission, renoncement). Sa règle : il transforme la vitalité d'une impression en une mesure — et les rituels « partiel » sont diagnostiqués, pas condamnés.

**Réconciliation culturelle** — l'intégration d'une culture différente (acquisition, nouvelle équipe) par identification des communs et discussion des divergences. Sa règle : la substitution produit une culture de façade ; la réconciliation est plus longue, et c'est la seule voie qui tient.

**Réconciliation d'apprentissages** — la résolution de la contradiction entre deux apprentissages par l'investigation de leurs contextes. Sa règle : la divergence de mesure révèle souvent une transformation, pas une erreur.
