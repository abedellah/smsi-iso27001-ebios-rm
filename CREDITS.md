# Crédits et sources

Ce dépôt réutilise et prolonge deux documents publiés par l'ANSSI. Cette page dit précisément d'où vient chaque élément.

## Source principale : le guide EBIOS RM

> ANSSI, **« La méthode EBIOS Risk Manager : le guide »**, version 1.5, septembre 2024
> (référence ANSSI-PA-048, ISBN 978-2-11-167161-4 en ligne).
> Publié sous **Licence Ouverte / Open Licence (Etalab, V1)**.
> Page du guide : <https://messervices.cyber.gouv.fr/guides/la-methode-ebios-risk-manager-le-guide>
> Fichier consulté le 21 septembre 2026.

L'ANSSI illustre sa méthode avec l'exemple d'**une entreprise fictive de biotechnologie fabriquant des vaccins** (guide, p. 11). Cette
entreprise, sa mission, ses valeurs métier, ses biens supports, ses événements redoutés, ses sources de risque, ses parties prenantes,
ses scénarios de risque et ses mesures viennent de ce guide. Elles sont reprises comme point de départ, avec la référence de page.

### Ce qui est repris du guide EBIOS RM

| Élément | Pages du guide |
|---|---|
| Présentation de l'entreprise fictive et de son niveau de maturité | p. 11 |
| Mission, valeurs métier, propriétaires et biens supports | p. 22 |
| Échelle de gravité G1 à G4 | p. 26 |
| Sept événements redoutés et leur gravité | p. 27 |
| Exemple de socle de sécurité (règles 8 et 37 du Guide d'hygiène) | p. 30 |
| Quatre couples source de risque / objectif visé, leurs cotations et justifications | pp. 37, 39, 40 |
| Parties prenantes, seuils de dangerosité, parties critiques, dangerosité de F2, F3 et P3, mesures sur l'écosystème | pp. 46, 47, 54 |
| Scénarios stratégiques SS1 et SS2 (cinq chemins d'attaque) | pp. 50, 51 |
| Scénario opérationnel de R1 (trois modes opératoires), méthode de cotation, échelle de vraisemblance | pp. 62 à 66 |
| Vraisemblance globale de R1 à R5 | p. 67 |
| Scénarios de risque R1 à R5, classes d'acceptabilité | pp. 72, 74, 75 |
| Douze mesures du plan de traitement, leurs responsables, freins, coûts, échéances et statuts | p. 77 |
| Modèle de fiche de risque résiduel, recommandation de cartes par jalon | pp. 78, 79 |
| Maintien de R3 à un niveau élevé, pistes envisagées, surveillance de la menace cybercriminelle, cadre de suivi et indicateurs | pp. 80, 81 |

## Seconde source : le Guide d'hygiène informatique

> ANSSI, **« Guide d'hygiène informatique : renforcer la sécurité de son système d'information en 42 mesures »**, version 2.0,
> septembre 2017. Publié sous **Licence Ouverte / Open Licence (Etalab, V1)**.
> Fichier : <https://messervices.cyber.gouv.fr/documents-guides/guide_hygiene_informatique_anssi.pdf>, consulté le 21 septembre 2026.

Les intitulés des 42 règles viennent de l'outil de suivi de ce guide. L'état d'application de chaque règle dans l'entreprise fictive
est un travail de ce projet (voir les étiquettes ci-dessous). Ce guide date de 2017 : des mises à jour ont pu paraître depuis.

## Ce qui est un travail original

Tout ce qui n'est pas dans les tableaux ci-dessus :

- la **couche ISO/IEC 27001** : contexte et périmètre, politique, méthode, plan de traitement, déclaration d'applicabilité des 93 mesures,
  objectifs et indicateurs, programme d'audit interne, revue de direction, support et amélioration ;
- les **compléments aux ateliers EBIOS RM** : justification des cotations, événements redoutés ER8 et ER9, couple SO5, scénario
  stratégique SS3, risques R6 et R7, scénarios opérationnels de R2 à R7, mesures ajoutées, risques résiduels, trajectoire ;
- l'**évaluation du socle** de sécurité de l'entreprise fictive ;
- les **constats** sur le cas de référence ;
- les **outils** de vérification et de génération (`tools/build.py`).

Les numéros de page sont ceux **imprimés dans les guides** (le fichier PDF du guide EBIOS RM a deux pages de plus en tête : la page imprimée
27 est la page 29 du PDF).

## Comment lire les sources dans les tableaux

| Étiquette | Sens |
|---|---|
| `[ANSSI p. N]` ou `ANSSI-EBIOS p. N` | Repris du guide EBIOS RM, page imprimée N |
| `[ANSSI p. N, reformulé]` | Repris du guide et reformulé pour la lisibilité |
| `[Original]` ou `Original` | Analyse ou complément de ce projet |
| `[Hypothèse]` ou `Hypothèse` | Choix fait par ce projet parce que le guide ne dit rien : à discuter, pas un fait |

## Autres références

- **Club EBIOS** : exemples d'études publiés (centre d'imagerie médicale, autres cas), cités comme points de comparaison. Leur contenu
  n'est pas reproduit.
- **ISO/IEC 27001:2022**. La norme est protégée par le droit d'auteur. Ce dépôt n'en reproduit pas le texte : les intitulés de l'Annexe A
  sont des paraphrases courtes, et les exigences des clauses 4 à 10 sont résumées.

## Ce que ce projet n'est pas

- Il n'est ni réalisé, ni relu, ni validé, ni approuvé par l'ANSSI, le Club EBIOS ou l'ISO. Aucun lien officiel n'est suggéré.
- Il ne décrit aucune entreprise réelle. L'entreprise est un cas pédagogique fictif.
- Il ne constitue ni un audit ni une certification.
