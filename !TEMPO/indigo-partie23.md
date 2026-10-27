
---

# Partie 23 : Les gabarits de prévention du niveau 6 — guide des remplissages

Les gabarits du niveau 6 ont été présentés dans les parties précédentes. Cette partie avance dans les gabarits les plus utiles — ceux qui font tomber les frontières du niveau 6.

## Gabarit 1 : Le registre des signaux faibles

```
REGISTRE DES SIGNAUX FAIBLES          Tenu par : L.N. (veille)

| # | Date | Signal (observation) | Qui | Tendance? | Confirmations | Élicitation? |
|---|------|---------------------|-----|-----------|---------------|--------------|
| 1 | 02/09 | build de nuit +40 min | L.N. | OUI | S.M. + build team | OUI |
| 2 | 05/09 | temps de réponse API +40% | S.M. | OUI | J.D. | OUI |
| 3 | 08/09 | docs divergent du modèle | J.D. | NON | — | — |
| 4 | 11/09 | tests flaky (3/ semaine) | L.N. | OUI | 2 personnes | OUI |
| 5 | 14/09 | build de nuit +40 min | L.N. | = signal #1 | — | — |
| 6 | 16/09 | tests flaky (4/ semaine) | L.N. | = signal #4 | — | — |

RÈGLES DU REGISTRE :
- Une ligne = une observation (pas une interprétation).
- Un signal répété = une tendance (les lignes se marquent "= signal #n").
- Une tendance avec 2 confirmations indépendantes = élicitation déclenchée.
- Le registre est relu chaque semaine à l'atelier de prévention.
```

**Ce que le registre fait** : il transforme les observations en informations. Une observation isolée est un bruit — une tendance confirmée est un signal. Le registre est le lieu où le bruit devient signal (et le signal devient chantier).

## Gabarit 2 : Le chiffrage de morsure

```
CHIFFRAGE DE MORSURE                   Chantier : P-7
Dommage évité : la panne de build (le temps de dépassement
la fenêtre d'intégration continue, 8 personnes bloquées)

SANS PRÉVENTION (hypothèse) :
- Dommage : panne de build — 8 personnes × 5 jours = 40 personnes-jours
- Coût : blocage d'équipe, livraison retardée, moral
- Probabilité : 80% (la tendance était constante, +2 min/semaine)

AVEC PRÉVENTION (réel) :
- Action : 2 heures de correction (cache de téléchargement)
- Coût : 2 heures (une personne)
- Morsure : ~40 personnes-jours évités pour 2 heures investies
- Ratio : 1:20

ENTRÉE MÉMOIRE : MEM-042 (règle active : surveiller la tendance
du temps de build après toute modification d'infrastructure)
```

