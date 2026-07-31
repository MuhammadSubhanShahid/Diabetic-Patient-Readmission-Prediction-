Diabetic Patient Readmission Prediction 🏥

Predicts whether a diabetic patient will be **readmitted to hospital**, using the [Diabetes 130-US Hospitals (1999–2008)](https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008) dataset (101,766 records).

Workflow

1. **Cleaning** – removed duplicates, handled `"?"` as missing, dropped `weight`/ID columns, imputed nulls (median/mode).
2. **Encoding** – binary target (`readmitted`: 0/1), one-hot encoded categorical features (→ 2,452 features).
3. **Modeling** – 80/20 stratified split, `StandardScaler`, trained **Logistic Regression**.
4. **Evaluation** – accuracy score, confusion matrix, visualizations.

Results

| Metric | Value |
|---|---|
| Accuracy | **62.6%** |
| Test samples | 20,354 |

**Confusion Matrix:** TN 8,054 · FP 2,919 · FN 4,688 · TP 4,693

Tech Stack

Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

How to Run

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```
Download the dataset, place it in the project folder, then run `diabetic.ipynb`.

Future Improvements

- Try Random Forest / XGBoost for better accuracy
- Handle class imbalance (SMOTE)
- Add precision, recall, F1, ROC-AUC
- Feature selection / PCA

License

MIT License
