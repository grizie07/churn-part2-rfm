# Part 2 — RFM Segmentation & Retention Strategy

D2C Customer Churn Capstone | Snapshot date: `2025-09-30`

## What's in this repository

| File | Description |
|---|---|
| `rfm_segmentation.ipynb` | Main notebook: RFM scoring, segment assignment, all charts |
| `segments.csv` | One row per customer with segment name and key features |
| `retention_strategy.md` | Segment-by-segment retention actions + budget prioritization |
| `manual_review_cases.md` | 10 specific customer IDs with non-obvious decisions |
| `requirements.txt` | Python dependencies |

## Setup & Run

```bash
git clone <your-repo-url>
cd churn-part2-rfm

pip install -r requirements.txt

# Place all dataset CSVs in the same folder as the notebook:
#   rfm_modeling_snapshot.csv
#   intervention_history.csv

jupyter notebook rfm_segmentation.ipynb
```

## Segments Created

| Segment | Count | Churn Rate |
|---|---|---|
| Champions | 401 | 10.2% |
| Loyal Customers | 578 | 25.4% |
| Promising New | 265 | 21.9% |
| At-Risk | 390 | 72.1% |
| Dormant | 372 | 91.1% |
| Discount Sensitive | 130 | 63.8% |
| High Value Unhappy | ~66 | ~55% |
| Silent Disengaged | 19 | 84.2% |
| Needs Attention | 245 | 66.1% |

## Key Design Decisions

- RFM scores use **quintile-based scoring (1–5)** with `rank(method='first')` on F and M to handle ties
- Segments use **RFM + 2 non-RFM signals**: support ticket count and discount usage
- Budget allocation prioritises At-Risk and High Value Unhappy segments
- Dormant customers are excluded from active budget (too far gone, low ROI)
