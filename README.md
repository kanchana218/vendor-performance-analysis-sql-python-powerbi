# Vendor Performance Analysis Retail Inventory amd Sales
_ Analyzing vendor efficiency and profitability to support strategic purchasing and inventory decision using SQL,Python, and power BI

---

## Table of contents
- <a href="#overview">Overview</a>
- <a href="#busness-problem">Business Problem</a>
- <a href="#datasets">Dataset</a>
- <a href="#tools--technologies">Tools and Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
- <a href="#research- questions--key-findings">Research Questions and Key Findings</a>
- <a href="#dashboard">Dashboard</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#author--contacts"> Author & Contacts</a>

---
<h2><a class="anchor" id="overview"></a>Overview</h2>
This project evaluates vendor Performance and retail inventory dynamics to drive strategic insights for purschasing,pricing and inventory optimization .
A complete data pipeline was built using sql for ETL,
Python for Analysis and hypothesis and testing and power BI for visualization.

---
<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Effective inventory and sales management are critical in the retail sector. 
This project aims to:

- Identify uderperforming brands needing pricing or promotional adjustments

- Determine vendor contributions to sales and profits

- Analyze the cost-benifit of bulk purchase

- Investigate inventory turnover inefficiencies
- Statistically validate differences in vendor profitability


---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- Multiple csv files located in '/data/' folder (sales,vendor,inventory)

- Summary table created from ingested data and used for analysis


---

<h2><a class="anchor" id ="tools--technologies"></a>Tools & Technologies</h2>

- SQL (Common Table Expressions,Joins,Filtering)

- Python (Pandas,Matplotlib,seaborn,scipy)

- Power BI(Interactive Visualization)

- Github

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>


vendor-perfomance-analysis/

│

├── README.md

├── .gitignore

├── requirements.txt

│ Vendor Performance Report.pdf

│

├── notebooks/ # Jupyter notebooks

│ ├── exploratory_data_analysis.ipynb

│ └── vendor_performance_analysis.ipynb

│

├── scripts/ # Python scripts for ingestion and processing

│ ├── ingestion_db.py

│ └── get_vendor_summaryy1.py

│

├── Dashboard/ # Power BI dashboard file

│ └── Vendor_Performance_Report.pbix


---
<h2><a class ="anchor" id="data-cleaning--preparation"></a> Data Cleaning &Preparation</h2>

- Removed transactions with:
  - Gross Profit ≤ 0
  - Profit Margin ≤ 0
  - Sales Quantity = 0
- Created summary tables with vendor-level metrices
- Converted data types,handled outliers,merged lookup tables

---

<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

**Negative or Zero values Detected:**
- Gross Profit:Min -52,002.78(loss-making sales)
- Profit margin: Min -∞ (sales at zero or below cost)
- Unsold Inventory: Indicating slow-moving stock

**Outlier Identified:**
- High freight Cost (up to 257k)
- Large Purchase/Actual Prices

**Correlation Analysis:**
- Weak between Purchase Price & Profit
- Strong Between Purchase Qty & Sales Qty (0.999)
- Negative between Profit Margin & Sales Price (-0.179)


---

<h2><a class ="anchor" id="research-questions--key-findings"></a> Research Questions & Key Findings</h2>

1. **Brands for Promotions**: 198 brands with low sales but high profit margins

2. **Top vendors**: Top 10 vendors = 65.69% of purchases - risk of over-reliance

3. **Bulk Purchasing Impact**: 72% cost savings per unit in large orders

4. **Inventory Turnover**: $2.71M worth of unsold inventory

5. **Vendor Profitability**:
    - High Vendors: Mean Margin = 31.17%
    - Low Vendors: Mean Margin = 41.55%
6. **Hypothesis Testing**:Statistically significant difference in profit margins - distinct vendor strategies


---

<h2><a class="anchor" id ="dashboard"></a>Dashboard</h2>

- Power BI Dashboard shows:
  - Vendor-wise Sales and margins
  - Inventory Turnover
  - Bulk Purchase savings
  - Performance Heatmaps

![Vendor Performance Dashboard] (images/vendor_performance_dashboard.png)

---

<h2><a class="anchor" id="how-to-run-this-project"<</a>How to Run This Project</h2>

1. Clone the repository:

'''bash

git clone  https://github.com/kanchana218/vendor-performance-analysis-sql-python-powerbi.git
'''

3. Load the csvs and ingest into database:
'''bash
python scripts/ingestion_db.py
'''
4. Create vendor summary table:
'''bash
python scripts/get_vendor_summaryy1.py
'''
5. Open and run notebooks:
    - 'notebooks/exploratory_data_analysis.ipynb'
    - 'notebooks/vendor_performance_analysis.ipynb'
6. Open Power BI Dashboard:
    - 'dashboard/vendor_performance_dashboard.pbix'

---
<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>

- Diversify vendor base to reduce risk
- Optimize bulk order strategies
- Reprice slow-moving,high-margin brands
- Clear unsold inventory strategically 
- improve marketing for underperforming vendors

---
<h2><a class="anchor" id="author--contacts"></a>Author & Contact</h2>

**Kanchana Kinnera**

Data Analyst

Email: a.kanchana.218@gmail.com

[linkedIn] (www.linkedin.com/in/kanchana-kinnera-3996ab59)










