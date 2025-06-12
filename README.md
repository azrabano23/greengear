# Green Gear 🌱

Smart Vehicle Classification for a Greener Tomorrow

# Project Overview:
The transportation sector accounts for over 24% of global CO₂ emissions, with road vehicles being the largest contributor.
(Source: International Energy Agency, 2023)

Despite the rise of hybrid and electric vehicles, consumers and businesses still struggle to identify which cars are truly eco-friendly based on meaningful performance metrics — not just marketing. Current classification systems often lack consistency, transparency, or adaptability to user-specific needs. There is a pressing need for a data-driven tool that intelligently classifies vehicles based on emissions-related attributes, making sustainability more accessible and measurable.

🌍 Why This Program Matters
Green Gear helps bridge the gap between environmental responsibility and informed consumer choice by using machine learning to classify cars as eco-friendly based on real-world performance indicators like fuel consumption, engine power, and fuel type.

This tool not only empowers eco-conscious consumers, but also supports automotive companies, market analysts, and policy researchers in tracking trends and improving sustainability efforts in the auto industry.

⚙️ What the Program Does

1. Data Processing & Feature Engineering
2. 
- Loads a vehicle dataset with fields like fuel type, fuel consumption, horsepower, and brand.
- Engineers new features (e.g., Efficiency per HP) to better capture eco-performance.
- Encodes categorical variables and standardizes numeric data for machine learning.

2. Eco-Friendly Classification

Classifies vehicles as eco-friendly if:
- Fuel type is Electric or Hybrid
- Fuel consumption is ≤ 5 L/100 km
- Horsepower is ≤ 150 HP

Uses Random Forest Classifier, trained with GridSearchCV for optimal performance.
Applies SMOTE oversampling to balance minority (eco-friendly) and majority classes.

3. Output & Insights
4. 
Generates:
- Classification report: Accuracy, Precision, Recall, F1 Score.
- Confusion matrix and feature importance plot for interpretability.
- Outputs a CSV file (eco_friendly_cars.csv) with:
- Eco-friendly prediction (Yes/No)
- Explanation for the classification per car

4. Model Deployment
Saves trained model and encoders (eco_friendly_model.pkl, label_encoders.pkl) for future reuse or API integration.

👤 Target Audience
Eco-Conscious Consumers
→ Helps users filter car options based on real-world environmental impact.

Automotive Manufacturers & Product Teams
→ Gain data-driven insights on what features correlate with eco-friendliness.

Market Researchers & Analysts
→ Track trends in fuel efficiency and sustainability across brands and segments.

Policymakers & Sustainability Advocates
→ Use the tool as a model for developing or evaluating green vehicle incentives.

📌 Key Applications
🚗 Consumer Guidance: Provide sustainability labels to cars on dealership platforms.

📈 Market Research: Analyze which brands and fuel types are evolving toward greener standards.

🛠️ Product Design: Inform R&D on which engine specs align with environmental benchmarks.


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

# 👤 Target Audience
Eco-Conscious Consumers
→ Helps users filter car options based on real-world environmental impact.

Automotive Manufacturers & Product Teams
→ Gain data-driven insights on what features correlate with eco-friendliness.

Market Researchers & Analysts
→ Track trends in fuel efficiency and sustainability across brands and segments.

Policymakers & Sustainability Advocates
→ Use the tool as a model for developing or evaluating green vehicle incentives.


# Business Use Cases
- Assists consumers in choosing sustainable vehicles.
- Provides manufacturers with data-driven insights to refine eco-friendly vehicle offerings.

# Key Applications:
- Consumer Guidance: Helps consumers identify eco-friendly cars that align with sustainability goals.
- Market Research: Assists automotive researchers in analyzing trends and developing greener solutions.
- Business Strategy: Supports manufacturers in targeting eco-conscious buyers and improving product design.
- Product Design: Inform R&D on which engine specs align with environmental benchmarks.
