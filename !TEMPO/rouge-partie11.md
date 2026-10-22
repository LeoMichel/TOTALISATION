
---

# Partie 11 : Les fiches-outils du praticien niveau 1

Chaque fiche est un outil tenu en une page, avec son usage, son format, et son exemple rempli. Elles sont conçues pour être imprimées, utilisées en atelier, et archivées au centre d'excellence une fois complétées.

## Fiche 1 : La fiche de spécification

**Usage :** pour chaque demande avant implémentation. Une demande, une fiche.

**Format :**

```
SPECIFICATION — [ID de la demande]          Date : ____
Titre : ______________________________________________

CONTEXTE (2-3 lignes) :
_______________________________________________________

BESOIN (le problème, pas la solution) :
_______________________________________________________

COMPORTEMENT ATTENDU (SI... ALORS...) :
1. SI _______________ ALORS _______________________
2. SI _______________ ALORS _______________________
3. SI _______________ ALORS _______________________

RÈGLES DE VALIDATION (comment on vérifie) :
_______________________________________________________

CAS LIMITES (les frontières) :
- ___________________________________________________
- ___________________________________________________

NON-BESOINS (ce qu'on ne fait pas) :
_______________________________________________________

Revue : dev ______ test ______ demandeur ______ (date : ____)
```

**Exemple rempli (extrait de la mission Faucon) :**

```
SPECIFICATION — DEM-2024-117          Date : 24 juin
Titre : Filtre combiné du rapport X

CONTEXTE : Le rapport X permet de filtrer par colonne. Les utilisateurs
combinent des filtres sans savoir que le comportement change.

BESOIN : Comprendre et prédire le résultat d'une combinaison de filtres,
y compris quand une colonne contient des valeurs vides.

COMPORTEMENT ATTENDU :
1. SI la colonne 1 est vide (valeur nulle) ALORS la ligne n'est PAS
   exclue par le filtre de la colonne 1.
2. SI deux filtres sont actifs ALORS ils se combinent par ET logique.
3. SI aucun filtre n'est actif ALORS toutes les lignes apparaissent
   (inchangé).

RÈGLES DE VALIDATION : les 3 comportements vérifiables en requête directe.

CAS LIMITES :
- Données historiques migrées avec nuls « métier » (non renseigné à l'époque) :
  traitées comme les autres nuls, pas de cas spécial.
- Plus de 3 filtres actifs simultanés : même règle de combinaison ET.

NON-BESOINS : pas de filtre OU, pas de sauvegarde de combinaisons nommées
(reportée à DEM-2024-131).

Revue : dev (S.M.) ✓ test (L.T.) ✓ demandeur (P.G.) ✓ (25 juin)
```

**Le test de qualité de la fiche :** un développeur peut implémenter sans poser de question. S'il pose une question, la fiche a un trou — et le trou est corrigé dans la fiche (pas seulement dans la conversation), pour la prochaine fois.

## Fiche 2 : La fiche de bug

**Usage :** pour chaque bug priorisé. Elle remplace le « priorité haute » par une décision argumentée.

**Format :**

```
BUG — [ID]                    Décidé le : ____
Titre : ______________________________________________

SYMPTÔME observé (factuel) :
_______________________________________________________

FRÉQUENCE :  ____ fois / ____ période   (mesuré, pas estimé)
IMPACT : qui est touché, à quoi il perd accès :
_______________________________________________________
RISQUE DU REPORT (ce qui se passe si on attend) :
_______________________________________________________

PRIORITÉ : critique / majeur / mineur   (selon les critères du 18 juin)
JUSTIFICATION en une phrase :
_______________________________________________________

DÉROGATION (si priorisée devant sa catégorie) :
Qui décide : ______ Pourquoi : ______ Jusqu'à quand : ______
Ce qu'on apprend : ___________________________________
```

**Exemple rempli :**

```
BUG — BUG-1247                Décidé le : 26 juin
Titre : Filtre combiné ignore les valeurs nulles

SYMPTÔME : les lignes avec valeur nulle en colonne 1 disparaissent
du rapport X quand un second filtre est actif.

FRÉQUENCE : 11 fois / 2 semaines (tickets support, mesurés)
IMPACT : les utilisateurs du rapport X perdent 30 à 40 % des lignes
attendues ; deux clients ont signalé des écarts de chiffres.
RISQUE DU REPORT : défiance envers les chiffres du rapport (le rapport
est utilisé pour des décisions budgétaires).

PRIORITÉ : majeur
JUSTIFICATION : fréquence mesurée élevée + impact sur décisions
budgétaires ; pas critique (contournement : rapport sans filtre).

DÉROGATION : aucune.
```

## Fiche 3 : La grille Go/No-Go

**Usage :** une grille par livraison. Voir le format complet en annexe A6 ; la version niveau 1 ci-dessous tient sur une page.

**Format :**

```
GO / NO-GO — [Version]                    Date : ____
Décideur : __________  Animation : __________

CRITÈRES (cocher avec la preuve nommée) :
[ ] Cas de validation exécutés    Preuve : ________________
[ ] Bugs critiques : 0 ou dérogation    Preuve : ________________
[ ] Spécification et code alignés    Preuve : ________________
[ ] Risques connus et acceptés    Preuve : ________________
[ ] Note de diffusion prête    Preuve : ________________

DÉCISION : Go / Go avec réserves / No-Go

RÉSERVES (une phrase chacune : quoi, qui, quand) :
1. ___________________________________________________
2. ___________________________________________________

COMPTE RENDU ARCHIVÉ LE : __________
```

