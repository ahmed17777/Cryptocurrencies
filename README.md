# Cryptocurrencies

Syed Ahmed 
June 28, 2021

## Overview 

This project utilizes unsupervised machine learning to create an analysis of the cryptocurrency market for Accountability Accounting. I will be preprocessing the data, using a clustering algorithm, and reducing dimensions in the dataset using Principal Component Analysis.

Martha is a senior manager for the Advisory Services Team at Accountability Accounting, one of our most important clients. Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked us to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data Martha will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what Martha is looking for, she has decided to use unsupervised learning. To group the cryptocurrencies, Martha decided on a clustering algorithm.

## Resources 

All data used in this analysis is from crypto_data.csv, which was retrieved from CryptoCompare. 

## Results 

### Preprocessing 

My first task was to view the raw data and preprocess it in order to perfrom PCA. This is the DataFrame that was created after performing the following: 
- All cryptocurrencies that are not being traded are removed 
- The IsTrading column is dropped 
- All the rows that have at least one null value are removed 
- All the rows that do not have coins being mined are removed 
- The CoinName column is dropped 

  ![1](https://user-images.githubusercontent.com/45697471/123692046-5a47a880-d824-11eb-8284-78af221d5ce1.png)
  
From here, the get_dummies() method was used to create a dataframe with variables for the text features to be used in PCA. The variables were also standardized using the StandardScaler fit_transfrom() function. 
 
### Dimension Reduction using PCA

Once the data was preprocessed, I used the PCA algorithm to reduce the dimensions of the dataframe created in the previous step to three principal components. Here is the dataframe that was created after this was done: 

  ![2](https://user-images.githubusercontent.com/45697471/123693263-d7bfe880-d825-11eb-97ac-9b9cf01d4637.png)

### Clustering Cryptocurrencies using K-means 





