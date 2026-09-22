<p align="center">
  <img src="assets/banner.svg?v=2" alt="SMSI ISO 27001 + EBIOS RM, bâti sur le cas de référence de l'ANSSI" width="100%">
</p>

# SMSI ISO/IEC 27001 et analyse de risques EBIOS RM sur le cas de référence de l'ANSSI

> **D'où vient l'entreprise.** Ce projet part du cas d'exemple **fictif** (une société de biotechnologie fabriquant des vaccins) publié
> par l'ANSSI dans *La méthode EBIOS Risk Manager : le guide* (v1.5, septembre 2024, Licence Ouverte Etalab V1). L'entreprise et les
> premiers éléments de l'étude viennent de ce guide. Le détail des emprunts est dans [`CREDITS.md`](CREDITS.md). Projet non affilié à
> l'ANSSI, au Club EBIOS ni à l'ISO.

*English summary: a personal project that builds an ISO/IEC 27001:2022 management system (ISMS) for the fictional vaccine-maker used as
the running example in ANSSI's official EBIOS Risk Manager guide, with EBIOS RM as the risk-assessment engine. The guide only sketches its
example; this project completes what it leaves open (missing operational scenarios, treatment plan gaps, a cybercriminal scenario), adds
the whole ISO 27001 layer (policy, method, Statement of Applicability for the 93 Annex A controls, audit programme, management review)
and critiques the reference case in six audit-style findings. Every row says whether it comes from the guide or is original work.
Deliverables are in French.*

## Le projet en bref

Le guide de l'ANSSI déroule les cinq ateliers d'EBIOS RM sur une entreprise fictive, mais de façon illustrative : un seul scénario
opérationnel est détaillé, des événements redoutés sont « en partie » recensés, le plan de traitement est incomplet, et rien n'est dit de
l'ISO 27001. Ce dépôt :

1. **construit le SMSI ISO/IEC 27001** de cette entreprise : contexte et périmètre, politique, méthode de risques, plan de traitement,
   déclaration d'applicabilité (93 mesures), objectifs et indicateurs, programme d'audit interne, revue de direction ;
2. **utilise EBIOS RM comme moteur d'appréciation des risques** (clause 6.1.2) : les cinq ateliers, complétés là où le guide s'arrête ;
3. **critique le cas de référence** en constats d'audit courts, avec la page du guide, le risque et une recommandation.

Le lien entre les deux cadres : une mesure de l'Annexe A n'est retenue que si un risque, un écart du socle ou une exigence la justifie, et
cette règle est **vérifiée automatiquement**.

## Résultats

<!-- synthese:debut -->
- **Socle de sécurité** (Guide d'hygiène de l'ANSSI) : 1 règle sur 42 appliquée sans restriction, 19 avec restrictions, 22 non appliquées.
- **Risques** : 7 scénarios (5 du guide, 2 ajoutés). Avant traitement : 5 de niveau élevé, 2 moyen ; score moyen 9,6. Après traitement : 1 élevé (R3, accepté par la direction avec revue datée), 4 moyens, 2 faibles ; score moyen 5,3.
- **Plan de traitement** : 26 mesures, dont 13 venues du guide et 13 ajoutées ; 2 terminées, 4 en cours, 20 à lancer.
- **ISO/IEC 27001, Annexe A** : 93 mesures décidées, dont 45 partiellement en place, 44 à mettre en œuvre et 4 exclues avec justification et approbation. Aucune n'est encore pleinement en place : c'est un SMSI à construire.
- **Ajouts à l'exemple du guide** : 2 événements redoutés, 1 couple source de risque / objectif visé, 1 scénario stratégique, 2 scénarios de risque, 6 scénarios opérationnels détaillés sur 7, 13 mesures.
<!-- synthese:fin -->

Voir aussi le [registre des risques](docs/tableaux/registre-risques.md) (cartographies avant et après traitement) et la
[trajectoire du risque](docs/tableaux/trajectoire-et-budget.md).

## Livrables

Les trois documents de synthèse, dans `reports/` :

