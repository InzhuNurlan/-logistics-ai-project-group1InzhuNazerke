# -logistics-ai-project-group1InzhuNazerke
 AI-Driven Smart Retail Supply Chain Intelligence System
An end-to-end machine learning project that transforms Walmart retail sales data into actionable supply chain intelligence — covering demand forecasting, delivery delay prediction, inventory optimization, supplier ranking, and transportation risk analysis.

👥 Group Members

Inzhu
Nazerke


📦 Dataset
Walmart Recruiting - Store Sales Forecasting Dataset
Source: https://www.kaggle.com/datasets/manjeetsingh/retaildataset
The project uses three interconnected files:

sales data-set.csv — historical weekly sales by store and department (45 stores, 2010–2012)
Features data set.csv — external factors per store and week (temperature, fuel price, CPI, unemployment, holiday flag, markdown promotions)
stores data-set.csv — store type (A, B, C) and store size in square feet

 Tools & Libraries
CategoryLibrariesData processingpandas, numpyVisualizationmatplotlib, seabornMachine Learningscikit-learn (LinearRegression, LogisticRegression, RandomForestRegressor, RandomForestClassifier, KMeans)Time Seriesstatsmodels (ARIMA), prophetEnvironmentJupyter Notebook, Python 3DashboardMicrosoft Power BI

 Folder Structure
retail-supply-chain-ai-project/
│
├── retail-supply-chain-ai-project_Inzhu_Nazerke.ipynb   # Main analysis notebook
│
├── data/
│   ├── sales data-set.csv                               # Raw weekly sales data
│   ├── Features data set.csv                            # Raw external features
│   └── stores data-set.csv                              # Raw store metadata
│
├── outputs/
│   ├── cleaned_retail_supply_chain_data.csv             # Cleaned & merged dataset
│   ├── powerbi_main_retail_data.csv                     # Power BI: sales & EDA
│   ├── powerbi_forecasting_data.csv                     # Power BI: demand forecast
│   ├── powerbi_logistics_data.csv                       # Power BI: delivery delays
│   ├── powerbi_inventory_supplier_data.csv              # Power BI: inventory & ABC
│   ├── optional_powerbi_supplier_summary.csv            # Supplier reliability ranking
│   └── optional_powerbi_route_summary.csv               # Route cost & efficiency
│
├── dashboard/
│   └── supply_chain_dashboard.pbix                      # Power BI dashboard file
│
└── README.md

 How to Run the Notebook

Clone or download this repository to your local machine.
Install the required libraries by running:

bash   pip install pandas numpy matplotlib seaborn scikit-learn statsmodels prophet

Place the raw data files (sales data-set.csv, Features data set.csv, stores data-set.csv) in the same directory as the notebook, or inside a data/ subfolder (update the file paths in the notebook if needed).
Open the notebook:

bash   jupyter notebook retail-supply-chain-ai-project_Inzhu_Nazerke.ipynb

Run all cells from top to bottom using Kernel → Restart & Run All.
The notebook will generate cleaned data files and Power BI-ready CSV exports automatically.


 Prophet may require separate installation on some systems: pip install neuralprophet or follow the Prophet installation guide.


 Project Structure & Analysis Modules
The notebook is organized into six analytical tasks:
TaskDescriptionTask 1Data loading, cleaning, merging, and feature engineeringTask 2Exploratory Data Analysis — sales trends, store types, holiday impact, correlationsTask 3Demand forecasting — Linear Regression, Random Forest, ARIMA, ProphetTask 4Delivery delay prediction — Logistic Regression, Random Forest ClassifierTask 5Inventory optimization — ABC Analysis, KMeans clustering, safety stock calculationTask 6Supplier & transportation analytics — route efficiency, risk scoring, bottleneck identification

 Key Business Insights
1.  Sales Are Seasonal — Prepare Before Peak Periods
Sales increase significantly during holiday periods. The company should prepare additional inventory and logistics capacity before high-demand weeks to avoid stockouts and delivery pressure.
2.  Random Forest Is the Strongest Forecasting Model
Random Forest Regressor significantly outperforms Linear Regression for weekly demand prediction. This confirms that retail demand follows non-linear patterns that simple regression models cannot fully capture. Machine learning is essential for accurate forecasting.
3.  Category A Departments Drive Most Revenue
ABC Analysis shows that Category A departments generate the majority of total sales. These departments should receive priority in replenishment planning and safety stock management to prevent revenue loss from stockouts.
4.  Delivery Delay Risk Peaks Under Multiple Pressure Factors
Delay risk is highest during weeks with high traffic, high fuel prices, holiday periods, long-distance routes, and critical priority orders. The predictive model can flag high-risk deliveries in advance, enabling preventive logistics action.
5.  West and South Routes Are the Costliest and Riskiest
West and South regions have the highest transportation costs and supply chain risk scores, especially with Same Day and Second Class shipping. These routes require focused cost optimization and logistics planning.

 Power BI Dashboard
 
