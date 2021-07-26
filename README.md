# Neural-Network to predict beer style
In the dataset we have, there is beer name, beer style, beer description and brewery, we also have 4 source features: alcohol by volumne; average rating, minum IBU and maximum IBU. We also have 11 tasting profile features which is defined by word counts found in up to 25 reviews of each beer. These features are astringency, sour, salty, fruits, hoppy, spices, malty, body, alcohol, bitter and sweet.

When we think about the rational of the prediction model, we came across the question that is should min IBU and max IBU be included in the prediction model?
As each beer style has its IBU range and there is high correlation between beer style and IBU range, so we decide to exclude Min IBU and Max IBU from our model features.
So the x values in our prediction model are 13 features and y values are beer style or average review ratings. 


The first question we addressed is if we can predict beer styles with the 13 beer features.

We have 112 beer styles but only 5539 rows of data, The first model we get is underfitting with low accuracy as there is not enough data to feed the model. In order to get a model with higher accuracy, we group the beer styles into more general categories, then we drop those beer styles with less than 150 rows of data and come up with 9 super beer styles. 

Beer style Prediction models we tried are logistic regression, support vector machine and normal neural network. Normal neural network has the highest accuracy which is 0.73. It is a good number and we can say it is possible to predict the beer style by analyzing beer review data. 
