# Contexte et périmètre du SMSI (ISO/IEC 27001, clause 4)

*Étiquettes : `[ANSSI p. N]` repris du guide, `[Original]` travail de ce projet,
`[Hypothèse]` choix à discuter. Voir [`CREDITS.md`](../CREDITS.md).*

## 1. L'organisme

Une entreprise de biotechnologie qui identifie et fabrique des vaccins `[ANSSI p. 22]`. Elle est
fictive : c'est le cas d'exemple du guide EBIOS RM de l'ANSSI `[ANSSI p. 11]`.

Son niveau de maturité en sécurité du numérique est estimé **faible**. Deux éléments existent :
une sensibilisation basique à l'arrivée des salariés et une charte informatique `[ANSSI p. 11]`.
Ce point de départ compte pour l'ISO 27001 : le SMSI est à **construire**, pas à auditer.

## 2. Enjeux internes et externes (clause 4.1)

| Enjeu | Nature | Source |
|---|---|---|
| Maturité faible en sécurité du numérique | Interne | `[ANSSI p. 11]` |
| Recherche concurrentielle intense sur un vaccin en cours de finalisation | Externe | `[ANSSI p. 40]` |
| Activisme lié à la vaccination et aux tests sur animaux | Externe | `[ANSSI p. 37, 40]` |
| Dépendance à des prestataires et laboratoires dont la sécurité échappe à l'entreprise | Externe | `[ANSSI p. 46, 54]` |
| Rançongiciels visant les industriels | Externe | `[ANSSI p. 40]` (le guide écarte cette menace, voir le [constat 1](15-constats-sur-le-cas-de-reference.md)) |
| Cadre réglementaire pharmaceutique et sanitaire (qualité, libération des lots) | Externe | `[Hypothèse]` à préciser avec les textes applicables |
| Protection des données personnelles (salariés, essais cliniques) | Externe | `[Hypothèse]` RGPD, à cadrer |

## 3. Parties intéressées et leurs attentes (clause 4.2)

Les parties prenantes externes viennent de l'écosystème du guide `[ANSSI p. 46]`. Les attentes
sont une analyse de ce projet `[Original]`.

| Réf. | Partie intéressée | Attente vis-à-vis de la sécurité de l'information |
|---|---|---|
| C1 | Établissements de santé | Livraisons fiables, vaccins conformes et correctement étiquetés |
| C2 | Pharmacies | Idem, traçabilité des lots |
| C3 | Dépositaires et grossistes répartiteurs | Disponibilité de la distribution, exactitude des données de lot |
| P1 | Universités | Confidentialité des travaux partagés |
| P2 | Régulateurs | Conformité, traçabilité, notification des incidents |
| P3 | Laboratoires | Règles claires sur les données qui leur sont transmises |
| F1 | Fournisseurs industriels chimistes | Continuité des commandes, confidentialité des formules |
| F2 | Fournisseurs de matériel de production | Accès de maintenance encadrés |
| F3 | Prestataire informatique | Exigences de sécurité contractualisées |
| Int. | Direction, pharmacien, responsables qualité et production, DSI, salariés | Protection des valeurs métier, règles compréhensibles, formation |

## 4. Périmètre du SMSI (clause 4.3)

**Dans le périmètre** `[Original]`, à partir des valeurs métier du guide `[ANSSI p. 22]` :

- la recherche et développement (R&D) et ses serveurs bureautiques internes ;
- la fabrication des vaccins et les systèmes de production ;
- la traçabilité et le contrôle qualité et leurs serveurs ;
- les personnes, les processus et le site qui exploitent ces éléments.

**Interfaces** : les laboratoires, les fournisseurs de matériel et le prestataire informatique
`[ANSSI p. 22, 46]`. Ils hébergent ou maintiennent une partie des biens supports mais échappent au
contrôle direct de l'entreprise. Ils sont traités par les mesures relatives aux fournisseurs de
l'Annexe A (5.19 à 5.23) et par les scénarios de l'écosystème (atelier 3), comme le guide le
recommande pour les éléments dont la sécurité ne dépend pas directement de l'objet de l'étude
`[ANSSI p. 21, note 10]`.

**Hors périmètre** `[Hypothèse]` : les fonctions support administratives (RH, comptabilité) et les
activités commerciales. Le guide n'en parle pas. Ce choix limite l'étude aux trois valeurs métier et
sera réexaminé au prochain cycle.

## 5. Exigences légales et contractuelles (clause 4.2 c)

À établir `[Hypothèse]` : la liste exacte dépend du cadre applicable à une entreprise
pharmaceutique française. Pistes à instruire : RGPD, réglementation sur la fabrication et la
libération des médicaments, et la directive NIS2 (son application à ce secteur est à vérifier, elle
n'est pas affirmée ici).

## 6. Traçabilité vers la norme

| Exigence (paraphrase) | Où c'est traité |
|---|---|
| 4.1 Comprendre l'organisme et son contexte | §1 et §2 |
| 4.2 Comprendre les attentes des parties intéressées | §3 et §5 |
| 4.3 Déterminer le périmètre | §4 |
| 4.4 Mettre en place et améliorer le SMSI | Ensemble du dépôt |
