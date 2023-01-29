# Amazon Vine Analysis

The purpose of this project is to evaluate if there could be a bias on reviews from Vine reviewers (paid) vs non-Vine ones (unpaid). For this project I chose to analyze the VHS category. I conducted the analysis over total review votes above 20 (looking for significant reviews) and to avoid having division by zero errors later. Then, in order to find the most helpful review votes, I conducted a second filter for only helpful votes above 50% from the total. The hypothesis we want to test is Vine reviewers might tend to provide 5-star reviews on products due to conflict of interest and thus influence on potential customers. On the technical side of this project, I used Spark to ETL the data on Google Colab, and process it to PgAdmin. Also implemented AWS for storage of the final database in the cloud.


---


## Results

The following table provides a summary of the main findings for the VHS Category Reviews on Amazon:

![Vine Reviews](https://user-images.githubusercontent.com/113866707/215303097-ae19099c-7d7c-4cb6-9d68-59403c2e3727.png)


* How many Vine reviews and non-Vine reviews were there?

There was a total of 49 Vine reviews for this category and 151,400 from non-Vine. We can clearly identify that this category is not currently focused on Vine reviewers and depends mostly on non-Vine ones.


* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

From the 49 Vine reviewers of the category, only 9 provided 5-star reviews, whereas for non-Vine ones the total of 5-star reviews were 78,061.


* What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

From the Vine reviews, 18% provided a 5-star review. While for non-Vine reviews the proportion was 52%.


---

## Summary

* State if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.

.
