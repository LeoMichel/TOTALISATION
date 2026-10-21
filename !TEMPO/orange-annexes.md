
### Annexe A1 : Modèle de charte de mission niveau 2

**Charte de mission : passage au niveau 2 de TOTALISATION, équipe pilote**

**Objectif :** monter l'équipe pilote du niveau 1 (minimum viable) au niveau 2 de TOTALISATION en 8 semaines : spécifications modélisées (MBT/BPMN), outillage automatisation/documentation, planification livraisons N2, qualimétrie N2, politiques/conventions, couverture par types de test, socle pour l'IA.

**Durée :** 8 semaines, du [date] au [date].

**Rôles :**
- Sponsor : [nom] (débloque, endosse, protège)
- Coach(s) : [nom(s)] (facilite, ne produit pas les modèles ni les tests)
- Équipe pilote : [membres] (modélise, automatise, documente, livre)
- Chargé de livraison : [nom] (anime les rituels N2 à partir de la semaine 6)
- Gardien du centre d'excellence : [nom] (à partir de la semaine 8)

**Règles :**
1. Chaque semaine produit un livrable publié dans le centre d'excellence.
2. Une spécification n'est valide que si elle est modélisée (ou justifiée par écrit).
3. L'automatisation et la documentation partagent la même source : le modèle.
4. L'IA assiste, ne remplace pas : toute production de l'IA est relue et validée par l'équipe.
5. Les décisions sont écrites, datées et publiées.

**Signature :** sponsor ____ coach ____ équipe ____ chargé de livraison ____ (date ____)

### Annexe A2 : Modèle de contrat qualité niveau 2

**Contrat qualité de l'équipe [nom] - version 2.0**

**Engagements de l'équipe :**
1. Aucune spécification critique n'est acceptée sans modèle BPMN associé (ou dérogation écrite).
2. Les tests automatisés sont générés ou dérivés des modèles MBT quand un modèle existe.
3. La documentation produit est synchronisée avec les modèles ; toute divergence est une dérogation écrite.
4. La couverture par types de test est maintenue à jour dans la matrice de couverture.
5. Le Go/No-Go de niveau 2 est fondé sur des preuves d'automatisation et de couverture, pas sur des impressions.
6. L'IA est utilisée comme assistant de spécification et de documentation ; toute production de l'IA est relue et corrigée par l'équipe avant publication.
7. Les politiques et conventions sont revues [fréquence] et signées par l'équipe.

