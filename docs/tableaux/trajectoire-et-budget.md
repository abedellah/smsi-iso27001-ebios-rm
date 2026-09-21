# Trajectoire du risque et enveloppe budgétaire

*Fichier généré par `python tools/build.py` à partir de `data/`. Ne pas modifier à la main.*

Le guide EBIOS RM recommande d'associer une cartographie des risques résiduels à chaque grand jalon du plan (p. 79). Modèle simple de ce projet (hypothèse) : à chaque jalon, un risque est réduit de son niveau initial vers son niveau cible en proportion des mesures qui le traitent et qui sont terminées ou dont l'échéance est atteinte. Une mesure n'a d'effet qu'une fois mise en œuvre (guide, p. 53, note 26). C'est un outil de lecture, pas une mesure du risque réel.

| Risque | Score initial | T0 (aujourd'hui) | T0+6 mois | T0+12 mois | T0+18 mois | Score cible |
|---|---|---|---|---|---|---|
| R1 | 9 | 8,7 Élevé | 7,2 Moyen | 6,0 Moyen | 6,0 Moyen | 6 Moyen |
| R2 | 6 | 5,5 Moyen | 4,0 Moyen | 3,5 Moyen | 3,0 Faible | 3 Faible |
| R3 | 12 | 12,0 Élevé | 10,0 Élevé | 9,3 Élevé | 9,0 Élevé | 9 Élevé |
| R4 | 8 | 8,0 Élevé | 5,6 Moyen | 4,4 Moyen | 4,0 Moyen | 4 Moyen |
| R5 | 4 | 4,0 Moyen | 3,4 Faible | 3,0 Faible | 3,0 Faible | 3 Faible |
| R6 | 16 | 16,0 Élevé | 9,9 Élevé | 6,6 Moyen | 6,0 Moyen | 6 Moyen |
| R7 | 12 | 12,0 Élevé | 8,4 Élevé | 6,0 Moyen | 6,0 Moyen | 6 Moyen |
| **Moyenne** | 9,6 | 9,5 | 6,9 | 5,5 | 5,3 | 5,3 |
| **Risques au niveau Élevé** | 5 | 5 | 3 | 1 | 1 | 1 |

## Enveloppe budgétaire estimée

Mesures restant à réaliser (24 sur 26) : entre **380 et 1710 k€**, et 305 jours-hommes chiffrés (le guide ne donne des charges que pour deux mesures ; les autres sont des estimations de ce projet). Les bornes viennent de l'échelle + / ++ / +++ définie dans le plan (hypothèse).

| Priorité | Mesures | Budget |
|---|---|---|
| P1 | 14 | 230 à 1030 k€ |
| P2 | 8 | 150 à 660 k€ |
| P3 | 2 | 0 à 20 k€ |
