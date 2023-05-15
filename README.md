# Appliance-Energy-Prediction
Data driven prediction of energy use of appliances

# Aim-
Experimental data used to create regression models of appliances energy use in a low energy building.

# Project Summary -
The purpose of this research is to forecast the electricity consumption of a particular household in Belgium based on the temperature and humidity levels of various rooms in the facility and surrounding weather information over 4.5 months. The data set runs 4.5 months at 10 minutes. A ZigBee wireless sensor network is being used to monitor the home’s temperature and humidity levels. Around 3.3 minutes, each wireless node sent the temperature and humidity data. The wireless data was then averaged across intervals of 10 minutes. Every 10 minutes, m-bus energy meters collected the energy data. The experimental data sets were combined with the weather data from the closest airport weather station (Chievres Airport, Belgium), which was extracted from a public data set from Reliable Prognosis (rp5.ru). The data set has two random variables to test the regression models and exclude non-predictive characteristics (parameters).

# Problem Statement-
We should predict Appliance energy consumption for a house based on factors like temperature, humidity & pressure . In order to achieve this, we need to develop a supervised learning model using regression algorithms. Regression algorithms are used as data consist of continuous features and there are no identification of appliances in dataset.

# Define Your Business Objective?

The increasing trend in energy consumption is becoming cause of concern for the entire world, as the energy consumption is increasing year after year so is the carbon and greenhouse gas emission, the majority portion of the electricity generated is consumed by industrial sector but a considerable amount is also consumed by residential sector.

It is important to study the energy consuming behaviour in the residential sector and predict the energy consumption by home appliances as it consume maximum amount of energy in the residence. This project focuses on predicting the energy consumption of home appliances based on humidity and temperature.

This project aims to predict the energy consumption of home appliances. With the advent of smart homes and the rising need for energy management, existing smart home systems can benefit from accurate prediction. If the energy usage can be predicted for every possible state of appliances, then device control can be optimized for energy savings as well. This is a case of Regression analysis which is part of the Supervised Learning problem. Appliance energy usage is the target variable while sensor data and weather data are the features.

# Variables Description-
There are 29 features to describe appliances energy use :

date : time year-month-day hour:minute:second

lights : energy use of light fixtures in the house in Wh

T1 : Temperature in kitchen area, in Celsius

T2 : Temperature in living room area, in Celsius

T3 : Temperature in laundry room area

T4 : Temperature in office room, in Celsius

T5 : Temperature in bathroom, in Celsius

T6 : Temperature outside the building (north side), in Celsius

T7 : Temperature in ironing room, in Celsius

T8 : Temperature in teenager room 2, in Celsius

T9 : Temperature in parents’ room, in Celsius

T_out : Temperature outside (from Chievres weather station), in Celsius

Tdewpoint : (from Chievres weather station), Â°C

RH_1 : Humidity in kitchen area, in %

RH_2 : Humidity in living room area, in %

RH_3 : Humidity in laundry room area, in %

RH_4 : Humidity in office room, in %

RH_5 : Humidity in bathroom, in %

RH_6 : Humidity outside the building (north side), in %

RH_7 : Humidity in ironing room, in %

RH_8 : Humidity in teenager room 2, in %

RH_9 : Humidity in parents’ room, in %

RH_out :Humidity outside (from Chievres weather station), in %

Pressure : (from Chievres weather station), in mm Hg

Wind speed: (from Chievres weather station), in m/s

Visibility :(from Chievres weather station), in km

Rv1 :Random variable 1, non-dimensional

Rv2 :Random variable 2, non-dimensional

Appliances : Total energy used by appliances, in Wh

# Manipulations on Dataset-

) Since, this is not a timeseries problem and we will focus on predicting the appliance consumption , we can ignore Date column.

Independent variables : 27(11 temperature, 10 humidity, 1 pressure, 2 randoms)

Dependent variable : 1 (Appliances)

# Observations-

Temperature columns - Temperature inside the house varies between 14.89 Deg & 29.85 Deg , temperature outside (T6) varies between -6.06 Deg to 28.29 Deg . The reason for this variation is sensors are kept outside the house.

Humidiy columns - Humidity inside house varies is between 20.60% to 63.36% with exception of RH_5 (Bathroom) and RH_6 (Outside house) which varies between 29.82% to 96.32% and 1% to 99.9% respectively.

Appliances - 75% of Appliance consumption is less than 100 Wh . With the maximum consumption of 1080 Wh , there will be outliers in this column and there are small number of cases where consumption is very high.

Lights column - Intially I believed lights column will be able to give useful information . With 11438 0 (zero) enteries in 14801 rows , this column will not add any value to the model . I believed light consumption along with humidity level in a room will give idea about human presence in the room and hence its impact on Appliance consumption. Hence, we will drop it during feature selection.

# Feature ranges-

Temperature : -6 to 30 deg

Humidity : 1 to 100 %

Windspeed : 0 to 14 m/s

Visibility : 1 to 66 km

Pressure : 729 to 772 mm Hg

Appliance Energy Usage : 10 to 1080 Wh

# Final result of all applied models-
![image](https://github.com/pratap-vj/Appliance-Energy-Prediction/assets/123111274/920f6eeb-f415-40fb-8bd5-f086e46ff354)

# Conclusion-
The overall conclusion of the project is as follows:

# Data Analysis: 
    The data analysis phase involved exploring and understanding the dataset. Various visualizations and statistical tests were performed to gain insights into the variables and their relationships.

# Feature Selection: 
    The feature selection process helped identify the most relevant variables for predicting appliance energy consumption. Some variables exhibited a strong correlation with the target variable, while others showed little to no relationship.

# Model Building: 
    Several machine learning models were built and evaluated for predicting appliance energy consumption. Different algorithms, such as linear regression, random forest, and gradient boosting, were employed. Evaluation metrics such as R2 score, RMSE, and training time were used to assess the performance of each model.

# Hyperparameter Tuning: 
    Hyperparameter tuning techniques were applied to improve the model performance. GridSearch CV was used to search for the best combination of hyperparameters, resulting in improved scores for some models.

# Model Selection: 
    Based on the evaluation metrics, the ExtraTreeRegressor model emerged as the best performer, with high R2 scores, low RMSE, and comparable training and test performance. This model was chosen as the final prediction model.

# Feature Importance: 
    The importance of features was assessed using the ExtraTreesRegressor model. The features RH_5(Humidity in bathroom), T1(Temperature in kitchen area), Windspeed and RH_1(Humidity in kitchen area) were found to have the highest importance for predicting appliance energy consumption.

# Business Impact: 
    The insights gained from the project can be valuable for various stakeholders. Understanding the factors influencing appliance energy consumption can help in making informed decisions for energy management, efficiency improvements, and cost savings. The chosen ExtraTreeRegressor model can be used to predict appliance energy consumption accurately, enabling proactive measures for energy optimization.

# The project successfully analyzed the dataset, built and evaluated multiple models, and selected the best performing model for predicting appliance energy consumption. The findings can contribute to making data-driven decisions for energy management and have a positive business impact.




