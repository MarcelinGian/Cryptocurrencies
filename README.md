# Cryptocurrencies
## Unsupervised Machine Learning Analysis
#### Analysis of cryptocurrency data using unsupervised machine learning to discover discover patterns or groups in the data. 

***
### Execution
#### Preprocessing the data for PCA (Principal_Component_Analysis):
 - Removal of croptocurrencies not being traded (IsTrading = False)
- Removal of rows that have at any null values
- Filter the Data so it only has rows where coins have been mined (TotalCoinsMined > 0)
- Removal of columns from the data that will not be used in the clustering algorithm
- Use the StandardScaler function to standardize features from the dataset

***
### Reducing Data Dimensions Using PCA:
- apply PCA to reduce the dimensions to three principal components
![PCA reduction](https://user-images.githubusercontent.com/105818879/193711899-537cd901-8bf6-4577-8106-10b473bcdab8.png)

***
### Clustering Crytocurrencies Using K-Means:
- Create an Elbow Curve using hvPlot to find the best value for K 
  - A strong horizontal line is observed at point 4
  - Running K-Means with k=4
![01ElbowCurve](https://user-images.githubusercontent.com/105818879/193712552-06d392db-f4e3-423c-aa8c-a4fa3ea9e80e.png)

***
### Visualizing Cryptocurrencies Results:
- Create a 3D-Scatter with the PCA data and the clusters
![023DScatter](https://user-images.githubusercontent.com/105818879/193712712-35f2cb5a-0b32-470e-94d9-a8c690f9e786.png)
- Create a hvplot.scatter plot using x="TotalCoinsMined" & y="TotalCoinSupply"
![03ScatterPlot](https://user-images.githubusercontent.com/105818879/193712811-25067d40-78d0-4432-a496-ee0673899fd8.png)
