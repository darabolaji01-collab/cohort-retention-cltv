# Submission Checklist and Run Guide

## Internship requirement checklist

| Requirement | Status | Where completed |
|---|---|---|
| Week 1 data loading | ✅ Done | `notebooks/01_data_cleaning_eda.ipynb` |
| Week 1 data cleaning | ✅ Done | `notebooks/01_data_cleaning_eda.ipynb`, `src/data_prep.py` |
| Missing value handling | ✅ Done | Missing `customer_id` removed for cohort work |
| Cancelled/refunded transactions removed | ✅ Done | Invoice numbers starting with `C`, negative quantities removed |
| Missing customer IDs handled | ✅ Done | Removed before cohort/CLTV analysis |
| Data validation checks | ✅ Done | Cleaning audit, cohort checks, retention checks |
| Feature engineering | ✅ Done | `line_total`, month columns, cohort columns, segments |
| Cohort Month calculation | ✅ Done | `notebooks/02_cohort_month_index.ipynb` |
| Cohort Index calculation | ✅ Done | `notebooks/02_cohort_month_index.ipynb` |
| Cohort count matrix | ✅ Done | `notebooks/03_cohort_retention_matrix.ipynb` |
| Retention matrix | ✅ Done | `outputs/retention_percentage_matrix.csv` |
| Retention percentage matrix | ✅ Done | `outputs/retention_percentage_matrix.csv` |
| AOV calculation | ✅ Done | `notebooks/04_cltv_analysis.ipynb` |
| Purchase frequency calculation | ✅ Done | `notebooks/04_cltv_analysis.ipynb` |
| Revenue calculations | ✅ Done | CLTV notebook and output CSVs |
| Customer segmentation | ✅ Done | Low, Medium, High value segments |
| Historical CLTV | ✅ Done | Overall, country, segment, and cohort CLTV tables |
| Cohort heatmap | ✅ Done | `outputs/cohort_retention_heatmap.png` |
| Retention curves | ✅ Done | `outputs/retention_curves.png` |
| CLTV charts | ✅ Done | `outputs/cohort_cltv_bar_chart.png` |
| Customer segment visuals | ✅ Done | `outputs/segment_revenue_share.png` |
| Executive business insights | ✅ Done | `reports/final_business_summary.md` |
| Final recommendations | ✅ Done | README and final report |
| Beginner-friendly explanations | ✅ Done | All notebooks and README |
| README completed | ✅ Done | `README.md` |
| Raw data excluded from GitHub | ✅ Done | `.gitignore` ignores `data/` |
| Notebook verification | ✅ Done | All notebooks were run successfully from top to bottom |

## Suggested commit stages

```text
fix: add real gitignore and improve data loading helpers
feat: build cohort retention matrix
feat: calculate historical cltv and customer segments
feat: add final visualizations and business summary
chore: add tests and final run instructions
```

## Exact git commands

```bash
git status

git add .gitignore gitignore.txt requirements.txt src/data_prep.py tests/test_data_prep.py
git commit -m "fix: add gitignore and improve data loading helpers"

git add notebooks/03_cohort_retention_matrix.ipynb outputs/cohort_count_matrix.csv outputs/retention_percentage_matrix.csv outputs/week2_retention_summary.md
git commit -m "feat: build cohort retention matrix"

git add notebooks/04_cltv_analysis.ipynb outputs/overall_cltv_summary.csv outputs/country_cltv_summary.csv outputs/customer_segment_summary.csv outputs/cohort_cltv_summary.csv outputs/week3_cltv_summary.md
git commit -m "feat: calculate historical cltv and customer segments"

git add notebooks/05_visualizations_insights.ipynb outputs/*.png outputs/week4_visualization_summary.md reports/final_business_summary.md
git commit -m "feat: add final visualizations and business insights"

git add README.md notebooks/01_data_cleaning_eda.ipynb notebooks/02_cohort_month_index.ipynb outputs/day1_data_profile.md outputs/day2_cleaning_summary.md outputs/day3_cohort_columns_summary.md outputs/cleaning_audit.csv outputs/cohort_sizes.csv reports/submission_checklist.md
git commit -m "docs: finalize readme and submission checklist"

git push origin main
```

## How to run the project from start to finish

1. Clone the repository.

```bash
git clone https://github.com/darabolaji01-collab/cohort-retention-cltv.git
cd cohort-retention-cltv
```

2. Create a virtual environment.

```bash
python -m venv .venv
```

3. Activate it.

Windows:

```bash
.venv\Scripts\activate
```

macOS/Linux:

```bash
source .venv/bin/activate
```

4. Install packages.

```bash
pip install -r requirements.txt
```

5. Add the dataset locally.

Create a `data/` folder and place the Online Retail file inside it:

```text
data/Online_Retail.xlsx
```

6. Launch Jupyter.

```bash
jupyter notebook
```

7. Run notebooks in order.

```text
01_data_cleaning_eda.ipynb
02_cohort_month_index.ipynb
03_cohort_retention_matrix.ipynb
04_cltv_analysis.ipynb
05_visualizations_insights.ipynb
```

8. Check that the project worked.

You should see these files in `outputs/`:

```text
cohort_count_matrix.csv
retention_percentage_matrix.csv
overall_cltv_summary.csv
customer_segment_summary.csv
cohort_retention_heatmap.png
retention_curves.png
cohort_cltv_bar_chart.png
segment_revenue_share.png
top_countries_revenue.png
```

9. Run tests.

```bash
pytest
```

Expected result:

```text
2 passed
```
