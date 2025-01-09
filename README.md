# greengear

# Project Overview:
This program leverages machine learning to classify vehicles as eco-friendly or not, based on key features like fuel type, fuel consumption, and horsepower. By identifying vehicles that meet eco-friendly criteria, it supports consumers in making sustainable choices and assists automotive businesses and researchers in tracking and improving eco-friendly offerings. The model analyzes data, generates predictions, and provides actionable insights to promote environmentally conscious transportation solutions.


# Technical Overview:

Features:

Data Loading and Preprocessing
- Loads a dataset of vehicles, including attributes like fuel type, fuel consumption, horsepower, and brand.
- Creates custom features like "Efficiency per HP" to evaluate fuel efficiency relative to engine power.
- Encodes categorical data using LabelEncoder and standardizes numerical features with StandardScaler.

Machine Learning Model
- Random Forest Classifier: Trained using grid search to identify eco-friendly cars, leveraging oversampling (SMOTE) to address class imbalance.
-Feature Importance: Visualizes the most significant attributes contributing to eco-friendly classification.

# Eco-Friendly Classification

Cars are classified as eco-friendly if:
- Fuel type is Electric or Hybrid.
- Fuel consumption is ≤ 5 liters/100 km.
- Horsepower is ≤ 150.

Predictions are adjusted using a custom probability threshold for improved performance.

# Insights and Results
- Outputs a detailed classification report, including accuracy, precision, recall, and confusion matrix visualizations.
- Appends predictions and reasons for classification to the dataset for clear interpretability.

# Output
- Saves a processed dataset (eco_friendly_cars.csv) with predictions and classification reasons.
- Stores the trained model and encoders for future use.

# Programming Insights:
- Coded in Python
- Scikit-Learn: For preprocessing, model training, evaluation, and grid search.
- Imbalanced-Learn: Used SMOTE to handle class imbalances in the dataset.
- Matplotlib & Seaborn: For visualizations like feature importance and confusion matrices.
- Pandas & NumPy: For efficient data manipulation and feature engineering.
- Model Deployment
- Saves the trained Random Forest model (eco_friendly_model.pkl) and label encoders (label_encoders.pkl) for reuse.

# Business Use Cases
- Assists consumers in choosing sustainable vehicles.
- Provides manufacturers with data-driven insights to refine eco-friendly vehicle offerings.

# Key Applications:
- Consumer Guidance: Helps consumers identify eco-friendly cars that align with sustainability goals.
 -Market Research: Assists automotive researchers in analyzing trends and developing greener solutions.
- Business Strategy: Supports manufacturers in targeting eco-conscious buyers and improving product design.

This project demonstrates advanced data analysis, machine learning, and environmental impact modeling, showcasing expertise in both technical development and practical applications.
