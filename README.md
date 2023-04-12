<center><h1>What makes a good wine?</h1></center>


### Data Source(s)
 
- Wine Review, [https://www.kaggle.com/zynicide/wine-reviews]
- World countries coordinates(JSON), [https://github.com/python-visualization/folium/blob/master/examples/data/world-countries.json]
- Wine photo - [http://www.imagefast.org/wine-bottle-silhouette-png/] (if you cannot access the link, copy and paste it to a browser manually)

##### Wine review Columns:
- designation: The vineyard within the winery where the grapes that made the wine are from
- points: The quality of wine rated by WineEnthusiast on a scale from 1-100, 100 being the best
- price: The cost for a bottle of the wine
- state: The province or state that the wine is harvested 
- region: The province or state (ie Napa) where the winery is located
- variety: The type of grapes used to make the wine (ie Pinot Noir)
- winery: The winery that made the wine

<hr>

## Executive Summary

This report provides an analysis and evaluation on what makes a good and tasty wine, whether quality wine comes with a heavy price tag. Method of analysis include trend, horizontal and vertical analyses as well as correlation analysis, Pearson correlation between prices and points. Results of data analysed show that prices and points are correlated with moderate strength according to the pearson correlation coefficient and significant value, also known as the p-value. In addition, the mean ratings of wine from various countries shows the most frequency highest point wines came from US, Italy and France. After further analysis, the wines produced from different countries holds different wine characteristics for example, wines from US tend to be more rich and fruity in flavor while wines from Italy/Spain are sweeter due to it's composition. 

### Methodology

#### Cleaning up data
In this section, the columns not required are removed and any data with null value in the rows were also removed using dropna().<br>
1. [Importing and cleanup Data](#Importing-and-cleanup-Data)

#### Comparing data with countries and points
Looking at different countries and the points collected, we managed to plot a map showcasing the average points of wines for each country<br>
2. [Country with the highest number of 100 points wines](#Country-with-the-highest-number-of-100-points-wines)<br>
3. [Map with Mean ratings of wine](#Map-with-Mean-ratings-of-wine(Folium))<br>

#### Comparing data with points and prices
In this segment, the pearson correlation is used to determine the relationship between prices and points as well as the strength of the said relationship. We also studied the skewness of the variables using boxplot<br>
4. [Higher price corresponds to high ratings wine?](#Does-higher-price-corresponds-to-high-ratings-wine?)<br>

##### Machine Learning
We further the study by creating a machine learning model to study the descriptions of each wine which predict the points.<br>
5. [Understanding wine description with NBClassifier](#Understanding-wine-description-with-Naive-Bayes-Classification-Algorithm)<br>
6. [Understanding wine description by countries with DecisionTree](#Understanding-wine-description-by-countries-with-DecisionTree)<br>
7. [Feature Importance with DecisionTree](#Feature-Importance-with-DecisionTree)<br>

##### Word Cloud
Examining the description from various country's wine and uncovering the max common words appeared using a Word cloud<br>
8. [Understanding wine description with wordcloud](#Understanding-wine-description-with-wordcloud)<br>

Lastly, [Conclusion](#Conclusion)

#### Extra feature: 

 - [Predicting description](#Testing-out-machine-learning-model-with-input-description)

