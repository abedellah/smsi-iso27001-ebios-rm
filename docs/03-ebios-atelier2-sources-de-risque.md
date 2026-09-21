# EBIOS RM, atelier 2 : sources de risque

*Étiquettes : `[ANSSI p. N]` repris du guide, `[Original]` travail de ce projet, `[Hypothèse]` choix à discuter.
Voir [`CREDITS.md`](../CREDITS.md). Données : [`data/ebios.yaml`](../data/ebios.yaml).*

## 1. Question de l'atelier

Qui ou quoi pourrait porter atteinte aux valeurs métier de l'atelier 1, et dans quel but ? Le résultat est une liste
de couples **source de risque / objectif visé** (SR/OV), évalués puis triés `[ANSSI p. 34]`.

## 2. Couples SR/OV

Les quatre premiers couples et leurs cotations viennent du guide `[ANSSI p. 39]`. Le cinquième est ajouté par ce projet
`[Original]`. La pertinence résulte de la motivation, des ressources et de l'activité de la source.

| Réf. | Source | Objectif visé | Motivation | Ressources | Activité | Pertinence | Retenu | Source de l'information |
|---|---|---|---|---|---|---|---|---|
| SO1 | Activiste | Saboter la prochaine campagne nationale de vaccination en perturbant la production ou la distribution | Significative | Modérée | Modérée | **Moyenne** | oui | `[ANSSI p. 39]` |
| SO2 | Concurrent | Voler des informations en espionnant les travaux de R&D | Importante | Significative | Importante | **Élevée** | oui | `[ANSSI p. 39]` |
| SO3 | Activiste | Divulguer des informations sur les tests animaliers | Modérée | Faible | Faible | **Faible** | non, à surveiller | `[ANSSI p. 39]` |
| SO4 | Cybercriminel | Menacer d'altérer la composition des vaccins pour extorquer une rançon | Modérée | Modérée | Faible | **Faible** | non, à surveiller | `[ANSSI p. 39]` |
| SO5 | Cybercriminel | Chiffrer les systèmes (rançongiciel) pour paralyser la production et obtenir une rançon | Importante | Significative | Importante | **Élevée** | **oui** | `[Original]` |

### Justification des cotations

Le guide recommande de garder une trace de chaque justification pour pouvoir réévaluer au cycle suivant
`[ANSSI p. 39]`.

| Couple | Justification | Source |
|---|---|---|
| SO1 | Regain d'activité médiatique de groupes anti-vaccins à la reprise du calendrier de vaccination antigrippale | `[ANSSI p. 40]` |
| SO2 | Publication scientifique annonçant l'aboutissement imminent des recherches sur un vaccin pour lequel les concurrents sont en compétition acharnée | `[ANSSI p. 40]` |
| SO3 | Deux intrusions d'activistes dans des abattoirs dans l'année, aucune dans un laboratoire | `[ANSSI p. 40]` |
| SO4 | Le rapport annuel de l'ANSSI signale plus de rançongiciels, mais peu de cas avérés sur un système industriel | `[ANSSI p. 40]` |
| SO5 | Le gain est purement financier et l'attaque n'exige aucune connaissance du vaccin : elle est opportuniste et industrialisée. Le socle de sécurité est faible (une seule règle du Guide d'hygiène sur 42 est pleinement appliquée, voir [le socle](tableaux/socle.md)). La direction juge elle-même la menace cybercriminelle préoccupante | `[Original]`, `[ANSSI p. 81]` |

### Pourquoi ajouter SO5

Le guide écarte la menace cybercriminelle au premier cycle (SO4, pertinence faible), puis note en atelier 5 que la direction
la met sous surveillance car elle représente pour elle « une préoccupation forte » `[ANSSI p. 81]`. Les deux positions sont
cohérentes pour SO4, qui vise une extorsion par altération de la composition des vaccins : un scénario très spécialisé et rare.
Elles laissent en revanche sans réponse la forme courante de la menace, le rançongiciel qui paralyse la production. SO5 la
couvre et ferme cet écart. Voir le [constat 1](15-constats-sur-le-cas-de-reference.md).

## 3. Croisement avec les événements redoutés

Le guide insiste : il faut confronter le point de vue de l'attaquant (SR/OV) à celui du défenseur (événements redoutés,
ER), pour vérifier que chaque couple retenu a un ER et que les ER importants ne sont pas oubliés. Tout objectif retenu hérite
de la gravité de l'ER associé `[ANSSI p. 40]`.

| Couple | Événement redouté associé | Gravité héritée |
|---|---|---|
| SO1 | ER6 : interruption de la production ou de la distribution pendant plus d'une semaine en pic d'épidémie | 4 |
| SO2 | ER3 : fuite des informations d'études et recherches | 3 |
| SO3 (secondaire) | ER3 | 3 |
| SO4 (secondaire) | ER7 : altération des résultats des contrôles qualité | 4 |
| SO5 | ER6 | 4 |

Les événements ER1, ER2, ER4, ER5, ER8 et ER9 ne sont visés par aucun couple retenu. `[Original]` Ils ne sont pas oubliés :
leur prévention passe par le socle de sécurité et par les mesures de continuité (voir l'[atelier 5](06-ebios-atelier5-traitement-du-risque.md)),
et ils seront revus au prochain cycle stratégique.

## 4. Couples secondaires et déclencheurs de réexamen

Les couples SO3 et SO4 sont mis sous surveillance, comme le guide le recommande pour les couples non retenus `[ANSSI p. 34]`.
Un déclencheur précis permet de savoir quand les réexaminer `[Original]`.

| Couple | Déclencheur de réexamen |
|---|---|
| SO3 | Intrusion d'activistes dans un laboratoire ou une usine pharmaceutique, en France ou en Europe |
| SO4 | Extorsion ou altération de produit documentée contre un fabricant pharmaceutique |

## 5. Cartographie des sources de risque

| Source | Couples | Pertinence maximale |
|---|---|---|
| Concurrent | SO2 | Élevée |
| Cybercriminel | SO4, SO5 | Élevée |
| Activiste | SO1, SO3 | Moyenne |

Sources non étudiées à ce cycle : acteur étatique et initié malveillant `[Hypothèse]`. Le guide ne les traite pas dans son
exemple ; un salarié corrompu est en revanche un mode opératoire de SO2 (voir l'[atelier 4](05-ebios-atelier4-scenarios-operationnels.md)).
