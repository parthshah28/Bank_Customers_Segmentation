# [Bank_Customers_Segmentation](https://github.com/parthshah28/Bank_Customers_Segmentation)
One of the key points for marketers is to know their customers and identify their needs. If the data about customers is available, data science can be applied to perform market segmentation. In this case study you have been hired as a consultant in bank in new york city.
The banks has data on their customers for the past 6 months.The marketing team wants to launch a targeted ad by dividing their customers into atleast 3 distinctive groups.

### Data Source: https://www.kaggle.com/arjunbhasin2013/ccdata

## Dataset:
Dataset has following features.
##### CUSTID: Identification of Credit Card holder 
##### BALANCE: Balance amount left in customer's account to make purchases
##### BALANCE_FREQUENCY: How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)
##### PURCHASES: Amount of purchases made from account
##### ONEOFFPURCHASES: Maximum purchase amount done in one-go
##### INSTALLMENTS_PURCHASES: Amount of purchase done in installment
##### CASH_ADVANCE: Cash in advance given by the user
##### PURCHASES_FREQUENCY: How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)
##### ONEOFF_PURCHASES_FREQUENCY: How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)
##### PURCHASES_INSTALLMENTS_FREQUENCY: How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done)
##### CASH_ADVANCE_FREQUENCY: How frequently the cash in advance being paid
##### CASH_ADVANCE_TRX: Number of Transactions made with "Cash in Advance"
##### PURCHASES_TRX: Number of purchase transactions made
##### CREDIT_LIMIT: Limit of Credit Card for user
##### PAYMENTS: Amount of Payment done by user
##### MINIMUM_PAYMENTS: Minimum amount of payments made by user  
##### PRC_FULL_PAYMENT: Percent of full payment paid by user
##### TENURE: Tenure of credit card service for user

## Feature Engineering:

### A. Missing Values
![](https://github.com/parthshah28/Bank_Customers_Segmentation/blob/main/images/1.png)

I filled up the missing elements with mean of the 'MINIMUM_PAYMENT' and the mean of the 'CREDIT_LIMIT'.

### B. KDE
KDE Plot represents the Kernel Density Estimate. KDE is used for visualizing the Probability Density of a continuous variable.KDE demonstrates the probability density at different values in a continuous variable.

I plotted distplot using seaborn. Distplot combines the matplotlib.hist function with seaborn kdeplot()
![](https://github.com/parthshah28/Bank_Customers_Segmentation/blob/main/images/2.png)

### C. Feature Scaling
For scaling StandardScaler has been applied.

## The optimal number of cluster using Elbow Method:
The elbow method is a heuristic method of interpretation and validation of consistency within cluster analysis designed to help find the appropriate number of clusters in a dataset. If the line chart looks like an arm, then the "elbow" on the arm is the value of k that is the best.
![](https://github.com/parthshah28/Bank_Customers_Segmentation/blob/main/images/3.png)

## Algorithms Used:
#### 1. KMeans
#### 2. PCA
Both are unsupervised learning algorithms.

I concatenated the clusters labels to original dataframe and Plotted the histogram of various clusters.

![](https://github.com/parthshah28/Bank_Customers_Segmentation/blob/main/images/5.png)

Then I applied PCA and Visualize the results.

![](https://github.com/parthshah28/Bank_Customers_Segmentation/blob/main/images/4.png)


To understand it in more detail go to [Bank_Customers_Segmentation.ipynb](https://github.com/parthshah28/Bank_Customers_Segmentation/blob/main/Bank_Customers_Segmentation.ipynb)


