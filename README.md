## INTRODUCTION

Hello, I'm Mike.  This project marks the culmination of my Google Business Intelligence Professional Certification course.

**Scenario:**

During my interview for a Business Intelligence (BI) position on the Google Fiber call center team, I am tasked with creating a dashboard tool. This tool will enable the team to analyze trends related to repeat calls. Specifically, they want to understand how frequently customers contact customer support after their initial inquiry. The goal is to assess the team's effectiveness in addressing customer questions during the first interaction.

![Google Fiber](https://github.com/mikepascua/GoogleFiberDashboard/assets/170308027/01dbbb9c-137b-4f37-9b35-5bebfd7c83c7)

## ABOUT THE COMPANY

In this fictional scenario, Google Fiber offers fiber optic internet services to individuals and businesses.  The customer service team, operating in their call centers within established service areas, handles incoming calls from customers.  Their primary goal is to explore trends related to repeat calls.  By analyzing these trends, the team aims to reduce the number of times customers need to call in order to resolve their issues effectively.

## BUSINESS PROBLEM
​
Repeat calls can have a significant impact on call centers.  It can lead to various challenges, including decreased productivity, customer churn, and demoralized agents.
​
* How often does the customer service team receive repeat calls from customers?
* What are the problem types that generate the most repeat calls?
* Which market city's customer service team receives the most repeat calls?
​
## SOLUTION

This dashboard has been created to explore trends in repeat callers, increase customer satisfaction, and improve operational optimization.

## METHODS AND PROCESSES

The datasets are fictionalized versions of the actual data this team works with. Because of this, the data is already anonymized and approved. However, I need to make sure that stakeholders have data access to all datasets so they can explore the steps I’ve taken. The data provided are from January to March 2022.

To anonymize and fictionalize the data, please refer to the following:

**new_market (market type)**

* market_1
* market_2
* market_3

**new_type (problem type)**

* type_1
* type_2
* type_3
* type_4
* type_5

Additionally, the dataset also records repeat calls over seven-day periods. The initial contact date is listed as contacts_n. The other call columns are then contacts_n_number of days since first call. For example, contacts_n_6 indicates six days since first contact. 

I accessed the data from the source and checked if the data is useful for analysis.  Then I uploaded it in BigQuery, combined the three tables into one dataset, explored the schema, and checked the data.  After that, I created a unified target table by using the **UNION ALL** statement and downloaded the result as a CSV file, so I could upload it on Tableau Public. 

![Union All BQ](https://github.com/mikepascua/GoogleFiberDashboard/assets/170308027/9aaef840-ca65-4d22-87ed-90b1000d1b34)

![Save as CSV BQ](https://github.com/mikepascua/GoogleFiberDashboard/assets/170308027/a51bf4e7-b512-4ca1-bc6b-69cf4cabd99c)

In Tableau, I also added three calculated fields:

* **Sum Calls** - sum of all calls (including the initial calls and repeat calls)
* **Sum Repeat** - sum of all repeat calls
* **Repeat Call Rate** - percentage of repeat calls over total calls

I also created a **Date Parameter** to filter the data to monthly and weekly period.

![Data Parameter](https://github.com/mikepascua/GoogleFiberDashboard/assets/170308027/ac16038f-0dc1-4a55-a77d-8c8aff1e81f1)

I used the following charts in Tableau for this project:  **Line, Bar, Summary Tiles, and a Summary Table.**

## DASHBOARD

This project provides a clear view of repeat call volumes in different markets and the type of problems they represent.

![Dashboard 1](https://github.com/mikepascua/GoogleFiberDashboard/assets/170308027/8303dd02-24ec-4aee-933b-8a965ffd2ccf)

![Dashboard 2](https://github.com/mikepascua/GoogleFiberDashboard/assets/170308027/b03308ef-cd19-49e1-94e8-02b9c7852133)

#### The dashboard can be viewed here: 

<https://public.tableau.com/views/GoogleBICapstoneProject-RepeatCallDashboard/Dashboard3?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link>

## INSIGHTS AND KEY FINDINGS
​
* Between January and March 2022, the customer service team received a total of 20,240 repeat calls, which accounts for 23.76% of all calls.  Notably, March had the highest number of repeat calls, reaching 7,606.
​
* Market 1 had the highest volume of repeat calls, primarily due to the sheer number of calls they received.  However, in terms of Repeat Call Rate, Market 3 took the lead.  Their average RCR falls within the range of 27.59% to 33.49%.
​
* In all three market types, the most common issues leading to repeat calls are type_5 and type_2.  Understanding these specific problem types allows the team to address them effectively and improve customer satisfaction.

## RECOMMENDATIONS

* The team should verify  the status of their network infrastructure and ensure it operates smoothly to minimize repeat calls.  Taking proactive steps to maintain a reliable network can significantly enhance customer satisfaction.

* Refresher Training - Proper training and knowledge enable agents to provide accurate answers, reducing the need for repeat calls.

* Create a self-service portal where customers can find answers to common queries without needing to call (FAQs, troubleshooting guide, and videos)









​
