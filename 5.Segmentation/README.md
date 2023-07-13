# Customer Segmentation & Segment Movement Analysis
[![](https://img.shields.io/badge/-K--Means-orange)](#) [![](https://img.shields.io/badge/-Classification-orange)](#) [![](https://img.shields.io/badge/-Python-green)](#) [![](https://img.shields.io/badge/-Google--Colab-green)](#)   

# 0) Project Overview
![ProjectOverview](./img/ProjectOverview.PNG)

# 1) Import Dataset
# 2) Create single customer view

# 3) Clustering
**Notebooks:** [Clustering Model](./V2_1_HDI_Segmentation.ipynb)  
**Google Colab:** [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jane-russ/MADT8101/blob/main/5.Segmentation/V2_1_HDI_Segmentation.ipynb)
#### Features
All the features are taken from single customer view table
#### Choosing K number of clusters
Choose `K = 4` with the lowest silhoette score of 0.26
![choosingK](./img/choosingK.PNG)

#### Clustering Result
![clustering_result](./img/clusterplot.png)

#### Feature Importance
With the cluster labels as classes to predict, train a Random Forest classifier.
![importance](./img/fimp.png)
#### Cluster Interpretation
![y21segment](./img/before.png)
With xxx

# 4) Classification
**Notebooks:** [Classification Model](./ChurnScoring.ipynb)  
**Google Colab:** [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jane-russ/MADT8101/blob/main/5.Segmentation/V2_2_HDI_Classification%(1).ipynb)
#### Model Evaluation
#### Model Results
![y21segment](./img/after.png)

# 5) Segment Movement Analysis
![mvtanalysis](./img/mvtanalysis.PNG)
