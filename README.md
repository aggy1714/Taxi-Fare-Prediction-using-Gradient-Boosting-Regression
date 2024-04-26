Project Overview
Created a Prediction Model that would predict the average Fare Prices of Autos'in Bengaluru based on features such as searches, bookings, drivers' earnings, and distance traveled. The model uses a Gradient Boosting Regressor and is evaluated using Root Mean Squared Error (RMSE). The dataset used contains detailed information about taxi trips and related metrics.

Dataset
Source: [https://www.kaggle.com/datasets/stacknishant/namma-yatri-cab-bookings-bangalore-open-data/data] 
Description: The dataset contains information about taxi searches, estimates, bookings, completed trips, and various related metrics from Namma Yatri.
Columns:
Ward, Searches, Bookings, Drivers' Earnings, Distance Travelled (km), Average Fare per Trip, and other related columns.
The target variable for prediction is Average Fare per Trip.

Model Details
Model Type: Random Forest Regressor
Features:
'Searches', 'Bookings', 'Completed Trips', 'Drivers\' Earnings', 'Distance Travelled (km)'
Target: Average Fare per Trip'

Performance Metrics
The model was evaluated on a test set to determine its accuracy and effectiveness. The key performance metric used was RMSE.

Root Mean Squared Error (RMSE): 10.577
The Gradient Boosting model performed better than other models such as Linear Regression, Decision Trees, and Random Forrest

Usage
To use the model for predictions, run the following script:
gb_reg_Reload = joblib.load("taxi_fare_prediction_model_Gradient_Boosting Model.pkl")
Test_Data_For_Predictions = Cleaned_Taxi_data[['Searches', 'Bookings', 'Completed Trips', 'Drivers\' Earnings', 'Distance Travelled (km)']].head(25) #You can use Sample data too
Fare_Prediction = gb_reg_Reload.predict(Test_Data_For_Predictions)
print("Predicted Fare is:" , Fare_Prediction)


Contact
For questions, Kindly reach out to linkedin.com/in/agnel-george-b57515194
