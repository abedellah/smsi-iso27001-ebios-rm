# Programme d'audit interne (ISO/IEC 27001, clause 9.2)

*Rédaction `[Original]`. Cas fictif : les dates sont relatives au début du plan (T0, 1er octobre 2026), `[Hypothèse]`.
Voir [`CREDITS.md`](../CREDITS.md).*

## 1. Objet

L'audit interne vérifie, à intervalles planifiés, que le SMSI est conforme aux exigences de l'organisme et de la norme, et qu'il est
mis en œuvre et entretenu de manière efficace. Le programme tient compte de l'importance des processus et des résultats des audits
précédents.

## 2. Principes

- **Impartialité** : un auditeur n'audite pas son propre travail. Le RSSI pilote le SMSI ; l'audit est donc conduit par une personne
  indépendante de la DSI et du RSSI : auditeur qualité formé, ou prestataire.
- **Critères** : la norme ISO/IEC 27001 (clauses 4 à 10), la politique de sécurité, le plan de traitement, la déclaration
  d'applicabilité et les exigences légales identifiées.
- **Preuves** : entretiens, documents, observation, échantillons de journaux et de comptes. Une mesure « mise en œuvre » sans
  preuve est considérée comme non conforme.
- **Résultats** : rapport écrit remis à la direction, non-conformités enregistrées dans le
  [registre](13-iso27001-support-et-amelioration.md) avec action corrective et échéance.
- **Confidentialité** : les rapports sont classés « confidentiel ».

## 3. Programme sur trois ans

Une certification est envisagée vers T0+15 mois `[Hypothèse]`. La norme exige qu'un audit interne complet et une revue de
direction aient eu lieu avant l'audit de certification : A1 et A2 y préparent, et la revue de direction MR2 les suit
(voir la [revue de direction](12-iso27001-revue-de-direction.md)). Le programme couvre l'ensemble du système en un cycle.

| Audit | Date | Périmètre | Objectif principal |
|---|---|---|---|
| A1 | T0+9 mois (juillet 2027) | Clauses 4 à 7 et 9 ; mesures organisationnelles 5.x et humaines 6.x ; règles 1 à 8 du socle | Vérifier que le SMSI est en place : contexte, politique, méthode de risques, déclaration d'applicabilité, compétences |
| A2 | T0+12 mois (octobre 2027) | Clauses 8 et 10 ; mesures technologiques 8.x et physiques 7.x ; règles 9 à 42 du socle | Vérifier l'efficacité des mesures techniques du plan de traitement, sur échantillon |
| A3 | T0+18 mois (avril 2028) | Suivi des non-conformités de A1 et A2 ; prestataires et laboratoires critiques ; scénarios R3, R6 et R7 | Vérifier les corrections ; confirmer la préparation à l'audit externe |
| A4 | T0+30 mois | Cycle complet, priorité aux risques élevés | Nouveau cycle après la certification |

Un audit supplémentaire peut être déclenché par un incident de sécurité majeur, un changement de prestataire critique ou une
évolution importante du périmètre.

## 4. Conduite d'un audit

1. **Préparation** : lettre de mission, plan d'audit, liste des documents demandés, calendrier des entretiens.
2. **Réunion d'ouverture** avec les responsables audités.
3. **Collecte des preuves** selon la liste de contrôle du §5.
4. **Constats** : conformité, non-conformité majeure, non-conformité mineure, observation, point fort.
5. **Réunion de clôture** et rapport dans les dix jours ouvrés.
6. **Suivi** : action corrective par non-conformité, responsable et échéance ; vérification de l'efficacité à l'audit suivant.

### Classement des constats

| Constat | Définition |
|---|---|
| Non-conformité majeure | Exigence de la norme non satisfaite, ou défaillance qui compromet l'atteinte des objectifs de sécurité (par exemple : aucune appréciation des risques, risque élevé sans acceptation) |
| Non-conformité mineure | Écart isolé ou sans conséquence immédiate sur le système |
| Observation | Point sensible ou piste d'amélioration, sans non-conformité |

## 5. Liste de contrôle par clause

