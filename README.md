# UDacityCapstone
Repo for UDacity Data Scientist Capstone

Please see link for the blog post [here](https://medium.com/@kevinpolitz/customer-segmentation-report-d51221710536). 

## Project Overview

In the highly competitive market of customer acquisition and retention, companies are constantly seeking to better understand their customer base. Analyzing existing customers' demographics and behavior patterns can provide valuable insights into potential target groups and help tailor marketing strategies to maximize customer acquisition and retention. This project aims to analyze demographics data for a mail-order sales company in order to identify potential new customers within the general population.

The project's origin lies in the need for an efficient and data-driven approach to customer segmentation, which can help the company focus its marketing efforts on the most promising segments of the population. The project will leverage two datasets: one containing demographic information about the company's existing customers, and another containing demographic information about the general population. By comparing the characteristics of the company's customers with those of the general population, we aim to identify key differences and similarities that can be used to target new customers more effectively.

## Problem Statement

The problem to be solved is to identify potential new customers for the mail-order sales company by analyzing and comparing the demographic characteristics of the company's existing customers with those of the general population. This will help the company better understand its customer base, focus its marketing efforts on the most promising segments of the population, and ultimately increase customer acquisition and retention.

To solve this problem, I will first preprocess and clean the provided datasets to ensure that they are suitable for analysis. Next, I will employ dimensionality reduction techniques like PCA to reduce the complexity of the data and speed up the analysis. I will then apply clustering algorithms such as K-means to segment the general population into distinct groups based on their demographic characteristics. By comparing the distribution of clusters in the customer dataset with those in the general population dataset, I will identify overrepresented and underrepresented clusters in the customer base. This information will be used to draw insights about the customer base relative to the general population and help target new customers more effectively.

The expected solution is a clear and actionable segmentation of the general population, highlighting the most promising segments for customer acquisition. This will enable the company to focus its marketing efforts on the identified target groups, leading to more efficient use of resources and improved customer acquisition and retention rates.

## Requirements

To run the code in this repository, you will need to have the following libraries installed:
1. numpy: A library for the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays.
`pip install numpy`

1. pandas: A fast, powerful, flexible, and easy-to-use open-source data analysis and data manipulation library built on top of the Python programming language.
`pip install pandas`

1. ast: The abstract syntax tree module is part of the Python standard library and does not require installation.

1. matplotlib: A plotting library for the Python programming language and its numerical mathematics extension NumPy.
`pip install matplotlib`

1. seaborn: A Python data visualization library based on matplotlib that provides a high-level interface for drawing attractive and informative statistical graphics.
`pip install seaborn`

1. scikit-learn: A machine learning library for Python, featuring various classification, regression, and clustering algorithms, including support vector machines, random forests, gradient boosting, k-means, etc.
`pip install scikit-learn`

1. imbalanced-learn: A Python package that offers a number of re-sampling techniques commonly used in datasets showing strong between-class imbalance.
`pip install imbalanced-learn`

1. joblib: A set of tools to provide lightweight pipelining in Python, particularly useful for caching of large computation results.
`pip install joblib`

After installing the required libraries, you can use the provided Jupyter Notebook with %matplotlib inline magic word to produce visualizations directly in the notebook.

## Metrics
In order to evaluate the performance of the segmentation model and the effectiveness of this approach, it is essential to define appropriate metrics. These metrics should capture the quality of the segmentation and provide a quantitative measure to compare different models or strategies.

For this project, I can use the following metrics:

1. Silhouette Score: The Silhouette Score measures the quality of clustering by calculating the similarity between data points within the same cluster and their dissimilarity to data points in other clusters. The score ranges from -1 to 1, with higher values indicating better clustering. This metric is suitable for the problem as it helps us assess the quality of the clusters obtained from the K-means algorithm, ensuring that the segments I identify are well-separated and cohesive.

1. Inertia (Sum of Squared Distances): Inertia is the sum of squared distances between data points and their assigned cluster centroids. Lower inertia values indicate better clustering, as data points are closer to their centroids. This metric is useful for determining the optimal number of clusters using the Elbow Method. In the project, minimizing inertia helps ensure that the clusters I identify are compact and well-defined.

1. ROC-AUC Score: The Receiver Operating Characteristic - Area Under the Curve (ROC-AUC) score is a performance measurement for classification problems at various thresholds settings. It measures the trade-off between true positive rate (sensitivity) and false positive rate (1-specificity) across different threshold values. An ROC-AUC score of 1 indicates perfect classification, while a score of 0.5 implies that the model performs no better than random chance. In this project, the ROC-AUC score helps us assess the model's ability to discriminate between different clusters, providing a comprehensive view of its performance.

## Results

#### Model Evaluation and Validation
To ensure that my solution is robust and reliable, I have employed a rigorous model evaluation and validation process. I utilized cross-validation to find the best parameters for the supervised learning models and assessed the performance of the clustering algorithm using various metrics.

The final model's qualities, such as parameters, were evaluated in detail. I compared the performance of different models, such as Logistic Regression and Random Forest using  ROC-AUC score. This allowed us to identify the best-performing model for predicting the cluster labels and ensure a high-quality segmentation of the general population.

I also used cross-validation to validate the robustness of the model's solution. By splitting the data into multiple folds and training and testing the model on different subsets of the data, I was able to obtain a more reliable estimate of the model's performance and ensure that it generalizes well to new data.

In addition to the supervised learning models, I evaluated the quality of my clustering solution using metrics like Silhouette Score and Inertia. These metrics helped us assess the quality of the clusters obtained from the K-means algorithm, ensuring that the segments I identified are well-separated and cohesive.

By comparing the results using different models, parameters, and techniques in tables and charts, I was able to gain a comprehensive understanding of the strengths and weaknesses of each approach and make informed decisions about the final solution.

#### Justification
The final results are discussed in detail, and the exploration as to why some techniques worked better than others and how improvements were made has been documented. I found that the combination of PCA and K-means clustering provided a good balance between computational efficiency and quality of the segmentation. The use of PCA allowed us to reduce the dimensionality of the data while preserving its structure, and K-means clustering helped identify distinct segments of the population based on their demographic characteristics.

On the other hand, I observed that certain supervised learning models performed better than others in predicting the cluster labels. For example, Logistic Regression outperformed the Random Forest model.

Furthermore, I found that using SMOTE for rebalancing the dataset was effective in addressing the class imbalance issue, leading to more accurate and robust predictions.

Overall, my approach demonstrates the value of using a combination of preprocessing, dimensionality reduction, clustering, and supervised learning techniques to identify potential new customers for the mail-order sales company and focus marketing efforts on the most promising segments of the population.



## Conclusion

#### Reflection
In this project, I tackled the problem of identifying potential new customers for a mail-order sales company by analyzing and comparing the demographic characteristics of the company's existing customers with those of the general population. I employed various data preprocessing techniques to clean and prepare the datasets for analysis. Dimensionality reduction using PCA helped us reduce the complexity of the data, and clustering algorithms such as K-means were applied to segment the general population into distinct groups based on their demographic characteristics.

By comparing the distribution of clusters in the customer dataset with those in the general population dataset, I identified overrepresented and underrepresented clusters in the customer base. This information allowed us to draw insights about the customer base relative to the general population and helped target new customers more effectively.

#### Improvement

While the current solution provides valuable insights into customer segmentation, there are several aspects that could be improved. One potential area of improvement is the choice of clustering algorithm. In this project, I used K-means clustering, which is sensitive to the initial placement of cluster centroids and assumes that clusters are spherical and have similar sizes. Exploring other clustering algorithms, such as DBSCAN or hierarchical clustering, might help us discover more complex and natural groupings in the data.

Another area for improvement is the feature selection process. In the current approach, I used PCA to reduce the dimensionality of the data. However, PCA is a linear technique and might not capture complex non-linear relationships between features. Alternative dimensionality reduction techniques, such as t-SNE or UMAP, could be explored to better preserve the structure of the data in the reduced-dimensional space.

Finally, I was a bit limited in my compute resources. It could be helpful to try a broader parameter search or use a library like Optuna for hyperparameter optimization. I could also try other machine learning models like XGBoost.

Comparing and contrasting these potential improvements with the current solution would help us assess their effectiveness and further enhance the understanding of the customer base and segmentation process.

## Licensing, Authors, Acknowledgements

Credits must be given to the [Arvato Bertelsmann](https://www.bertelsmann.com/#st-1) company for providing the data and the project, and to [Udacity](https://www.udacity.com/) for all of the course material and the Capstone Project.



