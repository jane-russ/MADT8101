# Customer Segmentation
[![](https://img.shields.io/badge/-K--Means-blue)](#) [![](https://img.shields.io/badge/-DAX-blue)](#) [![](https://img.shields.io/badge/-Python-blue)](#) [![](https://img.shields.io/badge/-Google--Colab-blue)](#) [![](https://img.shields.io/badge/-Power--BI-blue)](#) [![](https://img.shields.io/badge/-Dashboard-blue)](#)
## 1) Import Dataset
## 2) Generate Customer Single View
## 3) K-Means Clustering
**Notebooks:** [K-Means Model](./Revise_Clustering_Result.ipynb)  
**Google Colab:** [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jane-russ/MADT8101/blob/main/2.Basic%20Customer%20Analytics%20%26%20Single%20Customer%20View/Revise_Clustering_Result.ipynb)
#### Features
##### Overall Behaviour
* `FQ`
* `Total_Spend`
* `MTBP`
* `Life_Time`
* `ARPU`
* `CLTV`
* `MOD_CUST_LIFESTAGE_CD`
* `MOD_CUST_PRICE_SENSITIVITY_CD`
##### Price sensitivity Ratio
* `BASKET_PRICE_SENSITIVITY_LA`
* `BASKET_PRICE_SENSITIVITY_MM`
* `BASKET_PRICE_SENSITIVITY_UM`
* `BASKET_PRICE_SENSITIVITY_XX`
##### Basket Type Ratio
* `BASKET_TYPE_Small_Shop`
* `BASKET_TYPE_Top_Up`
* `BASKET_TYPE_Full_Shop`
* `BASKET_TYPE_XX`
##### Mission Ratio
* `BASKET_MISSION_Fresh`
* `BASKET_MISSION_Grocery`
* `BASKET_MISSION_Mixed`
* `BASKET_MISSION_Non_Food`
##### Basket Size Ratio
* `BASKET_SIZE_L%`
* `BASKET_SIZE_M%`
* `BASKET_SIZE_S%` 
 
#### Choosing K number of clusters
Choose `K = 4` with the lowest silhoette score of 0.11
![elbow](./elbow.png)
![silhoetterscore](./silhoetterscore_compare.PNG)
![silhoetterplot](./silhoetterplot_K4.png)

#### Clustering Result
![clustering_result](./clustering_result.png)

## 4) Clustering Result Analysis
**Notebooks:** [Clustering Result EDA](./Revise_Clustering_Result.ipynb)  
**Google Colab:** [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jane-russ/MADT8101/blob/main/2.Basic%20Customer%20Analytics%20%26%20Single%20Customer%20View/Revise_Clustering_Result.ipynb)

#### EDA
##### Describe Features
![describe1](./Features_Describe_Buying1.PNG)
![describe2](./Features_Describe_Buying2.PNG)
![describe3](./Features_Describe_PriceSensitivity.PNG)
![describe4](./Features_Describe_BasketType.PNG)
![describe5](./Features_Describe_MIssion.PNG)
![describe6](./Features_Describe_Size.PNG)
##### KDE
![kdeplot](./Features_KDE.png)
##### Bloxplot
![boxplot](./Features_Boxplot.png)
#### Feature Importance
With the cluster labels as classes to predict, train a Random Forest classifier.
![importance](./Features_Importance.png) 
## 5) Interpretation
