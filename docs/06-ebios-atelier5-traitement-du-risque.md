# EBIOS RM, atelier 5 : traitement du risque

*Étiquettes : `[ANSSI p. N]` repris du guide, `[Original]` travail de ce projet, `[Hypothèse]` choix à discuter.
Voir [`CREDITS.md`](../CREDITS.md).*

## 1. Synthèse des risques

Cinq scénarios de risque viennent du guide (R1 à R5), avec leurs gravités et vraisemblances `[ANSSI p. 67, p. 72]`. Deux sont
ajoutés (R6 et R7) `[Original]`. Tableau complet, cartographies avant et après traitement :
[`tableaux/registre-risques.md`](tableaux/registre-risques.md).

| Réf. | Scénario | Niveau initial | Niveau résiduel cible |
|---|---|---|---|
| R1 | Un concurrent vole des informations de R&D par un canal direct | 9 Élevé | 6 Moyen |
| R2 | Un concurrent exfiltre les informations détenues par le laboratoire | 6 Moyen | 3 Faible |
| R3 | Un concurrent vole des informations via le prestataire informatique | 12 Élevé | 9 **Élevé** (accepté) |
| R4 | Un activiste arrête la production par l'équipement de maintenance | 8 Élevé | 4 Moyen |
| R5 | Un activiste perturbe la distribution en modifiant l'étiquetage | 4 Moyen | 3 Faible |
| R6 | Rançongiciel déployé à partir du prestataire informatique | 16 Élevé | 6 Moyen |
| R7 | Rançongiciel après hameçonnage direct des salariés | 12 Élevé | 6 Moyen |

## 2. Stratégie de traitement

Le guide propose trois classes d'acceptabilité `[ANSSI p. 74]`, reprises telles quelles :

| Niveau | Acceptabilité | Décision |
|---|---|---|
| Faible | Acceptable en l'état | Aucune action |
| Moyen | Tolérable sous contrôle | Suivi et amélioration continue à moyen et long terme |
| Élevé | Inacceptable | Réduction impérative à court terme, sinon l'activité est refusée. Ici : réduction, ou acceptation formelle par la direction |

Le passage du score (gravité x vraisemblance) au niveau est défini dans [la méthode d'appréciation](08-iso27001-methode-appreciation-risques.md)
`[Hypothèse]` : faible de 1 à 3, moyen de 4 à 7, élevé de 8 à 16.

Traitement retenu : **réduire** les cinq risques élevés (R1, R3, R4, R6, R7). R2 et R5, moyens, sont réduits par les mesures
déjà prévues. Aucun risque n'est évité (arrêter l'activité) ni transféré (assurance) `[Hypothèse]` ; une assurance cyber pourrait
compléter le traitement de R6 et R7 et sera étudiée par la direction.

## 3. Plan de traitement

