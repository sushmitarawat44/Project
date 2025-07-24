# 📄 README.md — Customer Lifetime Value (CLTV) Prediction Project

## 📝 Project Title
Customer Lifetime Value (CLTV) Prediction using Machine Learning (XGBoost)

📊 Project Overview
This project aims to predict the Customer Lifetime Value (CLTV) using customer purchase behavior from historical transaction data. By engineering key behavioral features like Recency, Frequency, AOV (Average Order Value), and Tenure, a supervised regression model (XGBoost) is trained to estimate the lifetime revenue of each customer. The results are then used to segment customers into actionable tiers for marketing strategies.

---

## 📂 Dataset Information
Source: Kaggle — Ecommerce Data

Dataset Name: UK Online Retail Dataset (2010–2011)

File Used: data.csv

Size: ~540,000 transactions
### Columns Used:
InvoiceNo: Unique Order ID

CustomerID: Unique Customer Identifier

InvoiceDate: Date of transaction

Quantity: Units purchased

UnitPrice: Price per unit (in GBP)

Country: Customer's Country

## 🧹 Data Cleaning Steps
Removed Missing Values: Dropped rows where CustomerID, InvoiceDate, Quantity, or UnitPrice were null.
Filtered Out Cancelled Orders: Removed transactions where Quantity or TotalAmount was negative or zero.
Created New Column TotalAmount: Calculated as Quantity × UnitPrice.
Filtered Country (Optional):nKept only customers from United Kingdom (optional step for local market analysis).

## 🏗️ Feature Engineering
- Feature	Description
- Recency	Days since customer's last purchase
- Frequency	Number of unique purchase invoices (orders)
- AOV	Average Order Value = Total Spend / Number of Purchases
- Tenure	Days between the customer’s first and last purchase
- LTV (Target)	Total money spent by the customer

## 🤖 Modeling Approach

- Algorithm Used: XGBoost Regressor

- Train/Test Split: 80% Training, 20% Testing

- Evaluation Metrics:

- Mean Absolute Error (MAE)

- Root Mean Squared Error (RMSE)

## 🎯 Customer Segmentation
- Post-prediction, customers were segmented into 4 LTV tiers: 
Low

Medium

High

Very High
 
- Segmentation was done using quartile-based binning (qcut) on predicted LTV scores.

## 📈 Visualizations Created
- LTV Distribution Histogram
- Actual vs. Predicted LTV Scatter Plot
- Feature Importance Bar Chart
- Customer Segment Pie Chart

## 💾 Files Included
- File Name	Description
- CLTV_Prediction_Notebook.ipynb	Full Python notebook (Google Colab)
- cltv_predictions.csv	Output file with CustomerID, Predicted LTV, Segment
- ltv_distribution.png	LTV Distribution Plot
- actual_vs_predicted.png	Model Performance Plot
- feature_importance.png	Feature Importance Chart
- customer_segments.png	Pie Chart of Customer Segments
- xgb_ltv_model.pkl (optional)	Saved XGBoost model for future use

## 🚀 How to Run This Project
- Open Google Colab.
- Upload data.csv into Colab.
- Run the Jupyter notebook cells sequentially.
- Download the final cltv_predictions.csv and visual outputs.
- Optional: Load xgb_ltv_model.pkl to reuse the trained model.

---

## 🙌 Author
Sushmita Rawat
Aspiring Data Analyst | Python Enthusiast | Machine Learning Practitioner

📢 Contact
LinkedIn: https://www.linkedin.com/in/sushmita-rawat-143a46217/

Email: sushmitarawat456@gmail.com


