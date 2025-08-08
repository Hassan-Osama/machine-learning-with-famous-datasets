# Customer Segmentation using RFM Analysis & K-Means Clustering

## Project Overview
This project applies **RFM (Recency, Frequency, Monetary)** analysis to an **e-commerce dataset** and uses **K-Means clustering** to segment customers into meaningful groups.  
The goal is to help businesses **understand customer behavior** and develop **data-driven marketing strategies**.

---

## 📂 Dataset
The dataset contains transactional records from an online retailer.  
**Key columns used:**
- `CustomerID` – Unique identifier for each customer.
- `InvoiceDate` – Date and time of the transaction.
- `Quantity` – Number of items purchased.
- `UnitPrice` – Price per unit.
- `InvoiceNo` – Invoice number (used to filter cancellations).

You can download a similar dataset from:
- [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Online+Retail)
- [Kaggle – E-Commerce Data](https://www.kaggle.com/datasets/carrie1/ecommerce-data)

---

## Methodology
1. **Data Cleaning**
   - Removed missing `CustomerID` values.
   - Removed unnecessary columns (`Description`).
   - Converted `InvoiceDate` to datetime format.
   - Filtered canceled orders.

2. **Feature Engineering**
   - **Monetary (M):** `TotalSpent` = `Quantity × UnitPrice` aggregated per customer.
   - **Recency (R):** Days since the customer’s most recent purchase.
   - **Frequency (F):** Total number of transactions per customer.

3. **Exploratory Data Analysis**
   - Visualized customer distribution in 3D using `plotly`.
   - Checked correlations between R, F, and M.

4. **Clustering**
   - Standardized RFM features using `StandardScaler`.
   - Used the **Elbow Method** to find an optimal number of clusters.
   - Applied **K-Means** with 4 clusters.
   - Visualized clusters in 3D and 2D scatter plots.

5. **Cluster Ranking**
   - Assigned R, F, and M scores (1–4) to each cluster.
   - Interpreted cluster meaning for business actions.

---

## Cluster Summary

| Cluster | R | F | M | Interpretation |
|---------|---|---|---|----------------|
| **0** | 2 | 2 | 2 | Mid-range customers – Moderate activity and spending. |
| **1** | 4 | 4 | 3 | Champions – High recency & frequency, strong spending. |
| **2** | 3 | 3 | 4 | Big Spenders – High spenders but less recent/frequent than champions. |
| **3** | 1 | 1 | 1 | At Risk / Lost – Inactive with low spending and frequency. |

---

## Visualizations
- **3D scatter plots** for RFM distributions and clusters.
- **2D scatter plots** to understand relationships between R, F, and M.
- **Elbow Method plot** for selecting optimal cluster count.

---

## Business Applications
- **Cluster 1 – Champions:** Exclusive offers, VIP programs, early access.
- **Cluster 2 – Big Spenders:** High-end promotions, upselling opportunities.
- **Cluster 0 – Mid-range:** Encourage higher frequency through promotions.
- **Cluster 3 – At Risk / Lost:** Win-back campaigns and discounts.