- **[Étude EBIOS Risk Manager](reports/Etude-EBIOS-RM.docx)** (Word) — les cinq ateliers, résumés : l'essentiel de chaque atelier et les
  résultats marquants (le cloisonnement du réseau, l'ajout du scénario rançongiciel, la décision sur R3).
- **[Gouvernance du SMSI](reports/Gouvernance-du-SMSI.docx)** (Word) — politique de sécurité, programme d'audit interne, revue de direction.
- **[Classeur Excel](reports/SMSI-biotech-classeur.xlsx)** — le registre des risques et la déclaration d'applicabilité, avec de vraies
  formules (scores et niveaux calculés, pas figés).

Les documents Markdown ci-dessous vont plus loin : chaque affirmation y porte sa source (page du guide, ou travail original).

## Les documents

### Couche ISO/IEC 27001 (le cadre)

| Document | Clause |
|---|---|
| [01 Contexte et périmètre](docs/01-iso27001-contexte-et-perimetre.md) | 4 |
| [07 Politique de sécurité](docs/07-iso27001-politique-de-securite.md) | 5 |
| [08 Méthode d'appréciation des risques](docs/08-iso27001-methode-appreciation-risques.md) | 6.1.2, 8.2 |
| [09 Traitement des risques et déclaration d'applicabilité](docs/09-iso27001-traitement-et-applicabilite.md) | 6.1.3 |
| [10 Objectifs et indicateurs](docs/10-iso27001-objectifs-et-indicateurs.md) | 6.2, 9.1 |
| [11 Programme d'audit interne](docs/11-iso27001-audit-interne.md) | 9.2 |
| [12 Revue de direction](docs/12-iso27001-revue-de-direction.md) | 9.3 |
| [13 Support et amélioration](docs/13-iso27001-support-et-amelioration.md) | 7, 10 |
| [14 Traçabilité vers la norme](docs/14-tracabilite-iso27001.md) | 4 à 10 |

### Analyse de risques EBIOS RM (le moteur)

| Document | Atelier |
|---|---|
| [02 Cadrage et socle de sécurité](docs/02-ebios-atelier1-cadrage.md) | 1 |
| [03 Sources de risque](docs/03-ebios-atelier2-sources-de-risque.md) | 2 |
| [04 Scénarios stratégiques](docs/04-ebios-atelier3-scenarios-strategiques.md) | 3 |
| [05 Scénarios opérationnels](docs/05-ebios-atelier4-scenarios-operationnels.md) | 4 |
| [06 Traitement du risque](docs/06-ebios-atelier5-traitement-du-risque.md) | 5 |

### Critique et données

- [15 Constats sur le cas de référence](docs/15-constats-sur-le-cas-de-reference.md)
- Tableaux générés : [socle](docs/tableaux/socle.md), [parties prenantes](docs/tableaux/parties-prenantes.md),
  [registre des risques](docs/tableaux/registre-risques.md), [graphes d'attaque](docs/tableaux/scenarios-operationnels.md),
  [plan de traitement](docs/tableaux/plan-traitement.md), [déclaration d'applicabilité](docs/tableaux/declaration-applicabilite.md),
  [risques résiduels](docs/tableaux/risques-residuels.md), [indicateurs](docs/tableaux/indicateurs.md)
- [Classeur Excel](reports/SMSI-biotech-classeur.xlsx) : socle, événements redoutés, couples, parties prenantes, risques, modes
  opératoires, plan, déclaration d'applicabilité, indicateurs. Les scores et niveaux des risques et de la dangerosité y sont des formules.

## Lire les sources

Dans les tableaux, chaque ligne porte une étiquette : `[ANSSI p. N]` (repris du guide, page imprimée N), `[Original]` (travail de ce
projet) ou `[Hypothèse]` (choix à discuter). Voir [`CREDITS.md`](CREDITS.md).

## Comment c'est vérifié

Les données sont dans [`data/`](data). Le script [`tools/build.py`](tools/build.py) les contrôle, puis génère les tableaux et le classeur.
Il échoue notamment quand :

- une mesure de l'Annexe A n'a pas de décision, ou une exclusion n'a ni justification ni approbation ;
- une mesure du plan ne traite aucun risque, ou un écart du socle n'a aucune mesure ;
- un risque résiduel dépasse le risque initial, ou un risque résiduel élevé n'a pas d'acceptation formelle datée ;
- la vraisemblance recalculée d'un scénario diffère de celle du guide (R1 à R5) ou la dangerosité de F2, F3 et P3 diffère de celle du guide ;
- une valeur de départ d'un indicateur ne correspond pas aux données.

```bash
pip install -r requirements.txt
python tools/build.py           # vérifie et génère docs/tableaux et reports
python tools/build.py --check   # échoue si les fichiers générés sont périmés (utilisé en CI)
pytest                          # tests, dont des tests qui cassent les données volontairement
```

## Limites

- L'entreprise est fictive. Les hypothèses sont marquées, elles ne sont pas des faits.
- Le guide illustre la méthode : ses simplifications sont voulues. Les critiques montrent comment prolonger l'exemple, elles ne le
  disqualifient pas.
- L'état d'application du socle, les cotations des parties prenantes hors de celles du guide, les coûts, les échéances et les cibles des
  indicateurs sont des hypothèses. La trajectoire du risque est un modèle simple, pas une mesure.
- Ce n'est ni un audit, ni une certification, ni une étude validée par des professionnels.
- Le Guide d'hygiène informatique utilisé date de 2017 (v2.0) ; les intitulés de l'Annexe A de l'ISO 27001 sont des paraphrases, pas le
  texte de la norme.

## Licence

Le travail original de ce dépôt est sous licence MIT, voir [`LICENSE`](LICENSE). Les éléments repris des guides de l'ANSSI restent sous
**Licence Ouverte / Open Licence (Etalab V1)** et sont attribués dans [`CREDITS.md`](CREDITS.md).

---

*Projet personnel : LAGRINI Mohamed Abdellah*
