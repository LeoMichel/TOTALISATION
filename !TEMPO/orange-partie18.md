
---

# Partie 18 : Le carnet du praticien N2 — la rétrospective comme instrument

Le praticien du niveau 2 ne remplit pas les mêmes fiches que celui du niveau 1. Sa matière première n'est plus la spécification : c'est la boucle. Son carnet documente comment la boucle tourne — et où elle grippe.

## Le carnet du praticien N2 (un seul document, cinq fiches)

**Page de titre :**

```
CARNET DU PRATICIEN N2
Équipe : [nom]        Trimestre : [T1 - T4]
Praticien : [nom]     Coach : [nom]
```

**Les cinq fiches, dans l'ordre du cycle de boucle :**

1. La fiche de boucle (chaque cycle court : périmètre, délai, résultat, apprentissage)
2. La fiche de rétrospective (chaque fin de cycle : ce qui a marché, ce qui a grippé, un ajustement)
3. La fiche de correspondance (chaque mise en relation entre systèmes ou équipes)
4. La fiche de dette visible (chaque simplification repoussée, avec sa date limite)
5. Le tableau de bord de boucle (chaque vendredi : vitesse, régularité, ajustements appliqués)

**La différence avec le carnet N1 :** au niveau 1, les fiches documentent des livraisons. Au niveau 2, elles documentent des itérations. La fiche de boucle ne demande pas « qu'a-t-on livré ? » mais « qu'a-t-on appris ? » — et c'est cette question qui distingue un praticien N2 d'un praticien N1 avec plus de pratique.

## La fiche de rétrospective remplie (extrait réel)

```
RÉTROSPECTIVE — Cycle 7 (2 semaines)   Date : 12 octobre
Présents : M.L., S.D., K.B., A.R. (4/4)

CE QUI A MARCHÉ :
- Le découpage en tranches de 2 jours a tenu : 6 tranches sur 6
  livrées dans le cycle.
- Le point debout de 10 minutes a remplacé la réunion de 45 minutes :
  personne ne demande son retour.

CE QUI A GRIPPÉ :
- L'environnement de test : 3 des 6 tranches ont attendu la remise
  à jour (entre 2 et 5 heures chacune).
- La revue de code : faite en fin de cycle, elle a renvoyé 2 tranches
  en arrière — la boucle s'est mordue la queue.

UN AJUSTEMENT (un seul, pas dix) :
- La revue de code passe en revue croisée à la volée : chaque tranche
  est relue par un pair avant d'être intégrée, pas après le cycle.
  Test sur le cycle 8. Si le délai de re-travail tombe sous 10 % du
  temps de cycle, on garde.

SUIVI : le grippe environnement est documentée dans la fiche de dette
visible — la remise à jour automatique est une simplification
demandée depuis le cycle 3. Date limite : fin du trimestre.
```

**Ce que cette fiche remplie montre :** une rétrospective productive produit exactement un ajustement — pas une liste de vœux. L'ajustement a un test (le critère du cycle 8) et une date de décision. C'est ce qui distingue un ajustement d'une intention.

## La fiche de dette visible remplie

```
DETTE VISIBLE — Registre de l'équipe (extrait)
Équipe : Kalium    Trimestre : T3

| Simplification repoussée | Depuis | Coût courant | Date limite |
|---|---|---|---|
| Remise à jour auto de l'env. de test | cycle 3 | ~4 h/cycle | 30 nov. |
| Fusion des deux scripts de déploiement | cycle 1 | ~1 h/cycle | 15 déc. |
| Suppression du flag --legacy de l'API | T2 | confusion clients | 31 déc. |

Règle de la fiche : une dette sans date limite n'est pas une dette
documentée — c'est un vœu. Chaque entrée a un propriétaire et une
date. À la date, la dette est payée ou le refus est expliqué devant
l'équipe — jamais en silence.
```

**Le principe de la dette visible :** au niveau 1, la dette est invisible — elle s'accumule en silence. Au niveau 2, elle est nommée, chiffrée, et datée. Le praticien N2 ne cherche pas à éliminer toute la dette : il cherche à ce qu'aucune dette ne soit invisible. La visibilité change la conversation avec la direction — de « il faudrait nettoyer » à « voici le coût courant de chaque simplification repoussée, et la date à laquelle nous la traiterons ».

## La fiche de correspondance remplie

```
CORRESPONDANCE — Entre le système de facturation et le CRM
Établie le : 4 septembre   Par : M.L.   Validée par : S.D.

| Champ facturation | Champ CRM | Transformation | Vérifié par |
|---|---|---|---|
| CLI_NOM | account.name | concaténom prénom | test #12 |
| CLI_DATE | created_at | format JJMMAAAA → ISO | test #13 |
| CLI_STATUT | lifecycle_stage | table de correspondance | test #14 |

Zone grise documentée : le statut « en attente » n'existe pas côté
CRM. Décision du 11 septembre : « en attente » correspond à
« negotiation » avec un tag d'attente. Révisée au prochain cycle si
le service client signale des écarts.
```

**Le principe de la correspondance :** une table de correspondance n'est jamais terminée — elle est vérifiée, datée, et revisée. La colonne « vérifié par » n'est pas décorative : c'est le test qui prouve la correspondance. Une correspondance sans test est une supposition.

## Le rituel du carnet

**Le vendredi de boucle.** Le praticien N2 remplit son tableau de bord de boucle chaque vendredi : combien de cycles courts cette semaine, quelle régularité (écart-type des délais), quels ajustements appliqués. Trois chiffres, pas quinze. Le tableau du praticien N2 tient sur une ligne — parce qu'une boucle qui ne se décrit pas en une ligne n'est pas une boucle.

**L'archivage croisé.** Comme au niveau 1, chaque fiche complétée est archivée. Mais au niveau 2, l'archivage sert à autre chose : à la fin du trimestre, l'équipe relit les fiches de boucle de trois mois et voit sa propre trajectoire — vitesse, régularité, ajustements qui ont tenu et ajustements abandonnés. C'est le meilleur antidote à la démarche qualité cosmétique : une équipe qui relit ses propres fiches ne se raconte pas d'histoires.

**Le test du carnet N2 :** montrez-moi vos fiches de rétrospective du trimestre. Si chaque fiche contient un ajustement avec un test, votre boucle tourne. Si les fiches contiennent des listes de plaintes, votre rétrospective est une séance de débriefing — pas une boucle d'apprentissage.

## Le carnet comme transition vers le niveau 3

Le carnet du praticien N2 est aussi le pont vers le niveau 3. Le praticien qui arrive au VERT n'apprend pas de nouvelles fiches : il apprend à relier ses fiches entre elles. La fiche de boucle croise la fiche de correspondance (la boucle traverse-t-elle les frontières ?) ; la fiche de dette croise le tableau de bord (la dette ralentit-elle la boucle mesurablement ?).

C'est le schéma de toute la progression : chaque niveau n'ajoute pas un carnet, il relie le carnet précédent à une dimension nouvelle. Le praticien qui comprend cela ne commence jamais un niveau de zéro — il ouvre le carnet qu'il a déjà, et y ajoute la colonne qui manquait.
