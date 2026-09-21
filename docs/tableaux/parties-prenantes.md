# Cartographie de dangerosité de l'écosystème

*Fichier généré par `python tools/build.py` à partir de `data/`. Ne pas modifier à la main.*

Dangerosité = (dépendance x pénétration) / (maturité cyber x confiance), chaque composante de 1 à 4. Seuils du guide : veille 0,2 ; contrôle 0,9 ; danger 2,5. Les composantes de F2, F3 et P3 sont reconstituées pour retrouver les niveaux donnés par le guide (2, 3 et 2,25 puis 1,3, 2 et 1,5) ; les autres sont des hypothèses.

| Réf. | Partie prenante | Catégorie | Dép. | Pén. | Mat. | Conf. | Dangerosité | Zone | Critique | Après mesures | Source |
|---|---|---|---|---|---|---|---|---|---|---|---|
| C1 | Établissements de santé | Client | 2 | 1 | 3 | 3 | 0,22 | Veille | non | - | ANSSI-EBIOS p. 46 (liste), Hypothèse (cotation) |
| C2 | Pharmacies | Client | 1 | 1 | 2 | 3 | 0,17 | Hors seuil | non | - | ANSSI-EBIOS p. 46 (liste), Hypothèse (cotation) |
| C3 | Dépositaires et grossistes répartiteurs | Client | 2 | 2 | 3 | 3 | 0,44 | Veille | non | - | ANSSI-EBIOS p. 46 (liste), Hypothèse (cotation) |
| P1 | Universités | Partenaire | 2 | 2 | 2 | 2 | 1,00 | Contrôle | non | - | ANSSI-EBIOS p. 47, Hypothèse (cotation) |
| P2 | Régulateurs | Partenaire | 3 | 2 | 4 | 4 | 0,38 | Veille | non | - | ANSSI-EBIOS p. 46 (liste), Hypothèse (cotation) |
| P3 | Laboratoires | Partenaire | 3 | 3 | 2 | 2 | 2,25 | Contrôle | oui | 1,50 | ANSSI-EBIOS p. 47, p. 54 (2,25 puis 1,5) |
| F1 | Fournisseurs industriels chimistes | Prestataire | 3 | 2 | 3 | 2 | 1,00 | Contrôle | non | - | ANSSI-EBIOS p. 47, Hypothèse (cotation) |
| F2 | Fournisseurs de matériel de production | Prestataire | 2 | 3 | 1 | 3 | 2,00 | Contrôle | oui | 1,33 | ANSSI-EBIOS p. 47, p. 54 (2 puis 1,3) |
| F3 | Prestataire informatique | Prestataire | 3 | 4 | 2 | 2 | 3,00 | Danger | oui | 2,00 | ANSSI-EBIOS p. 47, p. 54 (3 puis 2) |
