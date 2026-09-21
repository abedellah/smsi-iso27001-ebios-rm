# EBIOS RM, atelier 1 : cadrage et socle de sécurité

*Brouillon. Étiquettes : `[ANSSI p. N]` repris du guide, `[Original]` travail de ce projet,
`[Hypothèse]` choix à discuter. Voir [`CREDITS.md`](../CREDITS.md).*

## 1. Cadre de l'étude

| Point | Décision | Source |
|---|---|---|
| Objet de l'étude | L'entreprise de biotechnologie fabriquant des vaccins (cas de l'ANSSI) | `[ANSSI p. 11]` |
| Mission | Identifier et fabriquer des vaccins | `[ANSSI p. 22]` |
| Cycle stratégique | 3 ans | `[Hypothèse]` le guide demande de fixer les durées sans en imposer |
| Cycle opérationnel | 12 mois | `[Hypothèse]` idem |

## 2. Valeurs métier

| Valeur métier | Nature | Description | Propriétaire | Source |
|---|---|---|---|---|
| Recherche et développement (R&D) | Processus | Identification et production des antigènes (fermentation, purification, inactivation, filtration, stockage), évaluation préclinique, développement clinique | Pharmacien | `[ANSSI p. 22, reformulé]` |
| Fabriquer des vaccins | Processus | Remplissage des seringues (stérilisation, remplissage, étiquetage) et conditionnement (étiquetage, emballage) | Responsable production | `[ANSSI p. 22, reformulé]` |
| Traçabilité et contrôle | Information | Informations permettant le contrôle qualité et la libération de lot | Responsable qualité | `[ANSSI p. 22, reformulé]` |

## 3. Biens supports

| Bien support | Description | Propriétaire | Valeur(s) métier | Source |
|---|---|---|---|---|
| Serveurs bureautiques internes | Stockent l'ensemble des données de R&D | DSI | R&D | `[ANSSI p. 22]` |
| Serveurs bureautiques externes | Stockent une partie des données de R&D | Laboratoires | R&D | `[ANSSI p. 22]` |
| Systèmes de production des antigènes | Machines et équipements informatiques produisant les antigènes | Laboratoires | R&D | `[ANSSI p. 22]` |
| Systèmes de production | Machines et équipements informatiques fabriquant les vaccins à grande échelle | DSI et fournisseurs de matériel | Fabriquer des vaccins | `[ANSSI p. 22]` |
| Serveurs bureautiques internes (traçabilité) | Stockent les données de traçabilité et de contrôle des différents processus | DSI | Traçabilité et contrôle | `[ANSSI p. 22]` |

Les biens dont le propriétaire est externe (laboratoires, fournisseurs) sont à la frontière du
périmètre : ils sont repris comme parties prenantes à l'atelier 3.

## 4. Échelle de gravité

Reprise du guide `[ANSSI p. 26]`, résumée.

| Niveau | Nom | Conséquence |
|---|---|---|
| G1 | Mineure | Aucun impact opérationnel ni sur la sécurité des personnes et des biens ; l'entreprise surmonte la situation sans trop de difficultés |
| G2 | Significative | Dégradation des performances sans impact sur la sécurité ; fonctionnement en mode dégradé |
| G3 | Grave | Forte dégradation, impacts significatifs possibles sur la sécurité des personnes ; sérieuses difficultés (mode très dégradé) |
| G4 | Critique | Incapacité d'assurer tout ou partie de l'activité, impacts graves possibles sur la sécurité des personnes ; la survie de l'entreprise est menacée |

## 5. Événements redoutés

Les sept événements sont ceux que le guide donne, qui précise qu'il s'agit d'**une partie** des
événements recensés `[ANSSI p. 27]`. La colonne « Justification » est un ajout de ce projet : le
guide recommande de conserver la justification de la cotation, sans la fournir `[ANSSI p. 27, note]`.

| Réf. | Valeur métier | Événement redouté | Impacts | Gravité | Justification | Source |
|---|---|---|---|---|---|---|
| ER1 | R&D | Perte ou destruction des informations d'études et recherches, avec fort impact sur les futures autorisations de mise sur le marché | Missions et services, coûts de développement, gouvernance | 3 | Les années de travail se refont difficilement et retardent l'autorisation de mise sur le marché, sans mettre en cause la sécurité des personnes | `[ANSSI p. 27]` `[Original]` pour la justification |
| ER2 | R&D | Altération des informations d'études et recherches aboutissant à une formule de vaccin erronée | Sécurité ou santé des personnes, image et confiance, juridiques | 3 | Une formule erronée retarde le programme et coûte cher ; les essais cliniques et le contrôle qualité (ER7) sont là pour l'arrêter avant qu'elle n'atteigne des patients | `[ANSSI p. 27]` `[Original]` pour la justification |
| ER3 | R&D | Fuite des informations d'études et recherches de l'entreprise | Gouvernance, financiers | 3 | Perte d'avance sur des concurrents en course pour le même vaccin | `[ANSSI p. 27]` `[Original]` pour la justification |
| ER4 | R&D | Interruption des phases de tests des vaccins pendant plus d'une semaine | Missions et services, financiers | 2 | Retard et surcoût, l'activité continue en mode dégradé | `[ANSSI p. 27]` `[Original]` pour la justification |
| ER5 | Fabriquer des vaccins | Fuite du savoir-faire concernant le processus de fabrication et les tests qualité | Financiers | 2 | Avantage concurrentiel perdu, sans effet immédiat sur la production | `[ANSSI p. 27]` `[Original]` pour la justification |
| ER6 | Fabriquer des vaccins | Interruption de la production ou de la distribution de vaccins pendant plus d'une semaine pendant un pic d'épidémie | Sécurité ou santé des personnes, image et confiance, financiers | 4 | Pénurie de vaccins au pire moment : impact sur la santé publique et sur la survie de l'entreprise (niveau G4) | `[ANSSI p. 27]` `[Original]` pour la justification |
| ER7 | Traçabilité et contrôle | Altération des résultats des contrôles qualité aboutissant à une non-conformité sanitaire | Sécurité ou santé des personnes, image et confiance, juridiques | 4 | Des lots non conformes peuvent atteindre des patients : impact sanitaire et juridique majeur | `[ANSSI p. 27]` `[Original]` pour la justification |

### Compléments proposés

Le guide dit que la liste est partielle. Deux événements redoutés sont ajoutés par ce projet
`[Original]`. Leur cotation est à discuter.

| Réf. | Valeur métier | Événement redouté | Impacts | Gravité | Justification |
|---|---|---|---|---|---|
| ER8 | Traçabilité et contrôle | Indisponibilité prolongée des données de traçabilité et de contrôle, qui bloque la libération des lots | Missions et services, financiers | 3 | Sans ces données, aucun lot ne peut être libéré : la distribution s'arrête, même si la production continue |
| ER9 | R&D | Divulgation de données personnelles liées aux essais cliniques ou aux salariés | Juridiques, image et confiance | 3 | Obligations de notification et atteinte à la confiance des participants |

## 6. Socle de sécurité

**Ce que dit le guide.** Le socle regroupe les mesures qui traitent les risques non ciblés et qui
n'ont pas besoin d'une approche par scénario : référentiels d'hygiène, règles internes, exigences de
tiers, normes, réglementation `[ANSSI p. 28]`. On évalue leur état d'application (vert : appliqué,
orange : appliqué avec restrictions, rouge : non appliqué) et on justifie les écarts `[ANSSI p. 29]`.
Le guide note que cette activité occupe une grande partie de l'analyse de risque, et que le socle
peut aussi être traité dans le cadre d'un SMSI `[ANSSI p. 29, 31]`. C'est le cas ici.

**Exemple du guide.** Il donne une seule ligne à titre d'illustration `[ANSSI p. 30]` :

| Référentiel | État | Écarts | Justification |
|---|---|---|---|
| Guide d'hygiène informatique de l'ANSSI | Appliqué avec restrictions | Règle 8 (identifier nommément chaque personne qui accède au système) : un compte administrateur non nominatif existe pour l'ERP. Règle 37 (politique de sauvegarde des composants critiques) | L'ERP est une solution propriétaire qui n'admet pas d'autre compte d'administration ; la politique de sauvegarde est en cours de rédaction par un groupe de travail |

**Travail à faire** `[Original]` : évaluer l'ensemble du socle en s'appuyant sur le Guide d'hygiène
informatique de l'ANSSI et sur l'Annexe A de l'ISO 27001, en partant du niveau de maturité faible du
cas. L'état d'application de chaque règle sera une hypothèse cohérente avec ce niveau, et sera
présenté comme telle. Ce travail alimente directement la déclaration d'applicabilité.

Le guide indique aussi qu'en cas d'écarts trop importants, on peut concentrer l'effort sur le socle
avant de poursuivre `[ANSSI p. 31]`. Ce choix sera discuté une fois le socle évalué.
