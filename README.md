## Give Life: Predict Blood Donations

## Blood Donation Prediction
This project aims to predict the likelihood of whether or not a donor will give blood the next time the vehicle comes to campus.

## Dataset
Our dataset is from a mobile blood donation vehicle in Taiwan. The Blood Transfusion Service Center drives to different universities and collects blood as part of a blood drive. 

## Methodologies 
**Automated Machine Learning with TPOT:**

* The Tree-based Pipeline Optimization Tool (TPOT) was utilized for automated machine learning.
* TPOT automates the process of:
    * Feature selection.
    * Model selection (e.g., Random Forest, Gradient Boosting, Logistic Regression).
    * Hyperparameter tuning.
    * Pipeline construction.
* TPOT was configured to optimize for the appropriate evaluation metric (e.g., AUC, accuracy, F1-score), based on the project's goals.
* The number of generations and population size were adjusted to balance optimization time and model performance.
* The TPOT generated pipeline was exported as a `scikit-learn` pipeline.

**Model Evaluation:**

* The dataset was split into training and testing sets using `scikit-learn`'s `train_test_split` function.
* The trained TPOT pipeline was evaluated on the test set.
* Performance metrics, such as:
    * Area Under the ROC Curve (AUC).
* were calculated using `scikit-learn`'s metrics module.
* The results were analyzed to assess the model's predictive performance and identify potential areas for improvement.

## Libraries Used

* `pandas`: For data manipulation and analysis.
* `numpy`: For numerical computations.
* `scikit-learn`: For machine learning algorithms, preprocessing, and evaluation.
* `TPOT`: For automated machine learning pipeline optimization.
