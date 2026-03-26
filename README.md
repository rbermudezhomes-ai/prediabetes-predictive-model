### Predictive Screening Model for Prediabetes Detection

**Berkeley Haas Capstone Project** 

**Author: Rommel Bermudez**

March 2026

#### Executive Summary

**The Challenge:** Prediabetes (Class 1) is a critical "window of opportunity" for medical intervention, yet it is difficult to detect. In standard predictive models, this group is often overlooked resulting in a zero detection rate because their health markers are easily confused with healthy individuals.

**The Solution:** We developed a specialized Logistic Regression model using the UCI dataset, specifically optimized to find the "invisible" prediabetic population. We expanded the feature space by introducing 6 new experimental feature interactions such as BMI Risk Level, Metabolic Index, Early Warnings, Physical Fragility, Pre-Risk Score and Stress Score, to test if composite metrics could better surface subtle diagnostic signals within the prediabetic class.

Our model prioritizes **Recall as the primary success metric** to ensure maximum sensitivity. In a prediabetes screening context, the objective is to capture the 'invisible' at-risk population. A high-recall approach minimizes False Negatives, ensuring that individuals who require early intervention are not overlooked by the system.

#### Rationale

Prediabetes is defined as higher blood sugar level than normal, but not high enough to be diagnosed as Type 2 Diabetes. Approximately 98 million American adults have prediabetes, and 8 in 10 adults do not know that they have the condition.

The early detection of prediabetes is especially important because prediabetes represents a reversible stage where lifestyle changes can successfully avoid permanent systemic complications. Early intervention can reduce the risk of progressing to Type 2 Diabetes (T2D). Early detection reduces the staggering healthcare burden associated with treating T2D complications, such as kidney failure, blindness, and cardiovascular disease.

#### Research Question

How accurately can a machine learning model predict the early sign of prediabetes in individuals with normal blood sugar level?

#### Data Sources

The diabetes dataset is available in the UC Irvine repository - https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators. The data contains health information, survey data, and demographics about people along with their diagnosis of prediabetes/diabetes. The person's weight, age, clinical biomarkers, and lifestyle habits are among the determinants of prediabetes risk.
The Kaggle Diabetes Dataset - https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset is the version that contains the Multiclass Classification with Target 0, 1, 2. We will use this version in our Predictive Modeling.
 
#### Methodology

To model prediabetes using Logistic Regression, our analysis will include the essential steps to prepare the dataset with exploratory data analysis (EDA), data cleaning and preprocessing, visual plotting, feature interaction, binning, and feature engineering. We will also apply normalization, using techniques like StandardScaler to handle features on different scales. To identify the most significant risk factors—such as High Blood Pressure, BMI, and High Cholesterol—we utilized both Model Coefficients and Permutation Feature Importance. This dual approach integrates feature evaluation directly into the modeling process. By applying L2 Regularization, we penalized less impactful variables to prevent overfitting while simultaneously highlighting the predictive strength of our primary clinical indicators. Finally, we will evaluate the model’s performance using the Classification Report to calculate accuracy, precision, recall and the F1-score. Additionally, the Confusion Matrix and the ROC Curve (ROC-AUC) will be used to measure the model's overall ability to distinguish between prediabetic and healthy individuals.

To address the extreme 1:46 class imbalance, we implemented an automated Optimization Pipeline that moved beyond manual tuning to prioritize clinical sensitivity. By systematically evaluating thousands of combinations of SMOTE oversampling and Strategic Undersampling, we engineered an optimized training ratio that provided the model with a stronger signal for the minority class. This rigorous mathematical "stress test" ensured the model remained stable while achieving a 90% Recall rate, transforming a difficult diagnostic hurdle into a robust patient screening tool.


#### Results
To identify the most reliable screening tool, we benchmarked our optimized pipeline against a Random Forest model. The Optimized Logistic Regression was the clear winner for clinical application.

- While a standard Random Forest model only identified 6% of prediabetic cases, our tuned pipeline achieved a 0.90 Recall, successfully capturing 9 out of 10 at-risk individuals.

- We achieved this high sensitivity by prioritizing Patient Capture over Accuracy. In a medical screening context, we deliberately accepted a lower accuracy (30%) to ensure that high-risk patients are not "missed" by the system.

- Using a 3-fold Grid Search, we proved that a triple strategy — combining SMOTE, Undersampling, and Custom Class Weights (1:5:2) — provided the most stable and efficient predictive power for this extreme 1:46 imbalance.

#### Next Steps
While our current model excels at identifying at-risk individuals (90% Recall), the next phase of development will focus on reducing false alarms and improving the model's "confidence" (Precision).

- Integration of Bio-Markers: To move beyond general health surveys, we aim to incorporate objective clinical data such as HbA1c levels, fasting glucose readings, and insulin sensitivity markers. Adding these biological anchors will allow the model to distinguish between general metabolic stress and true prediabetic progression.

- Advanced Algorithmic Exploration: We will evaluate more complex architectures — such as XGBoost, LightGBM, or Neural Networks — using the high-sensitivity baseline we’ve already established. These models may better capture the non-linear "tipping points" in patient data that simpler models might miss.

- Precision-Recall Optimization: Our primary goal is to tighten the decision boundary. By refining our Grid Search to balance high sensitivity with better precision, we can reduce the number of false positives, ensuring that clinical resources are directed toward the patients with the highest verifiable risk.


#### Link to Project

- **Final Capstone Project** - [Predictive Screening Model for Prediabetes Detection](https://github.com/rbermudezhomes-ai/prediabetes-predictive-model/blob/main/prediabetes_capstone_project.ipynb) Jupyter Notebook
  
- Initial Draft Version - Feb 2026 - [Prediabetes Predictive Modeling](https://github.com/rbermudezhomes-ai/prediabetes-predictive-model/blob/main/prediabetes_model_capstone_v1.ipynb) Jupyter Notebook


##### Contact and Further Information

Rommel Bermudez

bermudez_homes@comcast.net
