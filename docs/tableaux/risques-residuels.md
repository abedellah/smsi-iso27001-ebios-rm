# Risques résiduels

*Fichier généré par `python tools/build.py` à partir de `data/`. Ne pas modifier à la main.*

Fiches établies sur le modèle proposé par le guide EBIOS RM (p. 78). Les niveaux résiduels sont des cibles : ils ne sont atteints que lorsque les mesures listées sont mises en œuvre.

## RR01 (R1) : Un concurrent vole des informations de R&D grâce à un canal d'exfiltration direct

- **Événement redouté :** ER3 : Fuite des informations d'études et recherches de l'entreprise
- **Analyse :** Les mesures M01, M07, M08, M11, N01, N02, N03 ferment les trois modes opératoires (hameçonnage, salarié corrompu, clé USB piégée) mais un salarié corrompu reste possible.
- **Mesures :** M01, M02, M07, M08, M11, N01, N02, N03, N07, N09.
- **Estimation :** gravité G3 puis G3 ; vraisemblance V3 puis V2 ; niveau Élevé (9) puis **Moyen** (6).
- **Gestion du risque résiduel :** tolérable sous contrôle ; suivi semestriel au comité de pilotage, réévaluation à chaque cycle opérationnel.

## RR02 (R2) : Un concurrent vole des informations de R&D en exfiltrant celles détenues par le laboratoire

- **Événement redouté :** ER3 : Fuite des informations d'études et recherches de l'entreprise
- **Analyse :** M06 (déjà terminée) réduit les données détenues par les laboratoires ; M03, M05 et M10 encadrent le laboratoire et l'interconnexion.
- **Mesures :** M03, M04, M05, M06, M10, N09.
- **Estimation :** gravité G3 puis G3 ; vraisemblance V2 puis V1 ; niveau Moyen (6) puis **Faible** (3).
- **Gestion du risque résiduel :** acceptable en l'état ; réexamen à chaque cycle stratégique.

## RR03 (R3) : Un concurrent vole des informations de R&D grâce à un canal d'exfiltration via le prestataire informatique

- **Événement redouté :** ER3 : Fuite des informations d'études et recherches de l'entreprise
- **Analyse :** La direction maintient ce risque à un niveau élevé : le prestataire résiste aux mesures de sécurité, qui changent ses méthodes de travail (p. 80). Les mesures ramènent la vraisemblance de 4 à 3 seulement.
- **Mesures :** M03, M04, M05, M07, M11, N04, N05, N09, N11.
- **Estimation :** gravité G3 puis G3 ; vraisemblance V4 puis V3 ; niveau Élevé (12) puis **Élevé** (9).
- **Gestion du risque résiduel :** accepté par la Direction générale le 30 septembre 2026 ; revue au plus tard le 31 mars 2027. Décision à prendre : Entrer au capital du prestataire pour modifier sa gouvernance de sécurité, ou changer de prestataire (p. 81). (ANSSI-EBIOS p. 80-81 pour la décision et la piste ; dates et responsable : Original)

## RR04 (R4) : Un activiste provoque un arrêt de la production des vaccins en compromettant l'équipement de maintenance du fournisseur de matériel

- **Événement redouté :** ER6 : Interruption de la production ou de la distribution de vaccins pendant plus d'une semaine pendant un pic d'épidémie
- **Analyse :** M13 fournit du matériel de maintenance maîtrisé par la DSI, M09 durcit le système industriel : la vraisemblance tombe à 1. La gravité reste 4 : un arrêt long en pic d'épidémie garde le même impact.
- **Mesures :** M03, M04, M05, M09, M12, M13, N06, N08, N09, N13.
- **Estimation :** gravité G4 puis G4 ; vraisemblance V2 puis V1 ; niveau Élevé (8) puis **Moyen** (4).
- **Gestion du risque résiduel :** tolérable sous contrôle ; suivi semestriel au comité de pilotage, réévaluation à chaque cycle opérationnel.

## RR05 (R5) : Un activiste perturbe la distribution de vaccins en modifiant leur étiquetage

- **Événement redouté :** ER6 : Interruption de la production ou de la distribution de vaccins pendant plus d'une semaine pendant un pic d'épidémie
- **Analyse :** N10 (double contrôle et intégrité de l'étiquetage) détecte l'altération avant expédition : la distribution n'est plus interrompue plus d'une semaine, la gravité passe à 3.
- **Mesures :** M02, M09, M12, N09, N10.
- **Estimation :** gravité G4 puis G3 ; vraisemblance V1 puis V1 ; niveau Moyen (4) puis **Faible** (3).
- **Gestion du risque résiduel :** acceptable en l'état ; réexamen à chaque cycle stratégique.

## RR06 (R6) : Un cybercriminel paralyse la production par un rançongiciel déployé à partir du prestataire informatique

- **Événement redouté :** ER6 : Interruption de la production ou de la distribution de vaccins pendant plus d'une semaine pendant un pic d'épidémie
- **Analyse :** N04, N05, N01 gênent le déploiement depuis le prestataire ; N06 (sauvegardes hors ligne testées) et M12 (continuité) ramènent l'interruption sous une semaine, donc gravité 3.
- **Mesures :** M02, M03, M04, M05, M07, M09, M11, M12, N01, N02, N04, N05, N06, N07, N08, N09, N11, N13.
- **Estimation :** gravité G4 puis G3 ; vraisemblance V4 puis V2 ; niveau Élevé (16) puis **Moyen** (6).
- **Gestion du risque résiduel :** tolérable sous contrôle ; suivi semestriel au comité de pilotage, réévaluation à chaque cycle opérationnel.

## RR07 (R7) : Un cybercriminel paralyse la production par un rançongiciel après hameçonnage direct des salariés

- **Événement redouté :** ER6 : Interruption de la production ou de la distribution de vaccins pendant plus d'une semaine pendant un pic d'épidémie
- **Analyse :** M01, N07, N03, N01 réduisent la probabilité de compromission et de propagation ; N06 et M12 limitent la durée d'interruption.
- **Mesures :** M01, M02, M07, M09, M11, M12, N01, N02, N03, N04, N06, N07, N08, N09, N13.
- **Estimation :** gravité G4 puis G3 ; vraisemblance V3 puis V2 ; niveau Élevé (12) puis **Moyen** (6).
- **Gestion du risque résiduel :** tolérable sous contrôle ; suivi semestriel au comité de pilotage, réévaluation à chaque cycle opérationnel.
