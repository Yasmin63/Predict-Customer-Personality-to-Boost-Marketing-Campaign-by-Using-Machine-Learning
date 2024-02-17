## Background
"A company can grow rapidly when it knows its customer personality behavior, so that it can provide better services and benefits to customers who have the potential to become loyal customers. By processing historical marketing campaign data to improve performance and target the right customers so that they can transact on the company's platform, from these data insights, our focus is to create a cluster prediction model to make it easier for companies to make decisions."



## Conversion Rate Analysis 

![image](https://github.com/Yasmin63/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/146631940/de5533b9-e423-4ead-8fa9-98c9be9ddb81)

The difference in income from the customer affectsthe conversion rate value, where for theconversion rate generally gets higher as income gets higher. The highest conversion rate value occurs in the income range of 90-100 million.
To increase the value ofconversion rate, it would be better if the marketing teamprioritize target customers who fall intoin the high income category, with income >= 80 million.

![image](https://github.com/Yasmin63/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/146631940/e76d35c5-08d5-4e52-a6fc-c88e08ec2c9d)

The difference in the number of transactions from customersaffect the conversion rate value, wherethe higher the amount of spending, the higher the conversion rate. 
The marketing team can maintain or improve its good performance, by providing rewards in the form of discounts for customers who spend above 2.5 million so that spending in the highest category can continue to increase.

![image](https://github.com/Yasmin63/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/146631940/569cc6ec-a12c-4886-a149-0870ea9dc484)

The age difference of the customer is not too differentsignificantly for the conversion rate value in the 20-80 age range, the highest conversion rate value is in the >80 age range.
The difference in age range has a considerable influence on the conversion rate. Recommendations that can be made include segmenting the market and providing content that is suitable for each segmentation based on age.



## Data Cleaning and Preprocessing
- Handling missing value. Drop features that have missing values include Income_Group, Income, Converson_Rate.
- Feature selection. Remove unnecessary feature for further feature encoding
- Feature Encoding. Perform feature encoding: Eduacation, Marital_Status, Age_Group, Spending_Group.
- Standardization. The Features that are standardized: Income, Recency, NumWebVisitsMonth, Age, Total_Spending, Total_Transaction



## Data Modeling
![image](https://github.com/Yasmin63/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/146631940/d16ea792-9a19-477e-af4d-3c5c9db18c85)

The graph above is the elbow method in terms of inertia where the size describes how far the data points in 1 cluster are from the cluster center. A significant decrease in distortion score value occurs from point 2 to point 3, after which the decrease in distortion score value is not too significant. This indicates that the elbow point of the plot is at k = 3, so the cluster recommendation from the dataset is divided into 3 clusters.

![image](https://github.com/Yasmin63/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/146631940/1015ed3e-9951-4872-a44e-1d4c9f1f989c)

Comparison between silhouette score metrics and number of clusters. Silhouette Score measures how close each data point is to the cluster they belong to compared to other clusters. The range of Silhouette Score values is -1 to 1, where a positive value indicates that the object is in the right cluster, while a negative value indicates that the object may be placed in the wrong cluster. In the Silhouette Score plot, the highest score is in cluster range 2 with a score value > 0.3.



## Customer Personality Analysis for Marketing Retargeting

The following is a visualization of some of the features for Cluster 0, 1, 2 and 3:
Income per Cluster: This plot shows the income profile for each cluster. Cluster 1 has the largest income, while Cluster 3 has the lowest income.
Age per Cluster: This plot shows the age profile for each cluster. Cluster 1 tends to have a higher age, while Cluster 3 has a lower age.
Spending per Cluster: This plot shows the average product purchase amount within each cluster. Cluster 1 stands out with a higher number of web purchases.

Cluster 0
Income: Low, well below the overall average.
Product Spending (`Mnt`, etc.): Low spending on all products.
Age (`Age`, `Age_Group`): Younger than average.
Cluster 1
Income (`Income`): Medium, overall average.
Product Spending (`Mnt`, etc.): Average spending on all products.
Age (`Age`, `Age_Group`): Exactly average.
Cluster 2
Income (`Income`): Medium, above the overall average.
Product Spending (`Mnt`, etc.): Above average spending on all products.
Age (`Age`, `Age_Group`): Above average.
Cluster 3
Income (`Income`): High, well above the overall average.
Product Spending (`Mnt`, etc.): High spending on all products.
Age (`Age`, `Age_Group`): Well above average.

![image](https://github.com/Yasmin63/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/146631940/3c009a56-1885-49f1-8d8e-ca336c5d35dc)

![image](https://github.com/Yasmin63/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/146631940/2361acdf-8184-471e-934c-823f32be1545)

![image](https://github.com/Yasmin63/Predict-Customer-Personality-to-Boost-Marketing-Campaign-by-Using-Machine-Learning/assets/146631940/86cbdf38-d1e9-495a-9d3a-7782f1ed1a87)


Business Recommendations:
By knowing the characteristics of each of these clusters, it is possible to adjust the marketing strategy to meet the needs and preferences of each group of customers. For example, for cluster 2 consisting of customers with high income and large total expenditure, the marketing team may consider offering premium products or services to them while cluster 1 with the opposite characteristics may be more responsive to discount offers or special promotions.
To reduce the number of very low customers and low value customers, we can inform them about our limited discount products and create cheap packages (such as buy 1 get 1 free) because they have the lowest total amount in our store.
To retain medium and high value customers, we can give them 'special treatment' such as providing bonuses and gifts.
















