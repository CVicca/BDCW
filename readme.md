In regards to the dataset chosen.
The dataset used for this exercise was the records of total rainfall over the UK spanning months and years. The data was 
originally split into the year, the twelve months and the total rainfall over that year. The data spanned from 1836 to 2023.
The year was removed from the pool and the total rainfall was replaced by checking if it was within 150 of the average of 
UK rainfall and titled accordingly.

In regards to the use and purpose of the dataset.
Predicting whether the rainfall will be within the average of the year. This can have multiple uses for example catching trends
in which subsiquent years have had repeatedly higher than average rainfall or catching possible droughts early on in the year 
to prepare.

On the topic of other papers dealing with a related topic to the data Analysis of Weather Forecasting Techniques (https://www.researchgate.net/publication/353428752_Analysis_of_Weather_Forecasting_Techniques)
compares and contrasts the costs and benefits of various models of predicting the weather forecast. Whist each model has a specialty
the other factors of weather always suffer or simply cannot be predicted by the models. Weather is, as is pointed out in the article, still a very difficult topic
to predict.

In regards to exploration of the dataset.
The original analysis of the dataset was completed using Random forest. This, however, only gave an accuracy rating of around
68.42%. There was a possibility that this was simply due to the nature of the dataset itself as weather and therefore rainfalll are
nutoriously hard to predict. However the confusion matrix showed that most incorrect predictions were heavily squewed towards the
average label with heavy rainfall having been the worst effected not containing a single correct prediction. The speculation
for this event was the lack of this result in the training set as it was much more common towards the end of the data set as
opposed to the beginning. With this conclusion in mind the response was to find a method to cluster the data to increase the 
likelyhood that it would be correctly trained to identify the three different types. KMeans was chosen to accomplish this but 
does not function when used with strings and as such the label of ann (annual) was repaced with a numberical representation:
0 for light rainfall, 1 for average rainfall and 2 for heavy rainfall. 
After implementing the use of KMeans to cluster data for the label the accuracy of the model increased to around 71.93%.
With the disparity in occurance of results with average rainfall containing a far greater number of results than light rainfall and light rainfall again containing a significntly
higher number of occurances than heavy rain it has been found difficult to get any accurate results on heavy rainfall.
