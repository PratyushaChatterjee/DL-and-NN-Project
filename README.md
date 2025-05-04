Analysis Report on Wearable Health Hackathon - Develop a solution to early diagnose 
diseases using non-invasive methods and health data 
1. Objective and Innovation 
This project was developed as a part of the Wearable Health Hackathon with the goal of 
building a robust solution for early disease diagnosis using non-invasive methods and 
health data analytics. The primary innovation lies in predicting cardiovascular disease 
(specifically, 10-year CHD risk) through machine learning models trained on structured 
health data. The approach emphasizes accessibility, preventive care, and real-time 
monitoring, which are all central to wearable health technologies. 
2. Data Acquisition and Preprocessing 
The analysis began with the CVD_FinalData.csv dataset, which includes vital clinical and 
lifestyle attributes such as age, sex, smoking status, cholesterol levels, blood pressure, and 
diabetes indicators. The data was: 
• Cleaned using .dropna() to remove incomplete records, 
• Label-encoded for binary categorical features, 
• One-hot encoded for multi-category features, and 
• Scaled using StandardScaler to ensure uniformity across features. 
To address the class imbalance—a common issue in medical datasets—SMOTE (Synthetic 
Minority Over-sampling Technique) was applied, which effectively balanced the dataset 
and ensured fair learning across both target classes. 
3. Model Selection and Evaluation 
The Random Forest Classifier was chosen due to its robustness in handling high-dimensional 
data, low risk of overfitting, and interpretability. A comprehensive GridSearchCV with 3
fold cross-validation (243 fits) was performed to tune hyperparameters such as: 
• n_estimators, 
• max_depth, 
• min_samples_split, and 
• min_samples_leaf. 
The 
best 
configuration 
found 
n_estimators = 50, max_depth = 5, min_samples_split = 2, min_samples_leaf = 1. 
Evaluation Results: 
was: 
• Accuracy: 100% 
• Precision, Recall, F1-Score: 1.00 for both positive and negative classes 
• These metrics highlight the model’s flawless classification capability on the test set. 
4. User Interface and Application 
To make this model practical and accessible, a Streamlit web application was developed: 
• Features intuitive UI components like sliders, dropdowns, and number inputs, 
• Accepts user health data and provides immediate CHD risk prediction, 
• Displays a rule-based risk score and ML-predicted outcome, 
• Includes an in-app chatbot for user support and FAQs, 
• Deployable via Ngrok for remote access. 
This user-centric design bridges the gap between technical prediction models and real-world 
usability, especially for patients or health workers with limited technical backgrounds. 
5. Impact and Relevance 
The integration of health informatics, AI, and wearable-compatible data flow supports the 
shift toward preventive healthcare and remote monitoring. The model can serve as the 
foundation for a broader system that: 
• Supports continuous health tracking, 
• Alerts users before critical stages, 
• Integrates with wearable devices for automated input, and 
• Improves healthcare access in rural or underserved regions. 
