<h1>Marketing Analysis for an Online-Retailer</h1>

<h2>Business Case</h2>
ShopEasy, an online-retailer of sports inventory, faced decreased engagement rates despite launching new marketing campaigns. The business was concerned about high marketing expenses and low ROI. Also, customer feedback analysis was needed. After completing this project I was able to identify key issues and provide actionable solutions.
<br />


<h2>Skills Applied</h2>

- <b>SQL for cleaning and transforming data</b> 
- <b>Python & Pandas for Sentiment Analysis</b>
- <b>DAX for creating new measures and calculations</b>
- <b>Power BI and PowerQuery for data-modelling and visualization</b>

<h2>Environments Used </h2>

- <b>SQL - SSMS</b>
- <b>Python - VisualStudio</b>
- <b>Power BI</b>


<h2>Page Sections:</h2>

<ol>
 <li>KPIs and Business Questions;</li>
 <li>Cleaning and transforming data in SQL;</li>
 <li>Customer Feedback analysis in Python;</li>
 <li>Visualization in Power BI;</li>
 <li>Analysis' results, conclusions and recommendations.</li>
</ol>

<h2>1. KPIs and Business Questions</h2>
<b>KPIs:</b> Engagement Rate, Click-Trhough Rate, Conversion Rate, Sentiment score by Product, Sentiment score by Conversion.
<p></p>

<b>Questions:</b>
<ol>
 <li>Is there a drop in customer engagement and satisfaction, and is it affecting our conversion rates?</li>
 <li>Which of our campaigns perform the best, and which the worst?</li>
 <li>How to optimize our efforts and meet ROI?</li>
 <li>How effective are our marketing strategies?</li>
 <li>What are our customers' needs and pain points?</li>
 <li>How we can improve our customer experience and boost our engagement and conversion rates?</li>
</ol>
<br />

<h2>2. Cleaning and transforming data in SQL</h2>
<b>Key constructs used within the SQL queries:</b>

- CTEs
- Window functions
- Joins

<p>Cleansing Products Table and creating price category column:</p>

<img width="514" height="228" alt="Image" src="https://github.com/user-attachments/assets/64e7aabb-ed83-425f-9f22-2e28838371f7" />

<p>Uploading customers data and joining two columns from another table to complete customers' information:</p>

<img width="428" height="192" alt="dim.customers" src="https://github.com/user-attachments/assets/f1715f48-c8d7-4f4e-9ad6-8967fc3f21a8" />

<p>Preparing Reviews table for future analysis and getting rid of double spaces:</p>

<img width="465" height="192" alt="fact.customer_reviews" src="https://github.com/user-attachments/assets/fa261832-786b-4dde-905c-368fa128bf0c" />

<p>Loading data of Customer Journeys, using CTEs and Window Functions to remove duplicates and avoid null-values in "Duration" column by replacing them with average duration per distinct day:</p>

<img width="664" height="418" alt="fact.customer_journeys" src="https://github.com/user-attachments/assets/d6de9072-01ad-489f-945f-06b2869b62b3" />

<h2>3. Customer Feedback analysis with Python</h2>
<b>Tech Stack used in Sentiment Analisys:</b>

- <b>Python (Pandas):</b> for data-manipulation and new columns creation
- <b>NLTK (VADER):</b> using a pre-trained model of lexical analysis to assess the tone of the text
- <b>SQL (pyodbc):</b> for extracting data from SQL Server's relational database 

Libraries preparation:

<img width="610" height="142" alt="Image" src="https://github.com/user-attachments/assets/fed9b477-88d1-43c1-9795-2585de4f0121" />
<p></p>

Extraction of data from SQL-Server. The "customer_reviews_df" variable becomes a table that contains customer IDs, feedback text, and ratings:

<img width="1160" height="284" alt="Image" src="https://github.com/user-attachments/assets/57574803-c160-4aa5-8593-e579134f14c0" />
<p></p>

Building a logic of the analysis with defined functions:
<ol>
 <li><b>calculate_sentiment(review)</b> - Takes the feedback text and returns a number from -1 (terrible) to 1 (fine). Uses VADER for this.</li>
 <li><b>categorize_sentiment(score, rating)</b> - Compares the emotion of the text and the rating that the customer has entered.</li>
 <li><b>sentiment_bucket(score)</b> - Groups numbers by ranges.</li>
</ol>
<img width="439" height="126" alt="Image" src="https://github.com/user-attachments/assets/0e9eedc0-7270-4eae-9022-83c02b419ce2" />
<p></p>
<img width="415" height="426" alt="Image" src="https://github.com/user-attachments/assets/9e36dbae-8ea8-4bc1-9540-24a1393614bb" />
<p></p>
<img width="343" height="183" alt="Image" src="https://github.com/user-attachments/assets/19547a09-dcdb-49a3-aeeb-e63913927e62" />
<p></p>

Applying those functions and getting a new csv-file with 3 new columns ("SentimentScore", "SentimentCategory", "SentimentBucket"):

<img width="843" height="154" alt="Image" src="https://github.com/user-attachments/assets/1e55263c-987e-48aa-a229-edcc4670ab36" />





<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
