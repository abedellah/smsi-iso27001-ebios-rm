# Socle de sécurité : état d'application du Guide d'hygiène de l'ANSSI

*Fichier généré par `python tools/build.py` à partir de `data/`. Ne pas modifier à la main.*

Référentiel : ANSSI, *Guide d'hygiène informatique*, v2.0, septembre 2017 (Licence Ouverte Etalab V1). Niveau évalué : standard. Les états sont ceux de l'entreprise fictive de biotechnologie ; ils s'appuient sur le guide EBIOS RM quand celui-ci en dit quelque chose, et sont sinon une hypothèse cohérente avec sa maturité faible (voir la colonne Source).

**Bilan : 1 règle appliquée sans restriction, 19 avec restrictions, 22 non appliquées (sur 42).**

## I. Sensibiliser et former

| Règle | État | Écart | Mesures | Annexe A ISO 27001 | Source |
|---|---|---|---|---|---|
| 1. Former les équipes opérationnelles à la sécurité des systèmes d'information | rouge | Aucune formation à la sécurité pour la DSI et les équipes de production | N13 | 6.3 | Hypothèse |
| 2. Sensibiliser les utilisateurs aux bonnes pratiques élémentaires de sécurité informatique | orange | Sensibilisation faite à la prise de poste seulement, ni régulière ni centrée sur l'hameçonnage ; une charte informatique existe | M01 | 6.3, 5.10 | ANSSI-EBIOS p. 11, p. 77 |
| 3. Maîtriser les risques de l'infogérance | rouge | Le prestataire informatique a des droits d'accès élevés et une sécurité faible ; les contrats n'imposent pas de niveau de sécurité | M03, M04, M05 | 5.19, 5.20, 5.21, 5.22, 5.23 | ANSSI-EBIOS p. 67, p. 77 |

## II. Connaître le système d'information

| Règle | État | Écart | Mesures | Annexe A ISO 27001 | Source |
|---|---|---|---|---|---|
| 4. Identifier les informations et serveurs les plus sensibles et maintenir un schéma du réseau | orange | Les valeurs métier et leurs supports sont identifiés (atelier 1) ; pas de schéma réseau à jour | M06, N11 | 5.9, 5.12 | Hypothèse |
| 5. Disposer d'un inventaire exhaustif des comptes privilégiés et le maintenir à jour | rouge | Pas d'inventaire des comptes privilégiés, dont celui du prestataire informatique | N05, N11 | 8.2, 5.16, 5.18 | Hypothèse |
| 6. Organiser les procédures d'arrivée, de départ et de changement de fonction des utilisateurs | orange | Procédure RH existante, sans lien systématique avec la suppression des accès informatiques | N11 | 5.11, 5.18, 6.5 | Hypothèse |
| 7. Autoriser la connexion au réseau de l'entité aux seuls équipements maîtrisés | rouge | Aucun contrôle des équipements qui se connectent au réseau | M13, N11 | 5.9, 8.1, 8.20 | Hypothèse |

## III. Authentifier et contrôler les accès

| Règle | État | Écart | Mesures | Annexe A ISO 27001 | Source |
|---|---|---|---|---|---|
| 8. Identifier nommément chaque personne accédant au système et distinguer les rôles utilisateur/administrateur | orange | Un compte administrateur non nominatif existe pour l'ERP | N04, N05 | 5.15, 5.16 | ANSSI-EBIOS p. 30 |
| 9. Attribuer les bons droits sur les ressources sensibles du système d'information | orange | Un salarié de la R&D récupère facilement les informations depuis son poste, sans supervision | M07, N05, N10 | 5.15, 5.18, 8.3 | ANSSI-EBIOS p. 64 |
| 10. Définir et vérifier des règles de choix et de dimensionnement des mots de passe | orange | Règles inscrites dans la charte informatique, non vérifiées techniquement | N04 | 5.17, 8.5 | Hypothèse |
| 11. Protéger les mots de passe stockés sur les systèmes | rouge | Mots de passe conservés sans protection particulière sur certains systèmes | N04 | 5.17, 8.24 | Hypothèse |
| 12. Changer les éléments d'authentification par défaut sur les équipements et services | orange | Éléments par défaut changés sur le réseau bureautique, pas sur les équipements industriels | M09 | 5.17, 8.9 | Hypothèse |
| 13. Privilégier lorsque c'est possible une authentification forte | rouge | Aucune authentification forte, y compris pour l'administration et les accès distants | N04 | 8.5 | Hypothèse |

