# AI-Driven Smart Retail Supply Chain Intelligence System

An end-to-end machine learning and business intelligence project that transforms a retail sales dataset into actionable supply chain insights. The project covers demand forecasting, delivery delay prediction, inventory optimization, supplier ranking, transportation cost analysis, and supply chain risk monitoring.

## Team Members

- Nazerke @nazhmdt
- Inzhu @InzhuNurlan

## Professor
- Muhamed Ali Ibrahim

## Project Overview

Retail companies need accurate demand forecasting, strong inventory planning, and efficient logistics operations. If demand is predicted incorrectly, the business may face stockouts, overstock, high transportation costs, or delivery delays.

This project builds an AI-driven retail supply chain intelligence system using Python and Power BI. Python is used for data cleaning, machine learning, forecasting, clustering, and risk analysis. Power BI is used to visualize the results and support business decision-making.

## Dataset

The project uses the Retail Dataset from Kaggle by Manjeet Singh.

Dataset source: https://www.kaggle.com/datasets/manjeetsingh/retaildataset

The original dataset includes three files:

- `sales data-set.csv` — weekly sales by store, department, date, and holiday status
- `Features data set.csv` — temperature, fuel price, markdowns, CPI, unemployment, and holiday status
- `stores data-set.csv` — store type and store size

After merging, the final dataset contains sales, store characteristics, economic indicators, markdown promotions, and time-based features.

## Important Note About Logistics Features

The original retail dataset does not include direct logistics variables such as shipping mode, warehouse, distance, traffic, supplier, route, or order priority.

To complete the required supply chain modules, proxy logistics features were created:

- Store groups were used to create regions
- Regions were connected to warehouses
- Store type was used as a proxy for shipping mode
- Weekly sales level was used to define order priority
- Fuel price, holiday status, and sales pressure were used to estimate traffic index
- Distance, fuel price, and traffic index were used to estimate transportation cost and lead time

This approach allowed us to build delivery delay prediction, supplier analytics, transportation analytics, and supply chain risk analysis.

## Project Tasks

### Task 1: Data Cleaning

The three datasets were loaded, checked, cleaned, and merged. Missing markdown values were replaced with 0, while missing CPI and unemployment values were filled with median values. Additional time-based and business features were created.

### Task 2: Exploratory Data Analysis

EDA was used to analyze weekly sales trends, yearly and monthly sales, holiday impact, store type performance, top stores, top departments, correlations, and outliers.

### Task 3: Demand Forecasting

Four forecasting methods were applied:

- Linear Regression
- Random Forest Regressor
- ARIMA
- Prophet

Random Forest Regressor performed the best for weekly sales prediction. ARIMA and Prophet were used for monthly sales forecasting and future inventory planning.

### Task 4: Delivery Delay Prediction

A delivery delay prediction module was built using proxy logistics features. The target variable was created using the logistic probability formula.

Models used:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

The module produced delay probabilities, high-risk route identification, and delivery performance insights.

### Task 5: Inventory Optimization

Inventory optimization was completed using:

- ABC Analysis
- K-Means Clustering
- Overstock and understock detection
- Reorder point recommendations

Departments were used as product categories because the dataset does not include direct product-level stock quantities.

### Task 6: Supplier and Transportation Analytics

Supplier and transportation performance were analyzed using proxy supply chain variables. Warehouses were treated as suppliers or distribution partners.

The module produced:

- Supplier rankings
- Lead time analysis
- Transportation cost analysis
- Route efficiency analysis
- Fuel and delay trends
- Logistics bottleneck identification
- Supply chain risk analysis

## Tools and Libraries

| Category | Tools / Libraries |
|---|---|
| Data Processing | pandas, numpy |
| Visualization | matplotlib, seaborn |
| Machine Learning | scikit-learn |
| Forecasting | statsmodels ARIMA, Prophet |
| Dashboard | Microsoft Power BI |
| Version Control | GitHub |

## Repository Structure

```text
.
├── README.md
├── retail-supply-chain-ai-project_Inzhu_Nazerke.ipynb
├── FP_logistics_Nazerke_Inzhu_presentation.pdf
├── dashboard.pdf
├── screenshots_InzhuNazerke.pdf
├── powerbi_main_retail_data.csv
├── powerbi_forecasting_data.csv
├── powerbi_logistics_data.csv
├── powerbi_inventory_supplier_data.csv
├── optional_powerbi_supplier_summary.csv
├── optional_powerbi_route_summary.csv
├── Features data set.csv
├── sales data-set.csv
└── stores data-set.csv
```

## Power BI Files

The main Power BI-ready files are:

- `powerbi_main_retail_data.csv`
- `powerbi_forecasting_data.csv`
- `powerbi_logistics_data.csv`
- `powerbi_inventory_supplier_data.csv`

Optional files:

- `optional_powerbi_supplier_summary.csv`
- `optional_powerbi_route_summary.csv`

These files were created from the Python notebook and used to build the Power BI dashboard.

## Key Results

- Sales show clear seasonal patterns and increase during holiday periods.
- Store Type A generates the highest total sales.
- Random Forest Regressor achieved the strongest weekly sales forecasting performance.
- Department, store size, store number, week, and CPI were important demand forecasting features.
- Delivery delay risk increases with high traffic index, fuel price, holiday weeks, distance, and sales pressure.
- ABC Analysis showed that Category A departments generate the majority of total sales.
- K-Means Clustering grouped departments by sales, demand volatility, store coverage, and markdown behavior.
- Warehouse_E had the highest supplier reliability score.
- West and South routes showed higher transportation cost and supply chain risk.

## Business Recommendations

- Use Random Forest for weekly demand forecasting because retail demand is non-linear.
- Monitor Category A departments weekly and maintain enough safety stock.
- Prepare additional inventory and transportation capacity before holiday periods.
- Monitor high-risk routes with high fuel price, traffic pressure, and long distance.
- Review Warehouse_S and Warehouse_W routes because they show higher risk.
- Use Power BI dashboards to track sales, forecasted demand, inventory status, delay risk, supplier reliability, and transportation bottlenecks.

## How to Run the Project

1. Download the original Kaggle dataset.
2. Open the notebook file: `retail-supply-chain-ai-project_Inzhu_Nazerke.ipynb`
3. Run all cells from top to bottom.
4. The notebook will clean the data, train models, generate outputs, and export Power BI-ready CSV files.
5. Open Power BI and load the exported CSV files.
6. Build dashboard pages using the prepared data.

## Project Outputs

The project includes:

- Cleaned and merged dataset
- EDA charts and insights
- Demand forecasting models
- Delivery delay prediction models
- Inventory optimization results
- Supplier and transportation analytics
- Power BI-ready CSV files
- Power BI dashboard
- Presentation file
- Screenshots file

## Conclusion

This project developed an AI-driven smart retail supply chain intelligence system using a retail sales dataset from Kaggle. The system combines Python-based machine learning and Power BI dashboards to support demand forecasting, inventory planning, delivery risk control, supplier ranking, and transportation cost optimization.

Although some logistics variables were not directly available in the original dataset, proxy features were created to complete the required supply chain analytics modules.
