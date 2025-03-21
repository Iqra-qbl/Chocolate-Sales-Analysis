
<<<<<<< HEAD

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

=======
# CHOCOLATE SALES ANALYSIS

Advanced Chocolate Sales Analytics project is a comprehensive data analysis tool designed to streamline the exploration, analysis, and visualization of chocolate sales data. Built for business intelligence and decision-making, this tool enables users to uncover sales trends, forecast demand, and optimize pricing strategies.

# ![Chocolate photo](images/choco3.png)


## Dataset Content

Datasets are taken from Kaggle.

https://www.kaggle.com/datasets/atharvasoundankar/chocolate-sales

Columns & Description:

Date-------------The transaction date of the chocolate sale.
Product Name-----Name of the chocolate product sold.
Category---------Type of chocolate (Dark, Milk, White).
Quantity Sold----Number of chocolate units sold in the transaction.
Revenue----------Total revenue generated from the sale.
Customer Segment-Type of customer (Retail, Wholesale).
Location---------Sales region or store location where the transaction took place.


## Business Requirements

Business Requirements for Chocolate Sales Analysis

1. Objective

The goal of this analysis is to understand factors affecting chocolate sales and optimize business strategies for increasing revenue, improving sales efficiency, and enhancing customer targeting.

2. Key Business Questions

What factors influence chocolate sales the most? (e.g., seasonality, region, product type)
Which products generate the highest revenue per sale?
Do certain salespeople outperform others, and why?
How do discounts or bulk shipments affect sales?
Are there regional differences in chocolate sales?

3. Business KPIs (Key Performance Indicators)

Total Sales Revenue – Measure of overall performance.
Average Revenue per Box Shipped – Indicates profitability per shipment.
Sales Growth Over Time – Month-over-month or year-over-year comparison.
Sales Performance by Country – Identifies high-performing regions.
Product Performance Analysis – Determines best-selling and most profitable products.
Salesperson Performance – Evaluates top-performing employees.

4. Data Requirements

Sales Data (Salesperson, Country, Product, Date, Amount, Boxes Shipped).
Timeframe Consideration – Seasonality trends based on monthly/quarterly data.
Customer Demographics (if available) – To analyze purchasing behavior.

5. Expected Deliverables

Sales Trends Analysis Report – Identifying peak sales periods and seasonality effects.
Product Performance Dashboard – Highlighting top-selling and high-revenue products.
Salesperson Performance Report – Comparing efficiency across different employees.
Revenue Optimization Strategy – Recommendations for improving profitability.





## Hypothesis and how to validate?
* List here your project hypothesis(es) and how you envision validating it (them) 

## Project Plan
* Outline the high-level steps taken for the analysis.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* Thank the people who provided support through this project.
>>>>>>> e87da7e10b56c0025689ce7238998ba67e4aa902