## IV. Sécuriser les postes

| Règle | État | Écart | Mesures | Annexe A ISO 27001 | Source |
|---|---|---|---|---|---|
| 14. Mettre en place un niveau de sécurité minimal sur l'ensemble du parc informatique | rouge | Niveau de sécurité des postes hétérogène ; correctifs appliqués sans rigueur | N02, N07 | 8.1, 8.7, 8.9 | ANSSI-EBIOS p. 64 |
| 15. Se protéger des menaces relatives à l'utilisation de supports amovibles | rouge | Les ports USB ne sont soumis à aucune restriction | N03 | 7.10 | ANSSI-EBIOS p. 64 |
| 16. Utiliser un outil de gestion centralisée afin d'homogénéiser les politiques de sécurité | orange | Gestion centralisée sur une partie du parc bureautique seulement | N07 | 8.9, 8.1 | Hypothèse |
| 17. Activer et configurer le pare-feu local des postes de travail | orange | Pare-feu local activé avec la configuration par défaut | N07 | 8.1, 8.20 | Hypothèse |
| 18. Chiffrer les données sensibles transmises par voie Internet | rouge | Les échanges de données avec les laboratoires ne sont pas chiffrés | M10 | 5.14, 8.24 | ANSSI-EBIOS p. 77 |

## V. Sécuriser le réseau

| Règle | État | Écart | Mesures | Annexe A ISO 27001 | Source |
|---|---|---|---|---|---|
| 19. Segmenter le réseau et mettre en place un cloisonnement entre ces zones | rouge | Pas de cloisonnement entre les réseaux internes, dont la R&D | M07, M09, N01 | 8.22 | ANSSI-EBIOS p. 64 |
| 20. S'assurer de la sécurité des réseaux d'accès Wi-Fi et de la séparation des usages | orange | Wi-Fi invité distinct, mais chiffrement et authentification non revus | N01 | 8.20, 8.21, 8.22 | Hypothèse |
| 21. Utiliser des protocoles sécurisés dès qu'ils existent | orange | Protocoles en clair encore utilisés en interne | M10 | 8.21, 8.24 | Hypothèse |
| 22. Mettre en place une passerelle d'accès sécurisé à Internet | orange | Pare-feu de périmètre présent, sans filtrage des contenus | N07 | 8.20, 8.23 | Hypothèse |
| 23. Cloisonner les services visibles depuis Internet du reste du système d'information | orange | Peu de services exposés, mais sans zone démilitarisée dédiée | N01 | 8.22, 8.20 | Hypothèse |
| 24. Protéger sa messagerie professionnelle | orange | Filtrage antispam de base ; un hameçonnage ciblé sur la messagerie des RH est jugé faisable | N07 | 5.14, 8.7, 8.23 | ANSSI-EBIOS p. 64 |
| 25. Sécuriser les interconnexions réseau dédiées avec les partenaires | rouge | Interconnexions avec les laboratoires et le prestataire sans filtrage ni chiffrement | M06, M10 | 5.14, 8.21, 8.20 | ANSSI-EBIOS p. 54, p. 77 |
| 26. Contrôler et protéger l'accès aux salles serveurs et aux locaux techniques | orange | Accès aux salles serveurs par badge, sans revue des droits ; le personnel d'entretien circule librement dans les bureaux | M08 | 7.1, 7.2, 7.3 | ANSSI-EBIOS p. 64 |

## VI. Sécuriser l'administration

