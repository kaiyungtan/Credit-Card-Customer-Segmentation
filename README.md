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

### Pairplot
![image](https://user-images.githubusercontent.com/69633814/102201348-41018f00-3ec6-11eb-9066-12279950deca.png)
### Heatmap for correlation
![heatmap](https://user-images.githubusercontent.com/69633814/102201244-1c0d1c00-3ec6-11eb-9e18-83d2ff0843d7.png)

Comments:
* Total credit cards and total visit online has medium positive correlation with average credit limit : 0.61,0.55 respectively.
* Total credit cards and total visit bank has medium negative correlation with total calls made : -0.65,-0.5 respectively.
* Total visit online and medium negative correlation with total visit bank : -0.55.

## K-means Clustering - Boxplot for analyse clusters 

![image](https://user-images.githubusercontent.com/69633814/102201466-6f7f6a00-3ec6-11eb-8bac-17a09487ddab.png)

![image](https://user-images.githubusercontent.com/69633814/102201659-b40b0580-3ec6-11eb-8dc1-1bf18b8730e9.png)

![image](https://user-images.githubusercontent.com/69633814/102201684-bb321380-3ec6-11eb-8c57-1499979b4d3d.png)

![image](https://user-images.githubusercontent.com/69633814/102201703-bff6c780-3ec6-11eb-9b27-6475abd7904d.png)

![image](https://user-images.githubusercontent.com/69633814/102201625-aa819d80-3ec6-11eb-82d3-25280d88fead.png)

Comments:
* Group 2 has an obvious distinction compare to group 0 and 1.
    * Customers who have average credit limit of 75k and above are in group 2.
    * Customers who have more than 7 credit cards are in group 2.
    * Customers who have visited online more than 6 times are in group 2.
* Group 1 has less credit cards compare to other groups - 1-4 credit cards.
* Group 1 has one attribute that is distinct from other group namely, customers who make calls more than 4 times.
* Group 0 visited bank more than other groups - more than 2 times and up to 5 times.
* Group 0 also less visited bank online compare to other groups.


## Key Questions:
* How many different segments of customers are there?
         
      * There are 3 different segements of customers in AllLife Bank credit card customer base.   
     
     
* How are these segments different from each other?

    Using k-means clustering labels as reference: (Group 0-2) 
          
       
         Group 1
       * Customers who have average credit limit below 25k and own credit cards 1-4 max.
       * Customers who seldom visit bank 0-2 times.
       * Customers who visit bank online moderately (1-5 times)
       * Customers who make most phone calls (4-10 times)
       * 34% of customers are in this group.  
       
         Group 2
       * Customers who have average credit limit above 75k and own most credit cards 7-10 max.
       * Customers who least visited bank 0-1 times.
       * Customers who most visit bank online . (7-15 times)
       * Customers who make least phone calls (0-2 times)
       * Only 7.3% of customers are in this group. 
       
         Group 0
       * Customers who have average credit limit between 25k and 75k and own credit cards 4-7 max.
       * Customers who most visited bank  2-5 times.
       * Customers who least visit bank online. (0-2 times)
       * Customers who make moderate phone calls (0-4 times)
       * Majority of customers are in this group - 58.4%.
