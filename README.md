✈️ Customer Booking Prediction (Forage Data Science Project)
📌 Project Overview

This project predicts whether a customer will complete a flight booking using historical booking data provided by British Airways (via Forage).
The task involved data exploration, feature engineering, machine learning modeling, and interpretation of results to provide actionable business insights.

📊 Dataset

The dataset contains 50,000 rows with customer booking details.
Key features include:

num_passengers → Number of passengers in booking

sales_channel → Sales channel (Internet, Travel Agent)

trip_type → Trip type (Round Trip, One Way, Circle Trip)

purchase_lead → Days between booking & travel date

length_of_stay → Days at destination

flight_hour → Flight departure hour

flight_day → Day of week of flight

route → Origin → Destination route

booking_origin → Country of booking

wants_extra_baggage → Extra baggage (Yes/No)

wants_preferred_seat → Preferred seat (Yes/No)

wants_in_flight_meals → Meals (Yes/No)

flight_duration → Flight duration in hours

booking_complete → Target variable (0 = Not Completed, 1 = Completed)

🛠️ Methodology
1. Exploratory Data Analysis (EDA)

Checked dataset shape, data types, and missing values

Converted categorical variables (sales_channel, trip_type, route, etc.) using One-Hot Encoding

Visualized booking completion rate (~15% completed, dataset is imbalanced)

2. Data Preprocessing

Mapped flight_day from weekday names to numeric

Applied StandardScaler to numeric features (purchase_lead, length_of_stay, flight_hour, flight_duration)

Handled class imbalance using SMOTE (Synthetic Minority Oversampling Technique)

3. Modeling

Trained Random Forest Classifier with class_weight="balanced"

Used GridSearchCV for hyperparameter tuning

Performed cross-validation to validate results

4. Evaluation

Accuracy ~ 83-85%

Improved recall for minority class (booking complete = 1) after SMOTE

Extracted feature importances to understand main drivers of booking

📈 Results
Model Performance (after tuning)

Accuracy: ~83%

Precision (Class 1): ~42%

Recall (Class 1): ~28% (improved with SMOTE)

F1-Score (Class 1): ~0.34

Key Insights (Top Features)

Purchase Lead (days before travel) strongly impacts booking completion

Length of Stay affects likelihood of confirmed booking

Sales Channel and Booking Origin play significant roles

Add-on requests (extra baggage, meals, preferred seat) correlate with higher booking completion probability

📊 Visualizations

Distribution of target variable (class imbalance)

Feature importance plot (Top 10 variables)

Confusion matrix of best model

📝 How to Run

Clone repo:

git clone https://github.com/Aaddrriikkaa15/British-Airways-Customer-Booking-Analysis.git
cd British-Airways-Customer-Booking-Analysis


Install dependencies:

pip install -r requirements.txt


Run Jupyter Notebook:

jupyter notebook


Open and run Customer_Booking_Prediction.ipynb

📦 Tech Stack

Python 3.12

Pandas, NumPy (Data wrangling)

Matplotlib, Seaborn (Visualization)

Scikit-learn (ML modeling, evaluation)

Imbalanced-learn (SMOTE handling)

📌 Deliverables

Jupyter Notebook: Full analysis & modeling

PowerPoint Slide: Summary of insights for management

README (this file)

📚 Learnings

Handling imbalanced datasets is crucial for business problems

SMOTE + class weights improve minority class detection

Feature importance provides actionable insights for marketing & booking strategies

✨ Developed as part of British Airways – Data Science Virtual Experience (Forage)
