# Méthode d'appréciation des risques (ISO/IEC 27001, clauses 6.1.2 et 8.2)

*Rédaction `[Original]`, à partir de la méthode EBIOS Risk Manager `[ANSSI]`. Voir [`CREDITS.md`](../CREDITS.md).*

## 1. Choix de la méthode

L'entreprise utilise **EBIOS Risk Manager** (ANSSI) comme méthode d'appréciation des risques du SMSI. ISO/IEC 27001 n'impose pas de
méthode : elle exige que le processus soit défini, produise des résultats comparables et reproductibles, et fixe des critères de
risque. La méthode est complétée par une approche par la conformité : le **socle de sécurité** (atelier 1) est évalué au regard du
Guide d'hygiène informatique de l'ANSSI et de l'Annexe A de l'ISO 27001.

## 2. Correspondance avec les exigences de la clause 6.1.2

| Exigence (paraphrase) | Où c'est traité | Support |
|---|---|---|
| a. Fixer et maintenir des critères de risque : acceptation et réalisation des appréciations | §3 et §4 | Ce document |
| b. Des appréciations répétées produisent des résultats cohérents, valides et comparables | §5 | Échelles, formules, contrôles automatiques |
| c. Identifier les risques liés à la perte de confidentialité, d'intégrité et de disponibilité, et leurs propriétaires | Ateliers 1 à 4 ; §6 | [Ateliers](02-ebios-atelier1-cadrage.md), [registre](tableaux/registre-risques.md) |
| d. Analyser les risques : conséquences, vraisemblance, niveau | Ateliers 1, 3, 4 ; §3 | Gravité, vraisemblance, score |
| e. Évaluer les risques : comparer aux critères, hiérarchiser | Atelier 5 ; §4 | [Stratégie de traitement](06-ebios-atelier5-traitement-du-risque.md) |
| Conserver l'information documentée sur le processus | §7 | Dépôt et [classeur Excel](../reports/SMSI-biotech-classeur.xlsx) |

## 3. Critères de risque

### Gravité `[ANSSI p. 26]`

| Niveau | Nom | Conséquence (résumé) |
|---|---|---|
| G1 | Mineure | Aucun impact opérationnel ni sur la sécurité des personnes ; l'entreprise surmonte sans difficulté |
| G2 | Significative | Dégradation des performances, sans impact sur la sécurité ; mode dégradé |
| G3 | Grave | Forte dégradation, impacts significatifs possibles sur la sécurité des personnes ; mode très dégradé |
| G4 | Critique | Incapacité d'assurer tout ou partie de l'activité, impacts graves possibles sur la sécurité ; la survie est menacée |

La gravité d'un scénario est celle de l'événement redouté qu'il vise, coté en atelier 1. Un événement redouté est coté sur son
impact le plus grave, et la justification est conservée `[ANSSI p. 27]`.

### Vraisemblance `[ANSSI p. 66]`

V1 peu vraisemblable, V2 vraisemblable, V3 très vraisemblable, V4 quasi certain. La vraisemblance d'un scénario est celle de son
mode opératoire de moindre effort (voir l'[atelier 4](05-ebios-atelier4-scenarios-operationnels.md)).

### Niveau de risque `[Hypothèse]`

Score = gravité x vraisemblance, de 1 à 16.

| Niveau | Score | Acceptabilité `[ANSSI p. 74]` |
|---|---|---|
| Faible | 1 à 3 | Acceptable en l'état, aucune action |
| Moyen | 4 à 7 | Tolérable sous contrôle : suivi et amélioration continue |
| Élevé | 8 à 16 | Inacceptable : mesures de réduction à court terme, sinon acceptation formelle par la direction |

Les seuils de score sont un choix de ce projet : le guide fournit les trois classes d'acceptabilité, pas le découpage chiffré. Le
découpage choisi classe en niveau élevé les scénarios de gravité 4 dès V2, de gravité 3 dès V3 et de gravité 2 à V4.

## 4. Critères d'acceptation

| Situation | Qui décide | Condition |
|---|---|---|
| Risque résiduel faible | Propriétaire du risque | Aucune |
| Risque résiduel moyen | Propriétaire du risque, contrôle par le RSSI | Suivi au comité de pilotage, réévaluation à chaque cycle opérationnel |
| Risque résiduel élevé | **Direction générale uniquement** | Acceptation écrite avec motif, date et **date de revue** ; piste de réduction identifiée |

Le propriétaire d'un risque est le responsable de la valeur métier que l'événement redouté atteint `[Original]` : le pharmacien
pour R1 à R3 (fuite des travaux de R&D, ER3), le responsable production pour R4 à R7 (interruption de la production ou de la
distribution, ER6). Le responsable qualité, propriétaire de la traçabilité, n'a pas de scénario propre à ce cycle : ses événements
redoutés (ER7, ER8) sont couverts par le socle et par la mesure N10.
Les propriétaires approuvent le plan de traitement et acceptent les risques résiduels (clause 6.1.3 f).

## 5. Reproductibilité et cohérence

- **Échelles fixées** ci-dessus : deux analystes utilisent les mêmes définitions.
- **Justification écrite** de chaque cotation, conservée avec la donnée (colonnes de justification), pour permettre de la réévaluer
  à un cycle suivant `[ANSSI p. 39]`.
- **Calculs automatiques** : le score, le niveau, la dangerosité des parties prenantes et la vraisemblance des scénarios sont
  calculés, jamais saisis. Le script `tools/build.py` échoue si un résultat contredit une donnée du guide (dangerosité de F2, F3
  et P3, vraisemblance de R1 à R5) ou si une règle de cohérence est violée : un risque résiduel plus élevé que le risque initial,
  un risque élevé sans acceptation, une mesure sans risque, un écart du socle sans mesure.
- **Cycles** : cycle stratégique tous les 3 ans, cycle opérationnel tous les ans `[Hypothèse]` ; réévaluation hors cycle sur
  déclencheurs (voir l'[atelier 5](06-ebios-atelier5-traitement-du-risque.md)).

## 6. Identification des risques et de leurs propriétaires

Les valeurs métier et leurs propriétaires : [atelier 1](02-ebios-atelier1-cadrage.md). Les événements redoutés couvrent les trois
critères de la sécurité de l'information :

| Critère | Événements redoutés |
|---|---|
| Confidentialité | ER3, ER5, ER9 |
| Intégrité | ER2, ER7 |
| Disponibilité | ER1, ER4, ER6, ER8 |

## 7. Résultats et conservation

Les résultats de l'appréciation sont conservés comme information documentée : données dans [`data/`](../data),
tableaux générés dans [`docs/tableaux/`](tableaux), classeur Excel dans [`reports/`](../reports). L'historique est celui du dépôt.
Le [registre des risques](tableaux/registre-risques.md) est l'enregistrement principal. La clause 8.2 (exécution de l'appréciation à
intervalles planifiés et lors de changements importants) est couverte par les cycles et les déclencheurs ci-dessus.
