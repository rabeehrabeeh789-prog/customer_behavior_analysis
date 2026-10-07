# Customer Shopping Behavior Analysis

This project takes a customer shopping dataset from raw CSV to an exploratory analysis, SQL investigation, and Power BI report. It looks at who is shopping, what they buy, how they pay and receive orders, and how discounts and subscriptions relate to purchasing behavior.

## What I did

- **Prepared the data in Python:** explored 3,900 customer purchase records across 18 fields, checked missing values, and filled missing review ratings with the median for each product category.
- **Created analysis-ready fields:** standardized column names, grouped customers into age bands, and translated purchase-frequency labels into approximate day intervals. The notebook also checks that `Promo Code Used` and `Discount Applied` contain the same values in this dataset, then removes the duplicate field.
- **Loaded the prepared data into MySQL:** the notebook uses SQLAlchemy and PyMySQL to write the data to a `customer` table for querying.
- **Investigated business questions in SQL:** compared revenue by gender and subscription status; examined discount use, reviews, shipping, repeat purchasing, customer segments, age groups, and popular items within categories.
- **Built a Power BI report** and prepared a written report and presentation to communicate the analysis.

## Questions explored

The SQL analysis includes queries to explore:

1. Revenue by gender.
2. Discounted purchases above the average purchase amount.
3. Products with the highest average review ratings.
4. Average spend for Standard versus Express shipping.
5. Average spend and total revenue for subscribers and non-subscribers.
6. Products with the highest share of discounted purchases.
7. New, Returning, and Loyal customer segments based on previous purchases.
8. The three most purchased items in each category.
9. Subscription status among repeat buyers with more than five previous purchases.
10. Revenue by age group.

These are questions the project investigates; the notebook, SQL, report, and Power BI file contain the analysis and its outputs.

## Dataset

`customer_shopping_behavior.csv` contains 3,900 records and 18 original columns, including age, gender, purchased item and category, purchase amount, location, season, review rating, subscription status, shipping type, discount use, previous purchases, payment method, and purchase frequency. The notebook derives `age_group` and `purchase_frequency_days` for analysis.

## Project files

| File | What it contains |
|---|---|
| `customer_shopping_behavior.csv` | Source shopping behavior dataset |
| `Customer_Shopping_Behavior_Analysis.ipynb` | Python data exploration, cleaning, feature preparation, and MySQL loading steps |
| `customer_behavior.sql` | SQL queries for the business questions above |
| `customer_behavior.pbix` | Power BI report |
| `Customer_Shopping_Behavior_Analysis_Report.pdf` | Written project report |
| `Customer_shopping_behavior_presentation.pptx` | Presentation of the project |

## How to explore the project

Start with the notebook to see how the data is prepared. Review the SQL file to see the analysis questions and query logic, then open the Power BI report for the visual view. The PDF report and presentation provide additional summaries.

To run the notebook, use Python with Jupyter and the packages imported in the notebook. The database-loading section expects a MySQL database and uses SQLAlchemy with PyMySQL. Open the `.pbix` file with Power BI Desktop. The SQL script expects the prepared data in a MySQL table named `customer`.

## License

Released under the MIT License. See [LICENSE](LICENSE).
