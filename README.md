# Amazon_Vine_Analysis
Big Data
**MODULE 16**

**Challenge**

**Amazon Vine Program**

**Overview:** We areanalyzing Amazon reviews written by members of the paid Amazon Vine program. I have picked dataset &quot;Outdoors&quot; from Amazon Dataset and did my analysis.
[This is the link to file] (https://mc16outdoors.s3.amazonaws.com/amazon_reviews_us_Outdoors_v1_00.tsv)


I used PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then, I used Pandas to determine if there is any bias toward favorable reviews from Vine members in the dataset.

**Results:**

1. How many Vine reviews and non-Vine reviews were there?

- Total Vine Reviews – 107
- Total non-Vine Reviews - 21005

2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

- Total 5-Star Vine Reviews - 56
- Total 5-Star non- Vine Reviews - 39869

3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

- Percentage 5-Star Vine Reviews – 52.34
- Percentage 5-Star non-Vine Reviews – 52.69

**Summary:**

As per my analysis, there is no evidence of bias for reviews in the Vine program. The percentage 5-start rating for paid (52.34) and unpaid (52.69) reviews is almost same.

However, in order to support this assumption further everyone wants to hear the review from the person who has actually used it that is if we have verified their purchase. So while considering the unpaid vine program users we should also consider the verified\_purchase column.

In addition to that, if we have data - how old is the review that would also help us in our analysis because the quality of the product keep on evolving with time.
