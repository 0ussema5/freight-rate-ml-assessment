# Freight Rate ML Assessment

## Setup
pip install -r requirements.txt

## Files
- `notebook.ipynb` — full EDA, preprocessing, modeling, and prediction pipeline
- `data/` — provided input files (train_test.csv, validation.csv, december_chart_inputs.csv)
- `validation_predictions.csv` — final predictions for the 12,000 validation loads
- `december_predictions.csv` — completed December chart inputs with predicted_rate filled
- `score.py` — provided scorer (unmodified)
- `scorer_results/candidate_december.png` — output chart from score.py

## How to reproduce
1. Open `notebook.ipynb` and run all cells top to bottom (or run as a script if converted to .py).
2. This generates `validation_predictions.csv` and `december_predictions.csv`.
3. Run the scorer:
   python score.py --predictions validation_predictions.csv --december-predictions december_predictions.csv
4. Output chart is saved to `scorer_results/candidate_december.png`.

## Approach summary
See `report.pdf` for full details on data validation, EDA, feature engineering, 
model selection, train/validation split rationale, and December chart interpretation.
