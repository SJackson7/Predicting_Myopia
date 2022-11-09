# Predicting Myopia
## Process
For this exercise, I was tasked to utilize unsupervised machine learning to determine if patients with myopia can be placed into distinct groups. To accomplish this, I took the following actions:

### Prepared the Data
* Read the myopia.csv file into a Pandas DataFrame
* Removed the "MYOPIC" column from the dataset
  * Doing this removes bias in an unsupervised model
* Standardized the dataset to that columns containing larger values will not influence the outcome more that columns with smaller values

### Applied Dimensionality Reduction
* Performed PCA preserving 90% of the explained variance
* Further reduced the dataset dimensions with t-SNE and visually inspected the results below via scatterplot

![image](https://user-images.githubusercontent.com/104914008/200868777-64571371-bd48-4a37-9bca-5618f403f0ec.png)

### Performed Cluster Analysis with K-means
* Created an elbow plot to identify the best number of clusters using a FOR loop to determine the inertia for each "k" between 1 through 10

![image](https://user-images.githubusercontent.com/104914008/200868803-b7d61276-fadd-4465-b72d-b609c5cf5fa2.png)
* Using the optimal number of clusters (3) based on the elbow plot, the below chart is a result of the PCA transformed data for k-means modelling

![image](https://user-images.githubusercontent.com/104914008/200868850-f047bc04-bcf5-4c5a-b7a1-4272b9bd1e60.png)

### Myopia Cluster Findings
The following observations are for myopia clusters after data preparation, reduction, and cluster analysis:
* The optimal number of clusters appears to be 3, therefore patients can be clustered in 3 groups.
* Some clear clusters formed after performing K-Means, however accuracy would benefit from a largest dataset as well as additional testing and training using the above models since the clusters have some scattering.

## References
Reduced dataset from [Orinda Longitudinal Study of Myopia conducted by the US National Eye Institute](https://clinicaltrials.gov/ct2/show/NCT00000169)
