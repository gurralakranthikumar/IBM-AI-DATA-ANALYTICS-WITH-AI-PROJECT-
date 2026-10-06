# E-commerce Sales & Customer Analytics With Bob AI Agent 

**Author:** G Kranthi Kumar
**Program:** AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026 | BharatCares

## Project description
This project analyses five years (2021 to 2025) of e-commerce orders to understand sales, profit, products, delivery performance and customer behaviour. It then groups customers into four segments using **RFM features (Recency, Frequency, Monetary) and K-Means clustering**, and suggests a business action for each segment.

## Dataset
**E-Commerce Sales and Customer Analytics** (Kaggle):
https://www.kaggle.com/datasets/datascikhan/e-commerce-sales-and-customer-analytics

| File | Content |
|---|---|
| `ecommerce_sales_customer_analytics_150k.csv` | 138,116 orders, 46 columns |
| `order_items.csv` | 397,569 order lines |
| `product_catalog.csv` | 1,175 products |
| `customer_master.csv` | 25,000 customers |
| `dataset_statistics.csv` | Publisher's summary statistics |

## Technologies used 
IBM Bob Agent, pandas, NumPy, Matplotlib, Seaborn, scikit-learn (StandardScaler, K-Means, PCA, silhouette score), Jupyter Notebook.

## Setup and run
1. Install Or setup IBM bob Agent.
2. Download the dataset from the Kaggle link above and place the five CSV files in the same folder as the notebook (or in a `data/` sub-folder).
3. Open and run the notebook:
   ```
   jupyter notebook KranthiKumar_EcommerceAnalytics.ipynb
   ```
   Choose **Run All**. It takes about a minute. You can also run it in Google Colab by uploading the notebook and the CSV files.

The notebook writes `customer_segments.csv` (segment of every customer).

## What the notebook does
1. Loads the five files and checks data quality (duplicates, missing values, structural gaps).
2. Cleans and prepares features (dates, discount rate, order status flags).
3. Reproduces the business KPIs and checks them against the publisher's statistics.
4. Explores sales trend, channels, geography, products, discounts, delivery and ratings.
5. Builds RFM features, chooses k with the elbow method and silhouette score, and runs K-Means (k = 4).
6. Names and profiles the segments and exports them.

## Key results
- Net sales are flat at about 28.6M to 29.3M a year, with a large November and December peak.
- The USA gives about 58% of sales. Electronics sells the most but has the lowest margin (about 33%).
- Discounts of 50% or more cause negative margins; 45% of such orders lose money.
- Four segments: **Champions** (40% of customers, 61% of revenue), **Steady Regulars** (32%, 24%), **Discount Seekers** (16%, 11%) and **At-Risk / Lapsed** (12%, 4%).

## Important notes
- Amounts are in several currencies (USD, GBP, EUR and others) but are not converted, so totals are in the dataset's own units.
- Revenue analysis uses completed orders only (82% of all orders).
- The data appears simulated, so results describe this dataset only.

## Project files
- `KranthiKumar_EcommerceAnalytics.ipynb`: code
- `requirements.txt`: dependencies
- `KranthiKumar_ProjectReport.docx`: full report
- `README.md`: this file
