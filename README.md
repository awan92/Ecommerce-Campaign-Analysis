# Ecommerce Campaign Analysis to get possible Marketing Campaigns for promoting the New Product
A fast-food chain plans to add a new item to its menu. However, they are still undecided between the three possible marketing campaigns for promoting the new product. In order to determine which promotion has the greatest effect on sales, the new item is introduced at location in several randomly selected markets. A different promotion is used at each location, and the weekly sales of the new item are recorded for the first four weeks.
- Tools : Google Sheets

## Overview of Dataset
There are 7 columns in campaign dataset, such as:
- MarketID : Unique identifier for market
- MarketSize : Size of market area by sales
- LocationID : Unique identifier for store location
- AgeOfStore : Age of store in years
- Promotion : One of three promotions that were tested
- Week : One of four weeks when the promotions were run
- SalesInThousand : Sales amount for a specific LocationID, promotion and week

## Store Characteristics of Market Size
- **Small** : Only 15 stores with the small market size, the average age of store is 10.8 years old, with the youngest is 1 years old and the oldest is 28 years old, the average sales is $57.4K, with the lowest is $36.17K and the highest is $70.6K.
- **Medium** : There are 80 stores with medium market size, the average age of store is 8.78 years old, with the youngest is 1 years old and the oldest is 27 years old, the average sales is $43.98K, with the lowest is $17.34K and the highest is $65.11K.
- **Large** : There are 42 stores with large market size, the average age of store is 7 years old, with the youngest is 1 years old and the oldest is 24 years old, the average sales is $70K, with the lowest is $39.36K and the highest is $99.65K.

## Campaign Effect
There is not so much difference between each promotion that affected general sales. However we suggest to focus on promotions 3 which generate the most sales.

![Campaign Effect](https://user-images.githubusercontent.com/100940506/232796727-55520543-d934-4819-b43e-3fd93e4da2b5.PNG)

## Promotion vs Market Size
To determine if the market size affect the result of campaign we divided three test between market size using t-test in which we assumpt the variance is not equal.
**Hypothesis for each t-test :**
- **H0** : Different market size has no effect to generated sales.
- **H1** : Different market size affected generated sales.
In which we will reject H0 if P-Value (calculated) < P-Value Threshold (0.05) 

## Large vs Medium

![Large vs Medium](https://user-images.githubusercontent.com/100940506/232798127-da43711a-e33b-4b8e-b60a-2a7e3cd0420f.PNG)

**Conclution :**
P-Value (Calculated) < P-Value threshold, it means reject H0. In which market type affected the results of campaign significally.

## Large vs Small

![Large vs Small](https://user-images.githubusercontent.com/100940506/232798764-0150356b-b70c-4336-8c58-ef1875a0fe9a.PNG)

**Conclution :**
P-Value (Calculated) < P-Value threshold, it means reject H0. In which market type affected the results of campaign significally.

## Medium vs Small

![Medium vs Small](https://user-images.githubusercontent.com/100940506/232799231-d8a6b259-64a6-4d08-bab0-7c3a3e8c667f.PNG)

**Conclution :**
P-Value (Calculated) < P-Value threshold, it means reject H0. In which market type affected the results of campaign significally.

## Sales vs Market Size vs Age of Store

![image](https://user-images.githubusercontent.com/100940506/232799821-f16e871d-e450-416d-bd78-ef83fcfc442c.png)

P-Value for both independents variables are less than P-Value threshold (0.05) it means both variables (market size & age of store) are affected generated sales.

**SalesinThousands** = 21.6273404 **MarketSize** + 0.5320943264 **AgeofStore**
