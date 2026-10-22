
---

# Partie 26 : Les gabarits remplis du niveau 7 — récits, jurisprudence, épilogue

## Gabarit 1 : Récit de transmission rempli

```
RÉCIT — Le premier bug que personne ne voulait croire
Raconté le : premier lundi de chaque trimestre (rituel 1)
Par : le praticien fondateur (transmis à M.T. par le compagnonnage)

QUAND : l'automne 1987, dans le bureau de mon père, l'enfant
que j'étais à l'époque. J'avais 10 ans.

CE QUI S'EST PASSÉ :
1. Mon père avait construit une application de comptabilité
   pour un client. Je regardais par-dessus son épaule, et j'ai
   remarqué que le total de la colonne ne correspondait pas au
   sous-total affiché plus haut. J'ai dit : « Papa, le chiffre
   est différent. »
2. Mon père a répondu : « Non, c'est bon, je viens de vérifier. »
   Il ne l'avait pas vérifié — il l'avait cru vérifié, parce que
   le code ressemblait à ce qu'il attendait.
3. J'ai insisté : « Mais papa, regarde. » Il a regardé. Puis il
   s'est arrêté. Un long silence. Puis il a dit : « Tu as raison. »
   Et il a corrigé le bug en cinq minutes.
4. Ce que je n'avais pas compris à l'époque : le bug n'était pas
   dans le code. Le bug était dans la conviction de mon père —
   dans le fait qu'il croyait avoir vérifié. C'est ce moment qui
   m'a appris que les convictions (les miennes, celles des autres)
   sont toujours à vérifier.

CE QUE ÇA A COÛTÉ : deux heures de vérification, un fichier
corrompu (avant le système de sauvegarde), et la fierté d'un
adulte devant son enfant. Ce coût est petit. Mais il a fondé
trente ans de pratique.

CE QU'ON A APPRIS : « une affirmation n'est pas testable tant
que quelqu'un ne l'a pas testée ». Cet apprentissage est
l'apprentissage fondateur de la collection — celui qui a
commencé tout, avant que le mot TOTALISATION existe.

POURQUOI CE RÉCIT EST RA CONTÉ : chaque fois que quelqu'un
dans l'organisation dit « c'est bon, je viens de vérifier »,
une personne évoque ce récit. Et le « viens de vérifier »
devient un « je viens de vérifier, et voici le test ». C'est
la transformation qui fait tout.
```

## Gabarit 2 : Jurisprudence remplie (le dilemme de la validation)

```
JURISPRUDENCE — J-1                        Cré le : 06/10/2025
CONSOLIDÉE : 06/10/2025, 15/02/2026, 08/05/2026 (3 épisodes)

LE DILEMME : confiance dans la personne (croire le développeur
senior qui dit « c'est bon ») vs fiabilité du test (vérifier
avec un artefact).

L'ÉPISODE INITIAL : le premier bug (voir récit MEM-001), où le
développeur senior (mon père) croyait avoir vérifié — et
n'avait pas vérifié. Le bug a été trouvé par un enfant de
10 ans qui n'avait aucun pouvoir, aucune expertise, aucune
légitimité. Il avait une observation : « le chiffre est
différent ».

LA DÉCISION PRISE : à partir de ce jour, toute affirmation
« c'est bon » doit être accompagnée d'un artefact testable
(le test, le rapport, la preuve). L'expérience de la personne
ne remplace pas la preuve.

LE PRÉCÉDENT ÉTABLI : « Quand l'expérience et la preuve entrent
en tension, la preuve l'emporte — et le questionnement est
toujours bienvenu, quelle que soit la source. »

LES ÉPISODES DE CONSOLIDATION :
- 06/10/2025 : première application dans une revue de code
  (le code du développeur senior a été testé comme les autres)
- 15/02/2026 : l'équipe voisine a demandé une dérogation
  (« notre senior garantit la qualité ») — refusée, la preuve
  demande un test. L'équipe voisine a accepté et trouvé 3 bugs.
- 08/05/2026 : le praticien lui-même a été testé par un nouveau
  (« votre spécification, elle est testable comment ? ») — la
  spécification a été améliorée. Le praticien a remercié le
  nouveau en public.

LA CONFORMATION : chaque tentative d'infraction (croire sans
tester) a produit un bug. Chaque application (tester toujours)
a produit une confiance renforcée. Le précédent est conforté
par ses échecs d'infraction autant que par ses succès.
```

## Gabarit 3 : Épilogue du praticien fondateur rempli

