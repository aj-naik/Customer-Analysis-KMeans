# Customer-Marketing-Segmentation-KMeans
Analysis of customer banking records and sorting behaviour patterns into different clusters using KMeans and performing dimensional reduction using PCA. 
The code is pretty self-explainatory

# Data Description
CUSTID: Identification of Credit Card holder 

BALANCE: Balance amount left in customer's account to make purchases

BALANCE_FREQUENCY: How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)

PURCHASES: Amount of purchases made from account

ONEOFFPURCHASES: Maximum purchase amount done in one-go

INSTALLMENTS_PURCHASES: Amount of purchase done in installment

CASH_ADVANCE: Cash in advance given by the user

PURCHASES_FREQUENCY: How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)

ONEOFF_PURCHASES_FREQUENCY: How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)

PURCHASES_INSTALLMENTS_FREQUENCY: How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done)

CASH_ADVANCE_FREQUENCY: How frequently the cash in advance being paid

CASH_ADVANCE_TRX: Number of Transactions made with "Cash in Advance"

PURCHASES_TRX: Number of purchase transactions made

CREDIT_LIMIT: Limit of Credit Card for user

PAYMENTS: Amount of Payment done by user

MINIMUM_PAYMENTS: Minimum amount of payments made by user  

PRC_FULL_PAYMENT: Percent of full payment paid by user

TENURE: Tenure of credit card service for user

# Initial Data Analysis
Mean of balance is $1500

'Balance_Frequency' for most customers is updated frequently ~1

For 'PURCHASES_FREQUENCY', there are two distinct group of customers

For 'ONEOFF_PURCHASES_FREQUENCY' and 'PURCHASES_INSTALLMENT_FREQUENCY' most users don't do one off puchases or installment purchases frequently 

Very small number of customers pay their balance in full 'PRC_FULL_PAYMENT'~0

Credit limit average is around $4500

Most customers are ~11 years tenure


# Project History
Did this project under coursera's guided projects in september 2020 but I couldn't comprehend some of the parts. After getting a better understanding of concepts involved, I revisited and modified the project in december. Doing the project again brought me a better understanding about unsupervised learning, KMeans and PCA and analysing financial data. Got a lot of insights from the data as well as end result.

# Project Steps
- Performed EDA and had a look at plots.
- After gaining relevant information, cleaning the data I found that the data is skewed so sclaed the dataset.
- Used the elbow method to determine the optimal number of clusters to be formed. I could go with both 7 and 8 according to plot but went with 8 clusters.
- Applied inverse transformation to get sense of the output
- Then used the scaled data and classified each sample into a cluster using fit_predict method.
- Plotted histogram of every cluster and analysed that
- Used Principal Component Analysis for dimensionality reduction. Set the number of dimension as 2 so that the clusters could be plotted using scatterplot. Tried 3 dimensions and a 3d plot as well but the output was messy and not easily comprehensible.
- Plotted a scatterplot of the classified data with each cluster having an unique color for ease of understanding.

