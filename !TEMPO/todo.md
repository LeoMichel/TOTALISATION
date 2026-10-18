# Roadmap - Choses à faire

Légende : `[ ]` à faire · `[~]` en cours · `[x]` terminé

> Objectif : produire les 21 livres TOTALISATION au format `.md` à partir du dossier `ideas/`, en trois parties.

---

## 0. Rappels et consignes (à garder en tête)

- Écrire **TOTALISATION** (et non "ToTAL" ni "TOTAL") dans les textes courants.
- Marque : le logotype est **T̥T̯L̩S̯T̩˜**.
- Pas de tiret cadratin dans les textes (faute en français) : utiliser la virgule, le deux-points, les parenthèses, ou le tiret simple " - ".
- Guillemets droits `""` (pas de guillemets français).
- Ton clair, honnête, accrocheur : garder l'intérêt du lecteur.
- `ideas/` est en **lecture seule**. Les scripts vont dans `automata/`.
- Site web : **www.totalisation.com**
- Langue : **français canadien**, expressions **québécoises** avec parcimonie ; termes anglais courants conservés (*backlog*, *sprint*, *pipeline*...), équivalent français (GDT/OQLF) entre parenthèses à la première occurrence ; un glossaire commun assure la cohérence.
- Matière : toujours **puiser dans `ideas/`** pour écrire. Les partages d’expérience de l’auteur y sont essentiels : anecdotes, tranches de vie, héritage (*legacy*), récits de terrain. C’est ce qui donne du vivant aux livres.
- Matière manquante : s’il manque un vécu, une anecdote ou un document pour un livre, **le demander à l’auteur en créant un todo** dédié (ne pas inventer).
- Anti-duplication : éviter le plus possible la **duplication et la répétition inutile entre les livres**. Chaque livre a sa propre identité, sa raison, son but. Si un sujet appartient à un autre livre, y renvoyer au lieu de le réécrire.

---

## 1. Décisions de cadrage (à trancher en premier)

- [x] Confirmer le **format du livre imprimé** (poche 13 × 20 cm, souple, noir et blanc)
- [x] Fixer le **nombre de mots cible** par livre (~ 45 000 mots)
- [x] Fixer le **nombre de pages cible** par livre (~ 220 pages)
- [x] Valider le **découpage en trois parties** (1 / 13 / 7)
- [x] Confirmer le **nombre de livres** (21)
- [x] Définir le **public prioritaire** (audience large : Agile, QA, dev, archi, PO/PM, CTO...)
- [x] Écrire le **gabarit de livre** commun (structure de chapitre, annexes) : voir `livres/_gabarit.md`

---

## 2. Partie 1 - Présentation de l'art (1)

> Nature : l'identité de TOTALISATION. Présentation, introduction, sens, raison. Pas d'ateliers ni de guides pratiques.

- [x] T̥T̯L̩S̯T̩˜ ❖ L’éveil de la TOTALISATION (terminé, poussé sur GitHub avec couverture cover-L1)
  - **Statut :** matière extraite du ToTAL `ToTAL_Art_Realiser_Produit_Logiciel_v31.docx` (via `Tools/docx_text.txt`, ~1202 éléments)
  - **Thèmes collectés :**
    - Définition de la qualité → clarté → confiance → excellence
    - Collision terminologique : le mot `terminé (done)` est devenu un risque qualité
    - Métrique ≠ signal : une mesure peut être exacte et inutile ; un signal est simple et décisif
    - Qualité avant les tests ; rétrospective post-incident ; sur-qualité comme qualité mal placée
    - Carnets de terrain : scènes du bureau du père (Rayduf), expériences de CGI (stop qualité)
  - **Voir `!TEMPO/inventaire_vecu_lorigine.md`** (sections A–F)

---

## 3. Partie 2 - Réconciliation (13)

> Nature : continuité de la présentation de l'identité et des différences de TOTALISATION. Pas de guide pour la pratique : ni ateliers, ni exercices, ni roadmaps (réservés aux livres Guidance).

- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec le Centre d’Excellence
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec le cycle de vie de la réalisation du logiciel (SDLC)
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec les spécifications par la modélisation en continu
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec la mystérieuse cité de la qualité perdue
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec se mesurer pour s’améliorer par la qualimétrie
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec la science oubliée de l’investigation et de la recherche
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec attrape‑moi donc ce bug !
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec jongler intelligemment utilisant l’intelligence artificielle
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec le genèse humain de l’automatisation
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec le "BEASTEST" outil
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec les méthodologies, terminologies et meilleures pratiques
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec être sur la même longueur d’onde
- [ ] T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec la confiance vers la satisfaction jusqu’au succès

---

## 4. Partie 3 - Guidance opérationnelle (7)

> Nature : passage de la théorie vers la pratique. Seuls ces livres contiennent ateliers, exercices et roadmaps.

- [ ] T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (1) ROUGE
- [~] T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (2) ORANGE
  - **Statut :** squelette complet (8 semaines, 32 ateliers), poussé sur GitHub
  - **Thèmes :** MBT/BPMN, outillage automatisation + documentation produit, planification livraisons N2, qualimétrie N2, politiques et conventions N2, couverture par types de test, socle pour l'IA
  - **Prochaines étapes :** rédaction chapitre par chapitre, intégration du vécu Opal-RT (capsules), relire/harmoniser, couverture image (cover-L2) si disponible
- [ ] T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (3) JAUNE
- [ ] T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (4) VERT
- [ ] T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (5) BLEU
- [ ] T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (6) INDIGO
- [ ] T̥T̯L̩S̯T̩˜ ❖ Guidance opérationnelle du niveau (7) VIOLET

---

## 5. Process pour chaque livre

