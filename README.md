# Predicting Water Well Functionality in Tanzania

This project builds a multi-class classification model to predict the operational status of water wells across Tanzania with classes,  functional, functional needs repair, or non functional, using data from the Tanzanian Ministry of Water via DrivenData's [Pump It Up](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/) competition.

The goal is to help the Ministry and NGO partners prioritize maintenance resources by identifying which wells are likely broken or at risk, shifting from reactive to proactive repair scheduling. Models explored include Logistic Regression, Decision Tree, and a tuned Random Forest, evaluated using macro recall to minimize the number of broken wells that go undetected.

---


## Notebooks

| Notebook | Description |
|---|---|
| `EDA.ipynb` | Business understanding, exploratory data analysis, feature selection, train/val/test split, and preprocessing pipeline |
| `first_model_classification.ipynb` | Baseline Dummy Classifier, Logistic Regression, and Decision Tree with depth tuning and feature importances |

**Run the notebooks in order.** `EDA.ipynb` generates the processed data files that notebooks first depend on.

---

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/tanzania-water-wells.git
cd tanzania-water-wells
```

### 2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Download the data
Create a free account at [DrivenData](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/) and download:
- `training_set_values.csv`
- `training_set_labels.csv`

Place both files in the `data/` folder.

### 4. Run the notebooks in order
```bash
jupyter notebook
```
Open and run `EDA.ipynb` first, then `first_model_classification.ipynb`, then `second_model_classification.ipynb`.

---

## Data

- **Source:** [DrivenData — Pump It Up: Data Mining the Water Table](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/)
- **Size:** 59,400 wells × 40 features
- **Target:** `status_group` — one of `functional`, `functional needs repair`, `non functional`
- **Split:** 60% train / 20% validation / 20% holdout test

---

## Results

| Model | Validation Accuracy | Validation Macro Recall |
|---|---|---|
| Dummy Classifier (baseline) | 0.5431 | 0.3333 |
| Logistic Regression | 0.6481 | 0.4510 |
| Decision Tree | 0.7172 | 0.5026 |


---

## Presentation

The non-technical stakeholder presentation is available here: [presentation.pdf](Tanzania Water Wells.pdf)

---

## Sources

- DrivenData. *Pump It Up: Data Mining the Water Table.* https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/
- Taarifa & Tanzanian Ministry of Water. *Water Point Data.*
