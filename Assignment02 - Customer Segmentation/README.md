# Customer Segmentation
## 1.) Import Dataset
The given Supermarket dataset contains 956K rows of sales transactions at sales-item level. Imported the file into Google BigQuery.

Note: the dataset received is just a part of Dunhumbly public dataset which is way more bigger. There seems to be historical data from only 2 stores from year 2006 to 2008.

## 2.) Prepare customer single view
### transfrom data
CUST_LIFESTAGE

OA, OF, OT, PE, YA, YF | 1,2,3,4,5,6
----- |------


Basket_Type

Top Up, Full Shop, Small Shop, XX	| 1,2,3,0
---- | ----


BASKET_DOMINANT_MISSION
Grocery, Fresh, Mixed, Nonfood, XX | 1,2,3,4,0
----- |------

### Define features
* Total visits = COUNT(DISTINCT BASKET ID)
* Ticket size = SUM(SPEND)/COUNT(DISTINCT BASKET ID)
* Total no. of SKUs
* TotalSpend = SUM(SPEND)
* FirstDate = MIN(SHOP_DATE)
* LastDate = MAX(SHOP_DATE)
* SHOP_HOUR = MEAN(SHOP_HOUR)
* LifeStage = MIN(CUST_LIFESTAGE)
* BasketType = MAX(BASKET_TYPE) BasketMission = MAX(BASKET_DOMINANT_MISSION)
* Total_days = LastDate - FirstDate +1
* recency = max(date) - (LastDate)

## 3.) Cluster customers
A Comparative Efficiency of Clustering using Silhouette, Calinski-Harabasz, Davies-Bouldin

![image](https://user-images.githubusercontent.com/92771399/147724184-832d8fec-0a53-495e-b0c1-c9255166d383.png)

The results of the run concluded that Spectral Clustering and KMeans Clustering were the most efficient in classification.

### KMeans Clustering
Create KMean model

#### Choosing K number of clusters
Choose K = 5

![image](https://user-images.githubusercontent.com/92771399/147724269-bccf96f2-e28d-489b-9b8d-3ebec6c6b61a.png)

## 4.) Clustering Result Analysis
### Spectral Clustering

![image](https://user-images.githubusercontent.com/92771399/147724319-596259b9-7ff4-44e0-9c2a-c59ecfa32acf.png)

As a result of using Spectral Clustering in segmentation, it is evident that the classification is poor.

### KMeans Clustering

![image](https://user-images.githubusercontent.com/92771399/147724363-5e897fa8-dcf1-4af8-93db-9ab19197b9d9.png)

![image](https://user-images.githubusercontent.com/92771399/147724384-fa179049-87cc-4c4b-8666-62bb6a59d699.png)

## 5.) Interpretation
![image](https://user-images.githubusercontent.com/92771399/147724420-3eab522f-3c01-453b-af2f-7fb508c0980d.png)