Vingt-six mesures, dont treize viennent du guide (douze du plan, `[ANSSI p. 77]`, et une sur l'écosystème, `[ANSSI p. 54]`) et
treize sont ajoutées. Le plan complet, avec responsables, freins, coûts, échéances, priorités et statuts, est dans
[`tableaux/plan-traitement.md`](tableaux/plan-traitement.md). Il suit la présentation du guide en quatre axes :
gouvernance, protection, défense et résilience `[ANSSI p. 77]`.

Ce que ce projet ajoute au plan du guide `[Original]` (voir le [constat 4](15-constats-sur-le-cas-de-reference.md)) :

- une **priorité** pour chaque mesure (le guide n'en donne que pour deux) ;
- une **échéance** pour chaque mesure, et un coût pour toutes ;
- un rattachement de chaque mesure aux **règles du socle** qu'elle corrige et aux **mesures de l'Annexe A** de l'ISO 27001 ;
- le rattachement au risque et le responsable de la mesure de chiffrement des échanges avec les laboratoires (M10), qu'il manque
  dans le guide ;
- treize mesures pour couvrir les écarts du socle que le guide laisse sans réponse et les risques R6 et R7.

La mesure la plus rentable est **N01** (cloisonnement), qui gêne six scénarios sur sept (voir l'[atelier 4](05-ebios-atelier4-scenarios-operationnels.md)).
Les mesures de priorité 1 sont celles qui traitent les risques initialement les plus élevés (R6, R3, R7, R1) et les parties
prenantes critiques.

**Trajectoire.** [`tableaux/trajectoire-et-budget.md`](tableaux/trajectoire-et-budget.md) montre l'évolution attendue du risque
à T0+6, +12 et +18 mois, comme le guide le recommande pour chaque jalon `[ANSSI p. 79]`. Le tableau montre aussi combien de risques restent au niveau élevé à chaque jalon, sous l'hypothèse
que les échéances soient tenues. L'enveloppe budgétaire y est aussi estimée, avec
l'échelle de coût définie dans le plan.

## 4. Risques résiduels

Une fiche par risque, sur le modèle du guide `[ANSSI p. 78]` : [`tableaux/risques-residuels.md`](tableaux/risques-residuels.md).

### Le cas de R3

Le guide décide de **maintenir R3 à un niveau résiduel élevé** malgré les mesures : le prestataire informatique est
« relativement opposé » à la mise en place des mesures de sécurité, qui changent profondément ses méthodes de travail
`[ANSSI p. 80]`. Deux pistes sont évoquées pour maîtriser ce risque : entrer au capital du prestataire pour modifier sa
gouvernance de sécurité, ou changer de prestataire `[ANSSI p. 81]`.

Ce projet garde cette décision et la formalise comme l'ISO 27001 l'exige (clause 6.1.3 f : les propriétaires des risques
approuvent le plan de traitement et acceptent les risques résiduels) `[Original]` :

| Élément | Contenu | Source |
|---|---|---|
| Risque | R3, résiduel G3 x V3 = 9, niveau élevé | `[Original]` |
| Décision | Maintenir le niveau résiduel élevé, sous acceptation formelle | `[ANSSI p. 80]` |
| Piste envisagée | Entrer au capital du prestataire, ou en changer | `[ANSSI p. 81]` |
| Acceptation | Direction générale, le 30 septembre 2026 | `[Original]` (le guide ne nomme ni responsable ni date) |
| Décision finale attendue | Au plus tard le 31 mars 2027 | `[Original]` |
| Revue de l'acceptation | Au plus tard le 31 mars 2027, et à chaque revue de direction | `[Original]` |
| Mesures pendant l'attente | N04 et N05 (limiter ce que le prestataire peut faire même s'il est compromis), M03 et M05 (contrats et audits), M11 (détection) | `[Original]` |

## 5. Cadre de suivi

Le guide recommande de piloter le risque par des indicateurs et un comité de pilotage : tous les six mois au démarrage, puis tous
les douze mois en rythme de croisière `[ANSSI p. 81]`. Ce projet reprend ce rythme.

- **Comité de pilotage SSI** : direction générale, RSSI, DSI, pharmacien, responsables qualité et production, DPO. Il suit les
  indicateurs, l'avancement du plan et l'évolution des risques `[ANSSI p. 81]`. Il alimente la [revue de direction](12-iso27001-revue-de-direction.md).
- **Indicateurs** : treize indicateurs, dont les exemples du guide (comités tenus, mesures passées à En cours ou Terminé, budget
  consommé, écarts du socle réduits) : [`tableaux/indicateurs.md`](tableaux/indicateurs.md), [objectifs](10-iso27001-objectifs-et-indicateurs.md).
- **Cycles** : cycle stratégique de 3 ans et cycle opérationnel de 12 mois `[Hypothèse]`, fixés en atelier 1.

### Déclencheurs d'une réévaluation hors cycle `[Original]`

- un incident de sécurité significatif, chez l'entreprise ou chez un prestataire critique ;
- la publication d'une vulnérabilité grave sur un composant du système d'information ou du système industriel ;
- un changement de prestataire informatique, de fournisseur de matériel ou de laboratoire ;
- un des déclencheurs des couples secondaires SO3 et SO4 (voir l'[atelier 2](03-ebios-atelier2-sources-de-risque.md)) ;
- un nouveau texte applicable (par exemple NIS2, dont l'application à ce secteur reste à vérifier).

## 6. Surveillance de la menace cybercriminelle

Le guide indique que la direction souhaite mettre la menace cybercriminelle « sous surveillance » `[ANSSI p. 81]`. Ce projet la
traite : le couple SO5 est retenu et les risques R6 et R7 sont étudiés et traités. La mesure ISO 5.7 (renseignement sur les
menaces) fournit la veille demandée.
