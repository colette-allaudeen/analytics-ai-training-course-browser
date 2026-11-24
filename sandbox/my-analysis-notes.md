# Analysis Notes: Monthly Active Customers by Vertical

## What the Query Does

The query counts distinct active customers per month for the past 6 months, broken out by business vertical. A customer is "active" if they completed at least one job in that month. It uses a date spine to ensure every month appears in the output even with zero activity, and calculates month-over-month growth using a LAG window function.

## What the Output Shows

- **HVAC and Plumbing** are the two largest verticals, both growing steadily at 2–4.5% MoM.
- **Landscaping** is growing extremely fast — 33–57% MoM every month, from 312 customers in October 2025 to 1,847 in March 2026.
- **Electrical** dipped 4.8% in the most recent month (March 2026) after positive growth in prior months.
- **Cleaning** is small but consistent, growing 2–6% most months.

## One Thing to Investigate Further

Landscaping's growth is too consistent and steep to accept without explanation. Before surfacing this number to a stakeholder, I'd want to understand whether it reflects real customer acquisition, a vertical reclassification, a new partnership, or a data quality issue. A follow-up query breaking down Landscaping customers by acquisition source and cohort would be the right next step.
