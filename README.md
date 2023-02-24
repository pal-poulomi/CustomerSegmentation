# CustomerSegmentation
Supermarket Customer Segmentation - Unsupervised learning

## Data Collection
 - Dataset used is publicly available Mall_Customers.csv, that has 200 rows and 5 columns indicating the customer id, gender, age, annual income and spending score of each customer
## Exploratory Data Analysis and Visualization
- checking the data for null values
- renaming columns
- Univariate EDA, checking the distribution of each column using seaborn distplot, kdeplot and boxplot
- Bivariate EDA using two columns at a time and visualizing using seaborn scatterplot/pairplot, also using groupby for gender to visualize distribution of data across categorical columns
- Visualizing the correlation between numeric columns using heatmap

## Model Building
- Models built for Univariate, Bivariate and Multivariate cluster analysis
- Mainly used KMeans model, used inertia scores and elbow method to find the best K value and also calculated the mean value of age, annual income and income score for each cluster
- For the bivariate analysis, the 5 clusters and their centroids are visualized through a seaborn scatterplot
- simple prediction of a new datapoint is performed on the multivariate cluster model
## Evaluation of models
- I used other clustering models such as Agglomerative Clustering, Gaussian Mixture Model and Birch model along with KMeans to compare their performances using the metrics Silhouette score, Calinski Harabasz score and Davies Bouldin score
## Insights
- Checking the clusters for bivariate analysis we see that the target/ideal cluster is Cluster 2 since it consists of customers with high income and high spending score 
- 54% of Cluster 2 customers are women so companies can look for ways to attract these customers with marketing campaigns targeting popular items in this cluster
- Cluster 0 (less income, high spend score) presents an interesting opportunity to market to the customers on sales event on popular items
- Comparing the model performance metric scores it is clear that KMeans is the best algorithm for this particular use case, it has the highest Silhouette score, highest Calinski score and least Davies Bouldin score among all the models evaluated, however this might change with a different kind of data