| Règle | État | Écart | Mesures | Annexe A ISO 27001 | Source |
|---|---|---|---|---|---|
| 27. Interdire l'accès à Internet depuis les postes ou serveurs utilisés pour l'administration du système d'information | rouge | Les administrateurs utilisent leur poste habituel, avec accès à Internet | N07 | 8.2, 8.23 | Hypothèse |
| 28. Utiliser un réseau dédié et cloisonné pour l'administration du système d'information | rouge | Pas de réseau d'administration dédié | M09, N01 | 8.22, 8.2 | Hypothèse |
| 29. Limiter au strict besoin opérationnel les droits d'administration sur les postes de travail | rouge | De nombreux utilisateurs disposent de droits d'administration locaux | N07 | 8.2, 8.18 | Hypothèse |

## VII. Gérer le nomadisme

| Règle | État | Écart | Mesures | Annexe A ISO 27001 | Source |
|---|---|---|---|---|---|
| 30. Prendre des mesures de sécurisation physique des terminaux nomades | orange | Câbles antivol et consignes de base pour certains déplacements | N07 | 7.9, 7.10 | Hypothèse |
| 31. Chiffrer les données sensibles, en particulier sur le matériel potentiellement perdable | rouge | Disques des portables non chiffrés | N07 | 8.24, 7.9 | Hypothèse |
| 32. Sécuriser la connexion réseau des postes utilisés en situation de nomadisme | orange | Accès distant par VPN sans authentification forte | N04 | 6.7, 8.20, 8.21 | Hypothèse |
| 33. Adopter des politiques de sécurité dédiées aux terminaux mobiles | rouge | Aucune politique pour les téléphones et tablettes | N07 | 8.1, 6.7 | Hypothèse |

## VIII. Maintenir à jour le système d'information

| Règle | État | Écart | Mesures | Annexe A ISO 27001 | Source |
|---|---|---|---|---|---|
| 34. Définir une politique de mise à jour des composants du système d'information | rouge | Manque de rigueur dans l'application des correctifs de sécurité, noté à maintes reprises | N02 | 8.8, 8.19 | ANSSI-EBIOS p. 64 |
| 35. Anticiper la fin de la maintenance des logiciels et systèmes et limiter les adhérences logicielles | rouge | Systèmes de production anciens, fin de support non suivie | M09, N02 | 8.8, 7.13 | Hypothèse |

## IX. Superviser, auditer, réagir

| Règle | État | Écart | Mesures | Annexe A ISO 27001 | Source |
|---|---|---|---|---|---|
| 36. Activer et configurer les journaux des composants les plus importants | rouge | Aucune supervision des actions ; journaux non centralisés | M11 | 8.15, 8.16, 8.17 | ANSSI-EBIOS p. 64, p. 77 |
| 37. Définir et appliquer une politique de sauvegarde des composants critiques | rouge | La politique de sauvegarde est en cours de rédaction par un groupe de travail | M12, N06 | 8.13 | ANSSI-EBIOS p. 30 |
| 38. Procéder à des contrôles et audits de sécurité réguliers puis appliquer les actions correctives associées | rouge | Aucun audit de sécurité technique ou organisationnel du SI bureautique | M02, M05 | 5.35, 5.36, 8.34 | ANSSI-EBIOS p. 77 |
| 39. Désigner un référent en sécurité des systèmes d'information et le faire connaître auprès du personnel | vert | - | N09 | 5.2 | ANSSI-EBIOS p. 77 (un RSSI existe) |
| 40. Définir une procédure de gestion des incidents de sécurité | rouge | Pas de procédure formalisée de gestion des incidents | M04, N08 | 5.24, 5.25, 5.26, 5.27, 6.8 | Hypothèse |

## X. Pour aller plus loin

| Règle | État | Écart | Mesures | Annexe A ISO 27001 | Source |
|---|---|---|---|---|---|
| 41. Mener une analyse de risques formelle | orange | Analyse EBIOS RM en cours (ce projet) ; cycle stratégique et cycle opérationnel à installer | N09 | clause 6.1.2 | Original |
| 42. Privilégier l'usage de produits et de services qualifiés par l'ANSSI | orange | Un audit par un prestataire qualifié (PASSI) est prévu, pas d'autre usage de produits qualifiés | M02 | 5.21, 5.23 | ANSSI-EBIOS p. 77 |
