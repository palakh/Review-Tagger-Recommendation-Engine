# Review-Tagger-Recommendation-Engine
![CLV](https://cdn-images-1.medium.com/max/800/1*t870WiCzb-5zkLuGjDuDAA.png)

## INTRODUCTION
E-commerce industries are heavily reliant on marketing for Customer Acquisition and Retention. 

Recommendation Engines and Product reviews are an essential part of an online store's branding and marketing. They help build trust and loyalty therefore providing the customer accessibility to the their true demand and apt subset of reviews is crucial to reduce the conversion period. 

Another important factor for the company to focus on is their Inventory process since minute reductions in the delivery times can lead to higher customer retention as well. Identifying issues affecting the process is crucial.

## PROBLEM STATEMENT
The task at hand is to improve the overall experience for the consumer and ideally mitigating problematic areas. We focus on 3 main things over here - 
1. Recommendation Engine - Recommend the correcr subset of products based on consumer affinity 
2. Review Tagger - Allow the consumers to select the subset of reviews they wish to read through pattern identification thereby reducing conversion time
3. Inventory Process - Focus on the overall inventory process to understand why the process is lagging and provide recommendations to improve the efficiency

Finally, provide the overall analysis

## APPROACH AND CONCEPTS

* **Data gathering and cleaning** - We are considering two types of datasets 
1. The dataset contains 105,571 reviews for ~6000 products split in 68 different categories
2. Inventory Process dataset informs the process each product has followed within 7 day timeline


* **Data Pre-processing** - 
1. Creating a Serial Indexing for products
2. Extracting Retail and Rental Price
3. Converting height column from string to numeric in inches
4. Variable type conversions (e.g. datetype, int etc)
5. Data Imputation using mean method
6. Resolve Scraping issues (eg Bust Size contains bodytype)
7. Understanid products with no reviews and looking for some similarity
8. Splitting Data into meaningful information (Product Info)
9. Running Topic Modeling to observe which clothes are not selected and do they have any similarities


## **Exploratory Data Analysis** - 

1. According to occasions, Weddings has the most diverse range with respect to the rental prices which is justified since during the inception of the company, major attraction was weddings and parties.

2. We observe products following a linear relationship between retail and rental price. Most of our producte lie in the retail in greater or less than 250 dollars and rental in less than 50 dollars.

3. 96 products have no reviews. Out of no review products, 86% are imported. Most of these clothes are made of polyester or cotton and are either printed or floral, are wrap dresses or tops/skirts with zippers. We don't see any correlation between no_reviews items - not liked by a lot and rental and retail prices.

## **Modeling** - 
  * Review Tagger: For the model implementation, we have follwed 
  
  
  * Segmentation: To achieve segmentation, we perform clustering on all 3 metrics individually - Recency, Frequency, and Monetary value. k-means is used as the model and based on the optimum number of clusters, we perform weighted sum and achieve an overall score. After analyzing the mean Recency, Frequency, and monetary values of these clusters, we can observe three major groups being formed. We will label then Low Value, Mid Value, and High-Value customers



## REPOSITORY DETAILS
[Code](https://github.com/palakh/Review-Tagger-Recommendation-Engine/tree/main/Code)
