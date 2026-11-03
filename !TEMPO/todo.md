# Roadmap - Choses à faire

Légende : `[ ]` à faire · `[~]` en cours · `[x]` terminé

> Objectif : produire les **9 livres TOTALISATION** au format `.md` à partir du dossier `ideas/`.
> L01 = L'éveil · L02 = LEGACY (toute la différence par la réconciliation) · L03 à L09 = les 7 livres Guidance couleurs (ROUGE → VIOLET), livres de **pratique opérationnelle** (exercices, ateliers, formations, travaux, pratiques opérationnelles, évaluations).
> Cible : **45 000 mots minimum par livre**. Statut au 2026-11-03 : **les 9 livres atteignent la cible**.

---

## 0. Rappels et consignes (à garder en tête)

- Écrire **TOTALISATION** (et non "ToTAL" ni "TOTAL") dans les textes courants.
- Marque : le logotype est **T̥T̯L̩S̯T̩˜**.
- Pas de tiret cadratin dans les textes : utiliser la virgule, le deux-points, les parenthèses, ou le tiret simple " - ".
- Guillemets droits `""` (pas de guillemets français).
- Ton clair, honnête, accrocheur : garder l'intérêt du lecteur.
- `ideas/` est en **lecture seule**. Les scripts vont dans `automata/`, le temporaire dans `!TEMPO/`.
- Site web : **www.totalisation.com**
- Langue : **français canadien**, expressions québécoises avec parcimonie ; termes anglais courants conservés (*backlog*, *sprint*, *pipeline*...), équivalent français (GDT/OQLF) entre parenthèses à la première occurrence.
- Matière : toujours **puiser dans `ideas/`** (anecdotes, tranches de vie, héritage). C'est ce qui donne du vivant aux livres. Ne jamais inventer : noter ce qui manque en todo.
- Anti-duplication : chaque livre a sa propre identité. Si un sujet appartient à un autre livre, y renvoyer au lieu de le réécrire.
- **Répartition :** la théorie, les définitions et le glossaire restent dans L01/L02. Les 7 livres couleurs sont **100 % pratique** : ateliers, exercices, formations, travaux, évaluations. Rien de théorique.
- **Mission Faucon / Opal-RT :** l'expérience vécue occupe **uniquement les 6 premières semaines du livre ROUGE** (les semaines 5-6 sont post-mandat : transit, ancre). Les pages 1 à 4 du ROUGE restent dans les 4 premières semaines.

---

## 1. Décisions de cadrage (tranchées)

- [x] Format du livre imprimé (poche 13 × 20 cm, souple, noir et blanc)
- [x] Nombre de mots cible par livre (45 000 minimum)
- [x] **Nombre de livres : 9** (consolidé depuis le plan initial de 21, abandonné)
- [x] Public prioritaire (audience large : Agile, QA, dev, archi, PO/PM, CTO...)
- [x] Les livres couleurs = pratique seulement, pas de théorie
- [x] Faucon/Opal-RT confiné aux 6 premières semaines du ROUGE

---

## 2. Les 9 livres - état

| # | Livre | Fichier (dans `livres/`) | Mots | Statut |
|---|-------|--------------------------|------|--------|
| L01 | L'éveil de la TOTALISATION | `T̥T̯L̩S̯T̩˜ ❖ L'éveil de la TOTALISATION.md` | ~84 000 | [x] Terminé |
| L02 | Toute la différence par la réconciliation du LEGACY | `T̥T̯L̩S̯T̩˜ ❖ Toute la différence par la réconciliation du ''LEGACY''.md` | ~46 300 | [x] Terminé |
| L03 | Guidance opérationnelle du niveau (1) ROUGE | `T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (1) ROUGE.md` | ~50 700 | [x] Terminé |
| L04 | Guidance opérationnelle du niveau (2) ORANGE | `T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (2) ORANGE.md` | ~47 200 | [x] Terminé |
| L05 | Guidance opérationnelle du niveau (3) JAUNE | `T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (3) JAUNE.md` | ~47 400 | [x] Terminé |
| L06 | Guidance opérationnelle du niveau (4) VERT | `T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (4) VERT.md` | ~47 300 | [x] Terminé |
| L07 | Guidance opérationnelle du niveau (5) BLEU | `T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (5) BLEU.md` | ~47 600 | [x] Terminé |
| L08 | Guidance opérationnelle du niveau (6) INDIGO | `T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (6) INDIGO.md` | ~48 000 | [x] Terminé |
| L09 | Guidance opérationnelle du niveau (7) VIOLET | `T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (7) VIOLET.md` | ~47 300 | [x] Terminé |

Total : ≈ 462 300 mots. Validation par comptage `Get-Content -Raw` + split mots.

> L09 VIOLET a un rôle particulier : conclusion de la collection, passage à l'autonomie et à la maîtrise (TOTALISATION master). La suite s'y fait par amélioration continue : tout ce qu'il faut est en place, il faut juste continuer.

---

## 3. Matière `ideas/` - exploitation

- [x] Extraction complète des 40 fichiers / 4 sous-dossiers de `ideas/` (21,4 Mo) vers `!TEMPO/ideas-extract-complet/` et `!TEMPO/acaq-final/`
- [x] 28 documents ACAQ-OPAL exploités (Mission Faucon → ROUGE, semaines 1 à 6)
- [x] 6 documents Mission Faucon exploités
- [x] 3 documents ToTAL docx exploités
- [x] `vecu.txt` lu au complet, vécu réparti dans les livres appropriés
- [x] `petal.zip` : 3 documents RH seulement (avantages sociaux, bonification, CV) - non exploitable pour le contenu (0 %), noté comme faux négatif
- [x] Anciens brouillons de livres (L1 Origine parties A/B/C, L15 Guide Rouge parties A/B/C, etc.) exploit] Inventaire complet et pourcentage d'utilisation : voir `!TEMPO/INVENTAIRE_IDEAS_COMPLET_v2.md`

---

## 4. Documentation de la collection (alignée sur 9 livres)

- [x] `README.md` - réécrit proprement, 9 livres, comptes de mots réels, sans mojibake
- [x] `PLAN_COLLECTION.md` - aligné sur la structure 9 livres
- [x] `!TEMPO/todo.md` - le présent fichier
- [x] `!TEMPO/ETAT_IDEAS.md` - aligné 9 livres + acquisitions récentes (guides L17/Jaune/Orange/Rouge, SRC_L02, SRC_COE_v2)
- [x] `!TEMPO/INVENTAIRE_IDEAS_COMPLET_v2.md` - à jour
- [x] `!TEMPO/PLAN_PLACEMENT_GLOBAL.md` - à jour

---

## 5. Reste à faire (prochaines étapes)

- [ ] QA finale par livre : aucun `[À remplir]`, aucune prescription incomplète, ROUGE pages 1-4 dans les 4 premières semaines, chaque livre ≥ 45 000 mots
- [x] Nettoyer `!TEMPO/petal-extrait/` (contenu RH non exploitable) : retiré du dépôt git
- [x] `!TEMPO/livrables.tar.gz` (ancienne structure 21 livres) : retiré du dépôt git
- [x] Commit final + `git push origin main` (push réussi 2026-11-03 : 1114076..b7df02c) (le push précédent a été interrompu par une demande d'authentification)
- [ ] Couvertures d'images (cover-L1 à cover-L9) si disponible
- [ ] Préparer l'export imprimé (PDF) par livre
