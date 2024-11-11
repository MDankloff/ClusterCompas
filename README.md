# Using SHAP Values for Clustering-based Bias Identification
This repository contains the code associated with our paper: "Using SHAP Values for Clustering-Based Bias Identification." 

# Repository Structure
The repository is organized into 5 Notebooks:
    Pre-processing Notebooks (2):
        Data cleaning, error labeling, and computing SHAP values to set up experimental conditions.
        Includes preliminary visualizations using t-SNE.
    Clustering Notebooks (3):
        Each notebook covers a different clustering approach: K-Means, K-Prototypes, and DBSCAN.

We provide 5 notebooks, 2 for the pre-processing and 3 for each different clustering method (K-Means, K-Prototypes, DBSCAN).
In the pre-processing notebooks, we provide the code for cleaning the data, adding the error labels and SHAP values to create the experimental conditions. Also, some preliminary visualizations are provided with tsne.

Per Clustering notebook:
* Utils for data prep, clustering, results and visualization
* Clustering
* Experimental set-up
* Evaluation results: Chi-square test and Silhouette score
* In-depth Analysis: one-vs-all cluster comparison and tsne 

# Paper abstract
A key form of AI bias occurs when a model produces higher error rates for specific demographic groups, which can be identified using sensitive features such as gender or ethnicity, or proxy features such as income or postcode. Explanation methods like SHAP are also used to address biases in AI models. However, it can be unknown beforehand for which features an AI model exhibits higher error rates, and which SHAP values are most informative for detecting such bias. The Hierarchical Bias Aware Clustering (HBAC) algorithm is an unsupervised method designed to identify clusters with higher error rates using any combination of features. We study whether including SHAP values as input features to HBAC can be beneficial for bias identification. We explore the HBAC results by combining different sets of features including SHAP values, error labels, regular and sensitive features.To evaluate the clustering performance for this specific purpose of bias identification, we propose three quality criteria: the clusters should exhibit (i) distinctive error rates, (ii) distinctive sensitive features, and (iii) general cluster separability. Using the COMPAS dataset, we experiment with three clustering methods that can be embedded within HBAC: K-means, K-Prototypes, and DBSCAN. Our study shows that when SHAP values are excluded from the HBAC input feature combinations, the identified clusters have high quality across all criteria and clustering methods. When SHAP values are included, the general cluster separability largely decreases for most of the feature combinations, while the other two criteria seldom improve. Furthermore, clustering using only SHAP values yields poor results for all quality criteria.These results question the usefulness of SHAP values as indicators for AI bias identification. Future work must further investigate such potential limitations of SHAP values, which might not be suitable for post-hoc bias analysis.

# Getting started
To replicate our experiments, you'll need the following datasets:
    Compas_error_shap.csv: Use this dataset to run the clustering analyses in the provided notebooks (K-Means, K-Prototypes, DBSCAN).
    compas-scores-two-years.csv: Use this original dataset from COMPAS for running the pre-processing notebooks.

# Run the notebook
git clone https://github.com/MDankloff/ClusterCompas.git

# Contact
This code was developed by Mirthe Dankloff and Emma Beauxis-Aussalet. 

For questions about the paper or code please contact: m.e.dankloff@vu.nl, e.m.a.l.beauxisaussalet@vu.nl.
