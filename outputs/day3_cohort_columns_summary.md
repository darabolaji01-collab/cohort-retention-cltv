# Week 3 — CLTV Analysis Summary

**Milestone:** Historical CLTV and customer segmentation completed.

## Files created

- `notebooks/04_cltv_analysis.ipynb`
- `outputs/overall_cltv_summary.csv`
- `outputs/country_cltv_summary.csv`
- `outputs/customer_segment_summary.csv`
- `outputs/cohort_cltv_summary.csv`

## Overall CLTV metrics

| Metric | Value |
|---|---:|
| Total revenue | **£8,887,208.89** |
| Number of orders | **18,532** |
| Unique customers | **4,338** |
| Average Order Value (AOV) | **£479.56** |
| Purchase Frequency | **4.27 orders per customer** |
| Historical CLTV | **£2,048.69 per customer** |

## Customer value segments

Customers were segmented using total customer spend:

- **Low value:** bottom 50%
- **Medium value:** 50% to 80%
- **High value:** top 20%

| Segment | Customers | Revenue | Revenue share | Historical CLTV |
|---|---:|---:|---:|---:|
| High value | 868 | £6,637,300.82 | 74.7% | £7,646.66 |
| Medium value | 1,301 | £1,556,034.91 | 17.5% | £1,196.03 |
| Low value | 2,169 | £693,873.16 | 7.8% | £319.90 |

## Business interpretation

The high-value segment is only about one-fifth of the customer base, but it produces almost three-quarters of the revenue. This is an important finding because retention actions should protect the best customers first, while still helping medium-value customers buy again.
