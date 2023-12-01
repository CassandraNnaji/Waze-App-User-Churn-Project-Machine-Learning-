# Predicting Waze App user Churn

# Overview 
Waze is a navigation app that helps drivers around the world get to where they need to go, in the most safe and efficient amount of time.
The goal of this project was to create a Random Forest and XGBoost Model to see which of the two best predicts if a user will remain or churn.
"Churn", quantifies the number of users who have uninstalled the Waze app or stopped using the app altogether.
The Waze leadership teams overall purpose of the model is to figure out what factors exactly drive user churn, to make better informed 
buisness decisions to pervent user churn, to improve user retention and grow Waze's buisness.
The project utilizes Waze users monthly data. What we do not know is what year and month the data was taken from. 
The Random Forest model performed with a precision score of 46%, a recall score of 12%, a f1 score of 20% and an accuracy score of 82%.
The XGBoost Model performed with a precision score of 45%, a recall score of 16%, a f1 score of 24% and an accuracy score of 82%.
The XGBoost model out performed the Random Forest model slightly. In both models precision and accuracy scores are pretty much the same.
But, overall the score in both models are lower that we would want them to be with the exception of accuracy score. 
In the case of using this model to predict user churn, neither of these models are strong enough predictors. But we can utilize the model
to further explore other efforts.

# Data Understanding
The data used was provided by the Google Advanced Data Analytics Professional Certificate program. It contains synthetic data created in partnership with Waze.
The original dataset contains 13 features and 14,999 entries. The features included information on sessions (The number of occurrence of a user opening the app during the month), label (“retained” or “churned”), total_sessions (total number of sessions since a user has onboarded), activity_days (number of days the user opens the app during the month), etc. After performing Exploritor Data Analysis, a few additional features were engineered. The newly engineered featured include, but are not limited to, km_per_driving_day (the mean number of kilometers driven on each driving day in the last month for each user), percent_sessions_in_last_month (the percentage of each user's total sessions that were logged in their last month of use), total_sessions_per_day (the mean number of sessions per day since onboarding).

# Modeling and Evaluation
