# Constats sur le cas de référence

*Lecture critique du cas d'exemple du guide EBIOS RM de l'ANSSI, sous forme de constats d'audit. Pages du guide imprimées.
Voir [`CREDITS.md`](../CREDITS.md).*

## Avant de lire

Le guide illustre une méthode avec un exemple **volontairement partiel** : il annonce lui-même que l'entreprise n'a recensé qu'une
partie des événements redoutés (p. 27), que le plan de traitement est proposé à titre illustratif (p. 78) et que l'équipe s'est
concentrée d'abord sur un premier scénario opérationnel (p. 62). Ces constats ne visent donc pas à disqualifier l'exemple. Ils
montrent où il faut aller plus loin quand on passe de l'illustration à une étude réelle, et ce que ce projet a fait à chaque fois.
Chacun s'appuie sur une page précise du guide.

Format : **constat**, **preuve**, **risque**, **recommandation**, **réponse dans ce projet**.

| N° | Constat | Gravité | Réponse dans ce projet |
|---|---|---|---|
| 1 | La menace cybercriminelle est écartée, puis jugée préoccupante, sans scénario ni mesure | Majeur | SO5, SS3, R6, R7 |
| 2 | Les événements redoutés sont partiels et sans justification | Mineur | ER8, ER9, justifications |
| 3 | Un seul scénario opérationnel sur cinq est détaillé, alors que les cotations de tous pilotent la matrice des risques | Majeur | Scénarios de R1 à R7 |
| 4 | Le plan de traitement est incomplet : priorités, échéances, coûts et rattachements manquants | Majeur | Plan complété |
| 5 | Le risque R3 est maintenu élevé sans responsable, date ni mesure d'attente | Majeur | Acceptation formelle datée |
| 6 | Les mesures ne sont pas reliées à un catalogue normalisé | Mineur | Correspondance avec l'Annexe A |

---

## Constat 1 : la menace cybercriminelle est écartée puis jugée préoccupante

