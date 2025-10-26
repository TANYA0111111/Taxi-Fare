🚖 Taxi Fare Prediction Model
📊 Project Overview

This project builds a machine learning model to predict taxi fares based on trip details such as distance, duration, surge pricing, number of passengers, and other cost components.
The goal is to help taxi operators and ride-hailing platforms estimate fares dynamically and accurately using historical trip data.

🎯 Objective

To develop and compare multiple regression models — Linear Regression, Decision Tree, and Random Forest — and determine which best predicts total taxi fare.
The project also includes exploratory data analysis (EDA) and visual insights into trip trends and pricing behavior.

🧠 Problem Statement

Given a dataset of taxi trips containing features like:

Distance traveled (Km)

Trip duration

Number of passengers

Surge pricing applied or not

Cost components (wait time, distance cost, tips, fees)

Predict the total fare (total_fare_new) of a ride.

📂 Dataset Description

Dataset: Taxi_Set.csv
Rows: 207,596
Columns: 13

Feature	Description
trip_duration_min	Duration of trip in minutes
distance_traveled_Km	Total distance covered (in Km)
KPH	Average speed (Km per hour)
wait_time_cost	Cost incurred during waiting time
distance_cost	Cost calculated based on distance
fare_w_flag	Base fare before adjustments
tip	Tip amount given by passenger
miscellaneous_fees	Additional service fees
num_of_passengers	Number of passengers in the trip
surge_applied	Whether surge pricing was applied (True/False)
total_fare_new	Final fare to be predicted

All features were clean with no missing values, and datatypes were properly formatted.

🧩 Tech Stack

Language: Python

Libraries: pandas, numpy, seaborn, matplotlib, scikit-learn

Models Used:

Linear Regression

Decision Tree Regressor

Random Forest Regressor

🧪 Workflow
1️⃣ Data Preprocessing

Loaded and inspected data with pandas

Dropped redundant columns (trip_duration_sec, trip_duration_hr, wait_time_cost)

Converted surge_applied from boolean to integer for model compatibility

2️⃣ Exploratory Data Analysis (EDA)

Visualized key relationships and distributions:

Average Trip Duration by Number of Passengers (Bar Chart)

Trips with and without Surge Pricing (Pie Chart)

Distance vs Total Fare (Line Plot)

Feature Correlation Matrix (Heatmap)

3️⃣ Model Building

Trained and evaluated three models:

Model	Mean Squared Error (MSE)	R² Score
Linear Regression	—	—
Decision Tree Regressor	6.21	0.994
Random Forest Regressor	3.25	0.997

✅ Random Forest achieved the best performance, with very high accuracy and minimal prediction error.

4️⃣ Prediction Example

For a trip with parameters:

[12.47, 2.75, 13.23, 11.94, 24, 6.30, 1, 0]


Predicted total fare: $42.26

📈 Visual Insights
🧍‍♂️ Average Trip Duration by Number of Passengers

Shows how trip times vary with the number of passengers.

⚡ Trips with Surge Pricing

Pie chart showing percentage of trips with surge applied.

📏 Distance vs Total Fare

Illustrates a clear positive correlation between distance traveled and fare amount.

🔥 Correlation Matrix

Highlights the relationship between numerical features and total fare.

🧰 Model Evaluation

Performance metrics used:

Mean Squared Error (MSE) — measures average squared difference between actual and predicted values.

R² Score — indicates how well the model explains variance in the target variable.

🚀 How to Run the Project
Prerequisites

Install required Python libraries:

pip install pandas numpy seaborn matplotlib scikit-learn

Steps

Clone this repository

git clone https://github.com/your-username/taxi-fare-prediction.git
cd taxi-fare-prediction


Place the dataset Taxi_Set.csv in the project directory.

Open the notebook:

jupyter notebook final_code.ipynb


Run all cells to reproduce the analysis and model training.

🏁 Results

Random Forest Regressor achieved R² = 0.9971 and MSE = 3.25

Model effectively predicts taxi fares with high accuracy

Demonstrated complete end-to-end ML workflow:

Data cleaning

EDA

Model training & evaluation

Visualization & interpretation

📚 Future Improvements

Include real-time fare prediction using a web dashboard (e.g., Streamlit or Flask)

Perform feature engineering for time of day, weather, or location

Experiment with Gradient Boosting / XGBoost for comparison
