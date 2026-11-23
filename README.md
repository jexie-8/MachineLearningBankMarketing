# Bank Marketing ML Coursework

This project predicts whether a customer will subscribe to a term deposit before a marketing call.

## Dataset

- Source: UCI Machine Learning Repository - Bank Marketing
- URL: https://archive.ics.uci.edu/dataset/222/bank+marketing
- DOI: https://doi.org/10.24432/C5K306
- Original file: `data/bank-full.csv` (45,211 rows)
- Personalised file: `data/bank_personalized.csv` (36,168 rows)

The personalized dataset is a stratified 80% subsample generated with TKH Student ID `202300404` as the random seed. It is created in `notebooks/01_EDA.ipynb` and all reported results use this subsample only.

## Notebooks (run in this order)

Run the notebooks from inside the `notebooks/` folder, one after another. Later notebooks depend on files written by earlier ones.

| # | Notebook | Purpose | Writes |
|---|----------|---------|--------|
| 1 | `01_EDA.ipynb` | Creates the personalised subsample, then data audit and exploratory analysis | `data/bank_personalized.csv` |
| 2 | `02_preprocessing.ipynb` | Train/test split, feature engineering and preprocessing pipeline | - |
| 3 | `03_modelling.ipynb` | Compares four classifiers, tunes them, optimises thresholds, selects and saves the final model | `artifacts/best_model.joblib`, `artifacts/best_model_metadata.json` |
| 4 | `04_evaluation.ipynb` | Final one-time evaluation of the saved model on the held-out test set | - |
| 5 | `05_AI_Baseline_Logistic_Regression.ipynb` | Notebook produced by a generative AI tool for the AI baseline comparison, run on the same personalised data and split | - |

## Environment

Use Python 3 and install the pinned packages in `requirements.txt`:

```
pip install -r requirements.txt
```

The local `.venv` directory is intentionally excluded from version control.
