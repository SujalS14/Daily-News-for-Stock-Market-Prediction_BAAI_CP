# Daily-News-for-Stock-Market-Prediction_BAAI_CP
Kaggle Link: 'https://www.kaggle.com/datasets/aaron7sun/stocknews'

Week 1: Python + AI

DATE Row: The date when the news occurred and the market was tracked.

Diagnostics Question: "How many trading days in the dataset were between 0 to 1 days?"

Summary: During this class, I was able to learn about how to find different repositories, where I looked for a stock market repository using kaggle and I uploaded it into github and then I was able to use google colab notebook. The notebook leaded the news headlines data, cleaned it by removing unnecessary and missing values, and then made a bar graph to help visulatize the distribution of the target 'Label' column, which was a dataset in bar graph format.


**Q1. How many days had a label of 1 (market up)?**
```sql
SELECT COUNT(*) AS up_days
FROM data
WHERE label = 1
```
**Finding:** 1,065 of our 1,989 days (about 54%) had a label of 1.

**Q2. Which year had the most days with a label of 1?**
```sql
SELECT SUBSTR(date, 1, 4) AS year, COUNT(*) AS up_days FROM data
WHERE label = 1
GROUP BY year ORDER BY up_days DESC
```
**Finding:** 2013 leads with 146 up days. 2008 and 2016 are low because the data only covers part of those years.

**Q3. What are the top 5 months in 2008 with the most days where the label was 0?**
```sql
SELECT SUBSTR(date, 1, 7) AS month, COUNT(*) AS down_days FROM data
WHERE label = 0 AND SUBSTR(date, 1, 4) = '2008'
GROUP BY month ORDER BY down_days DESC LIMIT 5
```
**Finding:** October 2008 had the most down days, 16, during the financial crisis.
