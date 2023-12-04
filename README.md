# Predicting Waze App User Churn

# Overview 
Waze is a navigation app that helps drivers around the world get to where they need to go, in the most safe and efficient amount of time.
The goal of this project was to create a Random Forest and XGBoost Model to see which of the two best predicts if a user will remain or churn.
“Churn” quantifies the number of users who have uninstalled the Waze app or stopped using the app altogether.
The Waze leadership teams overall purpose of the model is to figure out what factors exactly drive user churn, to make better informed 
business decisions to prevent user churn, to improve user retention and grow Waze's business.
The project utilizes Waze user’s monthly data. What we do not know is what year and month the data was taken from. 

The Random Forest model performed with a precision score of 46%, a recall score of 13%, a f1 score of 20% and an accuracy score of 82%.
The XGBoost Model performed with a precision score of 44%, a recall score of 17%, a f1 score of 25% and an accuracy score of 82%.
The XGBoost model outperformed the Random Forest model slightly. In both model’s precision and accuracy scores are pretty much the same.
But, overall the score in both models are lower that we would want them to be with the exception of accuracy score. 
In the case of using this model to predict user churn, neither of these models are strong enough predictors. But we can utilize the model
to further explore other efforts.

# Business Understanding
The main stakeholders for this project are the Waze Data team, Finance and Administration Department Head and Operations Manager. The main problem they are trying to solve/understand is why they are losing users. They want to know what factors drive user churn. The model should help answer the questions
1. Who are the users most likely to churn?
2. Why do users churn?
3. When do users churn?

# Data Understanding
The data used was provided by the Google Advanced Data Analytics Professional Certificate program. It contains synthetic data created in partnership with Waze.
The original dataset contains 13 features and 14,999 entries. The features included information on sessions (The number of occurrence of a user opening the app during the month), label (“retained” or “churned”), total_sessions (total number of sessions since a user has onboarded), activity_days (number of days the user opens the app during the month), etc. After performing Exploratory Data Analysis, a few additional features were engineered. The newly engineered featured include, but are not limited to, km_per_driving_day (the mean number of kilometers driven on each driving day in the last month for each user), percent_sessions_in_last_month (the percentage of each user's total sessions that were logged in their last month of use), total_sessions_per_day (the mean number of sessions per day since onboarding).

# Modeling and Evaluation
The XGBoost model comprised of 300 decision trees that determined which features were important in predicting users that churned and users that remained. 
The plot below shows that km_per_hour, n_days_after_onboarding and percent_sessions_in_last_month are the top 3 most important features that determine if a user will churn or remain. It is also important to note that 7 out of the top 10 important features determining user churn or not, were engineered features that were added to the original dataset. The overall XGBoost model performed with 82% accuracy score and a 44% precision 
score.
![image](https://github.com/CassandraNnaji/Waze-App-User-Churn-Project-Machine-Learning-/assets/120784310/929e6135-1210-45d7-9c21-749162adf67b)

# Conclusion
This model is not a good predictor for user churn. Due to the fact that its recall score is 17%. Since we know that 7 out of the top 10 important features were engineered, we could reconstruct the model and try different combinations of predictive features to help reduce the noise from unpredictive variables. It can be recommended that we gather more data that shows how users specifically interact with the app. Such as does a user report/confirm accidents or road hazards.

