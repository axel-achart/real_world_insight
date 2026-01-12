# Real World Insight — Food Production & Economic Evolution

### English
-------

### Purpose
 - Transform FAO food-production data into actionable insights: clean the data, compute year-on-year growth, produce descriptive visualizations, and identify country profiles using clustering.

### Project structure
 - `data/`
	 - `raw/` : original FAO CSV files (raw data and codebooks)
	 - `clean/` : cleaned CSV exported by the notebook (`fao_clean.csv`)
 - `notebook/` : analysis notebooks
	 - `exploration.ipynb` : main exploratory analysis and figures
	 - `exploration_eng.ipynb` : English-labeled copy
	 - `conclusion.ipynb` : standalone conclusions and summary
 - `figures/` : generated figures (e.g., `top5_production.png`, `growth_barplot.png`, `country_clusters.png`)
 - `requirements.txt` : Python dependencies
 - `.gitignore` : recommended ignores (virtualenv, caches, figures optional)

### Data used
 - The project uses FAO production datasets (CSV). Source files are stored under `data/raw/` and include the main production table and auxiliary codebook files (item codes, element codes, area codes, flags).
 - Original source: Food and Agriculture Organization of the United Nations (FAO) — FAOSTAT data portal. See FAOSTAT (http://www.fao.org/faostat) for dataset metadata and codebooks.

### How to run
 1. Create and activate a Python virtual environment (recommended):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

2. Open and run `notebook/exploration.ipynb` in Jupyter Notebook or JupyterLab. The notebook performs cleaning, analysis, plotting and saves cleaned data to `data/clean/fao_clean.csv` and figures to `figures/`.

### Notes
 - The notebooks use vectorized operations for growth calculation and include a clustering pipeline (feature engineering at country level, scaling, KMeans with silhouette-based k selection, PCA visualization).
 - Review and verify `data/raw/` files and the FAO codebooks before running sectoral analyses.

</br>
</br>
</br>

### Français
-------

### But du projet
 - Transformer les données FAO (Food And Organization) sur la production alimentaire en insights exploitables : nettoyage, calcul des croissances annuelles, visualisations descriptives et profilage des pays par clustering.

### Structure du projet
 - `data/`
	 - `raw/` : fichiers FAO d'origine (CSV et codebooks)
	 - `clean/` : données nettoyées exportées par le notebook (`fao_clean.csv`)
 - `notebook/` : notebooks d'analyse (`exploration_fr.ipynb`, `exploration_eng.ipynb`, `conclusion.ipynb`)
 - `figures/` : figures générées (`top5_production.png`, `growth_barplot.png`, `country_clusters.png`)
 - `requirements.txt` : dépendances Python
 - `.gitignore` : fichiers et dossiers à ignorer

### Données et source
 - Les fichiers FAO (FAOSTAT) sont utilisés comme source principale. Ils sont placés dans `data/raw/`. Consultez le portail FAOSTAT (http://www.fao.org/faostat) pour la documentation et les codebooks (mappings d'items, définitions des éléments, codes de zone).

### Exécution
 - Voir la section "How to run" ci-dessus dans la section en Anglais pour créer un environnement virtuel et installer les dépendances.

### Remarques finales
 - Pensez à vérifier les correspondances d'items (fichier `Production_Crops_Livestock_E_ItemCodes.csv`) avant d'effectuer des analyses sectorielles précises. Le clustering fourni est une base de travail ; testez d'autres approches si nécessaire.