# E-commerce-Customer-Segmentation 

### Problem Statement:
* As an e-commerce platform, it is very important to profile your customers, dividing your client base into groups based on their needs and expectations. Grouping will help us come up with dedicated marketing strategies and will aid us in recommending products to different user bases. 
* In this project, we are interested in analyzing the content of an E-commerce database that lists purchases made by ∼4000 customers over a period of one year (1/12/2010 to 9/12/2011). 
* Based on this analysis, we would like to develop models to group the 4000 customers into different buckets. Such a model must take into account the similarity between the products purchased between the users (i.e. a user might purchase 2 different products which are very similar to each other), the spending patterns of a user, their meta information, etc. 

### Dataset:
* It contains a feature (Description) in a textual format.
* This feature contains the description of Products.
* Hence, NLP is used. (NLTK packages)

### 1st part: Grouping similar Products together:
* Data Compressing: 
     * removing Punctuations, short words, stop words,..
     * doing Lemmatisation: in order to find the root word
* Vectorization:
     * using Countvectorizer (Bag of Words model): Binary approach 
     * thus, text is converted into Numbers
* Modelling:
     * using k-means clustering
     * using Dimensionality reduction: to reduce the total features
            * Principal Component Analysis (PCA) is used
     * using Elbow plot:
            * optimal number of clusters is found to be 4
     * Applying k-means algorithm
            * with k-means++ initialization
 
 ### 2nd part: Grouping similar Customers:
  * Data preprocessing:
     * Encodings, dropping unnecessary features
  * Grouping:
     * Customers are grouped using CustomerID, aggregated using Mean value
  * Scaling is done using MinMax scaler
  * using Elbow plot : optimum no:of clusters is identified to be 5.
  * Modelling is done using k-means clustering


### Evaluating the model:
  * based on purity of clusters
  * SILHOUETTE SCORE of 0.35 shows that the clusters are not well separated and cohesion of datapoints within the cluster is weak.

### Conclusion:
  * Thus customers into 5 different buckets based similarity between the products purchased between the users , the spending patterns of a user, their meta information, etc.
