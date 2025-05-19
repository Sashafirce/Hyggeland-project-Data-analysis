# ![HYGGELAND logo](Hyggeland_Logo.png)

# **HYGGELAND Project "Minimal, Meaningful, where Hygge meet sustainability"** 
HYGGELAND Project involves analysing Data for Hyggeland to assess customers' behaviour, identify popular products to optimise pricing, and marketing strategies to improve sales. 
 
## **Dataset content**
The content of the HYGGELAND dataset is csv file which include data on products purchased, quantities, transaction dates and times of customers' purchases, prices of the products, customers' identifiers, and customers locations.

## **Business Requirements**
The HYGGELAND company has hired Sasha Firce, a Junior Data Analyst, to understand their customers' behaviour  and to optimise the prices. They want me to analyse their collected data to implement new marketing strategies in order to increase the sales.

## **Hypothesis and how to validate?**
1. Hypothesis:

“Cheaper products are responsible for the majority of revenue due to their high sales volume.”
 
 Validation Plan:

    - Group by description and compute: avg_unit_price, total_quantity, and total_revenue

    - Create scatterplot of avg_unit_price vs total_revenue

    - Segment into price tiers (cheap ≤ £4.13, premium > £4.13)

    - Compare revenue share by segment

✅ Confirmed: The analysis showed that all top 10 most sold products are priced below the premium threshold (£4.13). The average price of cheap products was £1.81, and they dominate sales volume. Histogram and scatterplot showed a concentration of demand at lower price points.

 2. Hypothesis:

“Most of Hyggeland’s revenue comes from a small set of top products (Pareto Principle).”

 Validation Plan:

    - Group by description and compute total_revenue

    - Rank by descending revenue and calculate cumulative revenue %

    - Plot Pareto chart (Step 49)

✅ Confirmed:The Pareto chart (Step 49) demonstrated that ~20% of products generate ~80% of total revenue. This confirms the 80/20 rule applies to your product line and suggests a core catalogue strategy is viable.

3. Hypothesis:

“Customers in high-income countries are willing to pay more per unit on average.”
 
 Validation Plan:

    - Group by country and calculate avg_unit_price

    - Compare top 10 countries by avg_unit_price and revenue (Step 50)

    - Cross-check with known income levels or cost-of-living indexes

✅ Confirmed:Bar chart of average unit price by country (Step 50) shows countries like Switzerland and Australia have higher avg. prices. UK shows high volume but lower avg. prices — matching expected cost-of-living patterns.   

 4. Hypothesis:

“There is a seasonal pattern in sales — most sales occur in Q4.”
 
 Validation Plan:

    - Use  of the quarter column to group and aggregate total_revenue

    - Plot quarterly sales trend using Plotly

    - Look for repeated Q4 spikes

✅ Confirmed: The Plotly quarterly and monthly trend charts indicate a sales spike in Q4 (Oct–Dec). This aligns with Holidays (Christmas) and end-of-year consumer behaviour patterns.

## **Project Plan**
1. High-Level Steps:

    - Data Collection: Used the Online Retail dataset (Excel format).

    - Data Cleaning: Removed nulls, fixed dtypes, filtered invalid entries (e.g., negative quantities).

    - Data Processing: Created derived fields like total_price, month, gross_profit.

    - Exploratory Analysis: Used descriptive statistics, segmentation, Pareto analysis.

    - Visualisation: Created histograms, bar charts, scatterplots, heatmaps, line trends (Seaborn + Plotly).

    - Pricing Analysis: Estimated price elasticity and customer value metrics.

2. Data Management Approach:

    - Centralised the cleaned dataset in a dedicated Input/ folder.

    - Maintained reproducibility using Jupyter Notebooks.

    - Tracked all code versions via GitHub (version control).

    - Used .venv for package isolation.

3.  Methodology Rationale:

    - Focused on descriptive and diagnostic analytics to identify high-impact areas.

    - Pricing elasticity and segmentation were used to uncover patterns in behaviour.

    - Chose Seaborn for static insights and Plotly for stakeholder-friendly interactivity.

## **Mapping Business Requirements to Data Visualisations**

| Business Requirement                          | Mapped Visualisation                            | Rationale                                                                 |
|----------------------------------------------|--------------------------------------------------|---------------------------------------------------------------------------|
| Identify top-selling products                | Bar chart (Top 10 products: quantity & avg price)| Highlights bestsellers and distinguishes premium vs. cheap using colour. |
| Understand seasonal demand trends            | Quarterly/Monthly line trend (Plotly)            | Reveals peak shopping periods (e.g. Q4) to inform marketing and inventory.|
| Segment products by performance              | Scatterplot (avg price vs quantity, hue=segment) | Categorises SKUs into segments (e.g. Bestseller, Dead Stock).             |
| Discover regional pricing potential          | Heatmap and Choropleth map                       | Highlights high-spend countries for geo-pricing strategies.               |
| Reveal revenue concentration                 | Pareto chart                                     | Identifies which products contribute most to total revenue.               |
| Assess price sensitivity                     | Regression model + Demand curve                  | Measures elasticity and guides pricing strategy.                          |
| Monitor profitability vs. revenue            | Profitability scatterplot                        | Helps balance revenue with profit margin insights.                        |
| Track pricing trends over time               | Line plot (monthly price & margin)               | Detects price patterns for pricing lifecycle decisions.                   |


## **Analysis Techniques Used**

1. Methods Used:

    - Descriptive statistics (.describe(), visual summaries)

    - Segmentation (rule-based: quantity, avg_price, revenue)

    - Revenue concentration (Pareto analysis)

    - Time-series trend analysis

    - Linear regression (OLS for elasticity)

    - Visual analytics (Seaborn, Plotly)

2. Limitations & Alternatives:

    - Limited price variation for elasticity led to weak regression power. Could expand via synthetic price testing or A/B tests.

    - No gender data meant customer segmentation was limited. Inferred behaviour via spend, quantity, and region instead.

3.  Structure Justification:

    - Prioritised data cleaning first, then layered in EDA → segmentation → pricing insights → strategy.

    - Used a jupyter notebook format for clarity with the coding.

    - The step-by-step build-up made it possible to make changes right away based on what was found.

4. Use of Generative AI:

    - AI supported: Code debugging and optimisation (e.g., visual tweaks, seaborn vs plotly conversion), and the interpretation based on output of elasticity.


## **Ethical considerations**
• There were no issues with customers privacy since all of them were identified by a code number. One disadvantage is that make more difficult to do a customer segmentation by gender, age, or sex.

## **Development Roadmap**
• Internet conection
• Struggles with time management.
## **Main Data Analysis Libraries**
•	Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.
## Credits
• https://www.w3schools.com/python/pandas/pandas_analyzing.asp It helped me to understand and learn how to do the data analysis properly.
• https://copilot.microsoft.com/chats/NdbvxkFKX1cA4RBrX4jtu I used it specificaly log and syntax errors
• https://www.markdownguide.org/basic-syntax/ I needed to write the README document.

## **Media**
•The images used for  the present document was created with Canvas.

## **Acknowledgements**
•Thank the people who provided support through this project, especially Emma and Mark always patient and ready to help me any time.

•"Last but not least, I wanna thank me,
 I wanna thank me for believing in me
I wanna thank me for doing all this hard work, 
I wanna thank me for having no days off,
I wanna thank me for, for never quitting."