**La règle d'or de la fiche :** le compte rendu est rempli pendant la cérémonie, pas après. Un compte rendu « plus tard » n'existe pas — il est remplacé par des souvenirs divergents.

## Fiche 4 : La fiche de confirmation

**Usage :** 1 à 4 semaines après chaque diffusion. La grande boucle, sur une page.

**Format :**

```
CONFIRMATION — [Version livrée]           Date : ____
Demandeur : __________  Élicitation d'origine : [ID]

CRITÈRES DE SUCCÈS DE L'ÉLICITATION :
1. _______________ → atteint ? oui / partiel / non  (comment le sait-on)
2. _______________ → atteint ? oui / partiel / non
3. _______________ → atteint ? oui / partiel / non

USAGE RÉEL observé :
- Ce qui est utilisé comme prévu : _____________________
- Ce qui est utilisé autrement : _______________________
- Ce qui n'est pas utilisé : ___________________________

CE QU'ON APPREND (pour la prochaine élicitation) :
1. ___________________________________________________
2. ___________________________________________________

AJUSTEMENTS proposés : _________________________________
```

**Exemple rempli (extrait réel) :**

```
CONFIRMATION — Version 2.3 (rapport X)    Date : 17 juillet
Demandeur : P.G. (chef d'équipe)  Élicitation : DEM-2024-098

CRITÈRES DE SUCCÈS :
1. « Comprendre le résultat d'une combinaison de filtres »
   → atteint (P.G. démontre la combinaison attendue)
2. « Les chiffres concordent avec l'outil comptable »
   → partiel (concordent sauf pour les postes annulés — non élicité)
3. « Utilisé par les 3 équipes sans formation »
   → partiel (2 équipes sur 3 ; la 3e utilise encore l'export Excel)

USAGE RÉEL :
- Utilisé comme prévu : filtre simple, export mensuel
- Utilisé autrement : le filtre « colonne vide » est utilisé pour
  trouver les enregistrements incomplets (usage non prévu, utile)
- Non utilisé : la sauvegarde de filtres (personne ne l'a trouvé)

CE QU'ON APPREND :
1. Le critère « postes annulés » n'avait pas été élicité — l'élicitation
   doit inclure le traitement des enregistrements annulés.
2. La 3e équipe n'a pas été formée ; l'export Excel est son point d'entrée.
   → prochaine élicitation : demander l'outil actuel AVANT de proposer.

AJUSTEMENTS : ticket DEM-2024-124 (postes annulés) ; question d'outillage
pour la découverte des fonctions (la sauvegarde existe mais est invisible).
```

**Ce que cet exemple montre :** la confirmation a produit trois apprentissages concrets, dont deux modifiablent l'élicitation suivante. C'est exactement la grande boucle : la confirmation n'est pas un point d'honneur, c'est une machine à apprendre.

## Fiche 5 : Le registre des décisions

**Usage :** une ligne par décision prise en cérémonie (Go/No-Go, point de qualité, revue). Le registre est la mémoire exécutable de l'équipe.

**Format :**

| Date | Décision | Contexte (preuve) | Décideur | Levée / révision |
|---|---|---|---|---|
| | | | | |

**Exemple rempli (extrait d'un mois réel) :**

| Date | Décision | Contexte | Décideur | Levée |
|---|---|---|---|---|
| 03/07 | No-Go v2.2, dérogation | Test intermittent 1/20 (BUG-1301) | C.F. | 06/07 — corrigé |
| 10/07 | Sprint de synchronisation doc (4 divergences) | Signal doc/modèle à 4 | Équipe | 17/07 — fait |
| 17/07 | Bug-1247 priorisé majeur (pas critique) | Fréquence 11/2 sem. + impact budgétaire | Équipe + P.G. | — |
| 24/07 | Acheter la licence outil de test automatisé | E8 : 40 % des reprises = absence de tests | Sponsor | Reçu 02/08 |
| 31/07 | Reporter la confirmation DEM-118 (client absent) | Client en congés | L.T. | 14/08 |

**Ce que ce registre montre :** des décisions de nature variée (technique, organisationnelle, budgétaire) avec le même format. Et surtout : la décision du 24/07 — le budget accordé grâce au chiffrage E8. Le registre est aussi la mémoire de ce que la méthode a permis d'obtenir.

## Fiche 6 : Le tableau de bord minimal

**Usage :** la semaine 1 en installe un ; le niveau 1 n'en a besoin que d'un seul, mais vivant.

**Format :**

| Métrique | Valeur | Tendance | Décision si rouge | Décideur |
|---|---|---|---|---|
| Taux de reprise | | | | |
| Bugs critiques ouverts | | | | |
| Demandes spécifiées avant code (%) | | | | |

**Le conseil de conception :** une métrique que l'équipe regarde spontanément vaut mieux que trois métriques parfaites que personne ne consulte. Commencez avec une seule. La deuxième se mérite : elle arrive quand la première a déclenché une décision réelle.

## Comment utiliser les fiches

- **Imprimez-les** et gardez-les dans l'atelier. La version numérique est pour l'archivage ; la version papier est pour le travail.
- **Complétez-les pendant**, pas après. Une fiche remplie après la réunion est un souvenir ; pendant, c'est une preuve.
- **Archivez-les** au centre d'excellence avec leur date. Six mois plus tard, les fiches archivées sont votre historique — et la preuve de votre progression.

Le niveau 1 tient en six fiches. Ce n'est pas peu : c'est exactement ce qu'il faut pour que la qualité devienne visible, discutable et transmissible. Le niveau 2 (ORANGE) leur donnera des modèles, des outils et de l'automatisation — mais les six fiches resteront le socle : c'est sur elles que tout le reste se construit.
