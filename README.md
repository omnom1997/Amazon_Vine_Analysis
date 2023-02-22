# Amazon Vine Analysis

## Overview
The purpose for our analysis was to determine if there is any bias toward favorable reviews in the Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a servie that allows manufacturers and publishers to receive reives for their products. Companies like SellBy can pay a small fee to Amazon and provide products to Amazon Vine members who are then required to publish a review. There were 50 or so datasets of reviews for us to analyze, and we picked the video game dataset.

## Results
To begin our analysis process, we extracted our video game dataset into a DataFrame within an AWS RDS database which was connected to our PostgreSQL pgAdmin server. We then transformed the DataFrame into four separate DataFrames that match the table schema created within pgAdmin and loaded those new DataFrames into pgAdmin.

We then continued our analysis by using PySaprk in Google CoLab notebooks to determine if there was any bias towards reviews that we written as part of the Vine program. More specifically, we were determining if having a paid review made a difference in the percentage of five-star reviews.

### Questions and Answers
The results of our inital analysis were as follows:
1. How many vine reviews and non-vine reivews were there

![1](https://user-images.githubusercontent.com/114427019/220786798-75cf52be-d436-469e-87a7-93057487f3ca.png)

![2](https://user-images.githubusercontent.com/114427019/220786835-afee8a54-f3d8-4593-b6e7-afe928e2b781.png)

2. How many vine reviews were 5 stars? How many non-Vine reivews were 5 stars?

![3](https://user-images.githubusercontent.com/114427019/220786976-f427252b-dc75-4681-b959-1ff562614661.png)

![4](https://user-images.githubusercontent.com/114427019/220786991-4c8a6e1e-177e-4d86-85af-9e04b0cd667a.png)

3. What percentage of vine reviews were 5 stars? What percentage of non-vine reviews were 5 stars?

![5](https://user-images.githubusercontent.com/114427019/220787015-330eae4b-22ea-40d7-93a7-a5476f513181.png)

![6](https://user-images.githubusercontent.com/114427019/220787026-efd62de6-442b-4a07-a54c-37e85018f261.png)

## Summary
Based on our inital analsis, there is a positivity bias in the reviews for the Vine program. The percentage of paid five-star reviews is 51% and the percentage of unpaid five-star reviews is 39%. This analaysis is also very skewed because the number of paid reviews is 94 compared to the number of unpaid reviews which is 40,471. 

An additional analysis that we could perform is the same analysis of paid vs unpaid reviews on the raw Vine DataFrame instead of just the reviews with a majority of helpful votes. This would possibly enlarge the dataset that we're analyzing and possibly lead to greater insights about the Vine reviews as a whole rather than just the "helpful" reviews.
