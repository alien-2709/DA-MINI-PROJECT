# Telco Customer Churn: Exploratory and Confirmatory Data Analysis

**Course:** Data Analytics (CES2103), III Semester B.Tech., Computer Science and Engineering
**Institution:** School of Computer Engineering, Manipal Institute of Technology, MAHE
**Team:** Team_02

| Member | Roll No. | Registration No. | Section |
|---|---|---|---|
| Lavanya Sandeep Borkar | 17 | 251090050708 | CSE-I |
| Tanvi Choudhary | 63 | 251090052750 | CSE-I |
| Gauri Nikhil Chandak | 29 | 251090051220 | CSE-I |

## What this project does
1. Checks and cleans the Telco Customer Churn data (7,043 customers, 21 columns).
2. **EDA:** describes churn by tenure, charges, contract type and other attributes.
3. **CDA:** tests with a Pearson chi-square test whether churn is independent of contract type
   (chi-square = 1,184.60, df = 2, p < 0.001, Cramer's V = 0.41).
4. Supplementary (beyond the report): cross-validated predictive models with a held-out test set.

These are associations in observational data and do not establish causes.

## Repository contents
| Path | Description |
|---|---|
| `Telco_Churn_Analysis.ipynb` | Full analysis notebook (run top to bottom) |
| `data/WA_Fn-UseC_-Telco-Customer-Churn.csv` | Dataset, used exactly as supplied |
| `figures/` | 15 PNG figures written by the notebook |
| `tables/` | 25 CSV result tables written by the notebook |
| `results_summary.json` | Run summary written by the notebook |
| `requirements.txt` | Package versions of the reported run |
| `report/Team_02.pdf` | Submitted project report |

## Which part of the notebook feeds the report
Sections 1-4 of the notebook (data verification, EDA, statistical tests) correspond to the
report's Sections 3, 5 and 6. Sections 5-9 (train/test split, models, held-out evaluation,
interpretation) are supplementary and are not part of the report's analysis.

## How to run
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate      macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook Telco_Churn_Analysis.ipynb     # then Kernel > Restart & Run All
```
The full run takes about 3-5 minutes (most of it is the hyper-parameter grid search).
The random seed is fixed (42), so results are reproducible with the pinned versions.
The notebook looks for the CSV in `data/` and writes `figures/`, `tables/`,
`requirements.txt` and `results_summary.json` next to itself.

## Data source
"Telco Customer Churn", Kaggle (user: BlastChar), whose description credits the IBM sample data sets:
https://www.kaggle.com/datasets/blastchar/telco-customer-churn
The data are a fictional telecom company's sample data, so findings should not be generalised to a real operator.
