### Predictive Modeling for Prediabetes Detection

**Berkeley Haas Capstone Project** [tentative March 2026]

**Author: Rommel Bermudez**

#### Executive summary

The Challenge: Prediabetes (Class 1) is a critical "window of opportunity" for medical intervention, yet it is difficult to detect. In standard data models, this group is often overlooked resulting in a zero detection rate because their health markers are easily confused with healthy individuals.

The Solution: We developed a specialized Logistic Regression model using the UCI dataset, specifically optimized to find the "invisible" prediabetic population. We enhanced the model’s predictive power by introducing new features such as a Lifestyle Score and a Cardiovascular Interaction (High Blood Pressure + High Cholesterol), allowing for the detection of subtle diagnostic signals.


#### Rationale

Prediabetes is defined as higher blood sugar level than normal, but not high enough to be diagnosed as Type 2 Diabetes. Approximately 98 million American adults have prediabetes, and 8 in 10 adults do not know that they have the condition.

The early detection of prediabetes is especially important because prediabetes represents a reversible stage where lifestyle changes can successfully avoid permanent systemic complications. Early intervention can reduce the risk of progressing to Type 2 Diabetes (T2D). Early detection reduces the staggering healthcare burden associated with treating T2D complications, such as kidney failure, blindness, and cardiovascular disease.

#### Research Question

How accurately can a machine learning model predict the early sign of prediabetes in individuals with normal blood sugar level?

#### Data Sources

The diabetes dataset is available in the UC Irvine repository - https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators. The data contains health information, survey data, and demographics about people along with their diagnosis of prediabetes/diabetes. The person's weight, age, clinical biomarkers, and lifestyle habits are among the determinants of prediabetes risk.

 
#### Methodology

To model prediabetes using logistic regression, our analysis will include the essential steps to prepare the dataset with exploratory data analysis (EDA), data cleaning and preprocessing, visual plotting, feature binning, and feature engineering. We will also apply normalization, using techniques like StandardScaler to handle features on different scales. To identify the most significant risk factors, such as High Blood Pressure, BMI, High Cholesterol, etc., we will utilize feature selection methods like L1 Regularization. This approach integrates feature selection directly into the modeling process, penalizing less impactful variables not only to enhance the model and prevent overfitting but also highlights the feature importance of our primary predictors. Finally, we will evaluate the model’s performance using a confusion matrix to calculate accuracy, precision, recall and the F1-score. Additionally, the Confusion Matrix and the Area Under the Curve (ROC-AUC) will be used to measure the model's overall ability to distinguish between prediabetic and healthy individuals.


#### Link to project

- [Link to notebook 1]()


##### Contact and Further Information

Rommel Bermudez

bermudez_homes@comcast.net

+1 925 421 3669
