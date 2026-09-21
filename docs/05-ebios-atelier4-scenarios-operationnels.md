# EBIOS RM, atelier 4 : scénarios opérationnels

*Étiquettes : `[ANSSI p. N]` repris du guide, `[Original]` travail de ce projet, `[Hypothèse]` choix à discuter.
Voir [`CREDITS.md`](../CREDITS.md).*

## 1. Ce que le guide fournit, et ce que ce projet ajoute

Le guide détaille **un seul** scénario opérationnel, celui du risque R1 (attaque directe sur le SI de la R&D), sous forme de
graphe d'attaque avec trois modes opératoires `[ANSSI p. 62-64]`. Le guide précise que les cinq scénarios ont été élaborés par l'équipe
projet mais qu'ils « ne seront pas représentés ici » : il n'en donne que la vraisemblance globale `[ANSSI p. 66-67]`.

Ce projet :

1. **rédige les scénarios opérationnels de R2, R3, R4 et R5**, que le guide ne montre pas `[Original]` ;
2. **rédige ceux de R6 et R7**, les risques ajoutés `[Original]` ;
3. **reprend R1** avec les trois modes du guide, en y ajoutant des cotations élémentaires `[ANSSI p. 64]`, `[Original]` ;
4. **relie chaque action aux écarts du socle de sécurité** qui la facilitent, comme le guide le prévoit : les écarts du socle
   « constituent un fondement pour l'élaboration des scénarios opérationnels » `[ANSSI p. 30]`.

Les graphes sont dans [`tableaux/scenarios-operationnels.md`](tableaux/scenarios-operationnels.md) (générés à partir des données
et affichés directement par GitHub). Un graphe se lit de la reconnaissance à l'exploitation, en quatre grandes phases : connaître,
rentrer, trouver, exploiter `[ANSSI p. 63]`.

## 2. Méthode de cotation

1. Chaque **action élémentaire** reçoit une vraisemblance de V1 à V4, en confrontant les ressources et la motivation de la source de
   risque au socle de sécurité de l'objet étudié et à la vulnérabilité de l'écosystème `[ANSSI p. 65]`.
2. La vraisemblance d'un **mode opératoire** est celle de son action la plus difficile : l'attaquant échoue si un seul maillon
   résiste `[Original]`.
3. La vraisemblance du **scénario** est celle du mode de moindre effort pour la source de risque `[ANSSI p. 65]`.

Échelle `[ANSSI p. 66]` :

| Niveau | Nom | Signification |
|---|---|---|
| V1 | Peu vraisemblable | La source a peu de chance d'atteindre son objectif |
| V2 | Vraisemblable | Elle est susceptible de l'atteindre |
| V3 | Très vraisemblable | Elle l'atteindra probablement |
| V4 | Quasi certain | Elle l'atteindra certainement |

## 3. Contrôle de cohérence avec le guide

Le guide donne la vraisemblance globale de R1 à R5 `[ANSSI p. 67]`. Le script `tools/build.py` recalcule la vraisemblance de
chaque scénario à partir des cotations élémentaires et **échoue si le résultat diffère de la valeur du guide**. Les cotations
élémentaires sont de ce projet ; elles sont donc contraintes par un résultat connu, ce qui évite de les choisir pour arranger le
résultat.

| Risque | Vraisemblance du guide | Vraisemblance recalculée | Modes | Mode de moindre effort |
|---|---|---|---|---|
| R1 | V3 `[ANSSI p. 67]` | V3 | 3 | Hameçonnage du service RH, latéralisation, exfiltration |
| R2 | V2 `[ANSSI p. 67]` | V2 | 2 | Compromission du laboratoire, ou rebond par l'interconnexion |
| R3 | V4 `[ANSSI p. 67]` | V4 | 2 | Compromission du prestataire informatique |
| R4 | V2 `[ANSSI p. 67]` | V2 | 2 | Compromission du fournisseur de matériel, puis de son équipement de maintenance |
| R5 | V1 `[ANSSI p. 67]` | V1 | 2 | Propagation vers les serveurs de traçabilité, ou opérateur corrompu |
| R6 | V4 `[Original]` | V4 | 1 | Compromission du prestataire informatique, déploiement du rançongiciel |
| R7 | V3 `[Original]` | V3 | 2 | Hameçonnage direct, élévation de droits, propagation, chiffrement |

