# Scénarios opérationnels : graphes d'attaque

*Fichier généré par `python tools/build.py` à partir de `data/`. Ne pas modifier à la main.*

Un graphe par risque. Chaque bloc est un mode opératoire, lu de gauche à droite : de la reconnaissance jusqu'à l'exploitation. V1 à V4 est la vraisemblance élémentaire de l'action ; « règles » renvoie aux règles du Guide d'hygiène dont l'écart la facilite (voir [le socle](socle.md)). La vraisemblance du scénario est celle du mode de moindre effort, calculée dans [vraisemblances.md](vraisemblances.md).

## R1 : Un concurrent vole des informations de R&D grâce à un canal d'exfiltration direct

Gravité G3, vraisemblance V3 (ANSSI-EBIOS p. 72, p. 67).

```mermaid
flowchart LR
  subgraph R1_M1["Mode 1 : Hameçonnage du service RH ou canal préexistant, latéralisation, exfiltration"]
    direction LR
    R1_1_1["Reconnaissance externe par sources ouvertes<br/>V4"]
    R1_1_2["Intrusion par message d'hameçonnage sur la messagerie RH<br/>V3<br/>règles 2, 24"]
    R1_1_3["Reconnaissance du réseau bureautique du site de Paris<br/>V3<br/>règles 4"]
    R1_1_4["Latéralisation vers le réseau de la R&D<br/>V3<br/>règles 19"]
    R1_1_5["Exploitation d'un maliciel de collecte et d'exfiltration<br/>V3<br/>règles 14, 34, 36"]
    R1_1_1 --> R1_1_2 --> R1_1_3 --> R1_1_4 --> R1_1_5
  end
  subgraph R1_M2["Mode 2 : Corruption d'un salarié de la R&D"]
    direction LR
    R1_2_1["Reconnaissance externe avancée<br/>V2"]
    R1_2_2["Corruption d'un salarié de l'équipe R&D<br/>V2<br/>règles 2"]
    R1_2_3["Vol des données depuis le poste, sans supervision<br/>V4<br/>règles 9, 36"]
    R1_2_1 --> R1_2_2 --> R1_2_3
  end
  subgraph R1_M3["Mode 3 : Corruption du personnel d'entretien, clé USB piégée"]
    direction LR
    R1_3_1["Reconnaissance externe avancée<br/>V2"]
    R1_3_2["Corruption d'un prestataire d'entretien des locaux<br/>V3<br/>règles 26"]
    R1_3_3["Clé USB piégée connectée sur un poste de R&D<br/>V3<br/>règles 15, 26"]
    R1_3_4["Vol et exploitation des données de R&D<br/>V4<br/>règles 9, 36"]
    R1_3_1 --> R1_3_2 --> R1_3_3 --> R1_3_4
  end
```

## R2 : Un concurrent vole des informations de R&D en exfiltrant celles détenues par le laboratoire

Gravité G3, vraisemblance V2 (ANSSI-EBIOS p. 72, p. 67).

```mermaid
flowchart LR
  subgraph R2_M1["Mode 1 : Compromission du SI du laboratoire, exfiltration des copies de travaux"]
    direction LR
    R2_1_1["Reconnaissance des laboratoires partenaires (publications, sites)<br/>V4"]
    R2_1_2["Compromission du SI du laboratoire (hameçonnage, vulnérabilité)<br/>V2<br/>règles 3"]
    R2_1_3["Exfiltration des données de R&D que le laboratoire détient<br/>V3<br/>règles 25"]
    R2_1_1 --> R2_1_2 --> R2_1_3
  end
  subgraph R2_M2["Mode 2 : Rebond par l'interconnexion avec le laboratoire"]
    direction LR
    R2_2_1["Compromission du laboratoire<br/>V2<br/>règles 3"]
    R2_2_2["Passage par l'interconnexion non filtrée vers la R&D<br/>V2<br/>règles 25, 19"]
    R2_2_3["Exfiltration des données<br/>V3<br/>règles 36"]
    R2_2_1 --> R2_2_2 --> R2_2_3
  end
```

## R3 : Un concurrent vole des informations de R&D grâce à un canal d'exfiltration via le prestataire informatique

Gravité G3, vraisemblance V4 (ANSSI-EBIOS p. 72, p. 67).

```mermaid
flowchart LR
  subgraph R3_M1["Mode 1 : Compromission du prestataire informatique et usage de ses accès"]
    direction LR
    R3_1_1["Reconnaissance du prestataire informatique<br/>V4"]
    R3_1_2["Compromission du SI du prestataire, dont la sécurité est faible<br/>V4<br/>règles 3"]
    R3_1_3["Usage des droits d'accès élevés du prestataire sur les serveurs de R&D<br/>V4<br/>règles 5, 8, 13"]
    R3_1_4["Exfiltration par un canal de maintenance<br/>V4<br/>règles 36"]
    R3_1_1 --> R3_1_2 --> R3_1_3 --> R3_1_4
  end
  subgraph R3_M2["Mode 2 : Corruption d'un employé du prestataire"]
    direction LR
    R3_2_1["Reconnaissance externe avancée<br/>V2"]
    R3_2_2["Corruption d'un administrateur du prestataire<br/>V2<br/>règles 3"]
    R3_2_3["Vol des données de R&D<br/>V4<br/>règles 5, 36"]
    R3_2_1 --> R3_2_2 --> R3_2_3
  end
```

