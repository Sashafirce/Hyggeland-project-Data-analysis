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

    -Group by description and compute: avg_unit_price, total_quantity, and total_revenue

    =Create scatterplot of avg_unit_price vs total_revenue

    -Segment into price tiers (cheap ≤ £4.13, premium > £4.13)

    -Compare revenue share by segment

✅ Confirmed : analysis showed that all top 10 most sold products are priced below the premium threshold (£4.13). The average price of cheap products was £1.81, and they dominate sales volume. Histogram and scatterplot showed a concentration of demand at lower price points.

 2. Hypothesis:

“Most of Hyggeland’s revenue comes from a small set of top products (Pareto Principle).”
 Validation Plan:

    -Group by description and compute total_revenue

    -Rank by descending revenue and calculate cumulative revenue %

    -Plot Pareto chart (Step 49)

✅ Confirmed:The Pareto chart (Step 49) demonstrated that ~20% of products generate ~80% of total revenue. This confirms the 80/20 rule applies to your product line and suggests a core catalogue strategy is viable.

3. Hypothesis:

“Customers in high-income countries are willing to pay more per unit on average.”
 Validation Plan:

    -Group by country and calculate avg_unit_price

    -Compare top 10 countries by avg_unit_price and revenue (Step 50)

    -Cross-check with known income levels or cost-of-living indexes

✅ Confirmed:Bar chart of average unit price by country (Step 50) shows countries like Switzerland and Australia have higher avg. prices. UK shows high volume but lower avg. prices — matching expected cost-of-living patterns.   

 4. Hypothesis:

“There is a seasonal pattern in sales — most sales occur in Q4.”
 Validation Plan:

    -Use quarter column to group and aggregate total_revenue

    -Plot quarterly sales trend using Plotly

    -Look for repeated Q4 spikes

✅ Confirmed if:Your Plotly quarterly and monthly trend charts indicate a sales spike in Q4 (Oct–Dec). This aligns with Holidays (Christmas) and end-of-year consumer behaviour patterns.

## **Project Plan**
•	Outline the high-level steps taken for the analysis.
•	How was the data managed throughout the collection, processing, analysis and interpretation steps?
•	Why did you choose the research methodologies you used?

## **The rationale to map the business requirements to the Data Visualisations**
•	List your business requirements and a rationale to map them to the Data Visualisations 

## **Analysis techniques used**
•	List the data analysis methods used and explain limitations or alternative approaches.
•	How did you structure the data analysis techniques. Justify your response.
•	Did the data limit you, and did you use an alternative approach to meet these challenges?
•	How did you use generative AI tools to help with ideation, design thinking and code optimisation?

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
•	The images used for  the present document was created with Canvas.

## **Acknowledgements**
•	Thank the people who provided support through this project, especially Emma and Mark always patient and ready to help me any time.
"Last but not least, I wanna thank me,
 I wanna thank me for believing in me
I wanna thank me for doing all this hard work, 
I wanna thank me for having no days off,
I wanna thank me for, for never quitting."
