# Churn Scoring
[![](https://img.shields.io/badge/-Classification-orange)](#) [![](https://img.shields.io/badge/-Python-green)](#) [![](https://img.shields.io/badge/-Google--Colab-green)](#) 

**Notebooks:** [Classification Model](./ChurnScoring.ipynb)  
**Google Colab:** [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jane-russ/MADT8101/blob/main/4.ChurnScoring/ChurnScoring.ipynb)

## 1) Import Dataset
The data is an ecommerce dataset including the following: 
- CustomerID	Unique = customer ID
- Churn = Churn Flag
- Tenure = Tenure of customer in organization
- PreferredLoginDevice = Preferred login device of customer
- CityTier = City tier
- WarehouseToHome = Distance in between warehouse to home of customer
- PreferredPaymentMode = Preferred payment method of customer
- Gender = Gender of customer
- HourSpendOnApp = Number of hours spend on mobile application or website
- NumberOfDeviceRegistered = Total number of deceives is registered on particular customer
- PreferedOrderCat = Preferred order category of customer in last month
- SatisfactionScore = Satisfactory score of customer on service
- MaritalStatus = Marital status of customer
- NumberOfAddress = Total number of added added on particular customer
- Complain = Any complaint has been raised in last month
- OrderAmountHikeFromlastYear = Percentage increases in order from last year
- CouponUsed = Total number of coupon has been used in last month
- OrderCount = Total number of orders has been places in last month
- DaySinceLastOrder = Day Since last order by customer
- CashbackAmount = Average cashback in last month

Number of observations: 5,630   
Number of variables: 20

## 2) EDA
EDA Shows that the data is quite imbalance between churn and not churn customers. 
### Frequency distribution of categorical variables:
![FrequencyDistribution](./img/FrequencyDistribution.png)  

### Summary statistics of numerical variables by Churn Flag:  
![Describe1](./img/Describe1.PNG)
![Describe2](./img/Describe2.PNG)
![Describe3](./img/Describe3.PNG)

### Nurmerical variable distribution:
![KDE](./img/KDE.png)   

### Missing Value: 
-  `Tenure `                         264
-  `WarehouseToHome `                251
-  `HourSpendOnApp `                 255
-  `OrderAmountHikeFromlastYear `    265
-  `CouponUsed `                     256
-  `OrderCount `                     258
-  `DaySinceLastOrder `              307

* Based on KDE plot, there features (`Tenure ` , `WarehouseToHome `, `OrderAmountHikeFromlastYear ` , `CouponUsed ` , `OrderCount ` , `DaySinceLastOrder `) are skewed hence we used median to impute missing value
* For  `HourSpendOnApp ` , it is multinomial so we used mode to impute missing value

## 3) Feature Engineering
## 4) Model Creation & Evaluation
## 5) Result Feature Importance
