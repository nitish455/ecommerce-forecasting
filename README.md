# E-Commerce Demand Forecasting & Inventory Planning

## 📌 Project Overview

This project focuses on forecasting short-term e-commerce product demand and converting the forecast into an inventory replenishment recommendation.

The analysis uses historical order data to identify a high-demand product, forecast its demand for the next 4 weeks, and calculate inventory requirements such as safety stock and reorder point.

## 🎯 Business Objective

- Analyze historical e-commerce order data
- Identify high-demand products
- Forecast future weekly demand
- Estimate inventory requirements
- Determine whether inventory needs to be replenished

## 🔄 Project Workflow

**Historical Orders → Completed Orders → Demand Analysis → Product Selection → Weekly Forecasting → Inventory Planning**

## 📊 Selected Product

**Water Bottle Insulated**

The selected product is used to demonstrate the complete demand forecasting and inventory planning workflow.

## 🤖 Forecasting Model

**Random Forest Regressor**

Features used:

- Calendar features: Week, Month, Quarter
- Lag features: Lag 1, Lag 2, Lag 4, Lag 8
- Rolling averages: Rolling Mean 4, Rolling Mean 8

A chronological 80/20 train-test split is used to avoid data leakage.

A previous-week demand baseline is also used for comparison.

## 🔮 Forecasting

The model generates a **4-week recursive demand forecast** for the selected product.

The forecast is then used as an input for inventory planning.

## 📦 Inventory Planning

The project calculates:

- Average daily demand
- Demand variability
- Average delivery/lead time
- Safety stock
- Lead-time demand
- Reorder point
- Suggested replenishment quantity

### Reorder Decision

If current stock is below the calculated reorder point:

**REORDER NOW**

Otherwise:

**STOCK LEVEL ACCEPTABLE**

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Plotly
- Scikit-learn
- Jupyter Notebook

## 📂 Dataset

The original e-commerce dataset is **not included in this repository** because of its large file size.

To run the notebook locally:

1. Obtain the dataset separately.
2. Place `ecommerce_dataset.csv` in your local project directory.
3. Update the `DATA_PATH` in the notebook to point to your local dataset location.

## 📁 Project Structure

```text
ecommerce-forecasting/
│
├── ecommerce_demand_forecasting.ipynb
├── README.md
└── requirements.txt
