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
 <li>Data-modelling in Power BI;</li>
 <li>Creating measures in Power BI;</li>
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

<h2>Customer Feedback analysis with Python</h2>
<b>Tech Stack used in Sentiment Analisys:</b>

- <b>Python (Pandas):</b> for data-manipulation and new columns creation
- <b>NLTK (VADER):</b> using a pre-trained model of lexical analysist to assess the tone of the text
- <b>SQL (pyodbc):</b> for extracting data from SQL Server's relational database 






<img width="735" height="497" alt="Image" src="https://github.com/user-attachments/assets/14735803-83d6-4d04-8a7d-f3664aad927c" />

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
