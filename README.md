# Online Retail & E-Commerce: Exploratory Data Analysis (Python)

Exploratory data analysis of a synthetic online retail dataset (1,000 orders) to find what drives sales and where a business could act.

**Author:** Mohamed Riduvan Azber

## Project Goal
- Identify which payment methods, age groups, and customers generate the most sales
- Check whether review scores relate to spending
- Find when sales peak
- Turn the findings into clear business recommendations

## Dataset
[Online Retail & E-Commerce Dataset (Kaggle)](https://www.kaggle.com/datasets/ertugrulesol/online-retail-data)

The data is **synthetic**. Columns include order date, quantity, price, payment method, city, review score, gender, and age.

## Tools
Python, pandas, NumPy, matplotlib, seaborn, Jupyter / Google Colab

## Process
1. **Cleaning:** converted `order_date` to datetime, checked duplicates (none found), filled missing review scores with the mean, and filled missing gender values
2. **Feature engineering:** created `total_sales` (price x quantity), year, month, weekday, and age groups
3. **Outlier check:** boxplots of price, quantity, and total sales
4. **Univariate and bivariate analysis:** distributions, sales by payment method, age group, review score, and city
5. **Time trend:** monthly and weekday sales
6. **Correlation:** heatmap of numeric columns
7. **Insights and recommendations**

## Key Findings
- Total sales: about **737K** across 1,000 orders (average order value 737, average review score 3.99)
- **Cash on Delivery** leads with 37% of sales
- Customers aged **55+** generate about 35% of revenue
- **1-star customers** spend the least (average order 603 vs 724 to 762 for other scores)
- Sales peak in **August** and on **Fridays**
- The top 5 cities make up only about 2% of revenue, so no city dominates

## Recommendations
- Run promotions in August and on Fridays
- Target the 55+ segment with tailored offers
- Keep Cash on Delivery and reward online payment
- Investigate the causes of 1-star reviews

## Limitations
- The data is synthetic, so patterns may not match real customers
- Missing values were filled (mean review score, gender), which can add bias
- No customer ID, so repeat buying cannot be tracked

## Repository Files
| File | Description |
|------|-------------|
| `online_retail_eda.ipynb` | Full analysis notebook |
| `Charts/` | Saved visualizations |
| `Online_Retail_EDA_Purple.pptx` | Project presentation |

## How to Run
1. Download the dataset from Kaggle and place the CSV in the same folder as the notebook
2. Open `online_retail_eda.ipynb` in Jupyter or Google Colab
3. Run all cells (Runtime, then Restart and run all)

```
pip install pandas numpy matplotlib seaborn
```

## Next Steps
- Test the findings on a real-world dataset
- Run a hypothesis test on the review score gap
- Build a dashboard and track repeat customers