Chaque ligne indique le point à vérifier et la preuve attendue. C'est la base du plan d'audit, à adapter à chaque mission.

| Clause | Point à vérifier | Preuve attendue |
|---|---|---|
| 4.1 | Les enjeux internes et externes sont identifiés et revus | [Contexte](01-iso27001-contexte-et-perimetre.md) daté, dernière revue |
| 4.2 | Les parties intéressées et leurs exigences, dont légales, sont déterminées | Liste des parties intéressées, registre légal |
| 4.3 | Le périmètre est documenté, avec interfaces et exclusions | Périmètre approuvé |
| 5.1 | La direction montre son engagement : ressources, comités, revue | Procès-verbaux du comité de pilotage, budgets |
| 5.2 | La politique est approuvée, communiquée, disponible | [Politique](07-iso27001-politique-de-securite.md) signée, preuve de diffusion |
| 5.3 | Les rôles et responsabilités sont attribués et compris | Lettres de mission, organigramme |
| 6.1.2 | La méthode de risques est appliquée de façon cohérente | [Méthode](08-iso27001-methode-appreciation-risques.md), [registre](tableaux/registre-risques.md) à jour |
| 6.1.3 | La déclaration d'applicabilité est à jour et justifiée ; les propriétaires ont approuvé le plan | [Déclaration](tableaux/declaration-applicabilite.md), approbations signées |
| 6.2 | Les objectifs sont mesurables et suivis | [Objectifs](10-iso27001-objectifs-et-indicateurs.md), valeurs des indicateurs |
| 7.2 | Les compétences nécessaires sont assurées | Matrice de compétences, attestations de formation |
| 7.3 | Le personnel connaît la politique et son rôle | Résultats de sensibilisation, entretiens |
| 7.4 | Les communications internes et externes sont planifiées | [Plan de communication](13-iso27001-support-et-amelioration.md) |
| 7.5 | L'information documentée est maîtrisée | Registre des documents, versions, approbations |
| 8.1 | Les processus sont maîtrisés, les changements évalués, les prestations externalisées contrôlées | Procédures, contrats de prestataires, audits de tiers |
| 8.2 | Les appréciations de risques sont faites aux dates prévues et lors de changements importants | Dates des cycles, déclencheurs traités |
| 8.3 | Le plan de traitement est mis en œuvre ; des preuves existent pour les mesures « mises en œuvre » | Avancement du [plan](tableaux/plan-traitement.md), preuves par mesure |
| 9.1 | Les indicateurs sont mesurés et analysés | Valeurs, analyses, comptes rendus |
| 9.2 | Le programme d'audit est exécuté, les auditeurs sont impartiaux | Ce programme, rapports, indépendance |
| 9.3 | La revue de direction a lieu avec toutes les entrées et produit des décisions | [Comptes rendus](12-iso27001-revue-de-direction.md) |
| 10.1 | Le SMSI est amélioré en continu | Tendance des indicateurs, actions issues des revues |
| 10.2 | Les non-conformités sont corrigées et leurs causes traitées | [Registre des non-conformités](13-iso27001-support-et-amelioration.md) |
| Annexe A | Les mesures sélectionnées sont en œuvre ; les exclusions restent justifiées | Preuves par mesure sur échantillon, revue des exclusions |

## 6. Échantillonnage des mesures de l'Annexe A

Toutes les mesures ne peuvent être vérifiées à chaque audit. La règle retenue `[Original]` :

- toutes les mesures liées à un risque de niveau élevé (R3, R6, R7, R1, R4), et donc les mesures de priorité 1 ;
- un tiers des autres mesures, en tournant d'un audit à l'autre ;
- les mesures du plan passées au statut « Terminé » depuis l'audit précédent ;
- les quatre exclusions, pour vérifier qu'elles restent valides.

## 7. Compétence et indépendance des auditeurs

L'auditeur interne connaît la norme ISO/IEC 27001 (formation d'auditeur interne ou équivalent) et n'a pas de responsabilité sur
les processus audités. Pour les audits techniques (A2), le recours à un prestataire d'audit qualifié par l'ANSSI (PASSI) est
possible et cohérent avec la mesure M02 du plan.
