# Politique de sécurité de l'information (ISO/IEC 27001, clause 5.2)

*Projet de politique pour l'entreprise fictive de biotechnologie du cas ANSSI. Rédaction `[Original]`. Ce document n'est pas signé :
il montre ce qu'une direction devrait valider. Voir [`CREDITS.md`](../CREDITS.md).*

| | |
|---|---|
| Version | 0.1 (projet à valider) |
| Propriétaire | Direction générale |
| Rédaction | RSSI |
| Périmètre | [Contexte et périmètre du SMSI](01-iso27001-contexte-et-perimetre.md) |
| Revue | Au moins tous les 12 mois et après tout changement majeur |
| Validation | À signer par la direction générale : `[ ]` (non signé, cas fictif) |

## 1. Pourquoi cette politique

L'entreprise fabrique des vaccins. Une atteinte à ses systèmes peut retarder l'arrivée d'un vaccin, priver des patients d'un
produit au pire moment ou fausser un contrôle de qualité. La sécurité de l'information protège donc à la fois l'entreprise et la
santé des personnes. La direction s'engage à la traiter comme une exigence de fabrication au même titre que la qualité
pharmaceutique.

Le niveau de maturité de départ est faible `[ANSSI p. 11]`. La politique fixe la direction ; le plan de traitement des risques dit
comment y arriver.

## 2. Ce que nous protégeons

Les trois valeurs métier de l'entreprise `[ANSSI p. 22]` :

1. la **recherche et développement** : les travaux, formules et données d'essais ;
2. la **fabrication des vaccins** : la production, le remplissage et le conditionnement, et les systèmes industriels ;
3. la **traçabilité et le contrôle qualité** : les données qui permettent de libérer les lots.

## 3. Objectifs de sécurité

Ils sont mesurés par les [indicateurs](10-iso27001-objectifs-et-indicateurs.md) `[Original]` :

| Objectif | Ce que nous voulons |
|---|---|
| O1 | Ne jamais interrompre la production ou la distribution plus d'une semaine à cause d'un incident de sécurité |
| O2 | Empêcher la fuite ou l'altération des travaux de R&D et des données de qualité |
| O3 | Maîtriser les risques venant des prestataires, des fournisseurs et des laboratoires |
| O4 | Respecter les obligations légales, réglementaires et contractuelles |
| O5 | Améliorer chaque année le niveau de sécurité et le démontrer |

## 4. Principes

- **Décider par le risque.** Les mesures sont choisies parce qu'un risque ou une obligation les justifie. Le lien est écrit dans la
  déclaration d'applicabilité.
- **Moindre privilège.** Chacun, y compris nos prestataires, dispose des accès dont il a besoin et pas plus.
- **Défense en profondeur.** Aucune mesure seule ne protège les valeurs métier : réseau cloisonné, accès maîtrisés, détection,
  sauvegardes, continuité.
- **Sécurité chez les tiers.** Un prestataire ou un laboratoire qui accède à nos données doit respecter nos exigences, contrôlées
  par audit.
- **Preuve avant affirmation.** Une mesure est mise en œuvre quand on peut le démontrer.

## 5. Engagements de la direction

La direction générale s'engage à :

- fournir les moyens nécessaires au plan de traitement des risques ;
- accepter ou refuser formellement les risques résiduels élevés, avec une date de revue ;
- réunir le comité de pilotage tous les six mois au départ, puis tous les ans, et la revue de direction au moins une fois par an ;
- satisfaire aux exigences applicables et à l'amélioration continue du système de management ;
- faire connaître cette politique à tout le personnel et aux tiers concernés.

## 6. Rôles et responsabilités

| Rôle | Responsabilité |
|---|---|
| Direction générale | Approuve la politique, accepte les risques résiduels élevés, préside la revue de direction |
| RSSI | Pilote le SMSI, tient le registre des risques et la déclaration d'applicabilité, rend compte à la direction |
| DSI | Met en œuvre les mesures techniques du plan, exploite le système d'information |
| Pharmacien (R&D) | Propriétaire de la valeur métier R&D |
| Responsable production | Propriétaire de la valeur métier fabrication, sécurité du système industriel avec la DSI |
| Responsable qualité | Propriétaire de la valeur métier traçabilité et contrôle |
| DPO | Protection des données personnelles, relation avec les autorités de protection |
| Équipe juridique | Clauses de sécurité des contrats, veille réglementaire |
| RH | Sensibilisation, formation, arrivées et départs |
| Tous les salariés | Respecter la charte informatique et cette politique, signaler tout événement suspect |

## 7. Règles pour tous

- Utiliser les moyens informatiques dans le respect de la charte informatique existante `[ANSSI p. 11]`.
- Ne partager aucun mot de passe et utiliser l'authentification forte quand elle est disponible.
- Ne brancher aucun support amovible non autorisé.
- Signaler sans délai tout message suspect, perte d'équipement ou incident, au RSSI.
- Ne transmettre aux tiers que les données strictement nécessaires (règle du « juste besoin »).

## 8. Exceptions et manquements

Toute dérogation est demandée par écrit au RSSI, avec la raison, une mesure compensatoire et une date de fin. Un manquement
grave peut donner lieu à des mesures prévues par le règlement intérieur.

## 9. Revue

Cette politique est revue par la direction générale au moins une fois par an, lors de la revue de direction, ainsi qu'après un
incident majeur, un changement de périmètre ou une évolution du contexte réglementaire.

## 10. Correspondance avec la norme

| Exigence (paraphrase) | Où |
|---|---|
| 5.2 a : adaptée à l'organisme | §1 et §2 |
| 5.2 b : cadre pour fixer des objectifs | §3 |
| 5.2 c : engagement à satisfaire les exigences applicables | §5 |
| 5.2 d : engagement d'amélioration continue | §3 (O5) et §5 |
| 5.2 e à g : documentée, communiquée, disponible | §5 et §9 |