## R4 : Un activiste provoque un arrêt de la production des vaccins en compromettant l'équipement de maintenance du fournisseur de matériel

Gravité G4, vraisemblance V2 (ANSSI-EBIOS p. 72, p. 67).

```mermaid
flowchart LR
  subgraph R4_M1["Mode 1 : Compromission du fournisseur de matériel, puis de son équipement de maintenance"]
    direction LR
    R4_1_1["Reconnaissance du fournisseur de matériel<br/>V4"]
    R4_1_2["Compromission du SI ou des postes du fournisseur<br/>V3"]
    R4_1_3["Piégeage de l'équipement de maintenance utilisé sur le système industriel<br/>V3<br/>règles 7"]
    R4_1_4["Connexion au réseau industriel sans cloisonnement<br/>V3<br/>règles 19, 28"]
    R4_1_5["Modification des paramètres de production ou arrêt de la ligne<br/>V2<br/>règles 12, 35"]
    R4_1_1 --> R4_1_2 --> R4_1_3 --> R4_1_4 --> R4_1_5
  end
  subgraph R4_M2["Mode 2 : Piégeage de l'équipement de maintenance chez le fournisseur"]
    direction LR
    R4_2_1["Accès à l'équipement en cours de fabrication ou de préparation<br/>V2"]
    R4_2_2["Déclenchement lors de la maintenance sur site<br/>V3<br/>règles 7"]
    R4_2_3["Arrêt de la ligne de production<br/>V2<br/>règles 12, 35"]
    R4_2_1 --> R4_2_2 --> R4_2_3
  end
```

## R5 : Un activiste perturbe la distribution de vaccins en modifiant leur étiquetage

Gravité G4, vraisemblance V1 (ANSSI-EBIOS p. 72, p. 67).

```mermaid
flowchart LR
  subgraph R5_M1["Mode 1 : Propagation vers les serveurs de traçabilité et altération de l'étiquetage"]
    direction LR
    R5_1_1["Intrusion sur le réseau bureautique<br/>V3<br/>règles 24, 14"]
    R5_1_2["Latéralisation vers les serveurs de traçabilité<br/>V2<br/>règles 19"]
    R5_1_3["Altération des données d'étiquetage avant expédition<br/>V1<br/>règles 9"]
    R5_1_1 --> R5_1_2 --> R5_1_3
  end
  subgraph R5_M2["Mode 2 : Corruption d'un opérateur de conditionnement"]
    direction LR
    R5_2_1["Corruption d'un opérateur<br/>V2<br/>règles 2"]
    R5_2_2["Modification de l'étiquetage à la source<br/>V1<br/>règles 9"]
    R5_2_1 --> R5_2_2
  end
```

## R6 : Un cybercriminel paralyse la production par un rançongiciel déployé à partir du prestataire informatique

Gravité G4, vraisemblance V4 (Original).

```mermaid
flowchart LR
  subgraph R6_M1["Mode 1 : Compromission du prestataire informatique, déploiement du rançongiciel"]
    direction LR
    R6_1_1["Reconnaissance du prestataire informatique<br/>V4"]
    R6_1_2["Compromission du SI du prestataire<br/>V4<br/>règles 3"]
    R6_1_3["Usage des comptes privilégiés du prestataire<br/>V4<br/>règles 5, 8, 13"]
    R6_1_4["Propagation aux serveurs de R&D, de production et de traçabilité<br/>V4<br/>règles 19, 28"]
    R6_1_5["Chiffrement des systèmes et des sauvegardes<br/>V4<br/>règles 37"]
    R6_1_1 --> R6_1_2 --> R6_1_3 --> R6_1_4 --> R6_1_5
  end
```

## R7 : Un cybercriminel paralyse la production par un rançongiciel après hameçonnage direct des salariés

Gravité G4, vraisemblance V3 (Original).

```mermaid
flowchart LR
  subgraph R7_M1["Mode 1 : Hameçonnage direct, élévation de droits, propagation, chiffrement"]
    direction LR
    R7_1_1["Message d'hameçonnage envoyé aux salariés<br/>V4<br/>règles 2, 24"]
    R7_1_2["Exécution du maliciel sur un poste, droits d'administration locaux<br/>V3<br/>règles 14, 29"]
    R7_1_3["Propagation vers la production et la traçabilité<br/>V3<br/>règles 19"]
    R7_1_4["Chiffrement des systèmes et des sauvegardes<br/>V3<br/>règles 37"]
    R7_1_1 --> R7_1_2 --> R7_1_3 --> R7_1_4
  end
  subgraph R7_M2["Mode 2 : Clé USB piégée déposée dans les locaux"]
    direction LR
    R7_2_1["Dépôt de clés USB piégées<br/>V3<br/>règles 26"]
    R7_2_2["Exécution automatique sur un poste<br/>V2<br/>règles 15"]
    R7_2_3["Propagation et chiffrement<br/>V3<br/>règles 19, 37"]
    R7_2_1 --> R7_2_2 --> R7_2_3
  end
```
