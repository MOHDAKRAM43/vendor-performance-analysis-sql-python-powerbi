
# 📰 Vendor Performance Analysis - Retail Inventory & Sales

_Analyzing vendor efficiency and profitability to support strategic and inventory decisions using SQL, Python, and Power BI._

---

## 📌 Table of Contents
- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#research-questions--key-findings">Research Questions & Key Findings</a>
- <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
- <a href="#dashboard">Dashboard</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#final-recommendation">Final Recommendations</a>
- <a href="#author--contact">Author & Contact</a>

---
<h2><a class="anchor" id="overview"></a>Overview</h2>

This project evaluates vendor performance and retail inventory dynamics to drive strategic insights for purchasing, pricing, and inventory optimization. A complete data pipeline was built using SQL for ETL, Python for analysis and hypothesis testing, and Power BI for visualization.

---
<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Effective inventory and sales management are critical in the retail sector. This project aims to:
- Identify underperforming brands needing pricing or promotional adjustments.
- Determine vendor contributions to sales and profits.
- Analyze the cost-benefit of bulk purchasing.
- Investigate inventory turnover inefficiencies.
- Statistically validate differences in vendor profitability.

---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- Multiple CSV files located in `/vendor performane/` folder (sales, vendors, inventory)
- Summary table created from ingested data and used for analysis

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- SQL (Commmon Table Expressions, Joins, Filtering)
- Python (Pandas, Matplotlib, Seaborn, SciPy)
- Power BI (Interactive Visualizations)
- GitHub

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
vendor-performance-analysis/
├─ images/
│  └─ Screenshot 2025-11-14 001540.png
├─ README.md
|
|-- .gitignore
|-- requirements.txt
|-- Vendor Performance Report.pdf
|
|-- notebooks/                   #Jupyter notebooks
|   |-- exploratory_data_analysis.ipynb
|   |-- vendor_performance_analysis.ipynb
|
| scripts/                       # Python scripts for ingestion and processing
|   |-- ingestion_db.py
|   |-- get_vendor_summary.py
|
|-- dashboard/                   # Power BI dashboard file
|   |-- vendor_performance_dashboard.pbix
```

---
<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2

- Removed transactions with:
  - Gross Profit <= 0
  - Profit Margin <= 0
  - Sales Quantity = 0
- Created summary tables with vendor-level metrics
- Converted data types, handled outliers, merged lookup tables

---
<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

**Negative or Zero Values Detected:**
- Gross Profit : Min -52,002.78 (loss-making sales)
- Profit Margin: Min -∞ (sales at zero or below cost)
- Unsold Inventory: Indicating slow-moving stock

**Outliers Identified:**
- High Freight Costs (up to 257k)
- Large Purchase/Actual Prices

**Correlation Analysis:**
- Weak between Purchase Price & Profit
- Strong between Purhase Qty & Sales Qty (0.999)
- Negative between Profit Margin & Sales Price (-0.179)

---
<h2><a class="anchor" id="research-questions--key--findings"></a>Research Questions & Key Findings</h2>

1. **Brands for Promotions: 198 brands with low sales but high profit margins
2. **Top Vendors**: Top 10 vendors = 65.69% of purchase - risk of over-reliance
3. **Bulk Purchasing Impacts**: 72% cost savings per unit in large orders
4. **Inventory Turnover**: $2.71M worth of unsold inventory
5. **Vendor Profitability**:
    - High Vendors: Mean Margin = 31.17%
    - Low Vendors: Mean Margin = 41.55%
6. **Hypothesis Testings**: Statistically significant difference in profit margins - distict vendor strategies

---
<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>

- Power BI Dashboard shows:
  - Vendor-wise Sales and Margins:
  - Inventory Turnover
  - Bulk Purchase Savings
  - Performance Heatmaps

![Project Screenshot](images/Screenshot%202025-11-14%20001540.png)


---
<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Clone the Repository:
```bash
git clone https://github.com/MOHDAKRAM43/vendor-performance-analysis-sql-python-powerbi.git
```
2. Load the CSVs and ingest into databases:
```bash
python scripts/ingestion_db.py
```
3. Create vendor summary table:
```bash
python scripts/get_vendor_summary.py
```
4. Open and run notebooks:
   - `notebooks/exploratory_data_analysis.ipynb`
   - `notebooks/vendor_performance_analysis.ipynb`
5. Open power BI Dashboard:
   -`dashboad/vendor_performance_dashoard.pbix`

---
<h2><a class="anchor" id="final-recommendation"></a>Final Recommendation</h2>

- Diversity vendor base to reduce risk
- Optimize bulk order strategies
- Reprice slow-moving, high-margin brands
- Clear unsold inventory strategically
- Improve marketing for underproviding vendors

---
<h2><a class="amchor" id="author--contact"></a>Authorr & Contact</h2>

**Mohd Akram**
Data Analyst
✉ Email: imakram7860@gmail.com
in🔵🔗 [LinkedIn] (https://www.linkedin.com/in/mohd-akram-6a210a259/) 


  