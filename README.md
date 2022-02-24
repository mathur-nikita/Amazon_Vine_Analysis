# Amazon_Vine_Analysis

## Overview 

### Purpose

We are tasked with analyzing Amazon reviews written by members of the paid Amazon Vine program.  We have access to datasets containing reviews of a specific product type, and after selecting one of these datasets we are using the ETL process to extract the data, transform it, and then load it into an AWS RDS instance.  After that we are determining if there is any bias towards favorable reviews from Vine members in the chosen dataset.

### Resources

- Google Colab 
- PySpark
- pgAdmin
- AWS
- Amazon Review Dataset for Video Games 
  - (https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz)
- screenshots

## Results

After the table of Vine Reviews was loaded, the dataset was further refined to help with anaylsis and calculations.

### Dataset Refinement Steps

![1.PNG](https://github.com/mathur-nikita/Amazon_Vine_Analysis/blob/main/screenshots/1.JPG)

![2.PNG](https://github.com/mathur-nikita/Amazon_Vine_Analysis/blob/main/screenshots/2.JPG)

![3.PNG](https://github.com/mathur-nikita/Amazon_Vine_Analysis/blob/main/screenshots/3.JPG)

![4.PNG](https://github.com/mathur-nikita/Amazon_Vine_Analysis/blob/main/screenshots/4.JPG)

### Calculations

The following calculations were completed.

![5.PNG](https://github.com/mathur-nikita/Amazon_Vine_Analysis/blob/main/screenshots/5.JPG)

- How many Vine reviews and non-Vine reviews were there?
  - There were a total of 94 Vine reviews (paid).
  - There were a total of 40471 non-Vine reviews (unpaid).

- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
  - 48 Vine reviews had 5-star reviews.
  - 15663 non-Vine reviews had 5-star reviews.

- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
  - 51% of Vine reviews were 5-star reviews.
  - 39% of non-Vine reviews were 5-star reviews.

## Summary

Based on the results from this analysis, it would seem that there is potentially a slight positivity bias for reviews in the Vine program.  Just over half of the reviews of Vine members had 5 stars, but the percentage of non-Vine reviews was ~10% lower.  

Our current analysis looks at reviews from purchasers who are Vine members and those who aren't, but we could also take a look at the "verified_purchase" column to see if Vine members are more likely to leave certain reviews based on their verified member status.  We could also see if existing Vine members who left reviews have left ones that readers would find useful via the "helpful_votes" column.  We are also only considering 5-star reviews in our analysis, but we could adjust that to include 4-star reviews to see how positively Vine members and non-Vine members tend to respond.
