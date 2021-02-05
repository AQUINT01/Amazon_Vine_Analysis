# Amazon Vine Program Analysis
## Overview of the Analysis:
Amazon Vine is based on unbiased communication between selected reviewers (**Vine Members**), enrolled sellers, and buyers. Sellers enroll in the program and submit products to be reviewed by Vine Members. The goal is to provide customers with reliable feedback by using reviewers with a high "reviewer rank," meaning they submit frequent, honest feedback that other buyers consider helpful.

For this project,  I selected the dataset for ***Major Appliances***. I used PySpark to perform an ETL process for exporting the dataset, transformed the data, connected to an AWS RDS instance, and loaded the transformed data into pgAdmin.  Finally, I proceeded to use PySpark to detrermine if any bias existed towards favorable reviews from the Vine members in the major appliances product category.  




## Results:
The product category studied was for  Major Appliciances, a dataset totaling 96,840 records. 

![app_df](https://github.com/AQUINT01/Amazon_Vine_Analysis/blob/main/images/appliance_df.png)




Highlighted below is a **Snapshot** of the vendors who paid a small fee to Amazon to have their products reviewed by Vine [ member ] reviewers compared to non-Vine reviews.


### SNAPSHOT | 5-Star Reviews | Vine & non-Vine 
![5starStats](https://github.com/AQUINT01/Amazon_Vine_Analysis/blob/main/images/5star_stats.png)


* ####  Vine reviews vs. non-Vine Reviews
    - A total of 35 paid and 4,957 non-paid reviews were calculated.

* #### 5-Stars Reviews
    - 18 out of 35 paid reviews were 5-Star rated.
    - 1,963 out of 4,957 non-paid reviews were 5-Star rated.

* #### 5-Star Review percentages
    - 51.42%, 5-Star reviews were from Vine members.
    - 39.60%, 5-Star reviews were from non-Vine members.  




## Summary:
The Vine program does its best to discourage incentivize positive coverage to ensure a fair customer review system by enlisting trustworthy reviewers in the program who never deal with the maker of the products. However,  with 51.42% out of 35 Vine reviewers assigning 5-Star to major appliances , I can't guarantee positive reviews were accounted for but I'm confident that any bias is minimal given the stringent methodology for eliminating outliers. 

To guarantee a more bias-free review rate, I would recommend examining those selected 5-star rated appliances and comparing them with non-Vine reviews and looking into active Vine members' number of reviews and frequency to help improve trustworthiness.

