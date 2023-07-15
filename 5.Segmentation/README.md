# Customer Segmentation & Segment Movement Analysis
[![](https://img.shields.io/badge/-K--Means-orange)](#) [![](https://img.shields.io/badge/-Classification-orange)](#) [![](https://img.shields.io/badge/-Python-green)](#) [![](https://img.shields.io/badge/-Google--Colab-green)](#)   

# 0) Project Overview
![ProjectOverview](./img/ProjectOverview.PNG)

# 1) Import Dataset
HDI was started in 1986 by Mr. Peter Chia, who desired to provide a better life for his family. HDI emerged as a trailblazer in the development of the Network Marketing Business in Asia, specifically in Singapore, Malaysia, Indonesia, Hong Kong, and the Philippines. The company offers natural products from bee, they  have five main categories, namely supplements for adult & Kid, personal care, skincare, food and beverages.
#### Provided Dataset
1. data member : master data of downline and his/her sponsor
2. transaction 2021 - 2022 : contains sales by bill from year 2021 to 2022
#### Created Dataset
1. sponsor master : master data of sponsor and no. of downline per sponsor
2. salesbyitem 2021 - 2022 : extract json product file to sales quantiy by item

# 2) Create single customer view
base on datasets above, we create the following data single customer view table:      

![SCV](./img/SCV.png)     

- List of SCV Features
  
![feature](./img/feature.PNG)

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
![before2](./img/before2.PNG)

# 4) Classification
**Notebooks:** [Classification Model](./V2_2_HDI_Classification%20(1).ipynb)  
**Google Colab:** [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jane-russ/MADT8101/blob/main/5.Segmentation/V2_2_HDI_Classification%20(1).ipynb)
#### Model Evaluation
![ModelResults](./img/ModelResults.PNG)
#### Model Results
![after2](./img/after2.PNG)

# 5) Segment Movement Analysis
![mvtanalysis](./img/segmentation_movement.png)

![BeforeAfter](./img/Segmentation_BeforeAfter_final.PNG)

Movement Analysis:
- Successfully increase purchased quantity through increase in unique items in both Star group (online and offline)
- Drop-off of Gold (3) by 36%, transitioning to become stars rank (0, 1).
- Those who remained as gold level have doubled their purchases.
- Contrastingly, Diamond' spending has declined by 42%.
- The decrease in Gold level resulted in a 26% reduction in the number of Diamond, from 70 to 52 in 2022.

# 6) Business Recommendation
### Insights Recap 
- Do Good: Cross-category promotion Product Portfolio curation &  to increase unique items and sales qty
- Do Better: Membership retention (especially in gold and diamond tier) & Membership progress through tiers

### Next Steps: 
![nextsteps](./img/nextsteps.png) 
