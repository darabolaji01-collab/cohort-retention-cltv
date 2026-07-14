# Week 2 — Cohort Retention Matrix Summary

**Milestone:** Retention count matrix and retention percentage matrix completed.

## Files created

- `notebooks/03_cohort_retention_matrix.ipynb`
- `outputs/cohort_count_matrix.csv`
- `outputs/retention_percentage_matrix.csv`

## What the matrix means

- Rows = the month customers first purchased (`cohort_month`).
- Columns = months after first purchase (`cohort_index`).
- Month 0 = first purchase month, so retention is always 100% there.
- Month 1, Month 2, etc. show how many customers returned in later months.

## Validation checks

| Check | Result |
|---|---:|
| Month 0 retention is 100% for every cohort | Passed |
| Month 0 customer count equals all unique customers | 4,338 |
| Negative retention values | 0 |
| Retention values above 100% | 0 |

## Key retention findings

| Metric | Value |
|---|---:|
| Average Month 1 retention | **20.6%** |
| Average Month 2 retention | **22.1%** |
| Biggest visible issue | Most cohorts lose around 75–85% of customers after Month 0 |

## Beginner interpretation

The biggest drop happens immediately after the first purchase. This means the business should not wait too long before trying to bring customers back. A simple follow-up email, discount, or product recommendation within the first few weeks could help improve Month 1 retention.
