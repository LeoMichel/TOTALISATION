
---

# Annexe F : Le carnet du praticien N3 — les fiches de frontière, de risque, de dépendance et de circuit

Le praticien du niveau 3 (le livre VERT) a une matière première nouvelle : la frontière. Ses fiches documentent les zones où les systèmes se touchent, les zones où les risques se concentrent, et les zones où les dépendances se cachent.

## Les quatre fiches (dans l'ordre d'usage)

1. La fiche de frontière (chaque échange entre deux systèmes : contrat, test, responsable)
2. La fiche de risque (chaque risque identifié : probabilité, impact, signal, parade)
3. La fiche de dépendance (chaque dépendance : type, criticité, alternative, plan B)
4. La fiche de circuit (chaque circuit de validation croisée : qui valide quoi, dans quel délai)

**Le principe de ces fiches :** au niveau 2, les fiches documentent une boucle interne. Au niveau 3, elles documentent les interactions entre systèmes et entre équipes — et c'est là que les risques se concentrent. La fiche de frontière est la plus importante : une frontière non documentée est une zone de friction invisible.

## La fiche de frontière remplie (extrait réel)

```
FRONTIÈRE — Service de paie ↔ Service de temps
Établie le : 6 septembre   Par : K.T.   Revue : trimestrielle

CONTRAT :
- Entrée : une liste de temps validés (format ISO, une ligne par
  jour-personne)
- Sortie : un statut de traitement (accepté, rejeté, motif)
- Délai garanti : 24 heures ouvrées
- Délai d'erreur : rejet motivé en 24 heures

TESTS DE FRONTIÈRE :
| Test | Cas | Résultat attendu | Fréquence |
|---|---|---|---|
| T1 | Temps validé normal | accepté | chaque nuit |
| T2 | Temps validé double | rejeté (motif) | chaque nuit |
| T3 | Temps hors période | rejeté (motif) | chaque nuit |
| T4 | Service de temps indisponible | 24h ouvrées, pas de perte | mensuel |

RESPONSABLES :
- Côté temps : M.V.   Côté paie : S.L.   Arbitre : le comité

JOURNAL DES FRICIONS (dernier mois) :
- 3 rejets de type T2 (doublons) — cause : la validation manuelle
  côté temps ne bloque pas le double envoi. Action : ajout d'un
  identifiant d'envoi unique. Propriétaire : M.V. Échéance : 30 oct.
```

**Ce que cette fiche montre :** une frontière documentée est une frontière vivante. Le journal des frictions transforme un échange technique en relation explicite entre deux responsables — et le test T4 mesure le comportement du système en défaillance, pas seulement son comportement nominal.

## La fiche de risque remplie

```
RISQUE — Dépendance au service de temps externe
Identifié le : 12 septembre   Par : K.T.   Revisé : 15 octobre

| Dimension | Évaluation |
|---|---|
| Probabilité | moyenne (le service a déjà eu 2 indisponibilités) |
| Impact | élevé (la paie est bloquée, 400 personnes) |
| Détection | le test T4 (mensuel) |
| Parade | file d'attente persistante + replay manuel |
| Coût de la parade | 2 jours de développement |

HISTORIQUE :
- 15 octobre : la parade est en production. Test T4 mensuel confirmé.
- 12 septembre : risque identifié dans le registre, sans parade.
- 3 août : première indisponibilité réelle (4 heures, paie retardée).

RÈGLE : un risque avec parade documentée est un risque géré.
Un risque sans parade est un pari. Le registre distingue les deux —
et le comité arbitre les paris.
```

**Le principe de la fiche de risque :** un risque documenté n'est pas un risque éliminé — il est un risque converti en décision. La colonne « parade » est la seule qui transforme le registre de risque en plan de prévention. Un registre sans parades est une liste d'inquiétudes.

## La fiche de dépendance remplie

```
DÉPENDANCE — Le service de paie dépend du service de temps
Documentée le : 12 septembre   Par : K.T.   Revisée : 15 octobre

| Dimension | Évaluation |
|---|---|
| Type | fonctionnelle (les temps alimentent la paie) |
| Criticité | bloquante (sans temps, pas de paie) |
| Alternative | saisie manuelle des temps (coût : 2 j-pers./mois) |
| Plan B | la saisie manuelle activée en cas d'indisponibilité > 24h |

TEST DU PLAN B :
- Testé le 20 septembre : la saisie manuelle a été activée en
  simulation pendant 2 heures. Résultat : la paie a pu tourner, avec
  3 jours de travail de correction. Le plan B fonctionne, mais coûte
  3 jours — il faut le savoir avant d'en avoir besoin.

RÈGLE : un plan B non testé est un plan B imaginaire. La fiche de
dépendance exige un test réel du plan B — au moins une fois par an.
```

**Le principe de la fiche de dépendance :** documenter une dépendance, c'est la rendre visible. Tester son plan B, c'est le rendre réel. La différence entre les deux est la différence entre le registre de conformité et la pratique du niveau 3.

## La fiche de circuit remplie

```
CIRCUIT — Validation croisée des changements de paie
Documenté le : 18 septembre   Par : S.L.

| Étape | Qui | Délai | Critère |
|---|---|---|---|
| 1. Proposition | développeur | jour J | la fiche de frontière est à jour |
| 2. Revue technique | pair | J+1 | tests de frontière passent |
| 3. Revue métier | M.V. (temps) | J+2 | les temps ne sont pas altérés |
| 4. Validation | comité | J+3 | le registre de risque est à jour |

FRICION OBSERVÉ : l'étape 3 a pris 4 jours au lieu de 2 en septembre.
Cause : M.V. était en congés sans relève. Action : une règle de
relève est ajoutée au circuit — chaque étape a une relève nommée.

RÈGLE : un circuit sans relève est un circuit fragile. La fiche de
circuit exige une relève nommée pour chaque étape — comme le chantier
de prévention exige un binôme.
```

**Le principe de la fiche de circuit :** un circuit de validation est une frontière entre équipes — il mérite la même rigueur qu'une frontière entre systèmes. Le journal des frictions du circuit documente non pas les bugs techniques, mais les frictions humaines — et la relève nommée est la parade.

## Le carnet du praticien N3 : le test

**Montrez-moi vos fiches de frontière.** Si chaque frontière a un contrat, des tests, des responsables et un journal des frictions, votre niveau 3 est réel. Si vos fiches sont des tables de conformité remplies après coup, votre niveau 3 est une documentation.

**Le test du plan B.** Montrez-moi la dernière fois que votre plan B a été testé en réel. Si la réponse est « jamais », votre fiche de dépendance est un document — pas une prévention.

**Le test de la relève.** Montrez-moi les relèves nommées de votre circuit. Si chaque étape a une relève, votre circuit survit aux congés. Sinon, il survit aux bonnes semaines — et c'est le comportement des systèmes qui fonctionnent en temps calme et échouent en temps réel.
