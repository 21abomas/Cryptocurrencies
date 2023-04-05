# Cryptocurrencies
## Cryptocurrency Clustering Analysis
This project involves using unsupervised learning techniques to analyze and cluster cryptocurrencies based on their features. The main objective is to create a classification system for a new cryptocurrency investment portfolio.
 The project is divided into four parts:
### Part 1: Preprocessing the Data for PCA
In this part, the dataset is loaded into a Pandas DataFrame and preprocessed to prepare for Principal Component Analysis (PCA). The following steps are performed:

* Read in the crypto_data.csv file into a DataFrame named crypto_df.
* Keep only the cryptocurrencies that are being traded.
* Drop the IsTrading column.
* Remove rows with at least one null value.
* Filter the DataFrame to only include rows where coins have been mined.
* Create a new DataFrame that holds only the cryptocurrency names, and use the crypto_df index as the index for this new DataFrame.
* Remove the CoinName column from the crypto_df DataFrame.
* Use the get_dummies() method to create variables for the two text features, Algorithm and ProofType, and store the resulting data in a new DataFrame named X.
* Use the StandardScaler from the sklearn library to standardize the features in the X DataFrame.