- **Constat.** En atelier 2, le seul couple cybercriminel (menace d'altérer la composition des vaccins pour extorquer une rançon) est
  jugé de pertinence faible et n'est pas retenu. En atelier 5, la direction demande de le mettre « sous surveillance » car il « représente
  pour elle une préoccupation forte ». Aucun scénario, mesure ni déclencheur n'accompagne cette surveillance.
- **Preuve.** Pertinence faible : p. 39. Justification (rançongiciels en hausse mais « peu de cas avérés sur un système industriel ») : p. 40.
  Surveillance et préoccupation forte de la direction : p. 81.
- **Risque.** Le couple étudié est une forme très spécialisée de l'extorsion. La forme courante, un rançongiciel qui chiffre les
  systèmes et arrête la production, n'exige aucune connaissance du vaccin et n'est étudiée nulle part. Le raisonnement « peu de cas
  sur un système industriel » est une justification datée, qui perd de sa valeur à mesure que l'attaque se généralise. Or le socle du cas est
  faible, et la gravité serait maximale (interruption de plus d'une semaine en pic d'épidémie).
- **Recommandation.** Distinguer l'extorsion spécialisée du rançongiciel générique. Étudier le second. Définir la surveillance : qui, quoi,
  et quels événements la font passer en étude.
- **Réponse dans ce projet.** Couple **SO5**, scénario stratégique **SS3**, risques **R6** et **R7** (niveau initial élevé), mesures dédiées
  (sauvegardes hors ligne, cloisonnement, authentification forte, gestion de crise), déclencheur défini pour SO4, veille par la mesure ISO 5.7.
  Voir l'[atelier 2](03-ebios-atelier2-sources-de-risque.md).

## Constat 2 : événements redoutés partiels et sans justification

- **Constat.** Le guide donne sept événements redoutés et précise qu'il s'agit d'« une partie ». Aucun ne concerne l'indisponibilité
  des données de traçabilité (qui bloque la libération des lots) ni les données personnelles (essais cliniques, salariés).
  La justification de chaque cotation n'est pas fournie, alors que le guide recommande de la conserver.
- **Preuve.** Liste partielle et note sur la justification : p. 27.
- **Risque.** Sans justification, une cotation ne peut pas être réévaluée au cycle suivant ni contestée. Des événements importants
  restent hors de l'étude.
- **Recommandation.** Compléter la liste par métier, justifier chaque gravité.
- **Réponse dans ce projet.** Événements **ER8** et **ER9** ajoutés, justification de chacun des neuf. Voir l'[atelier 1](02-ebios-atelier1-cadrage.md).

## Constat 3 : cinq scénarios opérationnels cotés, un seul détaillé

- **Constat.** Le guide montre un graphe d'attaque pour un scénario seulement. Il indique que les cinq scénarios ont été élaborés par
  l'équipe projet mais qu'ils « ne seront pas représentés ici ». Leurs vraisemblances (V1 à V4) sont pourtant données et positionnent
  les risques dans la matrice.
- **Preuve.** Un seul scénario détaillé : pp. 62 à 64. Autres non représentés : p. 66. Vraisemblances : p. 67.
- **Risque.** Une note de vraisemblance sans modes opératoires est invérifiable : le lecteur ne peut ni la reproduire ni la remettre en
  cause, alors que la vraisemblance, avec la gravité, décide du niveau de chaque risque et donc de la priorité des mesures.
- **Recommandation.** Documenter chaque scénario retenu, au moins avec ses modes opératoires, ses actions élémentaires cotées et les
  écarts du socle qui les facilitent.
- **Réponse dans ce projet.** Les sept scénarios sont détaillés (50 actions élémentaires cotées). La vraisemblance de chaque scénario est
  recalculée et le script échoue si elle diffère de celle du guide pour R1 à R5. Résultat inattendu : l'absence de cloisonnement
  du réseau intervient dans six scénarios sur sept. Voir l'[atelier 4](05-ebios-atelier4-scenarios-operationnels.md).

## Constat 4 : plan de traitement incomplet

- **Constat.** Sur les douze mesures du plan : seules deux ont une priorité (P1 et P2) ; deux n'ont pas d'échéance (l'audit par un prestataire
  qualifié et la procédure de signalement, qui n'ont qu'une charge en jours-hommes) ; la mesure sur le système industriel n'a pas de coût ; celle sur le
  chiffrement des échanges avec les laboratoires n'a ni scénario de risque associé ni responsable. Le coût est exprimé en « + », « ++ » et « +++ »
  sans échelle. La position des risques résiduels n'est pas justifiée.
- **Preuve.** Tableau du plan : p. 77. Plan « à titre illustratif » : p. 78. Cartes des risques initiaux et résiduels : pp. 75 et 80.
- **Risque.** Un plan sans priorité, échéance et responsable ne peut pas être piloté ni budgété, et une mesure sans risque associé ne
  peut pas être justifiée. Des résiduels non justifiés ne peuvent pas être défendus devant la direction.
- **Recommandation.** Donner à chaque mesure un responsable, un risque, une échéance, une priorité et un coût selon une échelle définie ;
  justifier chaque niveau résiduel.
- **Réponse dans ce projet.** Les 26 mesures ont un responsable, un rattachement, une échéance, une priorité et un coût selon une échelle définie
  (moins de 10 k€, 10 à 50 k€, 50 à 200 k€, hypothèse). Chaque résiduel est justifié. Le script échoue si une mesure n'a ni risque ni
  événement redouté, ou si un écart du socle n'a aucune mesure. Voir l'[atelier 5](06-ebios-atelier5-traitement-du-risque.md).

## Constat 5 : R3 maintenu élevé, sans responsable ni date

- **Constat.** La direction maintient R3 à un niveau élevé, car le prestataire informatique résiste aux mesures. Elle évoque deux pistes,
  entrer au capital du prestataire ou en changer. Le guide ne nomme pas de responsable de cette décision, ne fixe pas d'échéance, ne prévoit
  pas de mesures pendant l'attente et n'indique pas quand le risque sera réexaminé.
- **Preuve.** Décision : p. 80. Pistes : p. 81.
- **Risque.** Un risque élevé accepté sans propriétaire, sans date de revue ni mesure transitoire devient un risque oublié. C'est aussi
  éloigné de ce que l'ISO/IEC 27001 attend : les propriétaires des risques approuvent le plan de traitement et acceptent les
  risques résiduels (clause 6.1.3 f).
- **Recommandation.** Consigner une acceptation formelle avec un responsable, une date, une revue et des mesures d'attente ; définir ce
  qui déclenche l'escalade.
- **Réponse dans ce projet.** Acceptation par la direction générale, décision attendue au plus tard le 31 mars 2027, revue à cette date, et mesures
  d'attente qui limitent ce que le prestataire peut faire même compromis (authentification forte N04, accès encadrés N05). Le script exige
  cet enregistrement pour tout risque résiduel élevé. Voir l'[atelier 5](06-ebios-atelier5-traitement-du-risque.md).

## Constat 6 : pas de lien avec un catalogue de mesures normalisé

- **Constat.** Les mesures du plan sont décrites en langage libre. Elles ne sont rapprochées d'aucun catalogue (ISO/IEC 27001, Annexe A),
  alors que le guide note que le socle de sécurité peut être traité dans un système de management de la sécurité de l'information.
- **Preuve.** Mesures libres : p. 77. Socle traité dans un SMSI : p. 29.
- **Risque.** Sans rapprochement, on ne sait pas quelles exigences normatives le plan couvre ni ce qu'il faut ajouter pour une certification.
- **Recommandation.** Rattacher chaque mesure à des mesures d'un catalogue normalisé et en déduire la déclaration d'applicabilité.
- **Réponse dans ce projet.** Chaque règle du socle et chaque mesure du plan est rattachée à des mesures de l'Annexe A, et la
  [déclaration d'applicabilité](tableaux/declaration-applicabilite.md) des 93 mesures en est déduite. Voir le [document 09](09-iso27001-traitement-et-applicabilite.md).

---

## Ce que le guide fait bien

Une critique équilibrée reconnaît aussi les points forts, dont ce projet s'inspire :

- la **cartographie de dangerosité** de l'écosystème, qui donne un critère chiffré pour désigner les parties prenantes critiques
  (pp. 44 à 47) ;
- la **décision assumée sur R3** : le guide montre un risque qu'on n'arrive pas à réduire et le dit (p. 80) ;
- le **modèle de fiche de risque résiduel** (p. 78) et la recommandation de suivre le risque à chaque jalon (p. 79) ;
- l'idée de **relier les écarts du socle aux scénarios opérationnels** (p. 30), qui a permis de repérer le rôle du cloisonnement ;
- une **méthode itérative** : deux cycles, stratégique et opérationnel (p. 11).

## Limites de ces constats

- Ils portent sur l'exemple, pas sur la méthode EBIOS RM.
- Ils se fondent sur les pages de l'exemple lues en détail : tous les ateliers de l'exemple et le socle. Une explication de l'un de
  ces points ailleurs dans le guide est possible, mais elle n'a pas été trouvée.
- La version étudiée est la 1.5 de septembre 2024. Une version ultérieure a pu corriger certains points.
