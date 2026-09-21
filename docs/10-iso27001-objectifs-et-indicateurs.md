# Objectifs de sécurité et indicateurs (ISO/IEC 27001, clauses 6.2 et 9.1)

*Rédaction `[Original]`. Les cibles sont des hypothèses de ce projet. Les exemples d'indicateurs du guide EBIOS RM
`[ANSSI p. 81]` servent de point de départ. Voir [`CREDITS.md`](../CREDITS.md).*

## 1. Objectifs de sécurité (clause 6.2)

La clause 6.2 demande que les objectifs soient cohérents avec la politique, mesurables quand c'est possible, suivis, communiqués et
mis à jour, et de préciser ce qui sera fait, avec quelles ressources, qui en est responsable, quand ce sera terminé et comment
les résultats seront évalués. Ils sont posés dans la [politique](07-iso27001-politique-de-securite.md) ; voici leur déclinaison.

| Objectif | Ce qui sera fait | Ressources | Responsable | Échéance | Évaluation |
|---|---|---|---|---|---|
| **O1** : ne jamais interrompre la production ou la distribution plus d'une semaine à cause d'un incident de sécurité | Sauvegardes hors ligne testées (N06), plan de continuité (M12), cloisonnement (N01), gestion de crise (N08), durcissement du système industriel (M09) | Budget priorité 1 et 2 du [plan](tableaux/plan-traitement.md) | Direction générale, DSI | T0+12 mois | I08, I10, I03 |
| **O2** : empêcher la fuite ou l'altération des travaux de R&D et des données de qualité | Protection des données de R&D (M07), authentification forte (N04), postes (N07), intégrité de l'étiquetage (N10), détection (M11) | Idem | RSSI, pharmacien | T0+12 mois | I01, I03, I09 |
| **O3** : maîtriser les risques des prestataires, fournisseurs et laboratoires | Clauses (M03), audits (M05), signalement d'incidents (M04), accès encadrés (N05), inventaire des comptes (N11) | Équipe juridique, RSSI | RSSI, PROC (juridique) | T0+18 mois | I07, I09 |
| **O4** : respecter les obligations légales, réglementaires et contractuelles | Registre des traitements (N12), contacts avec les autorités (5.5), veille réglementaire | DPO, équipe juridique | DPO | T0+12 mois | I11, I12 |
| **O5** : améliorer chaque année le niveau de sécurité et le démontrer | Gouvernance (N09), audit interne, revue de direction, comité de pilotage | Direction, RSSI | Direction générale | Continu | I01, I02, I11, I12, I13 |

## 2. Indicateurs (clause 9.1)

La clause 9.1 demande de déterminer ce qu'il faut surveiller et mesurer, les méthodes, quand mesurer, qui mesure et qui analyse.
Le tableau complet, avec formule, situation de départ, cible, fréquence et responsable, est généré à partir des données :
[`tableaux/indicateurs.md`](tableaux/indicateurs.md).

Les trois catégories suivies :

| Catégorie | Indicateurs | Ce qu'on veut savoir |
|---|---|---|
| **Avancement du plan** | I02 (mesures terminées), I13 (budget), I11 (comités tenus) | Le plan avance-t-il comme prévu ? Reprend les exemples du guide `[ANSSI p. 81]` |
| **Niveau de sécurité atteint** | I01 (socle), I03 (risques élevés), I04 (correctifs), I08 (restaurations), I09 (comptes), I10 (détection) | Le risque baisse-t-il vraiment ? |
| **Comportement et tiers** | I05 et I06 (hameçonnage), I07 (audits de tiers), I12 (non-conformités) | Les personnes et les partenaires suivent-ils ? |

## 3. Comment on mesure et qui analyse `[Original]`

| Question de la clause 9.1 | Réponse |
|---|---|
| Quoi mesurer | Les treize indicateurs ci-dessus |
| Méthode | Formule écrite pour chaque indicateur ; source de la donnée : registre des risques, plan de traitement, journaux, rapports d'audit, résultats des campagnes de sensibilisation |
| Quand | Fréquence de chaque indicateur (trimestrielle, semestrielle ou annuelle) ; consolidation avant chaque comité de pilotage |
| Qui mesure | Le responsable indiqué dans le tableau |
| Qui analyse | Le RSSI, puis le comité de pilotage, puis la direction lors de la revue de direction |
| Conservation | Les valeurs sont ajoutées au [classeur](../reports/SMSI-biotech-classeur.xlsx) à chaque échéance et conservées dans l'historique du dépôt |

## 4. Situation de départ et cibles

Les valeurs de départ sont celles de l'entreprise fictive au lancement du plan : une seule règle du Guide d'hygiène sur 42 est
appliquée sans restriction, deux mesures du plan sur 26 sont terminées, cinq risques sont de niveau élevé. Les cibles visent, à
douze mois, 30 règles sur 42 au vert, 70 % des mesures terminées et un seul risque élevé (R3, sous acceptation formelle) `[Hypothèse]`.

Le script de vérification calcule les valeurs de départ des indicateurs I01, I02 et I03 à partir des données ; les autres
valeurs de départ sont « non mesuré », ce qui est lui-même un constat : l'entreprise ne mesure pas encore ces sujets.
