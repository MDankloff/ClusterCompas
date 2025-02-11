# Using SHAP Values for Clustering-based Bias Identification
This repository contains the code associated with our paper: "Using SHAP Values for Clustering-Based Bias Identification." 

# Repository Structure
The repository is organized into 9 Notebooks:

 **Pre-processing Notebooks (3)**:
 
 Data cleaning, computing SHAP values and error labels to set up experimental conditions for the COMPAS and German Credit dataset. 
 
 Includes preliminary visualizations using t-SNE.
        
 **Clustering Notebooks (6)**:
 
Each notebook covers a different clustering approach: K-Means, K-Prototypes, and DBSCAN (3) for each dataset (x2).

Per Clustering notebook:
* Utils for data prep, clustering, results and visualization
* Clustering
* Experimental set-up
* Evaluation results: Chi-square test and Silhouette score
* In-depth Analysis: one-vs-all cluster comparison and t-SNE 

# Paper abstract
A form of AI bias occurs when a model produces higher error rates for specific demographic groups, which can be identified using sensitive features such as gender or ethnicity, or proxy features such as income or postcode.
Explanation methods like SHAP are also used to address biases in AI models. However, it can be unknown a priori which features lead to higher error rates and which SHAP values are most informative for identifying this bias.
The Hierarchical Bias Aware Clustering (HBAC) algorithm is an unsupervised method designed to identify clusters with higher error rates using any combination of features.
This study has two main objectives: (1) to assess whether including SHAP values in HBAC improves bias identification and (2) to explore how different feature sets – including SHAP values, error labels, sensitive and regular features – affect clustering performance for identifying bias.
We evaluated the quality of the clusters using three criteria: the clusters should exhibit (i) distinctive error rates, (ii) distinctive sensitive features, and (iii) general cluster separability.
Using the COMPAS and German Credit datasets, we experiment with different clustering methods that can be embedded within HBAC: K-Means, K-Prototypes, and DBSCAN.
Our results show that incorporating SHAP values does not improve bias identification and frequently worsens cluster quality. The best performance is achieved when clustering on sensitive features, particularly with K-Means and K-Prototypes.
These findings suggest that SHAP values may have limited utility for identifying bias through error rates, and future work should further examine their effectiveness in post hoc bias assessments.

# Getting started
To replicate our experiments, you'll need the following datasets:

**Compas_error_shap.csv**: Use this dataset to run the clustering analyses in the provided notebooks (compas_K-Means, compas_K-Prototypes, compas_DBSCAN).

**compas-scores-two-years.csv**: Use this original dataset from COMPAS for running the pre-processing notebooks.

**credit_all.csv**: use this dataset to run the clustering notebooks (german_credit_K-Means, german_credit_K-Prototypes, german_credit_DBSCAN).

**german_processed**: use this original dataset from UCI repository to run the pre-processing notebook (German_credit_exploratory) 

# Run the notebook
    git clone https://github.com/MDankloff/ClusterCompasCredit.git

# Contact
This code was developed by Mirthe Dankloff and Emma Beauxis-Aussalet. 

For questions about the paper or code please contact: m.e.dankloff@vu.nl, e.m.a.l.beauxisaussalet@vu.nl.
