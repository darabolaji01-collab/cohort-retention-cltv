# Final Business Summary — Cohort Retention & CLTV Analysis

## Project overview

This project analyzes customer retention and Customer Lifetime Value (CLTV) for an online retail business. The main idea is simple: customers are grouped by the month they first purchased, then I check how many of them returned in later months.

The dataset is the Online Retail transaction dataset, covering purchases from **December 2010 to December 2011**.

## Business problem

Getting new customers is expensive, so the business needs to know whether customers come back after their first purchase. If many customers buy once and disappear, the company may keep spending money on acquisition without building long-term value.

## Data cleaning summary

The raw data had several issues:

- cancelled invoices,
- returned/refunded transactions,
- missing customer IDs,
- duplicate rows,
- zero or negative prices.

After cleaning, the final analysis dataset contained:

| Metric | Value |
|---|---:|
| Clean rows | 392,692 |
| Unique customers | 4,338 |
| Unique orders | 18,532 |
| Countries | 37 |
| Total revenue | £8,887,208.89 |

## Retention findings

The cohort retention matrix showed that customers drop off quickly after their first purchase.

| Metric | Value |
|---|---:|
| Average Month 1 retention | 20.6% |
| Average Month 2 retention | 22.1% |
| Cohort index range | Month 0 to Month 12 |

### Interpretation

Month 0 is always 100% because it is the customer's first purchase month. The main issue is that only about one in five customers returns the next month. This suggests the business has a big early churn problem.

## CLTV findings

Overall historical CLTV:

| Metric | Value |
|---|---:|
| Average Order Value | £479.56 |
| Purchase Frequency | 4.27 orders per customer |
| Historical CLTV | £2,048.69 per customer |

Customer value segments:

| Segment | Customers | Revenue share | Historical CLTV |
|---|---:|---:|---:|
| High value | 868 | 74.7% | £7,646.66 |
| Medium value | 1,301 | 17.5% | £1,196.03 |
| Low value | 2,169 | 7.8% | £319.90 |

### Interpretation

The high-value customers are very important. They are only the top 20% of customers by spend, but they generate almost three-quarters of total revenue. Losing these customers would hurt the business more than losing a low-value customer.

## Recommendations

1. **Improve early retention.** Send a re-engagement email, product recommendation, or small discount 2–3 weeks after the first purchase.
2. **Protect high-value customers.** Give repeat buyers better service, loyalty rewards, or early access to popular products.
3. **Move medium-value customers upward.** Medium-value customers already show some buying interest, so targeted offers may turn them into high-value customers.
4. **Use CLTV when setting CAC.** The business should not spend the same amount to acquire every customer segment. High-CLTV segments can justify higher acquisition cost.
5. **Track cohorts monthly.** This analysis should be repeated every month so the team can see whether retention is improving.

## Limitations

- The dataset has only about 13 months of transactions.
- There is no marketing channel column, so I could not compare cohorts by acquisition source.
- December 2010 may include customers who were already active before the dataset started.
- The CLTV is historical, not a full predictive model.

## Future improvements

- Add marketing channel data if available.
- Analyze products/categories bought by high-value customers.
- Build a simple predictive CLTV model when more months of data are available.
- Create a dashboard in Power BI, Tableau, or Streamlit.
