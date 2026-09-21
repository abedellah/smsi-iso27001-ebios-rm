# Support et amélioration (ISO/IEC 27001, clauses 7 et 10)

*Rédaction `[Original]`. Cas fictif. Voir [`CREDITS.md`](../CREDITS.md).*

## 1. Ressources et compétences (clauses 7.1 et 7.2)

Les moyens sont ceux du [plan de traitement](tableaux/plan-traitement.md) : budget estimé, jours-hommes, responsables. Les compétences
nécessaires aux rôles qui influencent la performance du SMSI :

| Rôle | Compétences requises | Comment elles sont assurées |
|---|---|---|
| RSSI | Gestion des risques (EBIOS RM), ISO/IEC 27001, gestion de projet | Formation d'implémenteur ISO 27001 et à la méthode EBIOS RM ; expérience |
| DSI et équipes | Sécurité des systèmes d'information et des systèmes industriels, exploitation sécurisée | Formation (mesure N13), audit par un prestataire qualifié (M02) |
| Auditeur interne | ISO/IEC 27001, techniques d'audit, indépendance | Formation d'auditeur interne, ou prestataire |
| Pharmacien, responsables qualité et production | Rôle de propriétaire de risque : comprendre le lien entre sécurité et sécurité des patients | Séance de présentation des risques, appui du RSSI |
| DPO | Réglementation sur les données personnelles | Formation et veille |
| Direction générale | Rôle dans le SMSI : décider, accepter les risques, allouer des moyens | Séance de présentation avant la première revue |

Les preuves (attestations, comptes rendus de formation) sont conservées dans le dossier des ressources humaines.

## 2. Sensibilisation (clause 7.3)

Les personnes qui travaillent sous le contrôle de l'organisme connaissent la politique, leur contribution et les conséquences d'un
manquement. Aujourd'hui, la sensibilisation se limite à une session à la prise de poste et à la charte informatique
`[ANSSI p. 11]`. Le plan la renforce :

- campagne de sensibilisation à l'hameçonnage par un prestataire spécialisé (mesure M01, en cours) ;
- formation annuelle de tous les salariés et campagnes d'hameçonnage simulé (indicateurs I05 et I06) ;
- formation spécifique des équipes de la DSI et de la production (mesure N13) ;
- rappel de la politique à chaque revue de direction.

## 3. Communication (clause 7.4)

| Quoi | À qui | Quand | Par qui | Canal |
|---|---|---|---|---|
| Politique de sécurité | Tout le personnel, prestataires et laboratoires | À l'approbation, puis chaque année | Direction générale | Intranet, remise à l'arrivée, clause des contrats |
| Règles et consignes de sécurité | Tout le personnel | À l'arrivée et lors de changements | RSSI, RH | Sessions, affichage, messagerie |
| Alertes de sécurité | Personnel concerné | Selon l'événement | RSSI | Messagerie, point d'équipe |
| Incidents chez un prestataire ou un laboratoire | RSSI, équipe juridique | Sans délai | Prestataire ou laboratoire | Procédure de signalement (mesure M04) |
| Résultats des indicateurs et avancement | Comité de pilotage, direction | Tous les six mois | RSSI | Tableau de bord, comité |
| Notification d'incident aux autorités | ANSSI et CERT-FR, CNIL, autorités sanitaires selon le cas | Dans les délais légaux | DPO, direction | Procédures de gestion des incidents (N08) |

## 4. Informations documentées (clause 7.5)

### Registre des documents du SMSI

| Document | Clause | Fichier | Propriétaire | Revue |
|---|---|---|---|---|
| Contexte et périmètre | 4.1 à 4.3 | [01](01-iso27001-contexte-et-perimetre.md) | RSSI | Annuelle |
| Politique de sécurité | 5.2 | [07](07-iso27001-politique-de-securite.md) | Direction générale | Annuelle |
| Rôles et responsabilités | 5.3 | [07](07-iso27001-politique-de-securite.md), §6 | Direction générale | Annuelle |
| Méthode d'appréciation des risques | 6.1.2 | [08](08-iso27001-methode-appreciation-risques.md) | RSSI | Annuelle |
| Résultats de l'appréciation des risques | 6.1.2, 8.2 | [Registre](tableaux/registre-risques.md), [ateliers 1 à 5](02-ebios-atelier1-cadrage.md) | RSSI | À chaque cycle |
| Plan de traitement des risques | 6.1.3, 8.3 | [Plan](tableaux/plan-traitement.md) | RSSI | Semestrielle |
| Déclaration d'applicabilité | 6.1.3 d | [DdA](tableaux/declaration-applicabilite.md) | RSSI | Semestrielle |
| Objectifs de sécurité | 6.2 | [10](10-iso27001-objectifs-et-indicateurs.md) | Direction générale | Annuelle |
| Résultats de surveillance et de mesure | 9.1 | [Indicateurs](tableaux/indicateurs.md), [classeur](../reports/SMSI-biotech-classeur.xlsx) | RSSI | Semestrielle |
| Programme et rapports d'audit interne | 9.2 | [11](11-iso27001-audit-interne.md) | Auditeur interne | Annuelle |
| Comptes rendus de revue de direction | 9.3 | [12](12-iso27001-revue-de-direction.md) | Direction générale | Annuelle |
| Non-conformités et actions correctives | 10.2 | §6 ci-dessous | RSSI | Continue |
| Preuves de compétence | 7.2 | Dossiers RH | RH | Continue |

