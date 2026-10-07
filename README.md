# Two-Phase Flow Rate through Wellhead Chokes in Oil Wells - ML Mini Project

Machine learning-based prediction of two-phase liquid flow rate through oil wellhead chokes using the Sorush oil field dataset.

Course: UE24CS352A - Machine Learning, PES University

---

## 1. Problem Statement

Predicting liquid flow rate through wellhead chokes is an important problem in oil and gas production. Flow meters are expensive and hard to deploy across large fields, so the flow rate is often estimated from simple wellhead measurements.

Classical empirical correlations (Gilbert, Baxendell, Ros, Achong) use a small set of parameters and generalise poorly across fields. This project investigates machine learning regression models as an alternative.

The input parameters are:

- Choke size
- Wellhead pressure
- Oil specific gravity
- Gas-liquid ratio

---

## 2. Dataset

The project uses the **Sorush oil field dataset**: **7,245 observations** from **10 wells**.

| Variable | Description | Role |
|---|---|---|
| `D (1/64in)` | Choke size | Feature |
| `Pwh` | Wellhead pressure | Feature |
| `γo` | Oil specific gravity | Feature |
| `GLR` | Gas-liquid ratio | Feature |
| `QL` | Liquid flow rate | Target |

The original dataset is kept in `data/raw/`. Raw and processed data are excluded from Git tracking through `.gitignore`.

---

## 3. Workflow

1. Exploratory data analysis (EDA)
2. Data validation and quality checks
3. Outlier investigation
4. Preprocessing (cleaning, train/test split, scaling)
5. Regression model development
6. Model evaluation and comparison

---

## 4. Exploratory Data Analysis

Notebook: `notebooks/01_data_exploration.ipynb`

- Shape and column validation
- Missing-value and duplicate-row analysis
- Well-wise sample analysis
- Descriptive statistics, distributions and boxplots
- Pearson and Spearman correlation
- Feature versus target analysis
- Outlier investigation (IQR and 3-standard-deviation methods)

Figures are saved in `results/figures/` and statistical summaries in `results/metrics/`.

---

## 5. Data Preprocessing

Notebook: `notebooks/02_preprocessing.ipynb`

- Load the dataset and validate required columns
- Handle missing and duplicate observations
- Investigate extreme observations
- Separate features and target
- Train/test split
- Standardise features using training-set statistics
- Save processed datasets to `data/processed/`

---

## 6. Model Development and Evaluation (Next Stage)

Regression models for the continuous target `QL` will be trained and compared using:

- R² Score
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

Final results will be documented here once this stage is complete.

---

## 7. Repository Structure

```text
.
├── data/
│   ├── raw/
│   │   └── sorush_dataset.xlsx
│   └── processed/
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   └── 02_preprocessing.ipynb
├── results/
│   ├── figures/
│   └── metrics/
├── .gitignore
├── README.md
└── requirements.txt
```

---

## 8. Setup and Run

Clone the repository:

```bash
git clone https://github.com/Arnav060706/Two-Phase-Flow-Rate-through-Wellhead-Chokes-in-Oil-Wells-ML-Mini-Project.git
cd Two-Phase-Flow-Rate-through-Wellhead-Chokes-in-Oil-Wells-ML-Mini-Project
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter and run the notebooks in order:

```bash
jupyter notebook
```

1. `notebooks/01_data_exploration.ipynb`
2. `notebooks/02_preprocessing.ipynb`

---

## 9. Project Status

**Completed:** dataset exploration and validation, statistical and correlation analysis, missing-value and duplicate checks, outlier investigation, initial preprocessing.

**Next:** model training, evaluation, comparison and final model selection.

---

## 10. Reference

N. Nazari and T. Alshafloot, *Prediction of Two Phase Flow Rate through Wellhead Chokes in Oil Wells*, CS229 Final Project Report, Stanford University.

---

## 11. Contributors

- Arnav Sharath Hanchanur
- Bollavaram Santosh Kumar

---

## License

This repository is intended for academic and educational use.
