# Traçabilité vers l'ISO/IEC 27001:2022

*Où chaque exigence des clauses 4 à 10 est traitée dans ce dépôt. Les exigences sont paraphrasées. Voir
[`CREDITS.md`](../CREDITS.md).*

## Clauses 4 à 10

| Clause | Exigence (paraphrase) | Où c'est traité |
|---|---|---|
| 4.1 | Comprendre l'organisme et son contexte | [01, §1 et §2](01-iso27001-contexte-et-perimetre.md) |
| 4.2 | Comprendre les besoins et attentes des parties intéressées | [01, §3 et §5](01-iso27001-contexte-et-perimetre.md), [parties prenantes](tableaux/parties-prenantes.md) |
| 4.3 | Déterminer le périmètre du SMSI | [01, §4](01-iso27001-contexte-et-perimetre.md) |
| 4.4 | Établir, mettre en œuvre, maintenir et améliorer le SMSI | Ensemble du dépôt |
| 5.1 | Leadership et engagement de la direction | [07, §5](07-iso27001-politique-de-securite.md), [12](12-iso27001-revue-de-direction.md) |
| 5.2 | Politique de sécurité de l'information | [07](07-iso27001-politique-de-securite.md) |
| 5.3 | Rôles, responsabilités et autorités | [07, §6](07-iso27001-politique-de-securite.md) |
| 6.1.1 | Actions face aux risques et opportunités | [08](08-iso27001-methode-appreciation-risques.md), [09](09-iso27001-traitement-et-applicabilite.md) |
| 6.1.2 | Appréciation des risques | [08](08-iso27001-methode-appreciation-risques.md), ateliers [1](02-ebios-atelier1-cadrage.md) à [4](05-ebios-atelier4-scenarios-operationnels.md), [registre](tableaux/registre-risques.md) |
| 6.1.3 | Traitement des risques, déclaration d'applicabilité | [09](09-iso27001-traitement-et-applicabilite.md), [atelier 5](06-ebios-atelier5-traitement-du-risque.md), [plan](tableaux/plan-traitement.md), [DdA](tableaux/declaration-applicabilite.md) |
| 6.2 | Objectifs de sécurité et planification | [10, §1](10-iso27001-objectifs-et-indicateurs.md) |
| 6.3 | Planification des modifications | Déclencheurs de réévaluation, [atelier 5, §5](06-ebios-atelier5-traitement-du-risque.md) |
| 7.1 | Ressources | [13, §1](13-iso27001-support-et-amelioration.md), [plan et budget](tableaux/trajectoire-et-budget.md) |
| 7.2 | Compétences | [13, §1](13-iso27001-support-et-amelioration.md) |
| 7.3 | Sensibilisation | [13, §2](13-iso27001-support-et-amelioration.md) |
| 7.4 | Communication | [13, §3](13-iso27001-support-et-amelioration.md) |
| 7.5 | Informations documentées | [13, §4](13-iso27001-support-et-amelioration.md) |
| 8.1 | Planification et maîtrise opérationnelles | [Plan de traitement](tableaux/plan-traitement.md), suivi des tiers |
| 8.2 | Appréciation des risques à intervalles planifiés | [08, §5](08-iso27001-methode-appreciation-risques.md), cycles |
| 8.3 | Traitement des risques (mise en œuvre) | [Plan de traitement](tableaux/plan-traitement.md), [trajectoire](tableaux/trajectoire-et-budget.md) |
| 9.1 | Surveillance, mesure, analyse et évaluation | [10, §2 et §3](10-iso27001-objectifs-et-indicateurs.md), [indicateurs](tableaux/indicateurs.md) |
| 9.2 | Audit interne | [11](11-iso27001-audit-interne.md) |
| 9.3 | Revue de direction | [12](12-iso27001-revue-de-direction.md) |
| 10.1 | Amélioration continue | [13, §7](13-iso27001-support-et-amelioration.md) |
| 10.2 | Non-conformité et action corrective | [13, §5 et §6](13-iso27001-support-et-amelioration.md) |

## Annexe A

Les 93 mesures de l'Annexe A ont une décision dans la [déclaration d'applicabilité](tableaux/declaration-applicabilite.md).
Chacune est reliée, selon le cas, à un risque, à une règle du socle, à une exigence légale ou contractuelle, ou à une bonne pratique
justifiée ; les quatre exclusions portent une justification et une approbation.

## Lien avec EBIOS RM

| Étape ISO 27001 | Produit EBIOS RM |
|---|---|
| Identifier les risques (6.1.2 c) | Ateliers 1 à 3 : valeurs métier, événements redoutés, sources de risque, scénarios stratégiques |
| Analyser (6.1.2 d) | Ateliers 3 et 4 : gravité, vraisemblance des scénarios opérationnels |
| Évaluer (6.1.2 e) | Atelier 5 : niveau de risque et stratégie de traitement |
| Traiter, choisir les mesures (6.1.3 a et b) | Atelier 5 : plan de traitement ; atelier 3 : mesures sur l'écosystème |
| Socle de conformité | Atelier 1 : socle de sécurité, ici traité comme un volet du SMSI `[ANSSI p. 29]` |
| Suivi (9.1, 10) | Atelier 5 : cadre de suivi, indicateurs, comité de pilotage `[ANSSI p. 81]` |