**Règle des dérogations :** s'écartez du contrat si nécessaire, mais écrivez la dérogation : [qui décide] / [pourquoi] / [jusqu'à quand] / [ce qu'on apprend].

**Révision :** le contrat est relu à [fréquence]. Toute version modifie la précédente, jamais ne la remplace en silence.

**Signatures :** équipe ____ sponsor ____ décideur de livraison ____ (date ____)

### Annexe A3 : Modèle de rituel Go/No-Go niveau 2

**Durée :** 30 minutes. **Présents :** chargé de livraison (anime), équipe pilote, décideur de livraison.

**1. Critères de Go niveau 2 (à valider ensemble) :**
- [ ] Modèles BPMN à jour pour les processus concernés
- [ ] Tests MBT générés et exécutés, preuves collectées
- [ ] Couverture par types de test conforme à la matrice
- [ ] Documentation produit synchronisée avec les modèles
- [ ] Bug critique : 0 ou dérogation écrite ; bug majeur : traité ou décision datée
- [ ] Note de diffusion préparée (version, périmètre, qui informer)

**2. Décision :** Go / Go avec réserves / No-Go.

**3. Compte rendu (toujours rempli, même court) :**

| Champ | Contenu |
| --- | --- |
| Décision | Go / Go avec réserves / No-Go |
| Modèles à jour | oui / non / partiellement |
| Tests exécutés | nombre passé / nombre échoué |
| Couverture | conforme / non conforme à la matrice |
| Réserves | ce qui est accepté malgré tout, avec le pourquoi |
| Qui a tranché | nom, date |
| Prochaines étapes | si No-Go : quoi, par qui, pour quand |

---

### Annexe A4 : Modèle de rapport de maturité niveau 2

**Structure en deux pages maximum :**
1. **Contexte initial :** la situation au début du niveau 2 (ce qui existait, ce qui manquait).
2. **Parcours des 8 semaines :** tableau semaine / livrable / apprentissage.
3. **Audit des 7 éléments de niveau 2 :** tableau de niveau (1-3) avec preuves pour chacun.
   - Spécifications modélisées (MBT/BPMN)
   - Outillage automatisation/documentation
   - Planification des livraisons niveau 2
   - Qualimétrie niveau 2
   - Politiques et conventions
   - Couverture par types de test
   - Socle pour l'IA
4. **Métriques de mouvement :** 3 à 5 métriques, avant/après, commentées.
5. **Ce qui reste fragile :** les deux faiblesses de l'audit, sans filtre.
6. **Recommandations :** pérenniser / étendre / structurer, avec conditions et coût minimal.
7. **Signature :** l'équipe signe d'abord, la direction endosse ensuite.

**Règle d'écriture :** chaque affirmation est accompagnée d'une preuve (artefact, décision datée, métrique). Pas de preuve, pas d'affirmation.

### Annexe A5 : Guide de facilitation, le coach semaine par semaine (niveau 2)

| Semaine | Posture du coach | À faire | À ne jamais faire |
| --- | --- | --- | --- |
| 1 | Modélisateur | Poser le cadre MBT/BPMN, faire émerger les processus critiques, nommer les responsables | Dessiner les modèles BPMN à la place de l'équipe |
| 2 | Architecte d'outils | Structurer la chaîne modèle → test → documentation, définir les responsabilités de maintenance | Choisir les outils par prestige plutôt que par cohérence |
| 3 | Planificateur | Animer la planification livraisons N2, exiger des preuves d'automatisation | Présenter la planification comme un exercice administratif |
| 4 | Gardien du cap | Exiger le qualimétrage N2, faire écrire les politiques et conventions | Lisser les tensions avant qu'elles n'existent |
| 5 | Soutien sous tempête | Diagnostic sans illusion, chiffrer les blocages, remonter avec preuves | Motiver à coups de slogans |
| 6 | Celui qui se retire | Relayer un rituel, écrire le récit du virage, préparer sa sortie | Intervenir pendant le rituel relayé |
| 7 | Pédagogue du modèle | Animer la couverture par tests, encadrer l'usage de l'IA sur base solide | Laisser l'IA rédiger les spécifications originales |
| 8 | Archiviste | Aider à la preuve, céder le devant, rendre le mandat, signer le contrat v2.0 | Rédiger le rapport de maturité à la place de l'équipe |

### Annexe A6 : Calendrier type des 8 semaines (niveau 2)

**Semaine 1 :** lundi arrimage niveau 2 (2 h) · mardi-modélisation BPMN (3 h) · mercredi MBT (3 h) · vendredi livrable : cartographie des spécifications modélisées (1 h).

**Semaine 2 :** mardi outillage automatisation (3 h) · mercredi documentation produit vivante (3 h) · jeudi pipeline spécification → automatisation (3 h) · vendredi livrable : boîte à outils N2 validée (1 h).

**Semaine 3 :** [à intégrer selon le découpage réel — planification livraisons N2]

**Semaine 4 :** [à intégrer selon le découpage réel — qualimétrie N2 + politiques/conventions]

**Semaine 5 :** mardi diagnostic sans illusion (2 h) · mercredi remontage au sponsor (1 h 30) · jeudi allégement sans abandonner (1 h) · vendredi décision de poursuite.

**Semaine 6 :** lundi récit du virage (2 h) · mardi passage de relais (2 h, coach silencieux) · jeudi démonstration aux voisins (1 h 30) · vendredi autonomie confirmée.

**Semaine 7 :** mardi matrice de couverture par types de test (3 h) · mercredi socle pour l'IA (3 h) · jeudi Go/No-Go N2 (2 h) · vendredi livrable : couverture + IA encadrée.

**Semaine 8 :** mardi audit de maturité N2 (3 h) · mercredi contrat qualité v2.0 (2 h) · jeudi centre d'excellence opérationnel (2 h) · vendredi rapport de maturité + célébration (3 h).

**Rappel :** ce calendrier est un rythme par défaut. Décalez si nécessaire, mais conservez l'ordre : les dépendances entre livrables sont la colonne vertébrale du parcours.

---

## Notes de facilitation semaine par semaine (S1 à S8)
