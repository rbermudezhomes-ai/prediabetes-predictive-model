### Predictive Modeling for Prediabetes Detection

**Berkeley Haas Capstone Project** [March 2026]

**Author: Rommel Bermudez**

#### Executive summary

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


#### Link to project

- **Final Version** -[Predictive Modeling for Prediabetes Detection](https://github.com/rbermudezhomes-ai/prediabetes-predictive-model/blob/main/prediabetes_capstone_project.ipynb)
<br><br>
- Initial Version 1 - [Prediabetes Predictive Modeling Jupyter Notebook](https://github.com/rbermudezhomes-ai/prediabetes-predictive-model/blob/main/prediabetes_model_capstone_v1.ipynb)

##### Contact and Further Information

Rommel Bermudez

bermudez_homes@comcast.net

+1 925 421 3669
