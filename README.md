# Vehicle Insurance Claim Fraud Detection

<p align="left">
  <img src="https://img.shields.io/badge/Made%20With-Colab-blue?logo=googlecolab&logoColor=white&label=Made%20With" alt="Made with Colab">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License: MIT">
  <img src="https://img.shields.io/github/repo-size/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project" alt="Repo Size">
  <img src="https://img.shields.io/github/last-commit/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project" alt="Last Commit">
  <img src="https://img.shields.io/github/issues/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project" alt="Issues">
  <img src="https://img.shields.io/badge/Data%20Visualization-Python-yellow?logo=python" alt="Data Visualization: Python">
  <img src="https://img.shields.io/badge/Version%20Control-Git-orange?logo=git" alt="Version Control: Git">
  <img src="https://img.shields.io/badge/Host-GitHub-black?logo=github" alt="Host: GitHub">
  <img src="https://img.shields.io/github/forks/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project?style=social" alt="Forks">
  <img src="https://img.shields.io/badge/Project-Completed-brightgreen" alt="Project Status">
</p>

![Dashboard](https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/title_image.png?raw=true)

## Project Overview

Vehicle insurance fraud is a serious crime that undermines the integrity of the insurance system and increases costs for everyone. It involves elaborate schemes where individuals conspire to submit false or exaggerated claims regarding property damage or personal injuries following an accident. Common tactics include staged accidents, where criminals intentionally create collisions for profit; phantom passengers, where individuals who were not even present at the scene claim to have suffered severe injuries; and grossly exaggerated personal injury claims. These fraudulent activities not only harm honest policyholders but also strain resources that could be better allocated to legitimate claims. It is essential to recognize and combat these deceitful practices to protect the integrity of our insurance system.

For this project, a publicly available dataset was utilized, and various machine learning algorithms were applied, including `Logistic Regression`, `SVM`, `KNN`, `XGBoost`, `Decision Tree`, `Random Forest`, and `AdaBoost`. The performance of these models was evaluated using metrics such as accuracy, precision, recall, F1-score, and confusion matrices. Experiments were conducted on Google Colab, leveraging A100 GPU environments for faster training. The final deliverables include a comparative analysis of model performance, detailed visualizations, and recommendations for effective real-world fraud detection solutions.

## Dataset & Visualization
The dataset [`Vehicle Insurance Claim Fraud Detection`](https://www.kaggle.com/datasets/shivamb/vehicle-claim-fraud-detection) is sourced from Kaggle. It is formed of 32 features which are `Month` `WeekOfMonth` `DayOfWeek` `Make` `AccidentArea` `DayOfWeekClaimed` `MonthClaimed` `WeekOfMonthClaimed` `Sex` `MaritalStatus` `Age` `Fault` `PolicyType` `VehicleCategory` `VehiclePrice` `PolicyNumber` `RepNumber` `Deductible` `DriverRating` `Days_Policy_Accident` `Days_Policy_Claim` `PastNumberOfClaims` `AgeOfVehicle` `AgeOfPolicyHolder` `PoliceReportFiled` `WitnessPresent` `AgentType` `NumberOfSuppliments` `AddressChange_Claim` `NumberOfCars` `Year` `BasePolicy` and target `FraudFound_P` to detect if a claim application is fraudulent or not. The dataset contains 15420 entries labeled as either `0` (fraud not found) or `1` (fraud found). Some visualization of the dataset is included here.
<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_month.png?raw=true" alt="Bar Chart of Month" width="54%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_day_of_week.png?raw=true" alt="Bar Chart of Day of Week" width="43.15%" />
</p>

The first bar chart displays monthwise count of accidents. We can see that accidents occur the most in January and least in August. The second bar chart counts daywise accidents. It is evident that first and last working days of the week see the highest number of accidents while least on sundays. 

<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_day_of_week_claimed.png?raw=true" alt="Bar Chart of Day of Week Claimed" width="49%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_month_claimed.png?raw=true" alt="Bar Chart of Month Claimed" width="49%" />
</p>

From the the charts above we see that in May and January, insurance holders file for accident insurance claims the most, while lowest in August. Also, claims are high in weekdays but very few in weekends.

<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_sex.png?raw=true" alt="Bar Chart of Sex" width="33%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_marital_status.png?raw=true" alt="Bar Chart of Marital Status" width="33%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_age_of_policy_holder.png?raw=true" alt="Bar Chart of Age of Policy Holder" width="33%" />
</p>


