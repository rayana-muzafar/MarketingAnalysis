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

<h2>4. Data Visualization in Power BI</h2>
Creation of Calendar Table in DAX to ensure time accuracy:


<img width="687" height="335" alt="Image" src="https://github.com/user-attachments/assets/bffd0b2d-a4ba-4546-824b-4d81d237bdf9" />

Loading data model and building relationships:

<img width="526" height="407" alt="Image" src="https://github.com/user-attachments/assets/c063977b-fcb0-4664-ab67-21bd63ad53b0" />

Finally building a dashboard with key metrics.

<h2>5. Analysis' results, conclusions and recommendations</h2>

<b>Overview</b>

Conversion:
Throughout the 2024 and 2025 years conversion rate stays consistent and doesn’t show any significant drop-downs that wouldn’t repair in a couple of months.

Social Media:
In 2025 we experience a big fall in click-through rates and views which indicates a problem with our content.

Customer Feedback:
The average rating in last 2 years stays at the point of 3.6, which shows that our clients mostly satisfied by the quality of our products, but it also shows that we can improve customer feedback for products with average rating below 3.6.

<img width="892" height="502" alt="Image" src="https://github.com/user-attachments/assets/0a28188e-ffbe-4cfc-96bb-bb70c5ef449c" />

<b>Conversion Details</b>

Throughout the 2024 and 2025 Conversion rate varies between 8.48 – 8.55%, which indicates a good level of engagement on our site.
Dips in July and October appear to be isolated incidents or seasonal fluctuations requiring further granular data to explain.
The best-performing products are:
<ol>
<li>Hockey Stick with 20.83% of CR;</li>
<li>Climbing Rope with 20%;</li>
<li>Surfboard with 18.92%;</li>
<li>Cycling Helmet with 18.18%.</li>
</ol>

It is recommended to test new marketing campaigns on those products to get clearer insights on how our content is performing.
<img width="892" height="503" alt="Image" src="https://github.com/user-attachments/assets/fab25aab-bc84-40fd-8bc1-bd741171af54" />

<b>Social Media Details</b>

Falling views indicate the lack of interest to our content among the people who sees it. This may mean that the audience that happen to watch our content is not our target audience. To make any further conclusions we have to perform a deep customer analysis to target our future content on the portrait of our “ideal” clients.

In the beginning of the 2025 year we can see that our blog was getting the most attention. That may guide us to further investigation of our previous content strategies to get insights from our past experience.
The most views throughout the year showed Soccer Ball, Basketball, Baseball Glove and Boxing Glove, which may mean that content with those products was the most engaging for the audience.
The critical drop-down of CTR from 9% to 2.8% shows that even those who were previously engaged in our content stopped interacting with us, which means that we have to not only attract new audience but also engage our previous viewers.
<img width="894" height="502" alt="Image" src="https://github.com/user-attachments/assets/0a05d736-560f-4118-b5d6-dc8c560996de" />


<b>Customer Review Details</b>

2024 and 2025 show a stable average rating of 3.67, which means that the quality of our products hasn’t change and the satisfaction rate is pretty stable. 

Number of customer reviews by rating shows that prevalent ratings are 4 and 5 stars, which in addition to overall positive sentiment category of reviews tells us about an overall customer satisfaction.
While there’s no significant troubles in rating and all those numbers are stable, we still have opportunities for improvement. We should conduct a thorough analysis of customer feedback for product with average rating below 3.6 stars and find ways to improve customers’ satisfaction by those products (Yoga Mat, Ice Skates, Running Shoes, Dumbbells, Surfboard, Football Helmet).
<img width="892" height="503" alt="Image" src="https://github.com/user-attachments/assets/0299159b-9aee-4277-b8a8-74d0efba342a" />


<b>Reduced Customer Engagements and high Marketing Expences</b>

Despite a stable Conversion Rate (~8.5%), which confirms that the website and product offerings remain competitive, we observe a critical decline in Engagement Rate (from 10% in Jan, 2025 to 2.8%) and CTR (from 9% to 2,8%).
This divergence indicates that while we are successful at converting visitors, our top-of-funnel (marketing content) is failing to attract and retain interest. The current marketing spend is likely being wasted on non-engaging content or mismatched audiences.
The average rating throughout 2024 and 2025 has remained stable at 3.7. Sentiment analysis confirms that the majority of customer reviews are positive. This indicates that the decline in engagement is not driven by product quality or customer dissatisfaction, further pointing to the marketing strategy as the primary area for improvement.

<b>Recommendations</b>
<ol>
<li>Pivot the content strategy from high-frequency posting to high-quality, interactive formats (Video/User-generated content).</li>
<li>Implement A/B testing for CTAs (Call-to-Action) to identify what triggers clicks for the current audience.</li>
<li>Perform a target audience audit to ensure new campaigns are not reaching "cold" or irrelevant segments.</li>
<li>Perform a customer analysis to identify our “ideal” client.</li>
<li>Conduct a test of new marketing campaigns on products that show the best conversion rates.</li>
<li>Revise our content strategies from 4 first months of the year to see why our blog was performing better than other types of content.</li>
<li>Conduct a thorough analysis of customer feedback for product with average rating below 3.6 stars and find ways to improve customers’ satisfaction by those products.</li>
<li>Prioritize budget allocation to high-conversion products to maximize ROI while the content strategy is being revised.</li>
</ol>



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