```
ÉPILOGUE — Michel Bélanger                 Écrit le : [date de départ]

1. CE QUE LA COLLECTION A CHANGÉ CHEZ MOI
La collection ne m'a pas appris des techniques. Elle m'a appris
que la qualité n'est pas une discipline qu'on applique après
coup — c'est une conversation qu'on a pendant qu'on construit.
Cette conviction vient de Rayduf, du sous-sol, de l'oreille qui
savait ce qu'elle cherchait. Trente ans plus tard, elle tient.
Elle tient contre la pression, contre la mode, contre la
fatigue. Je ne sais pas si elle tiendra trente ans de plus —
mais je sais que trente ans de pratique l'ont renforcée, pas
usée.

2. CE QUE LA COLLECTION A CHANGÉ DANS L'ORGANISATION
L'équipe livrait 31 % de reprises en juin ; elle en livre 12 %
en décembre. Le temps de cycle est resté stable (+3 %) malgré
l'ajout des rituels. 1 incident de production en 6 mois (contre
5 sur la période précédente). Le lexique a 43 entrées vivantes.
Le pipeline a 412 tests bloquants qui tournent à chaque commit.
La documentation est citée par le support. Le canal des signaux
a produit 17 signaux confirmés, 2 chantiers de prévention, et
1 incident évité chiffré (2 h de correction vs 1 semaine de
blocage d'équipe).

3. CE QUE LA COLLECTION N'A PAS RÉSOLU
Le déséquilibre entre le volume de demandes et la capacité de
l'équipe reste — et le niveau 3 l'a nommé mais n'a pas pu le
corriger (c'est un problème de gouvernance, pas de méthode).
La dette sur les données historiques migrées n'a pas été
traitée (le niveau 2 l'a documentée, mais la correction dépasse
la capacité du trimestre). Les 2 équipes voisines n'ont pas
démarré la documentation vivante (le niveau 5 n'était pas
installé pour les inclure). La récurrence des demandes
« urgentes » (non urgentes en réalité) n'a pas été corrigée
(le niveau 3 a le SLA, mais le classement est contesté).

4. CE QUE JE CONFIE
Trois questions à garder vivantes :
- Est-ce que nos rituels sont vivants ou décoratifs ? (Vérifier
  chaque trimestre avec l'audit de vitalité — si les rituels
  se tiennent mais ne produisent rien, ils sont décoratifs.)
- Est-ce que nos valeurs ont coûté quelque chose récemment ?
  (Si non : elles sont des aspirations, pas des valeurs. Les
  aspirations ne sont pas fausses — mais il ne faut pas les
  confondre avec les valeurs.)
- Qui porte la collection dans trois ans ? (Commencer à
  transmettre maintenant — la transmission ne se délègue pas,
  elle se fait par le contact.)

5. MA PLUS GRANDE FIERTÉ
Le jour où M.T. a bloqué sa première demande sans spécification.
Elle a dit : « la grille ne me protège pas du client — elle me
protège de moi-même. » C'est le moment où j'ai su que la forge
avait réussi : les gens défendent les critères sans qu'on leur
demande. Ce jour-là, j'ai su que je pouvais partir — et que la
forge continuerait sans moi. C'est le plus beau cadeau qu'un
praticien peut recevoir : la preuve qu'il est remplaçable.

6. MA PLUS GRANDE LUCIDITÉ
L'incident de production du 12 mars : une fonctionnalité livrée
sans confirmation d'usage, parce que la deadline était pressée.
L'incident n'a pas coûté cher (2 heures de correction), mais il
m'a appris que les raccourcis ont un coût différé. J'aurais dû
confirmer. Je ne l'aurais pas fait parce que j'étais pressé.
La lucidité est venue de l'incident, pas de la théorie.

Je porte ces six leçons dans tout ce que je ferai ensuite. La
collection ne s'arrête pas avec moi — elle continue dans ceux
qui la vivent.
```

## Gabarit 4 : La conversation réconciliée remplie (deux apprentissages en tension)

```
RÉCONCILIATION D'APPRENTISSAGE — R-1        Cré le : 15/11/2024

APPRENTISSAGE A : « il faut 40 heures pour ajouter un modèle »
Source : le formateur vétéran, formé sur l'ancien pipeline
(saisie manuelle, montage manuel, vérification visuelle)

APPRENTISSAGE B : « il faut 1 heure pour ajouter un modèle »
Source : les nouveaux, formés sur le nouveau pipeline
(saisie guidée, presets, vérification automatisée)

LA TENSION : 40h contre 1h pour la même tâche — quelqu'un
se trompe, ou l'un des deux pipelines est mauvais.

L'INVESTIGATION :
- A a été appris dans : l'ancien pipeline (manuel).
- B a été appris dans : le nouveau pipeline (automatisé).

L'ARBITRAGE : les deux disent vrai — ils ne parlent pas du
même travail. A mesure l'artisanat complet ; B mesure l'effort
de l'outil. La tâche n'est pas la même, parce que le pipeline
a changé le travail.

SI LA TENSION ÉTAIT CULTURELLE : si le vétéran défendait son
ancien pipeline comme une identité (« notre façon de faire »)
plutôt que comme une mesure d'effort, l'arbitrage léger ne
suffirait pas — ce serait une réconciliation du LEGACY, et le
livre 2 en serait le manuel. Ici, les deux parties acceptent
la mesure d'effort comme mesure d'effort : l'arbitrage tient.

LE NOUVEL APPRENTISSAGE : « quand deux mesures du même intitulé
divergent, chercher si le travail sous-jacent a changé — la
divergence peut révéler une transformation, pas une erreur. »
→ MEM-055, relié à J-3 (les heures déclarées).
```

---

*Fin des gabarits remplis du niveau 7.*
