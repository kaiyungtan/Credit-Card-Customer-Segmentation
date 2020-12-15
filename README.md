# Credit Card Customer Segmentation

## Background: 
AllLife Bank wants to focus on its credit card customer base in the next financial year. They have been advised by their marketing research team, that the penetration in the market can be improved. Based on this input, the Marketing team proposes to run personalised campaigns to target new customers as well as upsell to existing customers. Another insight from the market research was that the customers perceive the support services of the back poorly. Based on this, the Operations team wants to upgrade the service delivery model, to ensure that customers queries are resolved faster. Head of Marketing and Head of Delivery both decide to reach out to the Data Science team for help.


## Objective: 
To identify different segments in the existing customer based on their spending patterns as well as past interaction with the bank.

## Key Questions:
1. How many different segments of customers are there?
2. How are these segments different from each other?
3. What are your recommendations to the bank on how to better market to and
service these customers? 


## Data Description:

Data is of various customers of a bank with their credit limit, the total number of credit cards the customer has, and different channels through which customer has contacted the bank for any queries, different channels include visiting the bank, online and through a call centre.

Columns description:
1. Sl_No Customer Key	- Customer Key is unique number for each customer. 
2. Avg_Credit_Limit	- average credit limit for each customer.
3. Total_Credit_Cards	- totalnumber of credit cards each customer own.
4. Total_visits_bank - total number of times customer visit bank
5. Total_visits_online	- total number of times customer visit online banking
6. Total_calls_made - total number of times customer make calls to bank.


## Steps:
* Perform univariate analysis on the data to better understand the variables and to get an idea about the number of clusters.
* Perform EDA and get insights. 
* Create visualizations to explore data and present the insights.  
* Execute K-means clustering use elbow plot and analyse clusters using boxplot.
* Execute hierarchical clustering (with different linkages) with the help of dendrogram and cophenetic coeff. 
* Analyse clusters formed using boxplot. 
* Calculate average silhouette score for both methods.  
* Compare K-means clusters with Hierarchical clusters. 
* Analysis the clusters formed, explain how one cluster different from another and answer all the key questions.  


## EDA
