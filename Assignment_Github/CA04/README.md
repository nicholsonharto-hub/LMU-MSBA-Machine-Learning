CA04 – Ensemble Models Income Classification

📌 Project Overview

This project applies four Ensemble Learning algorithms to predict whether an individual earns more than $50K per year using Census demographic and employment features.

The objective of this assignment is to:

Implement multiple ensemble classifiers

Analyze the effect of varying the number of estimators

Evaluate model performance using Accuracy and AUC

Compare ensemble methods

Identify the best-performing model

The entire notebook follows a structured modeling workflow from preprocessing to comparative analysis.


📊 Dataset

Dataset: Census Income Dataset
Source:
https://github.com/ArinB/MSBA-CA-03-Decision-Trees/blob/master/census_data.csv?raw=true

Target Variable

1 → Income > $50K

0 → Income ≤ $50K

The dataset contains demographic and employment-related features used for classification.


🏗 Project Structure

The notebook is organized into the following sections:

1. Data Foundation Process

Data loading

Train/test split using the provided flag column

Feature/target separation

One-hot encoding of categorical variables

Processing steps follow  the same methodology used in the Decision Tree Assignment, including train-test splitting, feature separation, and one-hot encoding.


2. Ensemble Modeling

Four ensemble models were implemented:

- Random Forest

- AdaBoost

- Gradient Boosting

- XGBoost

For each model:

The number of estimators was varied from 50 to 500 (step size = 50)

Accuracy was computed

AUC was computed

Performance trends were visualized


📊 3. Model Evaluation

Each model was evaluated using:

- Accuracy

- Area Under the ROC Curve (AUC)

AUC was selected as the primary metric for model comparison, as it provides a more reliable measure of classification performance across thresholds.

📈 Performance Summary

Model ranking based on AUC:

- Gradient Boost

- AdaBoost

- XGBoost

- Random Forest

Gradient Boosting achieved the highest overall AUC and demonstrated consistent performance improvements as the number of estimators increased.

XGBoost achieved optimal performance at lower estimator values but showed declining performance as additional boosting rounds were added, suggesting potential overfitting.


🧠 Key Insights

Boosting methods outperformed Random Forest on this dataset.

Increasing estimators generally improved performance for AdaBoost and Gradient Boost.

XGBoost may require additional tuning to prevent overfitting.

Diminishing returns were observed at higher estimator values.

Sequential boosting proved more effective than bagging for this classification task.


🛠 Technologies Used

- Python

- Pandas

- NumPy

- Scikit-learn

- XGBoost

- Matplotlib


📌 Conclusion

This project demonstrates the comparative effectiveness of ensemble learning methods for income classification. Among the evaluated models, Gradient Boosting delivered the strongest performance based on AUC.

The analysis highlights the importance of tuning ensemble size and understanding how estimator growth impacts model behavior and generalization.
