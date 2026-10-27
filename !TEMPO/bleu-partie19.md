
---

# Partie 19 : Les gabarits du niveau 5 remplis

Cette partie contient les gabarits de gouvernance du niveau 5 — remplis avec des exemples réels. Le praticien N5 les utilise comme point de départ, et les adapte au contexte de son organisation.

## Gabarit 1 : la charte du comité

```
CHARTE DU COMITÉ DE GOUVERNANCE [nom de l'organisation]
Version 1.2 — votée le [date] par les représentants de [n] équipes

1. PÉRIMÈTRE
Le comité traite les décisions qui dépassent le périmètre d'une équipe :
- les standards partagés (naming, déploiement, tests, revue)
- les seuils de qualité (SLA, taux de retour, couverture)
- les dépendances inter-équipes (chantiers communs, arbitrages)
- les règles du registre (documentation, révision, transmission)
Le comité ne traite pas :
- les décisions techniques dans le périmètre d'une équipe
- les choix de produit (priorités, roadmap)
- les questions d'équipe (composition, évaluation, carrières)

2. COMPOSITION
- Un représentant par équipe (nommé par son équipe, mandat de 6 mois)
- Un praticien de gouvernance (facilitateur, non-décideur)
- Un sponsor (décideur final en cas de blocage, co-signataire du registre)

3. FRÉQUENCE
- Comité complet : mensuel (60 minutes)
- Décisions urgentes : la règle d'urgence (décision solo documentée, re-examen obligatoire)
- Décisions asynchrones : la règle du délai (5 jours, silence = POUR par défaut)

4. DOCUMENTATION
Chaque décision est documentée dans le registre :
- la décision (une phrase, impérative)
- les preuves (données, cas réels, mesures)
- les POUR et les CONTRE (nommés, avec leurs arguments)
- la condition de révision (ce qui changerait l'avis)
- la date de re-examen (si applicable)

5. RÉVISION
La charte est révisée à chaque bilan annuel, ou par la convention de révision :
- toute demande de révision est documentée dans le registre
- le comité vote la révision (majorité simple des représentants)
- les révisions sont numérotées (v1.2, v1.3...) et datées
```

## Gabarit 2 : la fiche de décision du registre

```
REGISTRE DES DÉCISIONS — FICHE [numéro]
Date : [date]
Décision : [une phrase, impérative]
Périmètre : [quelles équipes, quels cas]
Preuves : [données, mesures, cas réels — avec les chiffres]
POUR : [nom(s) — arguments]
CONTRE : [nom(s) — arguments]
Condition de révision : [ce qui changerait l'avis — contexte, donnée, événement]
Re-examen : [date — si applicable]
Décision d'urgence : [oui/non — si oui, re-examen obligatoire]
Co-signataire : [sponsor — signature, date]
```

## Gabarit 3 : la fiche de dérogation

```
FICHE DE DÉROGATION — [numéro]
Date : [date]
Équipe : [nom]
Standard concerné : [nom du standard, référence du registre]
Dérogation demandée : [ce qui est fait à la place du standard]
Justification : [pourquoi le contexte est différent — ou pourquoi le standard est inadapté]
Durée : [exception permanente / exception temporaire (jusqu'à [date])]
Traitement : [exception formalisée (ajout au standard) / révision du standard déclenchée / standard maintenu]
Décision : [accordée / refusée — avec les raisons]
```

## Gabarit 4 : le bilan à l'échelle

```
BILAN ANNUEL DE GOUVERNANCE — [année]
1. Les décisions du registre
   - Nombre de décisions : [n] (dont [n] d'urgence, [n] asynchrones)
   - Révisées : [n] (condition de révision déclenchée : [n])
   - Sans condition de révision : [n] — à re-documenter
2. Les dérogations
   - Nombre : [n] (par équipe : [détail])
   - Dérogations en série : [équipes — traitement : exception formalisée / révision]
3. Les équipes
   - Couverture réelle : [x] équipes sur [n] utilisent la gouvernance
   - Poches décoratives : [équipes — traitement : transmission ciblée]
4. La charte
   - Révisions : [n] (v1.0 → v1.[x])
   - Sujets non couverts : [liste — à traiter par la convention de révision]
5. Les preuves
   - Données : [les mesures qui montrent l'effet de la gouvernance]
   - Cas réels : [les décisions qui ont évité des dégâts, ou les manquements]
```

## L'usage des gabarits

Les gabarits ne sont pas des formulaires à remplir — ils sont des points de départ à adapter. La charte qui tient sur deux pages est une charte qui survit ; la charte qui tient sur onze pages est une charte qui meurt. Le registre qui documente chaque décision avec ses preuves est un registre vivant ; le registre qui documente les décisions sans preuves est un registre de façade.

Le praticien N5 qui utilise les gabarits apprend une chose : la forme (la fiche, la section, la colonne) protège la substance (la décision réelle, la preuve réelle, la condition réelle). La forme sans substance est une façade ; la substance sans forme est une anecdote. La gouvernance réelle est la substance dans la forme.
