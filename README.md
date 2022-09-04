# Band Preference Prediction

**Introduction**

The purpose of this report is to predict the brand preference from customers for Blackwell Electronic to decide which manufacture should be pursued with a deeper strategic relationship. The prediction is made on two data survey, one is complete dataset, the other one is incomplete, corrupt dataset.


Below are the data features that were collected from customers:

1). 6 Features were used for training / testing mode ls:

**Salary** - not including bonus

**Age**

**Level of Education** (6 different levels range from Less Than High School Degree to Master’s / Doctoral Degree)

**Name of Primary Car** (19 different brands given, choice 20 is ‘None of the above’ if customer has a different car from the list)

**Zip Code** (9 zip codes given from New England to Pacific)

**Credit**

2). 1 Feature used for prediction

**Brand** -   0 - Acer,  1 - Sony


**Analysis**

**_Model Comparison and Selection for Training / Testing Data & Feature Importance_**

3 predictive models were used for training and testing dataset, the testing scores were pretty close between these models. As the above graph shows, Random Forest has the highest overall accuracy and kappa score when applying parameter mtry=4. Gradient Boosting has slight lower score, the tuneLength was set between 1 and 5, tuneLength 5 had higher score. C50 has the lowest score compare to the other two models. Therefore, Random Forest was selected for prediction as it has the highest training / testing score.

![image](https://user-images.githubusercontent.com/80385435/188296071-fa8b99ae-0417-443e-9a33-3f56d51b98b8.png)

<img width="709" alt="Screen Shot 2022-09-03 at 8 37 10 PM" src="https://user-images.githubusercontent.com/80385435/188296095-8bdcde01-9b8b-48b6-94a7-0b816abfbfc1.png">

All 3 models indicate the most important features from the dataset are Salary and Age, while Random Forest and Gradient Boosting models have Credit as the 3rd import feature, Car and ZipCode have little importance compare to other features, eLevel has 0 importance. The C50 model indicates ZipCode as the next important feature after Salary & Age, the other 3 features Car, eLevel and Credit have 0 importance. 


**_Brand Preference Prediction_**

The above graph shows the number of preferences for the computer brand ( Acer and Sony ) between Complete Survey data, Corrupt Survey data and the entire dataset. More customers preferred Sony brand in each single dataset,  over 9000 customers preferred Sony brand, and a bit over 5000 customers chose the Acer brand. 


**Conclusion**

<img width="594" alt="Screen Shot 2022-09-03 at 8 38 09 PM" src="https://user-images.githubusercontent.com/80385435/188296136-e0b177b0-389b-4c3c-89f9-a259aca0ab8a.png">


The predicted brand preference for customers from Blackwell Electronic is: 62% of customers prefer Sony and 38% of customers prefer Acer brand. 

The most important features that would affect the brand preference are (from most to least):
Salary, Age, ZipCode and Credit, the remaining features Car and Elevel are not that relevant to our prediction. 
