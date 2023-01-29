# Amazon Vine Analysis

The purpose of this project is to evaluate if there could be a bias on reviews from Vine reviewers (paid) vs non-Vine ones (unpaid). For this project I chose to analyze the DVD category. I conducted the analysis over total review votes above 20 (looking for significant reviews) and to avoid having division by zero errors later. Then, in order to find the most helpful review votes, I conducted a second filter for only helpful votes above 50% from the total. The hypothesis we want to test is Vine reviewers might tend to provide 5-star reviews on products due to conflict of interest and thus influence on potential customers. On the technical side of this project, I used Spark to ETL the data on Google Colab, and process it to PgAdmin. Also implemented AWS for storage of the final database in the cloud.


---


## Results

The following table provides a summary of the main findings for the DVD Category Reviews on Amazon:

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


From this analysis, we can conclude that there is no bias on this category for Vine reviewers since a) the whole Vine population of reviewers represent only 0.03% from the total, and only 18% Vine reviews have 5-star review.


As mentioned earlier, this analysis filters only reviews with total votes equal or greater than 20 and then a new filter based on helpful votes equal or greater than 50%. In order to have a broader analysis on the possible bias, it could be possible to lower the filtered standards.
For this case, I ran a similar test only changing parameters of filter from reviews with total votes equal or greater than 5 and then a new filter based on helpful votes equal or greater than 10%
Still, there is no present bias on 5-star reviews from Vine reviewers as seen in the following table:

![Captura de pantalla 2023-01-29 a la(s) 13 12 55](https://user-images.githubusercontent.com/113866707/215350474-da1d9767-6a2d-400f-bfaa-27d94330687e.png)

