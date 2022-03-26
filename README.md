# Cryptocurrency-Challenge

## Background

I've asked to create a report that includes what cryptocurrencies are on the trading market and to determine whether they can be grouped to create a classification system for this new investment.

I have been handed raw data, so I will first need to process it to fit the machine learning models. Since there is no known classification system, I will need to use unsupervised learning. I will use several clustering algorithms to explore whether the cryptocurrencies can be grouped together with other similar cryptocurrencies. I will use data visualization to share your findings with the investment bank.

## Data Preparation

Read crypto_data.csv into Pandas. The dataset was obtained from CryptoCompare.


Discard all cryptocurrencies that are not being traded. In other words, filter for currencies that are currently being traded. Once you have done this, drop the IsTrading column from the dataframe.


Remove all rows that have at least one null value.


Filter for cryptocurrencies that have been mined. That is, the total coins mined should be greater than zero.


In order for your dataset to be comprehensible to a machine learning algorithm, its data should be numeric. Since the coin names do not contribute to the analysis of the data, delete the CoinName from the original dataframe.


Your next step in data preparation is to convert the remaining features with text values, Algorithm and ProofType, into numerical data. To accomplish this task, use Pandas to create dummy variables. Examine the number of rows and columns of your dataset now. How did they change?


Standardize your dataset so that columns that contain larger values do not unduly influence the outcome.

## Dimensionality Reduction

I created dummy variables above dramatically increased the number of features in your dataset. I performed dimensionality reduction with PCA. For this project, I preserved 90% of the explained variance in dimensionality reduction.

Next, I further reduced the dataset dimensions with t-SNE and visually inspected the results. In order to accomplish this task, I ran t-SNE on the principal components: the output of the PCA transformation. I then created a scatter plot of the t-SNE output and observed whether there are distinct clusters or not.

## Cluster Analysis with k-Means

I lastly created an elbow plot to identify the best number of clusters. I used a for-loop to determine the inertia for each k between 1 through 10. I attempted to determine where the elbow of the plot is, and at which value of k it appears. My k-value appeared to be at 6 or 7. 

