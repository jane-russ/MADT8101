# Customer Segmentation
[![](https://img.shields.io/badge/-K--Means-blue)](#) [![](https://img.shields.io/badge/-DAX-blue)](#) [![](https://img.shields.io/badge/-Python-blue)](#) [![](https://img.shields.io/badge/-Google--Colab-blue)](#) [![](https://img.shields.io/badge/-Power--BI-blue)](#) [![](https://img.shields.io/badge/-Dashboard-blue)](#)

The diagram below describes how this project was implemented.


## 1) Import Dataset
The given Supermarket dataset contains 956K rows of sales transactions at sales-item level. The data include historical data from year 2006 to 2008.
We initially explore the data and found that members contributes to 85% of total sales. Hence, we want to segment customers into groups so that the supermarket have behaviour insights and able to customize the approach for each segment. 
![Dataset_Overview](./Dataset_Overview.PNG)

## 2) Generate Customer Single View
Total 3,439 customers
## 3) K-Means Clustering
**Notebooks:** [K-Means Model](./Revise_of_Supermarket_Clustering.ipynb)  
**Google Colab:** [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jane-russ/MADT8101/blob/main/2.Basic%20Customer%20Analytics%20%26%20Single%20Customer%20View/Revise_of_Supermarket_Clustering.ipynb)
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
