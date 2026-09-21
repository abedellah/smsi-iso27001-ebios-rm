# SMSI ISO/IEC 27001 et analyse de risques EBIOS RM sur le cas de référence de l'ANSSI

> **D'où vient l'entreprise.** Ce projet part du cas d'exemple **fictif** (une société de
> biotechnologie fabriquant des vaccins) publié par l'ANSSI dans
> *La méthode EBIOS Risk Manager : le guide* (v1.5, septembre 2024, Licence Ouverte Etalab V1).
> L'entreprise et les premiers éléments de l'étude viennent de ce guide. Le détail des emprunts
> est dans [`CREDITS.md`](CREDITS.md). Projet non affilié à l'ANSSI, au Club EBIOS ni à l'ISO.

*English summary: a personal project that builds an ISO/IEC 27001:2022 management system (ISMS)
for the fictional vaccine-maker used as the running example in ANSSI's official EBIOS Risk Manager
guide, using EBIOS RM as the risk-assessment engine. The guide only sketches its example; this
project completes the parts it leaves open, adds the whole ISO 27001 layer, and critiques the
reference case. Every row says whether it comes from the guide or is original work. Deliverables
are in French.*

## Ce que fait le projet

Le guide de l'ANSSI déroule les cinq ateliers d'EBIOS RM sur une entreprise fictive, mais de
façon illustrative : un seul scénario opérationnel est détaillé, des événements redoutés sont
« en partie » recensés, et rien n'est dit de l'ISO 27001. Ce dépôt :

1. **Construit le SMSI ISO/IEC 27001** de cette entreprise : contexte et périmètre, politique,
   méthode de risques, plan de traitement, déclaration d'applicabilité (93 mesures), programme
   d'audit interne, revue de direction. C'est le cadre du projet.
2. **Utilise EBIOS RM comme moteur d'appréciation des risques** (clause 6.1.2) : les cinq ateliers,
   complétés là où le guide s'arrête.
3. **Critique le cas de référence** sous forme de constats d'audit courts, avec la page du guide,
   le risque et une recommandation.

Le lien entre les deux : une mesure de l'Annexe A n'est retenue dans la déclaration d'applicabilité
que si un scénario de risque ou une exigence la justifie.

## Avancement

| Livrable | État |
|---|---|
| [Contexte et périmètre du SMSI (ISO 27001, clause 4)](docs/01-iso27001-contexte-et-perimetre.md) | Brouillon |
| [EBIOS RM, atelier 1 : cadrage et socle de sécurité](docs/02-ebios-atelier1-cadrage.md) | Brouillon, socle à compléter |
| EBIOS RM, ateliers 2 à 5 | À faire |
| Politique, méthode, plan de traitement, déclaration d'applicabilité | À faire |
| Programme d'audit interne et revue de direction | À faire |
| Constats sur le cas de référence | À faire |
| Classeur Excel (registre, plan de traitement, déclaration d'applicabilité) | À faire |

## Lire les sources

Dans les tableaux, chaque ligne porte une étiquette : `[ANSSI p. N]` (repris du guide),
`[Original]` (travail de ce projet) ou `[Hypothèse]` (choix à discuter). Voir
[`CREDITS.md`](CREDITS.md).

## Limites

- L'entreprise est fictive. Les hypothèses sont marquées, elles ne sont pas des faits.
- Le guide illustre la méthode : ses simplifications sont voulues. Les critiques visent à montrer
  comment prolonger l'exemple, pas à le disqualifier.
- Ce n'est ni un audit, ni une certification, ni une étude validée par des professionnels.
- Les intitulés de l'Annexe A de l'ISO 27001 sont des paraphrases, pas le texte de la norme.

## Licence

Le travail original de ce dépôt est sous licence MIT, voir [`LICENSE`](LICENSE). Les éléments
repris du guide de l'ANSSI restent sous **Licence Ouverte / Open Licence (Etalab V1)** et sont
attribués dans [`CREDITS.md`](CREDITS.md).

---

*Projet personnel : LAGRINI Mohamed Abdellah*
