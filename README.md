# **Public-need Project Proposal Airbnb-NYC**
What's the relationship between pricing and variables like type of room and location in NYC Airbnb renting places? How to invest smart in this business?
* Source: NYC Airbnb Open Data (Kaggle)
* Analysis: Structured Data. Dataset 49k rows
* Hypothesis: Is the average price per night significantly different in the 5 Counties of NYC? Hyphotesis testing to determine which are significantly different
* Model Comparison: Building 3 models to classify categories determined by pricing range per night of Airbnb renting places

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
The analysis is detailed in the rmd code and it is structured in the document Final.rmd. This Notebook does the following:
* a) Density map to define which are the counties with the highest concentration of renting places.
* b) Creation of 4 different categories based on pricing range and determined by the quartiles an median of the population.
* c) Building the three models through customized functions which returned a set of accuracy's values. 
* d) Comparison and hyphotesis testing to determine the best predictive model based on the greatest accuracy value.
* e) Which are the predicting variables impacting the model?
* f) Which are the combinations of these variables impacting significantly in the variable price
![HeatMap](https://github.com/marcel084/Public-need-Project-Proposal-Airbnb-NYC/blob/master/Images/HeatMap.png)  ![AccuracyModels](https://github.com/marcel084/Public-need-Project-Proposal-Airbnb-NYC/blob/master/Images/AccuracyModels.png) 
# **Results**
1. According to ANOVA results there is a significant difference among accuracy set of values' mean of the 3 predictive models, and ANN is the best model to predict the outcome with an average accuracy of 53% predicting the 4 different classes.
2. The variables impacting the most in this prediction are:
* Neighborhood type
* Type of room
3. Tukey results proved that the 3 levels in the variable type of room are significantly different among them. Meanwhile in the variable neighborhood group, only one level is significantly different from the rest, this neighborhood is Manhattan. 
Combinations of variables with price mean proven significantly different between them.

Combinations (Variables Room & Neighborhood) | Pvalue (ANOVA two-way)
----------------------- | -------------
Manhattan-Bronx | 5.118006e-10
Manhattan-Brooklyn | 4.014856e-05
Queens-Manhattan | 5.412145e-10
Staten Island-Manhattan | 7.765517e-09
Private room-Entire home/apt | 4.828220e-10
Shared room-Entire home/apt | 4.828218e-10
Shared room-Private room | 3.825168e-03

![AvgPrice](https://github.com/marcel084/Public-need-Project-Proposal-Airbnb-NYC/blob/master/Images/AvgPrice.png)





