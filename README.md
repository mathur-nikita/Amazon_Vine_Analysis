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
  - 39% of Vine reviews were 5-star reviews.

## Summary

In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
