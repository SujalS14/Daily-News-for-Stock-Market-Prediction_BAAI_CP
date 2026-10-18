# Daily-News-for-Stock-Market-Prediction_BAAI_CP
Kaggle Link: 'https://www.kaggle.com/datasets/aaron7sun/stocknews'

Week 1: Python + AI

DATE Row: One row = one trading day: the date, the top 25 news headlines, and a Label (1 = Dow went up, 0 = it went down).

Diagnostics Question: "Do the top world news headlines on a given day line up with whether the Dow Jones went up or down?"

Summary: During this class, I was able to learn about how to find different repositories, where I looked for a stock market repository using kaggle and I uploaded it into github and then I was able to use google colab notebook. The notebook leaded the news headlines data, found no duplicates and dropped 3 days with missing headlines, leaving 1,986 days. My bar chart shows slightly more up days (1) than down days (0).




Week 2: SQL

**Q1. How many days had a label of 1 (market up)?**
```sql
SELECT COUNT(*) AS up_days
FROM data
WHERE label = 1
```
**Finding:** 1062 of our 1989 days (about 53%) had a label of 1.

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




Week 3: Tableau

Dashboard URL: 'https://public.tableau.com/app/profile/sujal.singarapu/viz/DJIAMarketTrendsDashboard/DJIAMarketTrendsDashboard?publish=yes'
<img width="1511" height="826" alt="Dashboard" src="https://github.com/user-attachments/assets/991c4849-e15c-41b9-9d7f-1882112c52b0" />

**Finding Sentence:**
This week, when I worked on Tableau with my files, I was able to see what the data looked like. Before, it was just a lot of numbers, and I found it very random. However, with Tableau, I was able to actually understand what the data was trying to show because it made everything visual.