Détail des actions : [`tableaux/vraisemblances.md`](tableaux/vraisemblances.md).

## 4. Les scénarios en quelques lignes

**R1 : canal d'exfiltration direct** `[ANSSI p. 64]`. Trois modes : un hameçonnage de la messagerie des ressources humaines (ou un
canal caché préexistant) suivi d'une latéralisation, facilitée par l'absence de cloisonnement ; un salarié de la R&D corrompu, qui
récupère les données sans que rien ne soit supervisé ; une clé USB piégée branchée par un prestataire d'entretien corrompu, qui
circule librement hors des heures ouvrées. Le guide relève que le manque de rigueur dans l'application des correctifs facilite
l'exploitation `[ANSSI p. 64]`.

**R2 : via le laboratoire** `[Original]`. L'attaquant compromet le laboratoire, qui détient une partie des travaux, ou passe par
l'interconnexion non filtrée avec l'entreprise. Le guide note la mauvaise habitude de « tout diffuser » aux laboratoires
`[ANSSI p. 54]` : la mesure M06, déjà terminée, réduit la surface.

**R3 : via le prestataire informatique** `[Original]`. Le prestataire a des droits d'accès élevés et une sécurité faible : le vol est
« quasi certain », très facile pour un attaquant qui investit peu `[ANSSI p. 67]`. Un second mode passe par un administrateur du
prestataire corrompu.

**R4 : équipement de maintenance piégé** `[Original]`. Soit le fournisseur de matériel est compromis et son équipement de
maintenance piégé, soit l'équipement est piégé avant livraison. Branché sur le réseau industriel non cloisonné, il modifie les
paramètres ou arrête la ligne. La difficulté est dans la dernière action, qui demande de connaître le procédé : d'où V2.

**R5 : altération de l'étiquetage** `[Original]`. L'attaquant doit atteindre les serveurs de traçabilité, puis modifier les
données d'étiquetage avant expédition, sans que les contrôles ne le détectent : d'où V1.

**R6 : rançongiciel par le prestataire** `[Original]`. Même porte d'entrée que R3, mais l'attaquant ne cherche pas à voler : il déploie
un chiffrement sur les serveurs de R&D, de production et de traçabilité, sauvegardes comprises. Rien n'arrête la propagation
(pas de cloisonnement) et il n'y a pas de politique de sauvegarde en place (règle 37) : quasi certain.

**R7 : rançongiciel par hameçonnage direct** `[Original]`. Un message d'hameçonnage, un poste avec des droits d'administration locaux,
une propagation vers la production et la traçabilité, puis le chiffrement. Un second mode passe par une clé USB déposée dans les locaux.

## 5. Ce que les scénarios disent du socle de sécurité

Vingt et une règles du Guide d'hygiène apparaissent dans les 50 actions élémentaires. La règle qui revient le plus est la
**règle 19, cloisonner le réseau : elle facilite six des sept scénarios**. Ensuite viennent la sensibilisation (2), la supervision (36),
le niveau de sécurité des postes (14), la messagerie (24) et l'infogérance (3), chacune dans trois scénarios. `[Original]`

C'est un argument concret pour la priorité de la mesure **N01** (cloisonnement des réseaux) : c'est l'écart du socle dont la
correction gêne le plus de scénarios à la fois.

## 6. Limites

- Les cotations élémentaires sont un jugement d'analyste. Elles sont documentées dans les données pour être discutées.
- Les modes opératoires sont volontairement simples : le guide invite à ajuster la granularité à la maturité de l'organisation et
  à privilégier les modes de moindre effort `[ANSSI p. 62]`.
- Aucun exploit ni technique n'est détaillé : les actions restent au niveau des objectifs intermédiaires de l'attaquant.