- [ ] Rassembler la matière depuis `ideas/` (documents + vécu, anecdotes et tranches de vie de l'auteur)
- [ ] Si une matière manque, créer un todo pour la demander à l'auteur (ne pas inventer)
- [ ] Établir le plan (chapitres, annexes)
- [ ] Rédiger
- [ ] Relire / harmoniser le ton et le glossaire
- [ ] Mettre en forme `.md` dans `livres/`
- [ ] Rédiger la quatrième de couverture (accroche, bénéfices, note sur l'IA, photo de l'auteur)
- [ ] Préparer la couverture (recto, avec l'illustratrice)
- [ ] Préparer l'export imprimé (PDF)

---

## 6. Infrastructure & continuité

- [x] Gabarit de livre réutilisable (`livres/_gabarit.md`)
- [ ] Glossaire commun TOTALISATION
- [x] Charte de ton et de rédaction (consignes établies dans le README)
- [ ] Suivi d'avancement (livres faits / en cours / à faire)

---

## 7. Livre en cours : L’éveil de la TOTALISATION

Fichier : `livres/T̥T̯L̩S̯T̩˜ ❖ L’éveil de la TOTALISATION.md` (vide, 0 octet, à remplir depuis le gabarit `livres/_gabarit.md`).

Vécu et terrain à puiser dans `ideas/` (lecture seule, ne pas modifier) :

- `vecu.txt` (vécu personnel et professionnel, à lire au complet) : enfance (bureau du père, premier bug, injustice de ne pas être écouté), abandon puis retour via la musique et l'oncle Rayduf (monter, configurer, programmer, réseau, contrats), CGI (break de la qualité, automaticien), Desjardins, Vidéotron (coach QA), Beneva (fusion), Sherweb (sauvetage après retrait des QA), Petal qui s'engouffre (QA partout mais exclu de partout), Genius Solution (monde ERP, Onetool premier pas vers BEASTEST, concours de bugs, 3 QA pour 40 devs), Opal-RT (première implémentation TOTALISATION, mission impossible du "définir", Xray, IF... THEN...), Juris, Beenox, Infor, Mertec, Optel (traçabilité, Agile, automatisation mobile). Règle d'or notée par l'auteur : histoires biographiques professionnelles complètement anonymes, vie privée séparée.
- Petal (concepts qualité) : `ENCYCLOPEDIA+libre+du+logiciel,+pour+nous+tous++(Reference+officielle+Petal).docx` (et copie "(1).docx"), `Petal.url`.
- Alithya (travail des concepts qualité au service du client) : `Alithya.pdf`, `Alithya.xlsx`.
- ACAQ / Opal-RT (Mission Faucon, CGI) : `Mission-Faucon-CGI-Export-Complet-v2.html`, `Mission-Faucon-CGI-Export-Complet-v3.html`, `ACAQ-Mission faucon-120726-164644.pdf`, `ACAQ-Bilan mission qualite - suivi ROI par semaine-120726-164355.pdf`, `L15 — Guide Rouge — Mission Faucon — Partie A.pdf`, `L15 — Guide Rouge — Mission Faucon — Partie B.pdf`, `L15 — Guide Rouge — Mission Faucon — Partie C.pdf`, `L15 — Guide Rouge — TᵒTALiSATiᵒN — Partie A — Semaines 1 à 3.pdf`, `L15 — Guide Rouge — TᵒTALiSATiᵒN — Partie B — Semaines 4 à 6.pdf`, `L15 — Guide Rouge — TᵒTALiSATiᵒN — Partie C — Semaines 7 et 8.pdf`, `ToTAL_Art_Realiser_Produit_Logiciel+vecu_v30.docx`.
- VIA Rail (récent, agentisation avec les produits Atlassian) : aucun fichier VIA dans `ideas/` pour l'instant, voir todo dédié ci-dessous.
- Vécu diffus : d'autres anecdotes et tranches de vie se trouvent un peu partout dans les fichiers de `ideas/`, à aller chercher au fil de la rédaction (ne pas inventer, noter ce qui manque en todo).

- `L1 — L'Origine — Partie A — Le Premier Signal.pdf` (51 pages) : prologue personnel (le premier bug), prologue (la question qui a tout déclenché), introduction (pourquoi rien ne suffit), Partie 1 (le chaos normalisé : chapitres 1 à 3).
- `L1 — L'Origine — Partie B — La Question Fondatrice.pdf` (64 pages) : chapitre 4 (transformations sans clarification), Partie 2 (assurance qualité des grands concepts : chapitres 5 à 8), Partie 3 (chaîne clarté, qualité, confiance, excellence : chapitres 9 et 10).
- `L1 — L'Origine — Partie C — La Promesse des Vingt et Un Livres.pdf` (43 pages) : présentation des 21 livres, épilogue, annexes (lexique de base, structure de la collection).
- `L1 — L'Origine — ToTAL Réconciliation.pdf` (26 pages) : synthèse chapitres 1 à 4, épilogue (revenir au premier signal), conclusion (de la lucidité à l'origine).
- `LIVRE 1 — ToTAL - Origines et philosophie.pdf` (89 pages) : version complète, 12 chapitres en 3 mouvements (chaos normalisé, assurance qualité des concepts, chaîne clarté vers excellence durable), épilogue, conclusion, glossaire, phrases-repères, références.
- Référence : `ToTAL_Mapping_21_Livres.xlsx`, `feed-source-atomique-livre-total-destination-12.csv`

## 8. Livre en cours : Toute la différence par la réconciliation du 'LEGACY'

Fichier : `livres/T̥T̯L̩S̯T̩˜ ❖ Toute la différence par la réconciliation du ''LEGACY''.md`

Statut : **ACTIF** — 10 chapitres rédigés et structurés (Partie 1 : représentations · Partie 2 : pratiques · Épilogue · Annexes).
- Chapitres : la cité de la qualité perdue / la longueur d'onde / le bug / les méthodologies et termes / la qualimétrie / l'IA / l'automatisation / l'investigation / la confiance → satisfaction → succès / le BEASTEST.
- Partie 1 « représentations » et Partie 2 « pratiques » avec la destination L01 indiquée pour les sujets qui s'y recoupent.
- Épilogue et Annexes (A1 chronologie, A2 glossaire, A3 tableau comparatif legacy vs TOTALISATION).

## 9. Livre à venir : Réconciliation avec les méthodologies, terminologies et meilleures pratiques

Fichier : `livres/T̥T̯L̩S̯T̩˜ ❖ Réconciliation avec les méthodologies, terminologies et meilleures pratiques.md`

Statut : À faire (fais l'objet d'un chapitre dans le livre LEGACY ci-dessus).

Plan proposé pour le livre final (fusion de la matière ci-dessus, sans duplication) :

- Avant-propos : la scène fondatrice (le bureau du père, l'enfant, le premier bug)
- Introduction : pourquoi rien ne suffit, et pourquoi cela s'aggrave malgré tout
- Partie 1 (le chaos normalisé) : chapitres 1 à 4 (paradoxe moderne, accélérer ou stagner, pas de la mauvaise volonté, transformations sans clarification)
- Partie 2 (l'assurance qualité des grands concepts) : chapitres 5 à 8 (concepts à assurer, collisions terminologiques, qualité avant les tests, erreurs comme matière d'apprentissage)
- Partie 3 (chaîne vers l'excellence durable) : chapitres 9 à 12 (clarté, qualité holistique, confiance, excellence durable)
- Épilogue : revenir au premier signal. Conclusion : de la lucidité à l'excellence durable
- Annexes : glossaire bilingue, phrases-repères, tableaux, références

Prochaines étapes :

- [x] Rassembler et lire la matière L1 ci-dessus (sommaires et tables extraits)
- [ ] Valider le plan proposé avec l'auteur, dont les anecdotes et tranches de vie à intégrer
- [ ] Rédiger
- [ ] Relire / harmoniser (ton, glossaire, consignes)
- [ ] Rédiger la quatrième de couverture + photo de l'auteur
- [ ] Intégrer le vécu VIA Rail récent (agentisation avec les produits Atlassian) : aucun fichier VIA dans `ideas/` pour l'instant, matière à demander à l'auteur (cas concrets, résultats, anecdote pour L’éveil)
- [ ] Confirmer l'anonymisation du vécu professionnel (règle : histoires biographiques complètement anonymes, vie privée séparée) et quelles anecdotes Petal, Alithya et ACAQ prioriser pour L’éveil


- [x] Confirmer l'organisation des matières vécues — Mission Faucon/Opal-RT → Guide Rouge ; scènes du bureau du père → Origine (début) ; autres (ex. Desjardins) → livres appropriés (Sabotage, etc.)

- [x] Consolider le vécu pour L’éveil — inventaire structuré dans `!TEMPO/inventaire_vecu_lorigine.md` (sections A à F)
- [x] Vérifier la structure de travail : `ideas/` lecture seule · scripts dans `automata/` · temporaire dans `!TEMPO/`


## 6. Compte rendu de la mise à jour (2026-02-10)

### Corrections apportées

- **Inventaire corrigé** : `!TEMPO/inventaire_vecu_lorigine.md` pointe maintenant sur les vraies informations situées dans `ideas/`
- **Plan du livre L’éveil reconstitué** à partir des PDFs sources
- **Rapport des anomalies** : la phrase "Truite très jeune dans le bureau du père" n'a pas été retrouvée dans les fichiers extraits

### Plan du livre L’éveil de la TOTALISATION — ToTAL Réconciliation (livre fondateur)

**Fichiers sources `ideas/` :**
- `L1 — L'Origine — ToTAL Réconciliation.pdf` (26 p.) — synthèse complète
- `L1 — L'Origine — Partie A — Le Premier Signal.pdf` (51 p.) — Prologue personnel, Introduction, Partie 1
- `L1 — L'Origine — Partie B — La Question Fondatrice.pdf` (64 p.) — chapitre 4
- `L1 — L'Origine — Partie C — La Promesse des Vingt et Un Livres.pdf` (43 p.) — présentation des 21 livres

**Plan détaillé (extraits dans `Tools/origine_*.txt`) :**

- **Avant-propos** — Ce que ce livre est et ce qu'il n'est pas
- **Prologue personnel** — Le premier bug que personne ne voulait croire
  - Le bureau du père
  - L'enfant qui chicane la machine
  - Un archétype de tous les signaux ignorés
  - De l'enfant au praticien : la continuité d'un regard
- **Prologue** — La question qui a tout déclenché
  - L'Eureka ToTAL
  - Les symptômes du désordre ordinaire
  - La révélation : les concepts eux-mêmes
- **Introduction** — Pourquoi rien ne suffit, et pourquoi cela s'aggrave malgré tout
  - Les organisations logicielles modernes
  - Trois profils organisationnels
  - ORIGINALIUM, DREAM-TEAM et BEASTEST
  - La chaîne fondatrice
  - L'intelligence artificielle comme révélateur
- **Partie 1** — Le chaos que les organisations ont appris à normaliser
  - **Chapitre 1** — Le paradoxe des organisations modernes
    - Avoir tout, manquer de maîtrise
    - Scène ORIGINALIUM : La réunion de direction
    - Confondre activité et maîtrise
    - La première question ToTAL
  - **Chapitre 2** — Accélérer, stagner ou décélérer
    - Les trois profils en profondeur
    - ORIGINALIUM : les trois simultanément
    - Le faux remède : ajouter des ressources
    - Carnet de terrain de Karim (QA)
    - La vraie question
  - **Chapitre 3** — Le chaos n'est pas seulement de la mauvaise volonté
    - La tentation du coupable
    - Le chaos comme symptôme de système
    - Le blâme ferme les boucles d'apprentissage
    - Carnet de terrain — expérience de terrain
    - La qualité du système humain
- **Chapitre 4** — Quand les transformations s'ajoutent sans se clarifier
- **Épilogue** — Revenir au premier signal
- **Conclusion** — De la lucidité à l'origine
- **Chaîne conductrice :** Clarté → qualité → confiance → excellence durable

### Prochaines étapes

- [x] Rassembler et lire la matière L1 ci-dessus (sommaires et tables extraits)
- [x] Valider le plan du livre L’éveil avec les PDFs `ideas/L1 — L'Origine — ToTAL Réconciliation.pdf` + `Partie A/B/C/*.pdf`
- [ ] Rédiger le plan détaillé du livre L’éveil de la TOTALISATION (chapitres 1-4 recomposés)
- [x] Vérifier la structure de travail : `ideas/` lecture seule · scripts dans `automata/` · temporaire dans `!TEMPO/`
- [x] Confirmer l'organisation des matières vécues — Mission Faucon/Opal-RT → Guide Rouge (confirmé, capsules intégrées) ; scènes du bureau du père → Origine (début) ; autres (ex. Desjardins) → livres appropriés (Sabotage, etc.)
- [ ] Confirmer l'anonymisation du vécu professionnel (règle : histoires biographiques complètement anonymes, vie privée séparée) et quelles anecdotes Petal, Alithya et ACAQ prioriser pour L’éveil
- [ ] Extraire Alithya.pdf/xlsx
- [ ] Extraire clientToTAL/ (200+ PDFs)
- [ ] Définir le plan détaillé des 21 livres

### Anomalies signalées

- **Phrase "Truite très jeune dans le bureau du père"** — Non trouvée dans ToTAL, Petal, vecu.txt, atomique CSV. Probable artefact d'extraction ou fausse mémoire → à confirmer par l'utilisateur.
- **L'extraction "truite"** — Uniquement des artefacts de PDFs ToTAL.

