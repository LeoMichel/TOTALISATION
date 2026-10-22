
---

# Partie 16 : Les gabarits remplis du niveau 3

## Gabarit 1 : la séance Go/No-Go remplie (livraison du mardi 4 mars)

**Équipe :** Facturation, 9 personnes. **Séance :** vendredi 28 février, 10h00. **Décision visée :** Go pour mardi 4 mars.

**Critères Go/No-Go (les 12, avec leur statut) :**

| # | Critère | Seuil | Statut | Preuve |
|---|---------|-------|--------|--------|
| 1 | Pipeline vert sur main | 0 rouge | **Go** | Lien #4821, 27/02 18h |
| 2 | Tests bloquants au commit | 100 % | **Go** | 412/412 |
| 3 | Couverture sur code touché | ≥ 85 % | **Go** | 91 % |
| 4 | Analyse statique | 0 bloquant | **Go** | 0 bloquant, 3 informatifs |
| 5 | Trace de sécurité revue | Signée | **Go** | Signée 26/02 par M.D. |
| 6 | Note de version | Complète | **Go** | Rédigée 27/02 |
| 7 | Migration de données | Testée | **Go** (réserve levée 03/03) | Test sur copie prod, levée écrite |
| 8 | Plan de retour arrière | Documenté | **Go** | Doc §3.2, testé sur staging |
| 9 | Docs utilisateur | À jour | **Go** | 2 pages modifiées |
| 10 | Recette client | Validée | **Go** | PV 27/02 |
| 11 | Réserve ouverte bloquante | 0 | **Go** | 0 réserves ouvertes |
| 12 | Validation du chargé de livraison | Signée | **Go** | Signature prévue en séance |

