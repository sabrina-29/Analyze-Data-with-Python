# Analyze-Data-with-Python
Stroke Risk Factors – Exploratory Data Analysis (EDA)

📌 Project Overview

Stroke is a life-threatening medical condition caused by interrupted blood flow to the brain, leading to oxygen deprivation and potential long-term disability or death. It is primarily categorized into:
Ischemic stroke – blockage of blood flow
Hemorrhagic stroke – bleeding in the brain
Transient Ischemic Attack (TIA) – temporary blockage without permanent damage
Despite its severity, studies show that up to 80% of strokes are preventable, making early detection of risk factors critical.
This project performs a comprehensive Exploratory Data Analysis (EDA) to identify key demographic, clinical, and lifestyle factors associated with stroke risk, and to uncover patterns that may support early prevention strategies.

Objectives

Understand data structure, distributions, and key characteristics
Identify major demographic, lifestyle, and medical risk factors
Analyze relationships between features and stroke occurrence
Compare stroke prevalence across population groups
Create clear and insightful visualizations for interpretation and decision-

Research Questions

Are there differences in stroke prevalence between males and females?
How does age affect stroke risk?
What is the relationship between BMI, glucose levels, and stroke occurrence?
Does smoking increase stroke probability?
Is heart disease a strong predictor of stroke?
How is work type associated with hypertension and stroke?
Does residence type (urban vs rural) influence stroke risk?

Data Preprocessing

🔧 Missing Values Handling

Only BMI contained missing values
Missing values were imputed using median BMI per age group
Age was binned into groups to improve imputation accuracy
This approach preserves real-world distribution patterns

📈 Outlier Detection & Treatment

🔹 Glucose Levels

Highly right-skewed distribution
434 extreme high values (>200) detected
Values were clipped to range [23, 200]
Applied log transformation to reduce skewness
✔ Result: more normalized and model-friendly distribution

🔹 BMI

Slightly skewed distribution
Outliers detected at both extremes (<18 and >46)
Applied winsorization:
Values < 18 → set to 18
Values > 46 → set to 46
✔ Result: reduced noise and improved stability

🔢 Feature Encoding

Categorical variables were encoded for statistical and ML readiness:
Gender: Female → 0, Male → 1
Ever_married: No → 0, Yes → 1
Residence_type: Rural → 0, Urban → 1
Additionally, rows with "Other" gender were removed due to extremely low frequency.

📊 Dataset Overview

After preprocessing:

The dataset shows a strong class imbalance (low stroke rate)
Clear differences emerge between stroke vs non-stroke populations
Several variables show meaningful predictive potential
This confirms the dataset is suitable for further predictive modeling.

📈 Exploratory Data Analysis (EDA)

🔹 Univariate Analysis

Descriptive statistics were analyzed for:

Age
BMI
Average Glucose Level
Each feature was evaluated using:
Mean
Median
Min / Max
Standard deviation
This provided insights into distribution shape and variability.

🔹 Visual Analysis

The following analyses were performed:

Stroke distribution by age groups
Gender vs stroke rate
BMI & glucose distributions (before/after transformation)
Smoking status impact on stroke occurrence
Heart disease correlation with stroke
Work type vs hypertension/stroke
Residence type comparison
Marital status influence
Correlation heatmap of all numerical features

🧠 Key Insights & Findings

The analysis reveals several strong and consistent patterns:

Age is the strongest non-clinical predictor of stroke
Hypertension, heart disease, and high glucose levels show strong association with stroke risk
Smoking increases stroke probability
Certain work types and stress-related indicators correlate with hypertension
Stroke is a multifactorial condition, influenced by both lifestyle and medical history
The dataset shows clear separability between risk groups in multiple features

📌 Conclusion

This EDA highlights the importance of early risk detection and lifestyle awareness in stroke prevention. The findings support:

Early screening for high-risk populations
Monitoring of glucose, blood pressure, and heart conditions
Public health awareness for modifiable risk factors

🚀 Future Work

Build predictive machine learning models (Logistic Regression, Random Forest, XGBoost)
Handle class imbalance (SMOTE / weighting techniques)
Feature importance analysis
Risk scoring system for patients
Time-based or longitudinal medical data integration

🛠️ Technologies Used

Python
Pandas
NumPy
Matplotlib
Seaborn

🚀 How to Run

pip install pandas numpy matplotlib seaborn

Run the Jupyter Notebook to reproduce the full analysis and visualizations.
Is marital status linked to stroke occurrence?
Can work pressure or stress be indirectly associated with stroke via hypertension?
Which features are the strongest predictors of stroke?
