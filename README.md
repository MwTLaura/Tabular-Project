# Tabular-Project

![UTA-DataScience-Logo](https://github.com/user-attachments/assets/fec1b411-bda5-437a-9eb8-08a018eb84ae)

# **Predicting Digital Wellbeing Score from Behavioral and Mental Health Data**

## **One Sentence Summary:**
This repository uses behavioral and mental health data to predict digital wellbeing scores through machine learning regression models.

Dataset used: [Mental Health and Digital Behavior 2020–2024 on Kaggle](https://www.kaggle.com/datasets/atharvasoundankar/mental-health-and-digital-behavior-20202024)

---

## **Overview:**
This project aims to determine whether a person’s digital wellbeing score can be accurately predicted using data on their daily digital behavior and self-reported mental health indicators. The dataset used includes 500 entries, each representing a daily snapshot with features such as daily_screen_time_min, num_app_switches, sleep_hours, notification_count, social_media_time_min, focus_score, mood_score, anxiety_level, along with a calculated digital wellbeing score as the target variable.

The machine learning pipeline involves several key steps: handling outliers using IQR-based clipping, rescaling features with StandardScaler, and conducting exploratory data analysis using histograms, boxplots, and correlation heatmaps to better understand feature relationships. The regression task is approached using three models: Linear Regression, Random Forest, and XGBoost.

Model performance is evaluated using RMSE and R². Linear Regression outperforms the others with an RMSE of 0.59 and an R² score of 0.99, indicating a near-perfect fit. Random Forest and XGBoost also perform well, with slightly higher error but still strong predictive power. The results suggest that even simple models can effectively estimate digital wellbeing based on a few well-selected behavioral features, highlighting the potential for real-world applications in digital health monitoring, mental wellbeing assessment, or personalized feedback systems.

This repository contains all code and documentation necessary to reproduce the results, apply the models to new data, or extend the project with additional modeling approaches.


---

## **Summary of Work**
## **Data**

**Type**: CSV file with 500 daily user entries.

**Input Features (7):**

daily_screen_time_min, num_app_switches, sleep_hours, notification_count, social_media_time_min, focus_score, mood_score, anxiety_level.

**Target:** digital_wellbeing_score.

**Size:** ~8 KB.

**Split**: 80% training, 20% testing.

 ## **Preprocessing**
 
- Removed outliers using IQR-based clipping (1.5×IQR).

- Rescaled features using StandardScaler (Z-score normalization).

- No missing values were present.


---

## **Data Visualization**

**Histograms and boxplots were used to inspect distributions and outliers.**

<img width="592" alt="Image" src="https://github.com/user-attachments/assets/af1aa4ef-fd88-4a0f-b4ed-60988c929216" />

<img width="1117" alt="Image" src="https://github.com/user-attachments/assets/23e31d8c-e6f7-4ded-b9cd-bca26cb125e8" />


**Correlation heatmap confirmed linear relationships.**

<img width="694" alt="Image" src="https://github.com/user-attachments/assets/30d8039a-0d6e-4d03-a9e3-888abaef79ef" /> 


**Visual after scalling the data**

<img width="1116" alt="Image" src="https://github.com/user-attachments/assets/5bf9a3e5-3bb9-47a1-b9d7-a05cb9dfdc95" />


---

## **Problem Formulation**

**Input:** 7 numerical behavioral and self-reported features

**Output:** Continuous wellbeing score (regression)

**Models:**

- Linear Regression

- Random Forest Regressor

- XGBoost Regressor

### **Evaluation Metrics:**

- RMSE (Root Mean Squared Error)

- R² (Coefficient of Determination)


--- 

### **Training**

- Performed in Jupyter Notebooks using scikit-learn, numpy, pandas, and matplotlib

- StandardScaler used on all features

- Training time: Instant for LR, ~5–10s for RF/XGB

- Hardware: CPU only (no GPU required)


---

### **Performance Comparison**

<img width="246" alt="Image" src="https://github.com/user-attachments/assets/44e7d910-f125-48a7-8f85-0e64ad55b68e" />

<img width="590" alt="Image" src="https://github.com/user-attachments/assets/f97bcec5-4040-4043-a3b4-f2487ea450bb" />

---

## **Conclusion**

The project confirms that digital wellbeing can be accurately predicted from behavioral data using simple ML models.
Linear Regression was the most effective, likely due to the strong linearity in the dataset after preprocessing.

--- 

## **Future Work**

- Using a larger or more diverse dataset.

- Exploring interaction terms and feature engineering.

- Trying time-series.

---

## **How to Reproduce Results**

- Download the dataset from Kaggle: [Mental Health and Digital Behavior 2020–2024](https://www.kaggle.com/datasets/atharvasoundankar/mental-health-and-digital-behavior-20202024)
- Place the CSV file in your project folder before running the notebooks.
- Open the notebook digital_wellbeing_prediction.ipynb
- Install required packages: pandas, numpy, scikit-learn, matplotlib, xgboost
- Run all cells from top to bottom.
- The notebook performs preprocessing, trains and evaluates three regression models, and displays performance metrics and visualizations.


---

## **Overview of Repository**

**Dgital_Wellbeing_Prediction.ipynb**: 	Main notebook containing the full pipeline: data preprocessing, visualization, modeling, and evaluation.
**README.md**	:Project summary and documentation

---

## **References**
Kaggle Dataset: [Mental Health and Digital Behavior (2020–2024)](https://www.kaggle.com/datasets/atharvasoundankar/mental-health-and-digital-behavior-20202024)