**Ce que le chiffrage fait** : il transforme la prévention en argument. Une prévention sans morsure est une dépense — une prévention avec morsure est un investissement. Le chiffrage est le moment où la prévention devient défendable (au manager, au budget, à l'équipe).

## Gabarit 3 : La lettre de veille — gabarit avancé (avec projections)

```
LETTRE DE VEILLE — 28/09          Envoyée par : L.N. (veille)

VALEURS vs SEUILS (avec marges) :
- Temps de réponse API : 240 ms (seuil 500) — marge 48%
- Taux d'erreur HTTP : 0,1% (seuil 2%) — marge 20×
- Temps de build de nuit : 34 min (seuil 30) — ⚠ SEUIL FRANCHI
- Divergences doc/modèle : 1 (seuil 2) — marge 50%

TENDANCES (8 semaines de données) :
- Temps de build : 28 → 42 min (montée, +2 min/semaine)
  → PROJECTION : dans 4 semaines, 42 + 8 = 50 min
  → ZONE D'ALERTE : 50 min (dépassement de la fenêtre CI)
  → ACTION : chantier P-7 (porteur M.G., échéance 30/09)
- Temps de réponse API : 230 → 240 ms (stable)
- Taux d'erreur : 0,1% → 0,1% (stable)

MORSURES DOCUMENTÉES CE MOIS :
- P-7 : 40 personnes-jours évités (ratio 1:20) — MEM-042

ALERTES :
1. Temps de build : seuil franchi, tendance montante.
   Action : chantier P-7 en cours (livraison prévue 30/09).
   La lettre du 12/10 vérifiera la correction.

CONCLUSION : 1 alerte (traitée), 0 incident. 1 zone de
vigilance (infrastructure de build).

Prochaine lettre : 12/10.
```

**Ce que le gabarit avancé fait** : il transforme la lettre en veille. Une lettre qui ne montre que les valeurs est une surveillance — une lettre qui montre les tendances, les projections et les morsures est une veille. C'est la lettre qui prévient, pas celle qui constate.

## Gabarit 4 : La prévention de la prévention

```
PRÉVENTION DE LA PRÉVENTION           Revue : trimestrielle

La prévention peut échouer de 4 façons :
1. Le porteur sans temps (la prévention est une fiction)
2. L'échéance passée (la prévention est morte)
3. La morsure non mesurée (la prévention est une dépense)
4. La mémoire non remplie (la prévention n'est pas transmissible)

CE TRIMESTRE :
| Chantier | Porteur | Échéance | Morsure | Mémoire |
|----------|---------|----------|---------|---------|
| P-7 | M.G. | 30/09 | 40 pj (ratio 1:20) | MEM-042 ✓ |
| P-8 | S.M. | 15/09 | non mesurée | — ✗ |
| P-9 | J.D. | 30/09 | reporté 1× | — |
| P-10 | L.N. | 15/10 | en cours | — |

VERDICT :
- P-7 : prévention réelle (morsure + mémoire)
- P-8 : prévention dépense (morsure non mesurée) → à mesurer
- P-9 : prévention à risque (reporté 1×) → à traiter ou abandonner
- P-10 : prévention en cours

ACTION :
- Mesurer la morsure P-8 (avant la fin du mois)
- Traiter P-9 (ou l'abandonner documenté — un chantier reporté
  2× est abandonné)
- Vérifier la capacité préventive de P-10 (le porteur a-t-il
  son temps réservé ?)
```

**Ce que le gabarit fait** : il transforme la prévention en discipline. Les chantiers de prévention vivent ou meurent — et le gabarit documente les deux (les morsures réelles, les morsures négatives, les abandons). Une prévention jamais revue est une prévention morte.

## Gabarit 5 : La transmission du niveau 6

```
TRANSMISSION DU NIVEAU 6              Nouveau praticien : S.M.
Date de début : 01/09                 Durée : 30 jours

SEMAINE 1 — Écouter :
- S.M. observe les signaux faibles de l'équipe (5-10 observations)
- S.M. note les observations sans les interpréter
- Le praticien ne fait pas à la place

SEMAINE 2 — Trier :
- S.M. trie les observations : tendance vs isolé
- S.M. demande les confirmations indépendantes
- 1-2 tendances confirmées

SEMAINE 3 — Poser :
- S.M. conduit le premier atelier de prévention
- S.M. pose 1-2 chantiers (avec porteurs, échéances)
- Le praticien accompagne, ne fait pas

SEMAINE 4 — Mesurer :
- S.M. écrit la première lettre de veille
- S.M. consulte la mémoire sur un chantier
- S.M. documente ce que la consultation a révélé

VERDICT (30 jours) :
- Les rituels tiennent-ils sans le praticien ?
- Les chantiers sont-ils portés par l'équipe ?
- Les morsures sont-elles documentées ?
- Si oui : transmission réussie. Si non : la prévention
  dépend encore du praticien — reprendre.
```

**Ce que le gabarit fait** : il transforme la transmission en test. La transmission du niveau 6 n'est pas une description — c'est une pratique. Le nouveau praticien fait (écoute, trie, pose, mesure) ; l'ancien praticien accompagne (jamais à la place). Le test est le même : les rituels tiennent-ils sans le praticien ?

---

*Fin des gabarits de prévention du niveau 6.*
