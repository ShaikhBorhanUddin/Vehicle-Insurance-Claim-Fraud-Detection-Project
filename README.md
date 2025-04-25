# Vehicle Insurance Claim Fraud Detection

<p align="left">
  <img src="https://img.shields.io/badge/Made%20With-Colab-blue?logo=googlecolab&logoColor=white&label=Made%20With" alt="Made with Colab">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License: MIT">
  <img src="https://img.shields.io/github/repo-size/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project" alt="Repo Size">
  <img src="https://img.shields.io/github/last-commit/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project" alt="Last Commit">
  <img src="https://img.shields.io/github/issues/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project" alt="Issues">
  <img src="https://img.shields.io/badge/Data%20Visualization-Python-yellow?logo=python" alt="Data Visualization: Python">
  <img src="https://img.shields.io/badge/Result%20Visualization-LIME-green?style=flat&logo=LIME" alt="Result Visualization: LIME">
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
The dataset [`Vehicle Insurance Claim Fraud Detection`](https://www.kaggle.com/datasets/shivamb/vehicle-claim-fraud-detection) is sourced from Kaggle. It contains 15,420 records and 32 input features, with the target variable FraudFound_P, which indicates whether a claim was fraudulent (1) or not (0). The features include temporal details (Month, WeekOfMonth, DayOfWeek, etc.), vehicle information (Make, VehicleCategory, VehiclePrice), demographic attributes (Sex, MaritalStatus, Age), and claim-related variables such as PoliceReportFiled, WitnessPresent, and NumberOfSuppliments.

To understand the structure and distribution of the data, several exploratory visualizations were generated.

### Accident Trends:
<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_month.png?raw=true" alt="Bar Chart of Month" width="54%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_day_of_week.png?raw=true" alt="Bar Chart of Day of Week" width="43.15%" />
</p>

A bar chart of accident occurrences by month shows that January sees the highest number of reported accidents, while August sees the least. Similarly, Mondays and Fridays have the most accidents, with Sundays seeing the fewest.

### Claim Filing Patterns: 
<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_day_of_week_claimed.png?raw=true" alt="Bar Chart of Day of Week Claimed" width="49%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_month_claimed.png?raw=true" alt="Bar Chart of Month Claimed" width="49%" />
</p>

Claims are most frequently filed in May and January, with noticeably fewer in August. Weekday claim submissions are significantly more common than those on weekends.

### Demographic Distribution:

<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_sex.png?raw=true" alt="Bar Chart of Sex" width="32.5%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_marital_status.png?raw=true" alt="Bar Chart of Marital Status" width="32.5%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_age_of_policy_holder.png?raw=true" alt="Bar Chart of Age of Policy Holder" width="32.5%" />
</p>

The dataset is predominantly composed of male policyholders, with most individuals falling into the 30–50 age range. In terms of marital status, most policyholders are either married or single, with a smaller proportion being divorced or widowed.

### Police and Witness Reports:

<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_police_report_filed.png?raw=true" alt="Bar Chart of Police Report Filed" width="49%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_witness_present.png?raw=true" alt="Bar Chart of Witness Present" width="49%" />
</p>

A large number of claims lack police reports or eyewitness accounts, which may impact the likelihood of a claim being classified as fraudulent.

### Vehicle Insights: 

<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_vehicle_category.png?raw=true" alt="Bar Chart of Vehicle Category" width="49%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/bar_chart_of_vehicle_price.png?raw=true" alt="Bar Chart of Vehicle Price" width="49%" />
</p>

The majority of vehicles involved are sedans and sports cars, with most valued at under $40,000.

These visualizations provided key insights into the behavior and structure of the dataset, guiding both preprocessing and model development phases.

## Folder Structure
```bash
Email-and-SMS-Spam-Detection-Project
│
├── Dataset/                # Contains raw CSV files
├── src/                    # Model training, preprocessing scripts                 
│     |
|     └──   CNN_Spam_Detection_Dataset_214843.ipynb
|
├── Images/                 
├── requirements.txt        # Python dependencies
├── Licence                 # MIT License
└── README.md               # Overview of the project
```

## Project Workflow

This project follows a clear and structured pipeline to build, train, and interpret models for detecting spam in SMS and email messages. The steps below outline the end-to-end process from raw data to model explainability and future improvements.
- Upload Datasets
- Clean, Preprocess, and Feature Selection
- Model Selection
- Train Models
- See Results
- Visualize Decisions with Tools
- Suggest Future Development

## Experiments
For training quick, all model instaces were created simultaneously. There was no issues during training.

![Dashboard](https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/model_training.png?raw=true)

## Results

To assess the effectiveness of different machine learning models in detecting fraudulent vehicle insurance claims, seven algorithms were evaluated based on four key metrics: accuracy, precision, recall, and F1-score. Each of these metrics offers valuable insights into the models' abilities to accurately identify fraud, especially in a highly imbalanced dataset.

<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/accuracy.png?raw=true" alt="Accuracy" width="24%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/precision.png?raw=true" alt="Precision" width="24%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/recall.png?raw=true" alt="Recall" width="24%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/F1.png?raw=true" alt="F1 Score" width="24%" />
</p>

Starting with accuracy, all models performed comparably well. XGBoost stood out with the highest accuracy of 95.1%, while Random Forest (94.1%), SVM, Logistic Regression, and AdaBoost all hovered around 94%. KNN came in slightly lower at 93.8%, and Decision Tree scored the lowest at 91.0%.
Despite high accuracy, precision revealed the true discriminative power of each model. SVM achieved perfect precision (1.00), indicating every fraud it predicted was correct. Random Forest (0.80) and XGBoost (0.72) also performed well in minimizing false positives. In contrast, Logistic Regression and AdaBoost both failed to identify any fraudulent claims correctly (precision of 0.000), while KNN (0.316) and Decision Tree (0.272) showed weak precision.
The recall metric, which measures how well the models captured actual fraud cases, told a different story. Decision Tree slightly edged out XGBoost with a recall of 0.304, compared to 0.298. These two models were the most effective at identifying true frauds. The rest—including SVM (0.006), KNN (0.033), and Random Forest (0.022)—struggled, and both Logistic Regression and AdaBoost again recorded 0.000, failing to detect any fraud instances.
Finally, the F1-score, which balances both precision and recall, provided a consolidated view. XGBoost had the highest F1-score of 0.422, showing it struck the best balance between catching fraud and avoiding false positives. Decision Tree followed with an F1-score of 0.287, making it a reasonable alternative. All other models underperformed, with SVM (0.011), KNN (0.060), and Random Forest (0.043) offering limited utility. Logistic Regression and AdaBoost again failed with an F1-score of 0.000.

While several models achieved high accuracy, only XGBoost consistently demonstrated outstanding performance across all metrics. It exhibited strong fraud detection capabilities, providing a favorable balance between precision and recall, making it the most suitable model for this task.

## ROC and PR Curves

To further evaluate the classification capabilities of each model, ROC (Receiver Operating Characteristic) and PR (Precision-Recall) curves were analyzed. These curves provide deeper insight into the trade-offs between sensitivity, specificity, and precision in the presence of class imbalance.

<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/ROC.png?raw=true" alt="ROC Curve" width="49%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/PR.png?raw=true" alt="Precision-Recall Curve" width="49%" />
</p>

Among all models, XGBoost stood out as the most effective, achieving an ROC AUC of approximately 96%, indicating excellent discriminatory power between fraudulent and non-fraudulent claims. It also delivered the strongest PR curve, showcasing its ability to maintain high precision even at various levels of recall. AdaBoost and Random Forest followed with ROC AUCs around 83% and 80% respectively. However, their performance dropped significantly in the PR curve evaluation due to low recall values and sparse detection of the minority (fraudulent) class, which is critical in fraud detection tasks. Models like Logistic Regression, SVM, KNN, and Decision Tree failed to provide competitive ROC or PR curves. Their inability to effectively distinguish between classes, particularly the underrepresented fraud cases, was reflected in flat PR curves and low AUC scores. Despite achieving high accuracy, these models exhibited poor recall and precision, reaffirming the importance of choosing evaluation metrics that reflect class imbalance.

While accuracy alone seemed promising for many models, the ROC and PR analyses revealed that XGBoost was by far the most robust and reliable model for identifying fraudulent claims in this imbalanced classification scenario.
## Confusion Matrix

The explanation of confusion matrices are included in this section.

![Dashboard](https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/cm.png?raw=true)

The Logistic Regression and AdaBoost models both achieved perfect classification for the non-fraudulent class but completely failed to identify fraudulent claims, resulting in zero true negatives and 181 false negatives. This indicates that they labeled all samples as non-fraud, causing a recall and F1-score of 0.000, despite a deceptively high accuracy. SVM slightly improved upon this by identifying one true negative, reducing false negatives to 180, but the overall performance remained ineffective in fraud detection, mirroring the same flaw of overfitting to the majority class. KNN managed 13 false positives and 6 true negatives, with 175 false negatives, suggesting a modest improvement in balancing the classes. While not particularly strong, it at least recognized some fraudulent claims, unlike the previous models. XGBoost, the top-performing model, achieved a significantly better distribution, correctly identifying 127 true positives and 54 true negatives, while maintaining only 21 false positives. This balance led to its highest recall and F1-score, indicating effective fraud detection with minimal sacrifice to precision. Random Forest also showed improvement, recording 177 false negatives, 1 false positive, and 4 true negatives. Although it had high precision, the relatively large number of false negatives diminished its recall. Decision Tree exhibited the most balanced results after XGBoost, with 2696 true positives, 147 false positives, 126 false negatives, and 55 true negatives. While precision dropped due to higher false positives, its recall was the best among all models, helping it secure the second-highest F1-score. 

These confusion matrices clearly reveal that models like Logistic Regression, SVM, and AdaBoost struggled due to extreme class imbalance, while XGBoost and Decision Tree showed the best ability to identify both fraudulent and non-fraudulent claims effectively.

## Visualization

<p align="center">
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/lime_decision_tree.png?raw=true" alt="LIME Decision Tree" width="49%" />
  <img src="https://github.com/ShaikhBorhanUddin/Vehicle-Insurance-Claim-Fraud-Detection-Project/blob/main/Images/lime_xgboost.png?raw=true" alt="LIME XGBoost" width="47.55%" />
</p>


## Technology Used

This project was developed using various data science and machine learning technologies to ensure effective fraud detection. Python was the main programming language utilized, taking advantage of its extensive library ecosystem for data processing and modeling.

Data manipulation and preprocessing were conducted with Pandas and NumPy, while Matplotlib and Seaborn were used for visualizations. For building and evaluating machine learning models, libraries such as scikit-learn and XGBoost were employed. Model performance was assessed using metrics including Accuracy, Precision, Recall, F1-score, Confusion Matrix, ROC and PR curves.

## Future Development

To improve the effectiveness of the fraud detection system, future efforts should focus on expanding the dataset to include a wider range of recent fraud patterns. This enhancement would help the model generalize better. Additionally, implementing ensemble stacking techniques or incorporating deep learning models, such as neural networks, could potentially increase recall without compromising precision. Furthermore, integrating real-time detection capabilities and deploying the model via a web-based dashboard would enable practical and scalable use in production environments. Lastly, applying feature engineering with insights specific to the domain could significantly enhance the model's performance.

## Licence

This project is licensed under the MIT License.
You are free to use, modify, and distribute this project for personal or commercial purposes, provided that proper credit is given to the original author. See the LICENSE file for full details.

## Contact