### Règles de maîtrise `[Original]`

- **Identification** : nom explicite, numéro d'ordre, version et date ; l'historique est celui du dépôt Git.
- **Approbation** : toute version applicable est approuvée par le propriétaire du document avant diffusion.
- **Accès** : les documents du SMSI sont classés « interne » ; le registre des risques et les rapports d'audit sont « confidentiels ».
- **Conservation** : les enregistrements (comptes rendus, rapports, preuves) sont conservés au moins trois ans, soit un cycle
  d'audit de certification.
- **Modification** : par demande écrite, revue par le RSSI et approbation ; les modifications sont visibles dans l'historique.

## 5. Procédure d'action corrective (clause 10.2)

Quand une non-conformité apparaît (audit, incident, revue, constat d'un tiers) :

1. **Réagir** : contenir la situation, corriger, traiter les conséquences.
2. **Évaluer la cause** : rechercher la cause racine et vérifier si d'autres cas semblables existent.
3. **Décider et mettre en œuvre l'action corrective**, avec un responsable et une échéance.
4. **Vérifier l'efficacité** de l'action à l'audit suivant ou au comité de pilotage.
5. **Mettre à jour** le registre des risques et la déclaration d'applicabilité si nécessaire.
6. **Conserver la trace** dans le registre ci-dessous.

## 6. Registre des non-conformités et actions correctives

Écarts constatés à l'évaluation initiale du [socle de sécurité](tableaux/socle.md), enregistrés pour suivi. Les statuts sont ceux de
la mesure correspondante du [plan](tableaux/plan-traitement.md) `[Original]`.

| N° | Constat | Origine | Gravité | Action corrective (mesure) | Responsable | Échéance | Statut |
|---|---|---|---|---|---|---|---|
| NC-01 | Aucune politique de sauvegarde appliquée : elle est en cours de rédaction (règle 37) `[ANSSI p. 30]` | Socle | Majeure | Sauvegardes hors ligne testées (N06) | DSI | T0+6 mois | Ouverte |
| NC-02 | Pas de cloisonnement entre les réseaux internes, dont la R&D (règle 19) `[ANSSI p. 64]` | Socle | Majeure | Cloisonnement des réseaux (N01) | DSI | T0+12 mois | Ouverte |
| NC-03 | Correctifs de sécurité appliqués sans rigueur (règle 34) `[ANSSI p. 64]` | Socle | Majeure | Politique de mise à jour (N02) | DSI | T0+6 mois | Ouverte |
| NC-04 | Prestataire informatique à droits élevés sans exigence de sécurité contractuelle (règle 3) `[ANSSI p. 67, p. 77]` | Socle | Majeure | Clauses (M03), audits (M05), accès encadrés (N05) | Équipe juridique, RSSI | T0+18 mois | Ouverte, M03 en cours |
| NC-05 | Aucune supervision des actions ni des journaux (règle 36) `[ANSSI p. 64]` | Socle | Majeure | Surveillance renforcée (M11) | DSI | T0+9 mois | Ouverte |
| NC-06 | Ports USB sans restriction (règle 15) `[ANSSI p. 64]` | Socle | Mineure | Blocage par défaut (N03) | DSI | T0+3 mois | Ouverte |
| NC-07 | Compte administrateur non nominatif pour l'ERP (règle 8) `[ANSSI p. 30]` | Socle | Mineure | Authentification forte et comptes nominatifs (N04) | RSSI | T0+4 mois | Ouverte |

Les autres écarts du socle sont suivis dans le [tableau du socle](tableaux/socle.md) avec leur mesure de traitement.

## 7. Amélioration continue (clause 10.1)

L'amélioration vient de trois sources : les résultats des indicateurs, les audits internes, et la revue de direction. Le cycle
opérationnel annuel et le cycle stratégique de trois ans d'EBIOS RM `[ANSSI p. 11]` en fournissent le rythme.
