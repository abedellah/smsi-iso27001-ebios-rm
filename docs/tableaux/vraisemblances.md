# Vraisemblance des scénarios opérationnels

*Fichier généré par `python tools/build.py` à partir de `data/`. Ne pas modifier à la main.*

Vraisemblance d'un mode = la plus faible de ses actions ; vraisemblance du scénario = celle du mode de moindre effort pour l'attaquant (guide EBIOS RM, p. 65).

| Risque | Mode | Description | Actions élémentaires | Vraisemblance |
|---|---|---|---|---|
| R1 | Mode 1 | Hameçonnage du service RH ou canal préexistant, latéralisation, exfiltration | V4 > V3 > V3 > V3 > V3 | V3 |
| R1 | Mode 2 | Corruption d'un salarié de la R&D | V2 > V2 > V4 | V2 |
| R1 | Mode 3 | Corruption du personnel d'entretien, clé USB piégée | V2 > V3 > V3 > V4 | V2 |
| R1 | **Scénario** | Mode de moindre effort |  | **V3** |
| R2 | Mode 1 | Compromission du SI du laboratoire, exfiltration des copies de travaux | V4 > V2 > V3 | V2 |
| R2 | Mode 2 | Rebond par l'interconnexion avec le laboratoire | V2 > V2 > V3 | V2 |
| R2 | **Scénario** | Mode de moindre effort |  | **V2** |
| R3 | Mode 1 | Compromission du prestataire informatique et usage de ses accès | V4 > V4 > V4 > V4 | V4 |
| R3 | Mode 2 | Corruption d'un employé du prestataire | V2 > V2 > V4 | V2 |
| R3 | **Scénario** | Mode de moindre effort |  | **V4** |
| R4 | Mode 1 | Compromission du fournisseur de matériel, puis de son équipement de maintenance | V4 > V3 > V3 > V3 > V2 | V2 |
| R4 | Mode 2 | Piégeage de l'équipement de maintenance chez le fournisseur | V2 > V3 > V2 | V2 |
| R4 | **Scénario** | Mode de moindre effort |  | **V2** |
| R5 | Mode 1 | Propagation vers les serveurs de traçabilité et altération de l'étiquetage | V3 > V2 > V1 | V1 |
| R5 | Mode 2 | Corruption d'un opérateur de conditionnement | V2 > V1 | V1 |
| R5 | **Scénario** | Mode de moindre effort |  | **V1** |
| R6 | Mode 1 | Compromission du prestataire informatique, déploiement du rançongiciel | V4 > V4 > V4 > V4 > V4 | V4 |
| R6 | **Scénario** | Mode de moindre effort |  | **V4** |
| R7 | Mode 1 | Hameçonnage direct, élévation de droits, propagation, chiffrement | V4 > V3 > V3 > V3 | V3 |
| R7 | Mode 2 | Clé USB piégée déposée dans les locaux | V3 > V2 > V3 | V2 |
| R7 | **Scénario** | Mode de moindre effort |  | **V3** |
