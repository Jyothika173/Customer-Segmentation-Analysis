# Customer Segmentation Analysis

## Objective
Apply clustering to segment an e-commerce company's customers into distinct groups based on purchasing behaviour, so marketing can be targeted for each group.

## Dataset
Online Retail dataset (UCI). 541,909 transaction rows, reduced to 392,692 after cleaning, covering 4,338 customers.

## Tools
Python, pandas, scikit-learn (KMeans, StandardScaler), matplotlib, seaborn, Jupyter Notebook

## What I did
- [x] Loaded the data and handled missing and inconsistent values (removed rows with no CustomerID, cancelled invoices, zero or negative quantity and price, and duplicates)
- [x] Calculated purchase frequency, customer lifetime value and average purchase value
- [x] Selected 3 features for clustering: Recency, Frequency and Monetary (RFM)
- [x] Standardised the features with StandardScaler
- [x] Used the Elbow Method to choose K=3 and applied K-Means
- [x] Visualised the clusters with scatter plots (Recency vs Frequency, Frequency vs Monetary)
- [x] Profiled each cluster using mean RFM values
- [x] Plotted the number of customers per cluster
- [x] Wrote marketing recommendations for each segment

## Key findings
- The average customer placed about 4 orders and spent about £2,049, but the median is only about £669. A few big spenders pull the average up.
- 3 customer segments were found:

| Cluster | Segment | Avg recency (days) | Avg orders | Avg spend |
|---|---|---|---|---|
| 0 | Inactive / Lost | 247 | 1.6 | £630 |
| 1 | Regular / Active | 41 | 4.7 | £1,850 |
| 2 | VIP / Champions | 6 | 66.4 | £85,826 |

- Regular customers are the largest group. The VIP group is very small but by far the most valuable.

## Marketing recommendations
- **VIP:** loyalty rewards, early access to new products, exclusive offers and a personal thank-you, to keep them.
- **Regular:** upselling, cross-selling, bundles and reward points, to move them towards VIP.
- **Inactive:** win-back emails, discount coupons and a short feedback survey, without heavy spending.

## Files
- `Customer_Segmentation_Analysis.ipynb`: the notebook
- `Online Retail.xlsx`: the data
