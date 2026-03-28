
Sales Performance Dashboard using Python and Power BI
# Sales Performance Dashboard — Superstore Dataset

## Project Overview
An end-to-end data analysis project exploring sales trends, regional performance,
and profitability insights for a retail superstore. The project covers the full
analyst workflow: from raw data ingestion and cleaning in Python, through
exploratory analysis, to an interactive Power BI dashboard.



## Tools & Technologies
| Tool | Purpose |
|------|---------|
| Python (Pandas, Matplotlib, Seaborn) | Data cleaning & exploratory analysis |
| Google Colab | Cloud-based development environment |
| Power BI Desktop | Interactive dashboard & visualization |
| GitHub | Version control & portfolio sharing |



## Dataset
- **Source**: Sample Superstore Dataset (Kaggle)
- **File**: `Sample - Superstore.csv`
- **Records**: ~10,000 orders
- **Period**: 2014 – 2017
- **Fields**: Order Date, Region, Category, Sub-Category, Sales, Profit, Discount, Shipping Days, and more



#Full Project Process

# Step 1 — Data Loading
Loaded the raw CSV file directly in Google Colab using Pandas:
```python
df = pd.read_csv("/content/sample_data/Sample - Superstore.csv", encoding="latin-1")

Initial inspection revealed the dataset had 9,994 rows and 21 columns.



#Step 2 — Data Cleaning
Performed the following cleaning steps using Pandas:

- Converted `Order Date` and `Ship Date` columns to datetime format
- Stripped and standardized text columns (Region, Category, Segment, Ship Mode)
- Removed duplicate rows
- Dropped rows with missing values in critical columns (Sales, Profit, Order Date)
- Renamed all columns to lowercase with underscores for consistency



#Step 3 — Feature Engineering
Created the following new columns to enrich the analysis:

| New Column | Description |
|------------|-------------|
| `Order Month` | Month extracted from Order Date |
| `Order Year` | Year extracted from Order Date |
| `Order Quarter` | Quarter (Q1–Q4) from Order Date |
| `Shipping Days` | Days between Order Date and Ship Date |
| `Profit Margin` | Profit divided by Sales |

---

#Step 4 — Exploratory Analysis in Python
Generated 5 visualizations in Google Colab using Matplotlib and Seaborn:

1. Monthly Sales Trend** — Line chart showing revenue over time
2. Sales by Region** — Horizontal bar chart comparing 4 regions
3. Sales vs Profit by Category** — Grouped bar chart for 3 categories
4. Discount vs Profit** — Scatter plot showing impact of discounts
5. Top 10 Products by Revenue** — Bar chart of best performing products



#Step 5 — Key Business Metrics
Computed summary KPIs from the clean dataset:

| Metric | Value |
|--------|-------|
| Total Revenue | $2.30M |
| Total Profit | $286.40K |
| Avg Profit Margin | ~12% |
| Avg Shipping Days | 3.9 days |

---

# Step 6 — Power BI Dashboard
Imported `superstore_clean.csv` into Power BI Desktop and built an interactive dashboard containing:

KPI Cards** — Total Revenue ($2.30M) and Total Profit ($286.40K)
Line Chart** — Sum of Sales by Month (seasonal trend visible)
Bar Chart** — Sum of Sales by Region (West leads at ~$0.5M)
Scatter Chart** — Sum of Discount vs Sum of Profit by Category
Bar Chart** — Top Products by Sales (Canon, Fellowes, Cisco lead)
Donut Chart** — Sales by Category (Technology 36.4%, Office Supplies 32.3%, Furniture 31.3%)

Applied a custom theme for consistent professional styling across all visuals.

---

## Dashboard Preview
![Dashboard](dashboard_screenshot.png)

---

## Key Business Insights
1. **Q4 drives the highest monthly sales** — inventory and marketing should be prioritized ahead of the holiday season
2. **Discounts above 30% consistently produce negative profit** — especially in the Furniture category
3. **The West region leads all others in revenue** — its strategies could be studied and replicated in the underperforming South region
4. **Technology has the strongest profit margin** despite similar sales volume to Furniture
5. **Canon imageCLASS is the top revenue-generating product** across all years

---

## Repository Structure
```
superstore-sales-analysis/
├── superstore_analysis.ipynb   # Google Colab notebook (cleaning + EDA)
├── superstore_clean.csv        # Cleaned dataset exported from Python
├── Sales_Dashboard.pbix        # Power BI dashboard file
├── dashboard_screenshot.png    # Dashboard preview image
└── README.md                   # Project documentation
```

---

<img width="757" height="414" alt="image" src="https://github.com/user-attachments/assets/fad90d0c-ed45-444c-a988-a5ffc898bd33" />














<img width="759" height="454" alt="image" src="https://github.com/user-attachments/assets/1f024988-fcc6-4707-860c-c1bd8736a3c1" />