**Réserves actives :** une seule, la migration de données (#7), avec sa levée écrite prévue le lundi 3 mars (test sur copie de production, 14h00). Si la levée échoue, la livraison passe au jeudi 6 mars — le No-Go partiel est donc assumé en séance avec sa date de rattrapage.

**Décision :** **Go conditionnel** — livrer mardi 4 mars à 9h00, sous condition de la levée de la réserve #7 le lundi 3 mars. Si la levée échoue, la séance de rattrapage est prévue lundi 3 mars 16h00 (15 minutes).

**Le compte rendu (5 lignes, gabarit respecté) :**
> Go conditionnel pour mardi 4/03 9h. 12/12 critères Go, 1 levée de réserve en attente (migration, lundi 14h, preuve écrite). Rattrapage lundi 16h si échec. Prochaine séance : mardi 4/03 15h (post-livraison, 10 min).

## Gabarit 2 : la lettre de veille bimensuelle remplie (période du 1er au 15 mars)

**Chargé de veille :** S.R. **Période :** 1er–15 mars. **Type :** rapport de non-alerte.

> **Lettre de veille — 1er au 15 mars**
>
> **Alertes :** aucune. Aucun seuil franchi durant la période.
>
> **Valeurs observées (vs seuils) :**
> - Temps de réponse API (moy. 95e percentile) : 240 ms (seuil : 500 ms) — marge 52 %
> - Taux d'erreur HTTP 5xx : 0,2 % (seuil : 2 %) — marge 10×
> - File d'attente des jobs nocturnes : 12 min max (seuil : 45 min) — marge 73 %
> - Taux de re-classification des demandes : 6 % (seuil d'alerte : 15 %) — marge 60 %
> - Dérogations actives : 1 (levée prévue 18/03, statut on track)
>
> **Évolution vs période précédente :** temps de réponse stable (+4 ms, bruit normal). Taux d'erreur stable. Taux de re-classification en baisse (9 % → 6 %) : l'effet de la révision des critères du 12/02 se confirme.
>
> **Points de vigilance (sans alerte) :** la dépendance externe «Paie-Lite» a annoncé une version majeure pour avril — impact à évaluer dans la lettre du 16–31 mars.
>
> **Conclusion :** système sain. Aucune action requise. Prochaine lettre : 31 mars.

## Gabarit 3 : le journal de re-classification rempli (semaine du 10 au 14 mars)

| Jour | Demande | Classe initiale | Classe finale | Raison (écrite, 1 ligne) | Par |
|------|---------|-----------------|---------------|--------------------------|-----|
| Lun | #1042 | Standard | Complexe | Impacts 3 intégrations, non vu au triage | L.M. |
| Mar | #1047 | Complexe | Standard | Après analyse : 1 seul fichier, aucune intégration | S.R. |
| Mer | #1051 | Simple | Standard | 3,5 h d'effort estimé (seuil simple : 2 h) | L.M. |
| Jeu | #1053 | Standard | Standard | (aucune) | — |
| Ven | #1056 | Simple | Simple | (aucune) | — |

**Lecture de la semaine :** 3 re-classifications sur 5 demandes (60 %) — au-dessus du seuil d'alerte de 15 % pour la semaine, mais sous la moyenne mensuelle. Les raisons sont toutes écrites et toutes liées à des critères mal évalués au triage (pas à des contournements). **Action :** les 3 cas alimentent la revue des critères de triage du dernier vendredi du mois.

## Gabarit 4 : la dérogation écrite remplie (critère rouge assumé)

> **Dérogation n° 2024-031**
>
> **Livraison visée :** v2.7.1 — mardi 18 mars, 9h00.
> **Critère concerné :** #9 (docs utilisateur à jour) — **statut : rouge** (1 page sur 4 non mise à jour : la page «Export comptable»).
> **Risque documenté :** les utilisateurs de l'export comptable (2 personnes identifiées) pourraient appliquer l'ancienne procédure — impact limité à une séance de support.
> **Condition de levée :** la page est mise à jour et publiée au plus tard le jeudi 20 mars, 12h00.
> **Demandeur :** T.B. (sponsor). **Assumé par :** T.B.
> **Décision de la séance :** Go avec dérogation n° 2024-031.
> **Vérification de levée :** jeudi 20 mars, 14h00 — **levée effective, preuve : lien doc #887.**
> **Statut final : RÉSOLUE — clôturée le 20/03.**

## Variantes contextuelles : adapter le niveau 3 à votre réalité

**Variante A — équipe de 4 personnes.** Les rôles tournent par quinzaine (pas par mois : trop long pour 4 personnes ; pas par semaine : trop de rotation). Le chargé de livraison et le chargé de veille peuvent être la même personne à condition que le binôme existe et tourne aussi. La séance Go/No-Go dure 10 minutes. La lettre de veille est mensuelle. Ne sacrifiez jamais : la règle du report écrit, la confirmation systématique, la dérogation écrite.

**Variante B — équipe distribuée sur 3 fuseaux.** La séance Go/No-Go a un horaire tournant (une semaine sur trois, chaque fuseau a la séance en heure locale raisonnable). Le compte rendu est écrit pendant la séance (pas après) et partagé immédiatement — pour les fuseaux absents, la preuve écrite remplace la présence. La décision conditionnelle devient la norme : le fuseau qui exécute la levée de réserve n'a pas besoin d'assister à la séance initiale, il a besoin de la preuve écrite de la condition.

**Variante C — équipe de support avec interruptions fréquentes.** Les SLA par classe intègrent une 4e classe : « urgence » (réponse < 2 h, mais pas de délai de résolution garanti — le travail interrompu est repris, pas perdu). La règle du report écrit s'applique aussi aux interruptions : chaque interruption d'une demande en cours est notée (qui, quand, pourquoi, retour prévu), et le taux de reprise correct est un seuil de veille.

**Variante D — réglementation forte (santé, finance).** Les douze critères Go/No-Go deviennent quinze : les trois critères réglementaires (audit trail complet, revue de conformité signée, traçabilité des approbations) sont **non dérogeables** — la dérogation écrite ne s'applique pas à eux, jamais. Les autres critères peuvent déroger. Cette distinction (dérogeable / non dérogeable) doit être explicite dans la grille, pas implicite dans les têtes.

**Variante E — l'équipe qui démarre le niveau 3 en cours de trimestre.** Ne commencez pas tous les rituels en même temps : la séance Go/No-Go d'abord (elle crée la demande de preuves), puis le SLA par classe (il organise la demande), puis la veille (elle surveille ce que les deux premiers produisent). Trois semaines entre chaque. Le forgeage en cascade évite l'essoufflement du « tout en même temps ».

## Le gabarit de la rétrospective du niveau 3 (trimestrielle)

**Durée :** 60 minutes. **Participants :** toute l'équipe + le praticien. **Format :**

1. **Les chiffres du trimestre** (10 min) : livraisons Go, No-Go, Go conditionnels, dérogations (actives/levées/résolues), re-classifications, alertes de veille. Sans commentaire — juste les nombres.
2. **Ce qui a tenu** (15 min) : quel rituel a survécu à une urgence réelle ? Quelle règle a été utile sans qu'on y pense ? Nommez les preuves, pas les impressions.
3. **Ce qui a rompu** (15 min) : quel rituel a été reporté sans être repris ? Quelle règle a été contournée ? Pas de coupables — des patterns.
4. **Ce qu'on forge au trimestre suivant** (15 min) : maximum 3 chantiers, chacun avec un porteur et une date. Pas de chantier « on devrait » — seulement des chantiers « X fait Y avant le Z ».
5. **La sortie** (5 min) : la carte de fragilité mise à jour, affichée, datée.
