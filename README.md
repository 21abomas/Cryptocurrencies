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

# Part 2: Reducing Data Dimensions Using PCA

In this part, the dimensions of the preprocessed data are reduced using PCA. The following steps are performed:

* Apply PCA to reduce the dimensions of the X DataFrame to three principal components.
* Create a new DataFrame named pcs_df that includes the three principal components, and use the index of the crypto_df DataFrame as the index for pcs_df.

# Part 3: Clustering Cryptocurrencies Using K-means

In this part, the K-means algorithm is used to create an elbow curve to find the optimal number of clusters, and then the K-means algorithm is run on the preprocessed data to make predictions of the K clusters for the cryptocurrencies. The following steps are performed:

* Use the pcs_df DataFrame to create an elbow curve using hvPlot to find the best value for K.
* Use the KMeans algorithm from the sklearn library to make predictions of the K clusters for the cryptocurrencies' data using the pcs_df DataFrame.

# Part 4: Visualizing Cryptocurrencies Results

In this part, the results of the clustering analysis are visualized using different plots. The following steps are performed:

* Here is elbow curve plot with clusters

![bokeh_plot](https://user-images.githubusercontent.com/115948377/230134705-8972b033-2213-44e9-9d62-e59e463a3ed3.png)

* Here is 3D-Scatter plot with clusters

![newplot](https://user-images.githubusercontent.com/115948377/230135501-87cdbe4a-0347-4ac1-929c-532db2ddd902.png)

* Here is 2D-Scatter plot with clusters

![bokeh_plot1](https://user-images.githubusercontent.com/115948377/230135769-fc0294ef-b4c0-483e-8672-62c9362ea01e.png)
