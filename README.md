# EECS731_MS_Project_5
Project 5 - World Wide Products Inc.
  Shipping and delivering to a place near you
1. Set up a data science project structure in a new git repository in your GitHub account
2. Download the product demand data set from
https://www.kaggle.com/felixzhao/productdemandforecasting
3. Load the data set into panda data frames
4. Formulate one or two ideas on how feature engineering would help the data set to establish additional value using exploratory data analysis
5. Build one or more forecasting models to determine the demand for a particular product using the other columns as features
6. Document your process and results
7. Commit your notebook, source code, visualizations and other supporting files to the git repository in GitHub

This repository goes through the cleaning and preperation for the above dataset. The data set consists of different product time series data that was seperated into their individual values. That data was then analyzed by a series of statistical techniques to visuialaze how that data changes with time and what features could be designed to give the best prediction method. I found that rather than predicting the quantity of an single order on any given day it is better to predict a change in demand with respect to all the orders previously. From this realization I ended up with a series that consisted of a date and a cumlitave sum of order demand from previous days. I then chose to smooth the data by takign the sum every two weeks in an effort to make the behavior more predictable. The model I chose to use is an ARMA model. I used this because it is a moving average model and since the values for the demand are constantly changing I thought this would be benificial. The fit was good as expected for a dataseries that was this simple. I decided to try a different point. There was signifigant anomalies in the tail behavior of the new model and it shows on how well the ARMA was able to predict the tail behavior. Since that behavior is at the tail end of the dataset there isn't any data to outweigh that change. This caused the prediction to have a much wider confidence range than the previous data series. Overall time series problems are very complex and difficult to handle; however, they are certanly one of the most rewarding problems. 
