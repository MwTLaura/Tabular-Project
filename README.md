# Tabular-Project

![UTA-DataScience-Logo](https://github.com/user-attachments/assets/fec1b411-bda5-437a-9eb8-08a018eb84ae)

# **Predicting Digital Wellbeing Score from Behavioral and Mental Health Data**

## **One Sentence Summary:**
This repository uses behavioral and mental health data to predict digital wellbeing scores through machine learning regression models.

Dataset used: [Mental Health and Digital Behavior 2020–2024 on Kaggle](https://www.kaggle.com/datasets/atharvasoundankar/mental-health-and-digital-behavior-20202024)

---

## **Overview:**
This project aims to determine whether a person’s digital wellbeing score can be accurately predicted using data on their daily digital behavior and self-reported mental health indicators. The dataset used includes 500 entries, each representing a daily snapshot with features such as screen time, number of app switches, sleep hours, notification count, time spent on social media, mood level, and anxiety level, along with a calculated digital wellbeing score as the target variable.

The machine learning pipeline involves several key steps: handling outliers using IQR-based clipping, rescaling features with StandardScaler, and conducting exploratory data analysis using histograms, boxplots, and correlation heatmaps to better understand feature relationships. The regression task is approached using three models: Linear Regression, Random Forest, and XGBoost.

Model performance is evaluated using RMSE and R². Linear Regression outperforms the others with an RMSE of 0.59 and an R² score of 0.99, indicating a near-perfect fit. Random Forest and XGBoost also perform well, with slightly higher error but still strong predictive power. The results suggest that even simple models can effectively estimate digital wellbeing based on a few well-selected behavioral features, highlighting the potential for real-world applications in digital health monitoring, mental wellbeing assessment, or personalized feedback systems.

This repository contains all code and documentation necessary to reproduce the results, apply the models to new data, or extend the project with additional modeling approaches.

---

## **Summary of Work**
### **Data**

**Type**: CSV file with 500 daily user entries.

**Input Features (7):**

daily_screen_time_min, num_app_switches, sleep_hours,
notification_count, social_media_time_min, mood_level,
anxiety_level.

**Target:** digital_wellbeing_score (numeric).

**Size:** ~8 KB.

**Split**: 80% training, 20% testing.

 ### **Preprocessing**
 
Removed outliers using IQR-based clipping (1.5×IQR).

Rescaled features using StandardScaler (Z-score normalization).

No missing values were present.

---

## **Data Visualization**

Histograms and boxplots were used to inspect distributions and outliers.

<img width="592" alt="Image" src="https://github.com/user-attachments/assets/af1aa4ef-fd88-4a0f-b4ed-60988c929216" />



Correlation heatmap confirmed linear relationships.

<img width="694" alt="Image" src="https://github.com/user-attachments/assets/30d8039a-0d6e-4d03-a9e3-888abaef79ef" /> 

Most predictive features: screen_time, social_media_time, mood_level.





