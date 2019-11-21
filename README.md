# Text Clustering

Cluster lines/sentences into distinct groups.

## Requirements

- Python v3.6+
- Jupyter Notebook

**Libraries**

- Scikit Learn
- pandas
- scipy
- numpy
- matplotlib
- nltk
- wordcloud
- kneed


## Run

[Text Clustering.ipynb]


## Methodology

- The data is imported as a dataframe and cleaned for processing.  

- TfidfVectorizer is used to vectorize the tokens.  

- Using a dendogram, a minimum number of clusters can be intuitively determined and using the general formula the maximum number of clusters is determined.

- K means Elbow method is used over the range of `minimum number of clusters` to `maximum number of clusters`. Two measures are used to plot the graph -  
  
    1. Inertia - Sum of squared distances of samples to their closest cluster center.  
    2. Distortion - Average of the squared distances from the cluster centers of the respective clusters.  

- From each graph an elbow is determined and the one with higher silhouette score is chosen.  

- Finally, K means with determined number of clusters is used to cluster the document.
