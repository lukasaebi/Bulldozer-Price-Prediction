# Bulldozer-Price-Prediction

The main goal of this project was to predict the sale price of bulldozers sold from the start of 2011 to the end of April 2012. Training instances date from 1989 to the end of 2010.


**Properties**:
- **Big Dataset** <br>
The training set consists of 350'000 instances. This led to challenges regarding cross validation as it was very time intensive for other algorithms than linear regression. This forced me to cross validate with a subset of the instances to get results of the different feature engineering steps quicker.

- **Quasi Time Series** <br>
Only "quasi time series", because there were multiple instances per date. One way to handle it like a time series problem was to take the average saleprice per saleday. However, this average sale price per saleday wasn't really predictive. Nevertheless, the influence of time on the dependent variable was a valuable experience as in business cases time often is an important factor.

- **Lots of Missing Values** <br>
Most of the variables had missing values with some of them up to > 80%. Finding a strategy to handle the missing values in an intelligent way (dropping, imputing, additional missing column) was a central part of the iterated evaluation.

**Results**: <br>
- Average error of the baseline model could be **_reduced by ~1500$_**, although there was a massive price increase in the test set which was difficult to take into account.
- Model tended to be _too conservative_. Especially the sale price of most expensive bulldozers has been predicted too low.
