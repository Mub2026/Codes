# Flexibilité thermique des bâtiments multilogements / Thermal Flexibility of Multi-Unit Residential Buildings

**[Français](#version-française) · [English](#english-version)**

---

## Version française

Bonjour,

Je suis heureux de partager avec vous mes travaux de recherche sur la flexibilité thermique des bâtiments multilogements.

### L'essentiel à savoir

Les travaux de ce dépôt sont organisés en deux parties principales :
- les dossiers de rédaction (manuscrits, présentation et gabarit Overleaf) ;
- les dossiers des codes de programmation Python (`Identification_EKF` et `Simulateur_MPC_MUB`).

#### A. Les manuscrits

Les manuscrits sont mis à votre disposition pour révision. Ils comprennent un fichier Word en version française et les fichiers `main.tex` de l'article, dans les dossiers Overleaf, en versions française et anglaise.

#### B. Les codes de simulation Python

Les codes ont été développés avec Python 3.14.6 dans l'environnement VS Code. Ils sont écrits sous forme de cellules Jupyter Notebook et s'exécutent de manière séquentielle, de la première à la dernière cellule.

Chaque code principal utilise des fichiers de données CSV en séries temporelles :

1. **Identification par filtre de Kalman étendu (EKF)** : ce code utilise 32 fichiers CSV de séries temporelles exportées du modèle de bâtiment multirésidentiel (MUB) de 16 appartements conçu avec BEopt (version 2.8). Chaque appartement dispose de deux fichiers : « Chauffage » et « Roue libre ».
2. **Simulateur MPC MUB** : ce code utilise quatre fichiers de données :
   1. `bornes_recharge_ve.csv` ;
   2. `charge_non_flexibles.csv` ;
   3. `parametres_thermiques.csv` ;
   4. `temperature_exterieure.csv`.
3. **Simulateur de charge de base** (charges non flexibles et véhicules électriques) : ce code simule la charge de base, agrégée et désagrégée, sans chauffage. Ses résultats alimentent le Simulateur MPC MUB.

[↑ Retour en haut](#flexibilité-thermique-des-bâtiments-multilogements--thermal-flexibility-of-multi-unit-residential-buildings)

---

## English version

Hello,

I am pleased to share with you my research work on the thermal flexibility of multi-unit residential buildings.

### Key information

The work in this repository is organized into two main parts:
- the writing folders (manuscripts, presentation and Overleaf template);
- the Python code folders (`Identification_EKF` and `Simulateur_MPC_MUB`).

#### A. Manuscripts

The manuscripts are available for review. They include a French Word file and the paper's `main.tex` files, located in the Overleaf folders, in both French and English.

#### B. Python simulation codes

The codes were developed with Python 3.14.6 in VS Code. They are written as Jupyter Notebook cells and must be run sequentially, from the first cell to the last.

Each main code uses time-series data stored in CSV files:

1. **Extended Kalman Filter (EKF) identification**: this code uses 32 time-series CSV files exported from the 16-apartment multi-unit residential building (MUB) model built in BEopt (version 2.8). Each apartment has two files: "Heating" (*Chauffage*) and "Free-floating" (*Roue libre*).
2. **MUB MPC simulator**: this code uses four data files:
   1. `bornes_recharge_ve.csv` (EV charging stations);
   2. `charge_non_flexibles.csv` (non-flexible loads);
   3. `parametres_thermiques.csv` (thermal parameters);
   4. `temperature_exterieure.csv` (outdoor temperature).
3. **Base-load simulator** (non-flexible loads and electric vehicles): this code simulates the aggregated and disaggregated base load, excluding space heating. Its outputs feed the MUB MPC simulator.

[↑ Back to top](#flexibilité-thermique-des-bâtiments-multilogements--thermal-flexibility-of-multi-unit-residential-buildings)
