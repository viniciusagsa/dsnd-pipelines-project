# Approach on Fashion Forward Forecasting
*Data Scientist Nanodegree Program: Pipeline project*

This repository contains the code, data pointers, and notebooks for the DSND (Data Scientist Nanodegree) pipelines project. It demonstrates a simple ML pipeline: data ingestion, exploratory analysis, modeling (baseline and tuned models), and saving trained artifacts.

The repository layout (important paths)

- `starter/` — starter notebook and supporting files used to explore the dataset and iterate on models.
- `data/` — small sample data used by notebooks (contains `reviews.csv`).
- `models/` — directory where trained model files are saved (not tracked by git if large).
- `pipeline/` — a Python virtual environment used during development.

## Why this repo

This project is a compact example of building and evaluating ML pipelines. It includes:

- an exploratory notebook (`starter/starter.ipynb`) to inspect the dataset and engineer features;
- training experiments with a baseline RandomForest and XGBoost;
- saved model artifacts and a reproducible environment specification (`requirements.txt`).

## Getting started (Windows, PowerShell)

1. Create a fresh virtual environment (recommended) and activate it:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies:

```powershell
pip install -r requirements.txt
```

3. Open the `starter/starter.ipynb` notebook in Jupyter or VS Code and run the cells in order. The notebook will show EDA, baseline model training, hyperparameter search, and evaluation.

## Notes and tips

- If GridSearchCV hyperparameter tuning worsens MSE or generalization, check `grid_search.best_params_`, `cv_results_`, and residuals — tuning can select higher-variance models or be sensitive to the chosen scoring metric. Use nested CV or optimize the metric you care about (e.g., neg_mean_squared_error) to reduce selection bias.
- The repository contains a `pipeline/` folder that is a full virtualenv snapshot; do not commit environment-specific files. Instead recreate environments with `python -m venv` + `pip install -r requirements.txt`.
- If working with OneDrive (this repo is under OneDrive), be careful with file locks and sync conflicts when training models or writing artifacts.

## License

This project uses the repository license in `LICENSE.txt`.

## Final comments

Feel free to reach out on [LinkedIn](https://www.linkedin.com/in/viniciusagsa/) or through my [GitHub profile](https://github.com/viniciusagsa) if you’d like to discuss the project or collaborate on similar topics.
