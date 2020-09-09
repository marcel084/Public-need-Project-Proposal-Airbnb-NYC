# **Public-need-Project-Proposal-Airbnb-NYC**
What's the relationship between pricing and variables like type of room and location in NYC Airbnb renting places? How to invest smart in this business?
Source: NYC Airbnb Open Data
Analysis: Structured Data. Dataset 49k rows
Hypothesis: Is the average price per night significantly different in the 5 Counties of NYC. Hyphotesis testing to determine which are significantly different
Model Comparison: Building 3 models to classify categories determined by pricing range per night of Airbnb renting places

The analysis for this project is done with R
## Libraries
* `library(dplyr)`
* `library(ggmap`
* `library(maptools)`
* `library(tidyverse)`
* `ibrary(RColorBrewer)`
* `library(rpart)`
* `library(rpart.plot)`
* `library(e1071)`
* `library(AICcmodavg)`
* `library(nnet)`

# **The Analysis**
The analysis is detailed in the rmd code and it is structured the document Final.rmd. This Notebook does the following:
1. a) Density map to which are the counties with the highest concentration of renting places
1. b) Creation of 4 different categories based pricing range and determined by the quartiles an median of the population
1. c) Building the three models through customized functions which returned a set of accuracy's values 
1. d) Comparison and hyphotesis testing to determine the best predictive model based on the greatest accuracy.
1. e) Predicting variables impacting the model
1. f) Combinations of these variables impacting significantly in the variable price
# **Results**
1.ANN model is the best model to predict this class with an average accuracy of 52% in the prediction of 4 different classes.
1.The variables impacting the most in this prediction are:
2.Neighborhood type
2.Type of room
1.Tukey results proved that the 3 levels in the variable type of room are significantly different among them. Meanwhile in the variable neighborhood group, only one level is significantly different from the rest, this neighborhood is Manhattan. 


![HeatMap](https://github.com/marcel084/Public-need-Project-Proposal-Airbnb-NYC/blob/master/Images/HeatMap.png) ![AvgPrice](https://github.com/marcel084/Public-need-Project-Proposal-Airbnb-NYC/blob/master/Images/AvgPrice.png) ![AccuracyModels](https://github.com/marcel084/Public-need-Project-Proposal-Airbnb-NYC/blob/master/Images/AccuracyModels.png) 


