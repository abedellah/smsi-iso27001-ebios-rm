# Déclaration d'applicabilité (ISO/IEC 27001:2022, Annexe A)

*Fichier généré par `python tools/build.py` à partir de `data/`. Ne pas modifier à la main.*

Les intitulés sont des paraphrases courtes de l'Annexe A, pas le texte de la norme. Le statut est calculé à partir de l'état des règles du socle et des mesures du plan de traitement liées à la mesure de l'Annexe A ; les mesures sans lien sont décrites dans `data/soa_manuel.yaml`.

**Bilan : 0 mises en œuvre, 45 partielles, 44 à mettre en œuvre, 4 exclues (sur 93).**

| N° | Mesure | Thème | Applicable | Statut | Base du choix | Justification | Mesures du plan | Risques | Exclusion approuvée par |
|---|---|---|---|---|---|---|---|---|---|
| 5.1 | Politiques de sécurité de l'information | organisationnel | Oui | À mettre en œuvre | risque | Retenue pour traiter R1, R2, R3, R4, R5, R6, R7. | N09 | R1, R2, R3, R4, R5, R6, R7 | - |
| 5.2 | Fonctions et responsabilités liées à la sécurité de l'information | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R1, R2, R3, R4, R5, R6, R7 ; corrige l'écart à la règle 39 du Guide d'hygiène. | N09 | R1, R2, R3, R4, R5, R6, R7 | - |
| 5.3 | Séparation des tâches | organisationnel | Oui | À mettre en œuvre | risque | Retenue pour traiter R3, R6. | N05 | R3, R6 | - |
| 5.4 | Responsabilités de la direction | organisationnel | Oui | À mettre en œuvre | risque | Retenue pour traiter R1, R2, R3, R4, R5, R6, R7. | N09 | R1, R2, R3, R4, R5, R6, R7 | - |
| 5.5 | Contacts avec les autorités | organisationnel | Oui | À mettre en œuvre | légal | Établir les contacts pour notifier un incident : ANSSI et CERT-FR, autorités sanitaires, CNIL. | - | - | - |
| 5.6 | Contacts avec des groupes de spécialistes | organisationnel | Oui | À mettre en œuvre | bonne pratique | Rejoindre une communauté de veille du secteur santé et pharmaceutique. | - | - | - |
| 5.7 | Renseignement sur les menaces | organisationnel | Oui | À mettre en œuvre | bonne pratique | Veille sur la menace cybercriminelle et activiste, que la direction demande de surveiller (guide EBIOS RM p. 81). | - | - | - |
| 5.8 | Sécurité de l'information dans la gestion de projet | organisationnel | Oui | À mettre en œuvre | bonne pratique | Intégrer la sécurité dans les projets, dont la modernisation des systèmes industriels. | - | - | - |
| 5.9 | Inventaire des informations et des autres actifs | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R3, R6 ; corrige l'écart aux règles 4, 7 du Guide d'hygiène. | N11 | R3, R6 | - |
| 5.10 | Utilisation correcte de l'information et des actifs | organisationnel | Oui | Partielle | socle | Corrige l'écart à la règle 2 du Guide d'hygiène. | - | - | - |
| 5.11 | Restitution des actifs | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R3, R6 ; corrige l'écart à la règle 6 du Guide d'hygiène. | N11 | R3, R6 | - |
| 5.12 | Classification de l'information | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R2 ; corrige l'écart à la règle 4 du Guide d'hygiène. | M06 | R2 | - |
| 5.13 | Marquage de l'information | organisationnel | Oui | À mettre en œuvre | bonne pratique | Marquer les documents et données de R&D selon leur confidentialité. | - | - | - |
| 5.14 | Transfert de l'information | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R2 ; corrige l'écart aux règles 18, 24, 25 du Guide d'hygiène. | M06, M10 | R2 | - |
| 5.15 | Contrôle d'accès | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R3, R6 ; corrige l'écart aux règles 8, 9 du Guide d'hygiène. | N05 | R3, R6 | - |
| 5.16 | Gestion des identités | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R3, R6, R7 ; corrige l'écart aux règles 5, 8 du Guide d'hygiène. | N04 | R3, R6, R7 | - |
| 5.17 | Informations d'authentification | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R3, R6, R7 ; corrige l'écart aux règles 10, 11, 12 du Guide d'hygiène. | N04 | R3, R6, R7 | - |
| 5.18 | Droits d'accès | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R3, R6 ; corrige l'écart aux règles 5, 6, 9 du Guide d'hygiène. | N05, N11 | R3, R6 | - |
| 5.19 | Sécurité de l'information dans les relations avec les fournisseurs | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R2, R3, R4, R6 ; corrige l'écart à la règle 3 du Guide d'hygiène. | M03, N05 | R2, R3, R4, R6 | - |
| 5.20 | Sécurité dans les accords avec les fournisseurs | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R2, R3, R4, R6 ; corrige l'écart à la règle 3 du Guide d'hygiène. | M03, M04 | R2, R3, R4, R6 | - |
| 5.21 | Sécurité de la chaîne d'approvisionnement des TIC | organisationnel | Oui | Partielle | risque, socle | Retenue pour traiter R4 ; corrige l'écart aux règles 3, 42 du Guide d'hygiène. | M13 | R4 | - |
| 5.22 | Suivi et revue des services des fournisseurs | organisationnel | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R2, R3, R4, R6 ; corrige l'écart à la règle 3 du Guide d'hygiène. | M04, M05 | R2, R3, R4, R6 | - |
| 5.23 | Sécurité de l'information pour l'utilisation de services en nuage | organisationnel | Oui | Partielle | socle | Corrige l'écart aux règles 3, 42 du Guide d'hygiène. | - | - | - |
| 5.24 | Planification et préparation de la gestion des incidents | organisationnel | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R2, R3, R4, R6, R7 ; corrige l'écart à la règle 40 du Guide d'hygiène. | M04, N08 | R2, R3, R4, R6, R7 | - |
| 5.25 | Appréciation et décision sur les événements de sécurité | organisationnel | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R4, R6, R7 ; corrige l'écart à la règle 40 du Guide d'hygiène. | N08 | R4, R6, R7 | - |
| 5.26 | Réponse aux incidents de sécurité | organisationnel | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R2, R3, R4, R6, R7 ; corrige l'écart à la règle 40 du Guide d'hygiène. | M04, N08 | R2, R3, R4, R6, R7 | - |
| 5.27 | Retour d'expérience sur les incidents | organisationnel | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R4, R6, R7 ; corrige l'écart à la règle 40 du Guide d'hygiène. | N08 | R4, R6, R7 | - |
| 5.28 | Recueil de preuves | organisationnel | Oui | À mettre en œuvre | risque | Retenue pour traiter R4, R6, R7. | N08 | R4, R6, R7 | - |
| 5.29 | Sécurité de l'information pendant une perturbation | organisationnel | Oui | Partielle | risque | Retenue pour traiter R4, R5, R6, R7. | M12 | R4, R5, R6, R7 | - |
| 5.30 | Préparation des TIC à la continuité d'activité | organisationnel | Oui | Partielle | risque | Retenue pour traiter R4, R5, R6, R7. | M12, N06 | R4, R5, R6, R7 | - |
| 5.31 | Exigences légales, réglementaires et contractuelles | organisationnel | Oui | À mettre en œuvre | - | - | N12 | - | - |
| 5.32 | Droits de propriété intellectuelle | organisationnel | Oui | Partielle | légal | Protéger les droits sur les travaux de R&D (secrets industriels, brevets) et respecter les licences. | - | - | - |
| 5.33 | Protection des enregistrements | organisationnel | Oui | À mettre en œuvre | - | - | N12 | - | - |
| 5.34 | Vie privée et protection des données personnelles | organisationnel | Oui | À mettre en œuvre | - | - | N12 | - | - |
| 5.35 | Revue indépendante de la sécurité de l'information | organisationnel | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R1, R2, R3, R4, R5, R6, R7 ; corrige l'écart à la règle 38 du Guide d'hygiène. | M02, M05, N09 | R1, R2, R3, R4, R5, R6, R7 | - |
| 5.36 | Conformité aux politiques, règles et normes | organisationnel | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R1, R2, R3, R4, R5, R6, R7 ; corrige l'écart à la règle 38 du Guide d'hygiène. | N09 | R1, R2, R3, R4, R5, R6, R7 | - |
| 5.37 | Procédures d'exploitation documentées | organisationnel | Oui | À mettre en œuvre | bonne pratique | Documenter les procédures d'exploitation : sauvegarde, mise à jour, administration. | - | - | - |
| 6.1 | Vérification des antécédents | personnes | Oui | Partielle | légal, bonne pratique | Vérifications à l'embauche proportionnées au poste, dans le cadre du droit du travail. | - | - | - |
| 6.2 | Conditions d'emploi | personnes | Oui | Partielle | contractuel | La charte informatique existe (guide EBIOS RM p. 11) ; il reste à inscrire les obligations de sécurité dans les contrats. | - | - | - |
| 6.3 | Sensibilisation, apprentissage et formation | personnes | Oui | Partielle | risque, socle | Retenue pour traiter R1, R4, R6, R7 ; corrige l'écart aux règles 1, 2 du Guide d'hygiène. | M01, N13 | R1, R4, R6, R7 | - |
| 6.4 | Processus disciplinaire | personnes | Oui | À mettre en œuvre | bonne pratique | Prévoir la sanction des manquements graves aux règles de sécurité. | - | - | - |
| 6.5 | Responsabilités après la fin ou le changement d'emploi | personnes | Oui | Partielle | risque, socle | Retenue pour traiter R3, R6 ; corrige l'écart à la règle 6 du Guide d'hygiène. | N11 | R3, R6 | - |
| 6.6 | Engagements de confidentialité | personnes | Oui | Partielle | bonne pratique | Accords de confidentialité avec les salariés, les universités et les laboratoires. | - | - | - |
| 6.7 | Travail à distance | personnes | Oui | Partielle | socle | Corrige l'écart aux règles 32, 33 du Guide d'hygiène. | - | - | - |
| 6.8 | Signalement des événements de sécurité | personnes | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R4, R6, R7 ; corrige l'écart à la règle 40 du Guide d'hygiène. | N08 | R4, R6, R7 | - |
| 7.1 | Périmètres de sécurité physique | physique | Oui | Partielle | risque, socle | Retenue pour traiter R1 ; corrige l'écart à la règle 26 du Guide d'hygiène. | M08 | R1 | - |
| 7.2 | Accès physiques | physique | Oui | Partielle | risque, socle | Retenue pour traiter R1 ; corrige l'écart à la règle 26 du Guide d'hygiène. | M08 | R1 | - |
| 7.3 | Sécurisation des bureaux, salles et équipements | physique | Oui | Partielle | risque, socle | Retenue pour traiter R1 ; corrige l'écart à la règle 26 du Guide d'hygiène. | M08 | R1 | - |
| 7.4 | Surveillance de la sécurité physique | physique | Oui | À mettre en œuvre | bonne pratique | Surveiller les accès aux bâtiments et aux zones de R&D et de production. | - | - | - |
| 7.5 | Protection contre les menaces physiques et environnementales | physique | Oui | Partielle | bonne pratique | Protection contre l'incendie et l'eau des locaux techniques et de production. | - | - | - |
| 7.6 | Travail dans les zones sécurisées | physique | Oui | Partielle | bonne pratique | Règles de travail dans les zones de production et de R&D à accès restreint. | - | - | - |
| 7.7 | Bureau propre et écran vide | physique | Oui | À mettre en œuvre | bonne pratique | Bureau propre et verrouillage automatique des écrans. | - | - | - |
| 7.8 | Emplacement et protection du matériel | physique | Oui | Partielle | bonne pratique | Placer et protéger les équipements hors de la vue et de l'accès du public. | - | - | - |
| 7.9 | Sécurité des actifs hors des locaux | physique | Oui | Partielle | risque, socle | Retenue pour traiter R1, R6, R7 ; corrige l'écart aux règles 30, 31 du Guide d'hygiène. | N07 | R1, R6, R7 | - |
| 7.10 | Supports de stockage | physique | Oui | Partielle | risque, socle | Retenue pour traiter R1, R7 ; corrige l'écart aux règles 15, 30 du Guide d'hygiène. | N03 | R1, R7 | - |
| 7.11 | Services généraux (énergie, climatisation) | physique | Oui | Partielle | bonne pratique | Alimentation électrique secourue et climatisation des salles serveurs. | - | - | - |
| 7.12 | Sécurité du câblage | physique | Oui | À mettre en œuvre | bonne pratique | Protéger le câblage réseau et électrique contre l'interception et les dégradations. | - | - | - |
| 7.13 | Maintenance du matériel | physique | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R4, R5, R6, R7 ; corrige l'écart à la règle 35 du Guide d'hygiène. | M09 | R4, R5, R6, R7 | - |
| 7.14 | Mise au rebut ou réutilisation sécurisée du matériel | physique | Oui | À mettre en œuvre | bonne pratique | Effacer ou détruire les supports avant mise au rebut, avec traçabilité. | - | - | - |
| 8.1 | Terminaux des utilisateurs | technologique | Oui | Partielle | risque, socle | Retenue pour traiter R1, R4, R6, R7 ; corrige l'écart aux règles 7, 14, 16, 17, 33 du Guide d'hygiène. | M13, N07 | R1, R4, R6, R7 | - |
| 8.2 | Droits d'accès privilégiés | technologique | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R3, R6, R7 ; corrige l'écart aux règles 5, 27, 28, 29 du Guide d'hygiène. | N04, N05, N11 | R3, R6, R7 | - |
| 8.3 | Restriction d'accès à l'information | technologique | Oui | Partielle | risque, socle | Retenue pour traiter R1, R2, R3, R5, R6, R7 ; corrige l'écart à la règle 9 du Guide d'hygiène. | M06, M07, N10 | R1, R2, R3, R5, R6, R7 | - |
| 8.4 | Accès au code source | technologique | Non (exclue) | Exclue | - | L'entreprise ne développe pas de logiciel : il n'y a pas de code source à protéger (hypothèse de ce cas). | - | - | Direction générale |
| 8.5 | Authentification sécurisée | technologique | Oui | Partielle | risque, socle | Retenue pour traiter R3, R6, R7 ; corrige l'écart aux règles 10, 13 du Guide d'hygiène. | N04 | R3, R6, R7 | - |
| 8.6 | Dimensionnement des ressources | technologique | Oui | À mettre en œuvre | bonne pratique | Surveiller la capacité des serveurs et du réseau, notamment en pic d'épidémie. | - | - | - |
| 8.7 | Protection contre les logiciels malveillants | technologique | Oui | Partielle | risque, socle | Retenue pour traiter R1, R6, R7 ; corrige l'écart aux règles 14, 24 du Guide d'hygiène. | N07 | R1, R6, R7 | - |
| 8.8 | Gestion des vulnérabilités techniques | technologique | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R1, R4, R5, R6, R7 ; corrige l'écart aux règles 34, 35 du Guide d'hygiène. | M02, M09, N02 | R1, R4, R5, R6, R7 | - |
| 8.9 | Gestion de la configuration | technologique | Oui | Partielle | risque, socle | Retenue pour traiter R1, R4, R5, R6, R7 ; corrige l'écart aux règles 12, 14, 16 du Guide d'hygiène. | M09, N07 | R1, R4, R5, R6, R7 | - |
| 8.10 | Suppression de l'information | technologique | Oui | À mettre en œuvre | légal | Supprimer les données personnelles à la fin de leur durée de conservation. | - | - | - |
| 8.11 | Masquage des données | technologique | Oui | À mettre en œuvre | légal | Pseudonymiser les données personnelles des essais cliniques hors des usages qui l'exigent. | - | - | - |
| 8.12 | Prévention des fuites de données | technologique | Oui | Partielle | risque | Retenue pour traiter R1, R3, R6, R7. | M07 | R1, R3, R6, R7 | - |
| 8.13 | Sauvegarde de l'information | technologique | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R4, R6, R7 ; corrige l'écart à la règle 37 du Guide d'hygiène. | N06 | R4, R6, R7 | - |
| 8.14 | Redondance des moyens de traitement | technologique | Oui | Partielle | risque | Retenue pour traiter R4, R5, R6, R7. | M12 | R4, R5, R6, R7 | - |
| 8.15 | Journalisation | technologique | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R1, R3, R5, R6, R7 ; corrige l'écart à la règle 36 du Guide d'hygiène. | M11, N10 | R1, R3, R5, R6, R7 | - |
| 8.16 | Activités de surveillance | technologique | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R1, R3, R6, R7 ; corrige l'écart à la règle 36 du Guide d'hygiène. | M11 | R1, R3, R6, R7 | - |
| 8.17 | Synchronisation des horloges | technologique | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R1, R3, R6, R7 ; corrige l'écart à la règle 36 du Guide d'hygiène. | M11 | R1, R3, R6, R7 | - |
| 8.18 | Utilisation de programmes utilitaires à privilèges | technologique | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R1, R6, R7 ; corrige l'écart à la règle 29 du Guide d'hygiène. | N07 | R1, R6, R7 | - |
| 8.19 | Installation de logiciels sur les systèmes en exploitation | technologique | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R1, R4, R6, R7 ; corrige l'écart à la règle 34 du Guide d'hygiène. | M13, N02 | R1, R4, R6, R7 | - |
| 8.20 | Sécurité des réseaux | technologique | Oui | Partielle | risque, socle | Retenue pour traiter R1, R6, R7 ; corrige l'écart aux règles 7, 17, 20, 22, 23, 25, 32 du Guide d'hygiène. | N01 | R1, R6, R7 | - |
| 8.21 | Sécurité des services réseau | technologique | Oui | Partielle | risque, socle | Retenue pour traiter R2 ; corrige l'écart aux règles 20, 21, 25, 32 du Guide d'hygiène. | M10 | R2 | - |
| 8.22 | Cloisonnement des réseaux | technologique | Oui | Partielle | risque, socle | Retenue pour traiter R1, R3, R4, R5, R6, R7 ; corrige l'écart aux règles 19, 20, 23, 28 du Guide d'hygiène. | M07, M09, N01 | R1, R3, R4, R5, R6, R7 | - |
| 8.23 | Filtrage web | technologique | Oui | Partielle | risque, socle | Retenue pour traiter R1, R6, R7 ; corrige l'écart aux règles 22, 24, 27 du Guide d'hygiène. | N07 | R1, R6, R7 | - |
| 8.24 | Utilisation de la cryptographie | technologique | Oui | Partielle | risque, socle | Retenue pour traiter R1, R2, R3, R5, R6, R7 ; corrige l'écart aux règles 11, 18, 21, 31 du Guide d'hygiène. | M07, M10, N07, N10 | R1, R2, R3, R5, R6, R7 | - |
| 8.25 | Cycle de développement sécurisé | technologique | Non (exclue) | Exclue | - | Aucun cycle de développement logiciel : l'ERP et les systèmes industriels sont des produits acquis. | - | - | Direction générale |
| 8.26 | Exigences de sécurité des applications | technologique | Oui | À mettre en œuvre | bonne pratique | Exigences de sécurité dans les cahiers des charges des applications et systèmes acquis. | - | - | - |
| 8.27 | Architecture et principes d'ingénierie sécurisés | technologique | Oui | À mettre en œuvre | bonne pratique | Principes d'architecture sécurisée pour le SI et le système industriel (moindre privilège, défense en profondeur). | - | - | - |
| 8.28 | Codage sécurisé | technologique | Non (exclue) | Exclue | - | Aucun code n'est écrit par l'entreprise. | - | - | Direction générale |
| 8.29 | Tests de sécurité en développement et à la recette | technologique | Oui | À mettre en œuvre | bonne pratique | Tests de sécurité à la recette des systèmes acquis ou modifiés. | - | - | - |
| 8.30 | Développement externalisé | technologique | Non (exclue) | Exclue | - | Aucun développement n'est externalisé. Les prestations du prestataire informatique relèvent des mesures 5.19 à 5.22. | - | - | Direction générale |
| 8.31 | Séparation des environnements de développement, de test et de production | technologique | Oui | À mettre en œuvre | bonne pratique | Séparer les environnements de test et de production de l'ERP et des systèmes industriels. | - | - | - |
| 8.32 | Gestion des changements | technologique | Oui | Partielle | légal | Le contrôle des changements existe côté qualité pharmaceutique ; il reste à y ajouter le volet sécurité. | - | - | - |
| 8.33 | Informations de test | technologique | Oui | À mettre en œuvre | bonne pratique | Protéger les données utilisées pour les tests, en particulier les données personnelles. | - | - | - |
| 8.34 | Protection des systèmes pendant les tests d'audit | technologique | Oui | À mettre en œuvre | risque, socle | Retenue pour traiter R1, R5, R6, R7 ; corrige l'écart à la règle 38 du Guide d'hygiène. | M02 | R1, R5, R6, R7 | - |
