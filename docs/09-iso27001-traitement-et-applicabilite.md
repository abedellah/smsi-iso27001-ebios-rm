# Traitement des risques et déclaration d'applicabilité (ISO/IEC 27001, clause 6.1.3)

*Rédaction `[Original]`. Les intitulés de l'Annexe A sont des paraphrases courtes, pas le texte de la norme (voir
[`CREDITS.md`](../CREDITS.md)).*

## 1. Le processus, étape par étape

La clause 6.1.3 demande de choisir des options de traitement, de déterminer les mesures nécessaires, de les comparer à l'Annexe A,
d'établir la déclaration d'applicabilité, de formuler un plan de traitement et de faire approuver ce plan et l'acceptation des
risques résiduels par les propriétaires des risques.

| Étape (paraphrase) | Ce qui a été fait | Où |
|---|---|---|
| a. Choisir les options de traitement | Réduire les risques élevés ; aucune exclusion de l'activité ni transfert à ce cycle | [Atelier 5](06-ebios-atelier5-traitement-du-risque.md) |
| b. Déterminer les mesures nécessaires | 26 mesures : 13 du guide EBIOS RM, 13 ajoutées | [Plan de traitement](tableaux/plan-traitement.md) |
| c. Comparer avec l'Annexe A pour ne rien omettre | Chaque mesure est rattachée à des mesures de l'Annexe A ; les 93 sont passées en revue | [Déclaration d'applicabilité](tableaux/declaration-applicabilite.md) |
| d. Établir la déclaration d'applicabilité, avec justification des inclusions et exclusions | 93 décisions, 4 exclusions justifiées et approuvées | [Déclaration d'applicabilité](tableaux/declaration-applicabilite.md) |
| e. Formuler un plan de traitement des risques | Plan avec responsables, échéances, priorités, coûts | [Plan de traitement](tableaux/plan-traitement.md) |
| f. Obtenir l'approbation des propriétaires et l'acceptation des risques résiduels | R3 accepté par la direction générale ; autres risques à valider par leurs propriétaires | §4 ci-dessous |

## 2. Comment la déclaration d'applicabilité est construite

L'objectif est qu'**aucune mesure ne soit retenue sans raison, et qu'aucun risque ne soit traité sans mesure**. La
déclaration n'est donc pas saisie à la main : elle est calculée à partir de trois sources `[Original]`.

1. **Le socle de sécurité** : chaque règle du Guide d'hygiène est rapprochée de mesures de l'Annexe A (données
   [`socle.yaml`](../data/socle.yaml)). Une mesure de l'Annexe A liée à une règle non appliquée est retenue, avec la base « socle ».
2. **Le plan de traitement** : chaque mesure du plan liste les mesures de l'Annexe A qu'elle met en œuvre
   ([`mesures.yaml`](../data/mesures.yaml)). Une mesure de l'Annexe A liée à une mesure qui traite un risque est retenue avec la base
   « risque », et le risque est cité dans la justification.
3. **Les décisions manuelles** : pour les mesures de l'Annexe A que ni le socle ni le plan ne couvrent, une décision et sa justification
   sont écrites dans [`soa_manuel.yaml`](../data/soa_manuel.yaml), avec la base « légal », « contractuel » ou « bonne pratique ».

Le **statut** (mise en œuvre, partielle, à mettre en œuvre) est calculé à partir de l'état des règles du socle et du statut des
mesures du plan liés. Le script exige que chaque mesure de l'Annexe A ait une décision et une justification, qu'une mesure exclue
ne soit utilisée par aucune mesure du plan, et qu'une exclusion porte une justification et une approbation.

## 3. Résultats

Voir le [bilan et le tableau complet](tableaux/declaration-applicabilite.md). En résumé :

- aucune des 93 mesures n'est encore pleinement en place : le SMSI est à construire, ce qui correspond à une maturité de départ
  faible `[ANSSI p. 11]` ;
- **4 mesures sont exclues**, toutes liées au développement logiciel, que l'entreprise ne pratique pas : 8.4 (accès au code source),
  8.25 (cycle de développement sécurisé), 8.28 (codage sécurisé), 8.30 (développement externalisé). Chaque exclusion est justifiée
  et approuvée par la direction générale `[Hypothèse]` : c'est un choix propre à ce cas, à revoir si l'entreprise développe
  un jour des logiciels ;
- les mesures 8.26 (exigences de sécurité des applications acquises) et 8.29 (tests à la recette) restent applicables : elles
  s'appliquent aux systèmes achetés, comme l'ERP et les systèmes industriels.

### Couverture des risques

Chaque risque du registre est traité par des mesures rattachées à l'Annexe A. Le tableau ci-dessous relie chaque risque aux
familles de mesures de l'Annexe A qui le traitent ; les identifiants exacts sont dans le [plan de traitement](tableaux/plan-traitement.md).

| Risque | Familles de mesures mobilisées |
|---|---|
| R1 | Accès (5.15-5.18, 8.5), postes (8.1, 8.7), réseau (8.20-8.22), journalisation (8.15-8.16), sensibilisation (6.3), supports amovibles (7.10), sécurité physique (7.1-7.3) |
| R2 | Fournisseurs (5.19-5.22), échanges (5.14, 8.21, 8.24), minimisation des données (5.12, 8.3) |
| R3 | Fournisseurs (5.19-5.22), accès privilégiés (8.2, 5.18, 8.5), séparation des tâches (5.3), détection (8.15-8.16) |
| R4 | Systèmes industriels (8.9, 8.22, 7.13), fournisseurs (5.19-5.22), continuité (5.29-5.30, 8.13-8.14) |
| R5 | Intégrité des données (8.3, 8.15, 8.24), systèmes industriels, continuité |
| R6 | Fournisseurs, accès privilégiés (8.2, 8.5), cloisonnement (8.22), sauvegardes (8.13, 5.30), incidents (5.24-5.28) |
| R7 | Sensibilisation (6.3), postes (8.1, 8.7, 8.23), correctifs (8.8, 8.19), supports amovibles (7.10), sauvegardes, incidents |

## 4. Approbation et acceptation `[Original]`

Le cas est fictif : ces approbations sont des emplacements à faire signer, pas des signatures.

| Élément | Approuvé par | État |
|---|---|---|
| Plan de traitement des risques | Propriétaires des risques : pharmacien (R1 à R3), responsable production (R4 à R7) | À valider `[ ]` |
| Déclaration d'applicabilité | Direction générale, sur proposition du RSSI | À valider `[ ]` |
| Exclusions 8.4, 8.25, 8.28, 8.30 | Direction générale | Approuvées dans les données, à signer `[ ]` |
| Risque résiduel élevé R3 | Direction générale, le 30 septembre 2026 ; revue au plus tard le 31 mars 2027 | Accepté, motif : [atelier 5](06-ebios-atelier5-traitement-du-risque.md) |
| Risques résiduels moyens (R1, R4, R6, R7) | Propriétaires des risques | À valider `[ ]` |
| Risques résiduels faibles (R2, R5) | Propriétaires des risques | Acceptables en l'état |
