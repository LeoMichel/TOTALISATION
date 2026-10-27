
---

# Partie 25 : Le bilan de l'année préventive — gabarit détaillé

Le bilan de l'année préventive est le rituel annuel du praticien du niveau 6. Il répond à cinq questions — chacune avec ses chiffres, ses apprentissages, et ses recommandations. Ce gabarit est rempli sur la base de 12 mois de pratique réelle.

## Page 1 — Les chiffres de l'année

**Les incidents évités :**

| Incident évité | Chantier | Porteur | Coût évité | Coût prévention |
|---|---|---|---|---|
| Panne de build (fenêtre CI) | P-7 | M.G. | 40 personnes-jours | 2 h |
| Dégradation API (dépasser 500 ms) | P-11 | S.M. | 15 jours de latence | 3 h |
| Divergence doc critique (déploiement faussé) | P-14 | L.N. | 3 jours de debug | 4 h |
| **Total** | **3 chantiers livrés** | — | **~55 jours-personnes** | **9 h** |

**Les incidents NON évités (les chantiers abandonnés ou reportés) :**

| Incident survenu | Chantier (abandonné) | Cause de l'abandon | Coût du dommage |
|---|---|---|---|
| Régression migration données | P-9 (reporté 2×, abandonné) | Porteur en congés, non remplacé | 4 jours de debug |
| Divergence doc (fournisseur tiers) | P-16 (jamais posé) | Signal confirmé mais chantier non posé | 2 jours de correction |

**Ce que la page 1 dit :** 3 incidents évités (55 jours-personnes économisés pour 9 heures investies), 2 incidents survenus (6 jours-personnes de dommage pour 0 heure de prévention faite). Le ratio global : la prévention a coûté 9 heures et évité 55 jours. La non-prévention a coûté 6 jours et n'a rien coûté en prévention (car elle n'a pas été faite). **L'arbitrage est clair : la prévention a un ROI de 60:1 quand elle est faite — et un coût infini quand elle ne l'est pas.**

## Page 2 — Les leçons (3 apprentissages)

**Apprentissage 1 — Le signal faible est plus fiable que l'incident signalé.**
Ce que nous avions prédit : les tendances (le build monte, l'API dégrade) seraient les premiers signaux. Ce qui est arrivé : les tendances se sont confirmées 8 fois sur 9, et les signaux faibles (les observations individuelles) ont été les premiers à détecter les tendances — avant les métriques. Ce que cela apprend : le signal faible est la première ligne de défense, et les métriques sont la seconde. Ne pas les confondre.

**Apprentissage 2 — La capacité préventive est la condition nécessaire (mais pas suffisante).**
Ce que nous avions prédit : avec 10 % de capacité réservée, les chantiers se livreraient. Ce qui est arrivé : 3 chantiers livrés, 1 abandonné (porteur en congés, non remplacé), 1 jamais posé (le signal confirmé n'a pas déclenché le chantier — parce que le praticien n'était pas là pour le poser). Ce que cela apprend : la capacité préventive est nécessaire mais pas suffisante — le praticien ne doit pas être le seul à poser les chantiers, et le porteur doit avoir un relève (l'absence d'un porteur ne doit pas tuer un chantier).

**Apprentissage 3 — La lettre de veille est le rituel le plus rentable.**
Ce que nous avions prédit : les lettres de veille seraient lues par l'équipe. Ce qui est arrivé : les lettres ont été lues par l'équipe (92 % d'ouverture moyenne) ET par le manager (qui a utilisé les marges dans ses arbitrages). Ce que cela apprend : la lettre de veille est le seul document du niveau 6 qui sert à la fois à l'équipe (l'anticipation) et au manager (l'arbitrage). C'est le pont entre le niveau 6 et le niveau 5 — et il vaut 30 minutes par semaine.

## Page 3 — La résolution

**Ce que je m'engage à faire l'année prochaine :** conserver la règle de capacité préventive (10 %), former un praticien de relève (S.M. en binôme sur les chantiers P-16 et P-17), et intégrer les apprentissages à la spécification du niveau 7 (le praticien du niveau 7 aura besoin de cette mémoire).

---

*Fin du gabarit de bilan annuel préventif.*
