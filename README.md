# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


---

# Chocolate Sales Analysis Project

**Chocolate Sales Analysis** is a comprehensive data analysis project designed to explore, analyze, and visualize chocolate sales data across multiple countries. Built using Python and various data analysis libraries, this project provides insights into sales trends, product performance, and regional demand through intuitive visualizations and statistical analysis. The dataset is sourced from Kaggle (link provided below) and is of a reasonable size, well under the 100GB repository limit.

---

## Dataset Content

The dataset used in this project is the **Chocolate Sales Dataset** from Kaggle:  
[https://www.kaggle.com/datasets/atharvasoundankar/chocolate-sales](https://www.kaggle.com/datasets/atharvasoundankar/chocolate-sales)  

It contains detailed records of chocolate sales transactions, including:  
- **Amount**: Sales revenue in dollars  
- **Boxes Shipped**: Number of chocolate boxes shipped per transaction  
- **Country**: Six countries (Australia, Canada, India, New Zealand, UK, USA)  
- **Product**: Specific chocolate products (e.g., Smooth Silky Salty, 50% Dark Bites)  
- **Date**: Transaction dates spanning 2022  
- **Salesperson**: Names of salespeople (removed during cleaning)  

The dataset is relatively clean with no missing, empty, or duplicate values, making it suitable for analysis after minor preprocessing.

---

## Business Requirements

1. **Understand Sales Distribution**: Identify total sales and percentage contributions by country and product category.  
2. **Identify Top Performers**: Determine the top-selling products and countries driving revenue.  
3. **Analyze Efficiency**: Calculate revenue per box shipped to assess profitability across products and categories.  
4. **Explore Trends**: Investigate sales trends over time, focusing on seasonality and holiday impacts.  
5. **Visualize Insights**: Provide clear, actionable visualizations for stakeholders to understand key findings.

---

## Hypotheses and Validation

1. **H1: Sales follow seasonal trends, with higher revenue during peak holiday months.**  
   - **Validation**: Analyze monthly sales trends (e.g., January vs. February) using line charts and heatmaps.  
   - **Key Insight**: Holiday-driven sales spikes (e.g., January peak at $896,105).  

2. **H2: Certain countries have higher chocolate sales, and sales amount correlates with boxes shipped.**  
   - **Validation**: Compare total sales and boxes shipped per country using choropleth maps and bubble charts.  
   - **Key Insight**: Australia leads with $1,137,367, but correlation between sales and boxes shipped is weak (-0.0188).  

3. **H3: Premium chocolate products generate higher revenue per box shipped.**  
   - **Validation**: Calculate revenue per box shipped and visualize with box plots and stacked bar charts.  
   - **Key Insight**: Premium products like Smooth Silky Salty show higher efficiency.  

4. **H4: Some chocolate products drive revenue more efficiently than others, making them more profitable.**  
   - **Validation**: Assess sales and revenue per box shipped per product using bar and bubble charts.  
   - **Key Insight**: Smooth Silky Salty ($349,692) outperforms others in revenue and efficiency.

---

## Project Plan

1. **Data Collection**: Downloaded the dataset from Kaggle.  
2. **Data Processing**:  
   - Removed the "Salesperson" column (irrelevant to analysis).  
   - Converted "Amount" from string (with "$") to numeric data type.  
   - Standardized "Date" to YYYY-MM-DD format.  
   - Added columns: Day, Month Number, Month Name, Revenue per Box Shipped (Amount / Boxes Shipped).  
3. **Analysis**: Calculated total sales, percentages, trends, and efficiency metrics.  
4. **Visualization**: Created charts (e.g., bar, line, stacked bar) using Python libraries.  
5. **Interpretation**: Summarized key findings and validated hypotheses.

The data was managed using pandas for cleaning and analysis, ensuring consistency throughout the process. We chose these methodologies for their simplicity and effectiveness in handling structured data.

---

## Rationale for Mapping Business Requirements to Data Visualizations

- **Sales Distribution**: Treemap for percentage by country, bar chart for product category sales.  
  - *Rationale*: Highlights relative contributions clearly for stakeholders.  
- **Top Performers**: Bar chart for top 5 products and countries.  
  - *Rationale*: Simple and effective for ranking comparisons.  
- **Efficiency**: Stacked bar chart for revenue per box shipped by category.  
  - *Rationale*: Shows efficiency across dimensions.  
- **Trends**: Line chart for monthly sales trends.  
  - *Rationale*: Reveals temporal patterns intuitively.

---

## Analysis Techniques Used

- **Descriptive Statistics**: Calculated mean ($5,652.31), median ($4,868.50), min ($7), and max ($22,050) for sales.  
- **Correlation Analysis**: Computed Sales vs. Boxes Shipped correlation (-0.0188).  
- **Aggregation**: Summed sales by country, product, and category.  
- **Time Series Analysis**: Analyzed monthly sales trends.  

**Limitations**: The weak correlation limited insights into shipment efficiency. An alternative could be regression analysis to explore other variables (not present in the dataset). The data’s simplicity (no missing values) didn’t require advanced imputation techniques.

**Structure**: Techniques were applied sequentially—cleaning first, then descriptive stats, followed by visualizations—to build a logical flow. The dataset’s size and quality posed no significant limitations.

**Generative AI**: Used for ideation (e.g., suggesting visualization types) and code optimization (e.g., efficient pandas operations).

---

## Ethical Considerations

- **Data Privacy**: Salesperson names were removed to anonymize data, avoiding personal identification.  
- **Bias**: No evident bias in country or product data, though India’s high sales might reflect sampling bias (not explored further due to dataset limitations).  
- **Legal**: Dataset is publicly available on Kaggle under an open license, ensuring compliance.

---

## Dashboard Design

### Pages and Content
1. **Home**: Summary statistics (average sales, boxes shipped), key findings text block.  
2. **Sales by Country**: Choropleth map, treemap, top 5 countries bar chart.  
3. **Product Performance**: Bar chart (top 5 products), stacked bar (revenue per box).  
4. **Trends**: Line chart (monthly sales), heatmap (sales by month/day).  

**Communication**:  
- **Technical Audience**: Detailed stats and correlation insights in tables.  
- **Non-Technical Audience**: Simplified charts with annotations (e.g., "Australia leads with $1.14M").  

---

## Unfixed Bugs

- **Minor Rounding Error**: Revenue per box shipped occasionally shows slight discrepancies due to floating-point precision in Python. Left unfixed as it doesn’t impact insights significantly.  
- **Knowledge Gaps**: Initially unfamiliar with heatmap creation; resolved by studying Matplotlib/Seaborn documentation.

---

## Development Roadmap

- **Challenges**: Standardizing dates and handling weak correlations. Overcome by using pandas’ `to_datetime` and focusing on descriptive stats instead of predictive models.  
- **Next Steps**: Learn advanced visualization tools (e.g., Tableau) and time series forecasting techniques.

---

## Deployed on Tableau Public:

* Deployed with Tableau file Chocolate_sales_analysis.twbx in output folder.

* Steps:

1. Processed and cleaned the data using Python (pandas).
2. Exported the cleaned dataset as a CSV file.
3. Imported the CSV into Tableau Public.
4. Designed interactive dashboards with charts and filters as outlined in the Dashboard Design section.

Tableau was chosen for deployment due to its powerful visualization capabilities and ability to share interactive dashboards with a broad audience.

---

## Main Data Analysis Libraries

- **pandas**: Data cleaning, aggregation (e.g., `df.groupby('Country')['Amount'].sum()`).  
- **NumPy**: Statistical calculations (e.g., mean, std).  
- **Matplotlib/Seaborn**: Visualizations (e.g., bar charts, line plots).  

---

## Credits

### Content
- Dataset sourced from: [Kaggle Chocolate Sales Dataset](https://www.kaggle.com/datasets/atharvasoundankar/chocolate-sales).  
- Visualization ideas inspired by Seaborn documentation.  

### Media
- Icons for dashboard footer from [Font Awesome](https://fontawesome.com/).  

---

## Acknowledgements

Thanks to our team for collaborative efforts in data cleaning, analysis, and visualization design, and to xAI for providing Grok 3, which assisted with ideation and structuring this README.

---

