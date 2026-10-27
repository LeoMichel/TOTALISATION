
---

# Partie 16 : Les gabarits remplis du niveau 6

Cette partie présente les gabarits remplis par une équipe réelle — pour montrer le niveau de spécificité attendu au niveau 6. TOTALISATION ne remplace jamais la parole de l'équipe : il cadre, garde, et rend transmissible.

## Gabarit 1 : Signal faible rempli

```
SIGNAL — 14/09                    Déposé par : L.N.
J'AI REMARQUÉ : le build de nuit prend plus de temps que
d'habitude (42 minutes au lieu de 28). Pas d'erreurs, mais
la tendance est montante depuis la migration de
l'infrastructure de build.

QUAND / COMBIEN DE FOIS : première observation le 02/09,
confirmé 4 fois en 8 jours de build.

CONTEXTE : les branches de la nouvelle infrastructure
de build (post-migration).
```

**La suite du signal (documentée dans la revue) :**
Le signal a été confirmé par deux autres personnes (S.M. et l'équipe de build). Trois confirmations en 8 jours : la règle des trois confirmations déclenche l'élicitation proactive. L'élicitation (avec le demandeur pressenti : l'équipe de build) a révélé une dépendance cachée (un téléchargement à chaque build au lieu du cache). Le chantier P-7 a été créé, corrigé en 2 heures, et la morsure mesurée : ~1 semaine de blocage d'équipe évitée.

## Gabarit 2 : Chantier de prévention rempli

```
CHANTIER DE PRÉVENTION — P-7      Cré le : 12/09
Origine : signal du 04/09 confirmé (build +40 min, tendance)

LE PROBLÈME : SI rien n'est fait, ALORS le build dépasse le
délai d'intégration continue dans ~6 semaines — panne de
build pour toute l'équipe, au pire moment (démonstration
client prévue).

LA PRÉVENTION : investiguer la régression de build,
identifier la cause, corriger.

PREUVE ATTENDUE :
- l'incident évité : la panne de build
- le temps épargné : les jours de blocage de l'équipe
- la tendance corrigée : le temps de build retourne
  sous 30 minutes

PORTEUR : M.G. — 4 heures réservées (capacité préventive)
ÉCHEANCE : 30/09
STATUT : livré le 06/09 — morsure mesurée

APRÈS LA MORSURE :
La morsure réelle : dépendance cachée (téléchargement
à chaque build au lieu du cache), introduite 3 semaines
plus tôt. Chiffrée : 2 heures de correction vs ~1 semaine
de blocage (8 personnes) évitée. Ratio : 1:20.
Documenté dans la mémoire : MEM-042.
```

## Gabarit 3 : Entrée de mémoire remplie

```
MÉMOIRE — MEM-042                  Cré le : 07/09
THÈME : infrastructure de build ; dépendances cachées

L'APPRENTISSAGE : les dépendances cachées (téléchargements
à chaque build) se voient dans le TEMPS de build, pas dans
les erreurs — surveiller la tendance, pas les échecs.

D'OÙ ÇA VIENT : chantier P-7 (signal faible confirmé).
Chiffré : 2 heures de correction vs ~1 semaine de blocage
d'équipe évitée (8 personnes × 5 jours = 40 personnes-jours).

LA RÈGLE ACTIVE : toute modification de l'infrastructure
de build est suivie d'une semaine de surveillance du temps
de build (tendance, pas seulement succès/échec).

RELIONS : MEM-017 (les API tiers changent sans préavis),
MEM-031 (les régressions silencieuses).
TYPE : règle active.
```

## Gabarit 4 : Consultation mémoire remplie

```
CONSULTATION MÉMOIRE — infrastructure de build
Date : 15/09   Consulté par : S.M.   Durée : 20 minutes

THÈMES CHERCHÉS : "infrastructure build", "migration",
"dépendance", "cache"

ENTRÉES TROUVÉES : MEM-042, MEM-017, MEM-031
- Applicables directement : MEM-042 (la règle active :
  surveiller la tendance après toute modification)
- Applicables avec adaptation : MEM-017 (API tiers — le
  pattern est similaire : les dépendances externes se
  voient dans le temps, pas dans les erreurs)
- Inapplicables : MEM-031 (régression silencieuse — le
  pattern concerne les données, pas l'infrastructure)

RÈGLES ACTIVES HÉRITÉES (intégrées à la spécification) :
- Toute modification de l'infrastructure de build est
  suivie d'une semaine de surveillance du temps de build.
- Les dépendances externes sont documentées et testées
  au moment de l'introduction, pas après.

CAS LIMITES HÉRITÉS (à ajouter) :
- Si la dépendance est ajoutée par un tiers (bibliothèque),
  le test de non-régression couvre le temps de build aussi
  (pas seulement le succès).

NOUVEAU APPRENTISSAGE (ce que la consultation révèle) :
La consultation a révélé que la surveillance du temps de
build devrait être automatisée (seuil d'alerte à 30 min).
→ nouvelle entrée MEM-056 : "les métriques d'infrastructure
  (temps de build, temps de test) doivent être surveillées
  automatiquement — la surveillance manuelle ne détecte
  pas les tendances lentes."
```

## Gabarit 5 : Lettre de veille remplie

```
LETTRE DE VEILLE — 28/09          Envoyée par : L.N. (veille)

ALERTE : OUI — 1 seuil franchi cette semaine.

SEUIL FRANCHI :
- Temps de build de nuit : 34 minutes (seuil : 30 min)
  Confirmé 4 fois cette semaine. Investigation ouverte
  (chantier P-7, porteur M.G., échéance 30/09).

VALEURS OBSERVÉES (vs seuils, sans alerte) :
- Temps de réponse API : 240 ms (seuil : 500) — marge 48%
- Taux d'erreur HTTP : 0,1% (seuil : 2%) — marge 20×
- Divergences doc/modèle : 1 (seuil : 2) — marge 50%

ÉVOLUTION vs PÉRIODE PRÉCÉDENTE :
Temps de build en hausse (28 → 42 min sur 4 semaines).
Tous les autres indicateurs stables.

ACTION : le chantier P-7 est en cours (livraison prévue
lundi 30/09). La lettre du 12/10 vérifiera si la tendance
est corrigée.

CONCLUSION : 1 alerte (traitée), 0 incident. Système sain,
1 zone de vigilance (infrastructure de build).

Prochaine lettre : 12/10.
```

## Gabarit 6 : Projection remplie

```
PROJECTION — Temps de build de nuit    Faite le : 02/09
Par : S.M.                             Horizon : 4 semaines

TENDANCE OBSERVÉE (8 semaines de données) :
28 min → 42 min (progression constante, +2 min/semaine)

PROJECTION : dans 4 semaines, le temps de build sera à
50 minutes. SI la tendance continue (aucune correction).

ZONE D'ALERTE : 45 minutes (le délai d'intégration
continue est à 50 minutes — au-delà, le build dépasse
la fenêtre).

VALIDATION RÉTROACTIVE (remplie le 30/09) :
Valeur réelle : 34 minutes (après correction P-7)
Écart : -16 min de la projection (car la correction
a été faite avant l'échéance)
Verdict : fiable (la projection sous "si rien ne
change" aurait été 50 min — la correction a changé
la tendance)
Action : la projection est conservée (fiable dans son
hypothèse), et la morsure P-7 est documentée dans la
mémoire (MEM-042).
```

---

*Fin des gabarits remplis du niveau 6.*
