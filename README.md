What drives the price of a car?

1. Task at Hand

Identifying the key drivers for predicting the prices of used cars and what the customers look for when buying a car and how the second-hnd dealer should stock his 
inventory basis these recommendations.

2.Data Preparation

2.1 Analysed the missing data and existing columns in the supplied data
2.2 Dropped the non-useful columns – id and VIN
2.3 Analysed the price column using box plots
2.4 Some of the prices were in billions. Removed data where prices exceeded 500,000 USD. Applying Inter quartile rangeoutlier method would distort the data more than dropping those over 500,000 as this removed only 68 datapoints.
2.5 Also dropped data where car prices were below 50 USD and with odometer readings less than 500 km. This removed roughly 42,000 data points, most of which were zeros in the price and odometer columns.
2.6 Plotting a histogram of prices and log of prices shows, log of the prices is more normally distributed than the price itself.
2.7 TargetEncoder is then used to convert the categorical variables to numeric. This reduces the dimensionality of the dataset as opposed to using onehotencoder.
2.8 A correlation plot of the data showed that the price of car has the highest positive correlation to the model of the car and the highest negative correlation to the year of manufacturing.

3. Modeling

3.1 The sklearn library was used along with pipeline and GridSearchCV to find the best modela and the alpha parameter.
3.2 Ridge and lasso regression models were searched and the best estimator was found to be the Lasso Regressor with an alpha of 0.01.
3.3 The model score was found to be 60%
3.4 Permuation Importance was also used to determine the factors impacting the price prediction and the top 3 factors were found to be model of the car, odometer and transmission

4. Conclusions

4.1 Top selling models are f-150, silverado and camry. Maintaining stock in these models is recommended as they are the best-selling second hand car models
4.2 Second hand car drivers also look for cars with lower odometer readings and is the second highest criteria that a driver uses to decide to buy a second-hand car.
4.3 The top selling brands are Ford (17%) , Chevrolet (13%) and Toyota (8%) with median prices of 17,500 ; 16,500 and 14,000 USD respectively
4.4 For sales where a cylinder was quoted, 6 cylinder was the most popular with a median price of 15,400 USD followed by 4-cylinder cars with a median price of 9,000 USD and closely followed by 8 cylinder cars with a median price of 21,000 USD.
4.5 Four Wheel drive cars are the most popular with a median price of 20,500 USD
4.6 Cars with condition marked as good were the most popular with salvage being the least popular for obvious reasons
4.7 Pickup, truck and coupe seem to be the best-selling car types.
4.8 Automatic cars are the most popular second-hand car types
