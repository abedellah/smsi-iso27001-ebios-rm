# Registre des risques

*Fichier généré par `python tools/build.py` à partir de `data/`. Ne pas modifier à la main.*

Score = gravité x vraisemblance. Faible 1 à 3 (Acceptable en l'état) ; Moyen 4 à 7 (Tolérable sous contrôle : suivi et amélioration continue) ; Élevé 8 à 16 (Inacceptable : mesures de réduction à court terme, ou acceptation formelle par la direction).

| Réf. | Scénario de risque | G | V | Niveau initial | G rés. | V rés. | Niveau résiduel | Mesures | Source |
|---|---|---|---|---|---|---|---|---|---|
| R1 | Un concurrent vole des informations de R&D grâce à un canal d'exfiltration direct | G3 | V3 | 9 Élevé | G3 | V2 | 6 Moyen | M01, M02, M07, M08, M11, N01, N02, N03, N07, N09 | ANSSI-EBIOS p. 72, p. 67 |
| R2 | Un concurrent vole des informations de R&D en exfiltrant celles détenues par le laboratoire | G3 | V2 | 6 Moyen | G3 | V1 | 3 Faible | M03, M04, M05, M06, M10, N09 | ANSSI-EBIOS p. 72, p. 67 |
| R3 | Un concurrent vole des informations de R&D grâce à un canal d'exfiltration via le prestataire informatique | G3 | V4 | 12 Élevé | G3 | V3 | 9 Élevé | M03, M04, M05, M07, M11, N04, N05, N09, N11 | ANSSI-EBIOS p. 72, p. 67 |
| R4 | Un activiste provoque un arrêt de la production des vaccins en compromettant l'équipement de maintenance du fournisseur de matériel | G4 | V2 | 8 Élevé | G4 | V1 | 4 Moyen | M03, M04, M05, M09, M12, M13, N06, N08, N09, N13 | ANSSI-EBIOS p. 72, p. 67 |
| R5 | Un activiste perturbe la distribution de vaccins en modifiant leur étiquetage | G4 | V1 | 4 Moyen | G3 | V1 | 3 Faible | M02, M09, M12, N09, N10 | ANSSI-EBIOS p. 72, p. 67 |
| R6 | Un cybercriminel paralyse la production par un rançongiciel déployé à partir du prestataire informatique | G4 | V4 | 16 Élevé | G3 | V2 | 6 Moyen | M02, M03, M04, M05, M07, M09, M11, M12, N01, N02, N04, N05, N06, N07, N08, N09, N11, N13 | Original |
| R7 | Un cybercriminel paralyse la production par un rançongiciel après hameçonnage direct des salariés | G4 | V3 | 12 Élevé | G3 | V2 | 6 Moyen | M01, M02, M07, M09, M11, M12, N01, N02, N03, N04, N06, N07, N08, N09, N13 | Original |

## Cartographie du risque initial

| Gravité \ Vraisemblance | V1 | V2 | V3 | V4 |
|---|---|---|---|---|
| **G4** | R5 | R4 | R7 | R6 |
| **G3** | . | R2 | R1 | R3 |
| **G2** | . | . | . | . |
| **G1** | . | . | . | . |

## Cartographie du risque résiduel

| Gravité \ Vraisemblance | V1 | V2 | V3 | V4 |
|---|---|---|---|---|
| **G4** | R4 | . | . | . |
| **G3** | R2, R5 | R1, R6, R7 | R3 | . |
| **G2** | . | . | . | . |
| **G1** | . | . | . | . |
