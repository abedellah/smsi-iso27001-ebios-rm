<p align="center">
  <img src="assets/banner.svg?v=3" alt="SMSI ISO 27001 + EBIOS RM, CelerPay (établissement de paiement fictif)" width="100%">
</p>

# SMSI ISO/IEC 27001 et analyse de risques EBIOS RM — CelerPay

> **CelerPay n'existe pas.** C'est une entreprise entièrement fictive, inventée pour ce projet personnel : un établissement de
> paiement agréé ACPR, basé à Paris, avec un centre technique à Casablanca. Aucune donnée, aucune source externe : c'est un
> exercice construit de bout en bout, pas l'extension d'un cas publié par un tiers.

*English summary: a personal project that builds a full ISO/IEC 27001:2022 management system (ISMS) and an EBIOS Risk Manager
risk study for CelerPay, an entirely fictional payment institution (Paris, with a technical hub in Casablanca). Deliverables:
a Word EBIOS RM study, a Word governance document (security policy, internal audit, management review), an Excel workbook
(risk register, gap analysis, Statement of Applicability for the 93 Annex A controls, treatment plan, 18-month roadmap), and
a management restitution deck. Deliverables are in French.*

## Le projet en bref

CelerPay traite des paiements et des données bancaires pour ses clients marchands : une atteinte à ses systèmes peut interrompre
le service en pleine activité, exposer des données financières, ou compromettre ses obligations réglementaires (ACPR, DSP2,
TRACFIN). Ce dépôt construit, pour cette entreprise fictive :

1. **une analyse de risques EBIOS RM** complète : les cinq ateliers, du cadrage au traitement du risque ;
2. **un SMSI ISO/IEC 27001** : politique de sécurité, déclaration d'applicabilité des 93 mesures de l'Annexe A, plan de
   traitement, programme d'audit interne, revue de direction ;
3. **une feuille de route** sur 18 mois, avec trajectoire du risque et budget.

Le lien entre les deux cadres : une mesure de l'Annexe A n'est retenue que si un risque, un écart du socle de sécurité (42
règles évaluées) ou une exigence légale la justifie.

## Livrables

Quatre documents, dans `reports/` :

- **[Étude EBIOS Risk Manager](reports/Etude-EBIOS-RM-CelerPay.docx)** (Word) — les cinq ateliers, avec les résultats marquants :
  la dangerosité du centre technique de Casablanca, la règle de sécurité qui facilite le plus de scénarios, la décision sur R3.
- **[Gouvernance du SMSI](reports/Gouvernance-du-SMSI-CelerPay.docx)** (Word) — politique de sécurité, programme d'audit
  interne, revue de direction.
- **[Classeur Excel](reports/CelerPay-classeur.xlsx)** — socle de sécurité, registre des risques, déclaration d'applicabilité,
  plan de traitement, trajectoire du risque sur 18 mois et budget. Les scores et niveaux sont des formules, pas des valeurs
  figées.
- **[Diaporama de restitution](reports/Restitution-CelerPay.pptx)** (PowerPoint, 8 diapositives) — la synthèse pour une
  direction : chiffres clés, cartographie des risques, SoA, budget, limites à annoncer, décisions demandées.

## Résultats

- **Socle de sécurité** (42 règles évaluées) : 1 règle appliquée sans restriction, 18 avec restrictions, 23 non appliquées —
  une maturité volontairement faible, cohérente avec une jeune entreprise en forte croissance.
- **Risques** : 7 scénarios étudiés. Le centre technique de Casablanca (développement, support) concentre le risque : il
  apparaît dans deux scénarios stratégiques sur trois, et porte la dangerosité la plus élevée de l'écosystème.
- **Déclaration d'applicabilité** : 93 mesures décidées — 45 partiellement en place, 45 à mettre en œuvre, 3 exclues et
  justifiées (infrastructure entièrement hébergée en cloud, aucun développement externalisé). Aucune mesure encore pleinement
  en place : c'est un SMSI à construire.
- **Plan de traitement** : 26 mesures sur 18 mois, la plus rentable étant le cloisonnement du réseau.
- **Une décision assumée** : le risque R3 (vol de données via le centre technique) reste volontairement à un niveau élevé
  après traitement, avec une acceptation formelle de la direction et une date de revue — comme l'exige la clause 6.1.3 f de
  l'ISO/IEC 27001.

## Limites, honnêtement

- Le cas est entièrement fictif, étudié seul, sans les ateliers avec les parties prenantes d'une vraie organisation.
- L'état du socle de sécurité est une hypothèse cohérente avec le profil de l'entreprise, pas un audit constaté.
- Les coûts et échéances du plan de traitement sont des estimations, volontairement larges.
- Ce n'est ni un audit, ni une certification, ni un travail relu par des professionnels.

## Licence

Voir [`LICENSE`](LICENSE) (MIT) pour le code et la mise en forme de ce dépôt. Le contenu de l'étude (l'entreprise CelerPay, ses
risques, ses mesures) est un travail original de Mohamed Abdellah Lagrini.
