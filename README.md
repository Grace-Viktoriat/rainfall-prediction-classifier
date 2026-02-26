Rainfall Prediction Classifier
Overview
This project develops a machine learning model to predict whether it will rain based on historical weather observations from the Australian Bureau of Meteorology.
The workflow demonstrates an end-to-end machine learning pipeline, including:
•	Data cleaning and preprocessing
•	Data leakage analysis and mitigation
•	Feature engineering (seasonality extraction)
•	Stratified train-test splitting
•	Pipeline construction using ColumnTransformer
•	Hyperparameter tuning with GridSearchCV
•	Model evaluation using classification metrics
•	Feature importance analysis
Problem Framing
To avoid data leakage, the prediction task was reframed to:
Predict today’s rainfall using weather observations up to and including yesterday.
This adjustment ensures realistic feature availability at prediction time.
 Models Implemented
•	Logistic Regression
•	Random Forest Classifier (with hyperparameter optimization)

Metric	Random Forest
Cross-Validation Accuracy	~0.85
Test Accuracy	~0.84
True Positive Rate (Rain)	~0.50

Although overall accuracy was strong, class imbalance affected recall for rainy days.
Key Findings
•	Humidity at 3pm was the most important predictive feature.
•	Atmospheric pressure and sunshine were also strong predictors.
•	Random Forest performed slightly better than Logistic Regression when considering all evaluation metrics.
•	The dataset exhibited class imbalance (~76% dry days), influencing recall performance.
________________________________________
Technologies Used
•	Python
•	Pandas
•	Scikit-learn
•	Matplotlib
________________________________________
Skills Demonstrated
•	Feature Engineering
•	Handling Class Imbalance
•	Cross-Validation Strategy
•	Hyperparameter Tuning
•	Model Comparison
•	Performance Interpretation
