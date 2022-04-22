# Amazon_Vine_Analysis
Big Data
**MODULE 16**

**Challenge**

**Amazon Vine Program**

**Overview:** The purpose of this project is to analyze Amazon reviews written by members of the paid Amazon Vine program, a service that allows manufacturers and publishers to receive reviews of their products and determine if there are any biases between Vine members and Non-Vine member's reviews.

Companies that will pay a fee to Amazon and may provide free products to Vine members who are then required to publish a review. In order to determine if there is any bias towards favorable reviews from Vine members vs. non-members, we need to identify the percentage of 5 star ratings to total rating. As part of this exercise, we were asked to choose from 50 datasets to extract, transform and load into a dataframe in order to complete our analysis.  

I have picked dataset **Outdoors** from Amazon Dataset and did my analysis.
(https://mc16outdoors.s3.amazonaws.com/amazon_reviews_us_Outdoors_v1_00.tsv)

I used PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then, I used Pandas to determine if there is any bias toward favorable reviews from Vine members in the dataset.

**Results:**
The dataset had over 3 million reviews recorded. In order to focus on reviews that would be considered more likely to be helpful, we needed to filter the dataset by:

Count of Total Votes equal or greater than 20.
Percent of Helpful Votes to Total Votes equal or greater than 50%.

The results reduced the total number of reviews from 2M to 39.97K. This allowed us to answer the following questions:

1. How many Vine reviews and non-Vine reviews were there?

- Total Vine Reviews – 107

![](https://github.com/AditiOracle/Amazon_Vine_Analysis/blob/main/Resources/paid_total_reviews.png)

- Total non-Vine Reviews - 21005
- 
![](https://github.com/AditiOracle/Amazon_Vine_Analysis/blob/main/Resources/unpaid_total_reviews.png)

2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

- Total 5-Star Vine Reviews - 56

![](https://github.com/AditiOracle/Amazon_Vine_Analysis/blob/main/Resources/5_star_paid.png)

- Total 5-Star non- Vine Reviews - 39869

![](https://github.com/AditiOracle/Amazon_Vine_Analysis/blob/main/Resources/5_star_unpaid.png)

3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

- Percentage 5-Star Vine Reviews – 52.34

![](https://github.com/AditiOracle/Amazon_Vine_Analysis/blob/main/Resources/percentage_paid_5_star_.png)

- Percentage 5-Star non-Vine Reviews – 52.69

![](https://github.com/AditiOracle/Amazon_Vine_Analysis/blob/main/Resources/percentage_unpaid_5_star.png)

**Summary:**

As per my analysis, there is no evidence of bias for reviews in the Vine program. The percentage 5-start rating for paid (52.34) and unpaid (52.69) reviews is almost same.

However, in order to support this assumption further everyone wants to hear the review from the person who has actually used it that is if we have verified their purchase. So while considering the unpaid vine program users we should also consider the verified\_purchase column.

![](https://github.com/AditiOracle/Amazon_Vine_Analysis/blob/main/Resources/verified_purchase.png)

In addition to that, if we have data - how old is the review that would also help us in our analysis because the quality of the product keep on evolving with time.
