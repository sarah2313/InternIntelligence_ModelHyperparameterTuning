## Model Hyperparameter Tuning Documentation

### Overview of the Model & Dataset
- **Dataset Used**: Breast Cancer Dataset from Scikit-Learn.
- **Reason for Choice**: This dataset is widely used for classification tasks, making it suitable for testing and improving machine learning models.
- **Models Used**: 
  - **Random Forest** (Baseline Model)
  - **XGBoost** (Tuned Model)
- **Objective**: Optimize hyperparameters to improve model accuracy and generalization.

### Hyperparameter Tuning Approach
- **Grid Search CV**: Exhaustive search over a predefined hyperparameter grid.
- **Optuna Optimization**: Automated hyperparameter tuning using Bayesian optimization.
- **Comparison of Approaches**: Both tuning methods were compared to identify the best-performing model.

### Best Hyperparameters
- **Grid Search Best Parameters:**
  - `n_estimators`: 200
  - `max_depth`: 6
  - `learning_rate`: 0.1
  - `min_child_weight`: 3
  - `gamma`: 0.1
- **Optuna Best Parameters:**
  - `n_estimators`: 300
  - `max_depth`: 9
  - `learning_rate`: 0.15
  - `min_child_weight`: 5
  - `gamma`: 0.05

### Final Model Performance
| Model                     | Accuracy |
|---------------------------|----------|
| Random Forest (Baseline)  | 0.9561   |
| XGBoost (Tuned Grid)      | 0.9649   |
| XGBoost (Tuned Optuna)    | 0.9615   |

- **Key Findings:**
  - Grid Search tuning provided the highest accuracy improvement.
  - Optuna performed well but did not outperform Grid Search in this case.
  - Both tuning methods outperformed the baseline Random Forest model.

### Code & Results
- **Feature Importance**: Visualized to understand the most influential factors.
- **Confusion Matrix**: Displayed to analyze classification performance.
- **ROC Curve**: Evaluated to compare model performance across different thresholds.
- **Comparison Chart**: Showcased performance differences between tuning methods.

### Summary of Findings
1. **Standardized Features** to enhance model performance.
2. **Tuned Hyperparameters using two different methods**: Grid Search and Optuna.
3. **Grid Search provided the best results**, outperforming both Random Forest and XGBoost tuned with Optuna.
4. **Feature Importance Analysis** helped in identifying key factors for prediction.
5. **Confusion Matrix and ROC Curve** provided insights into classification performance.
6. **Final Recommendation**: Grid Search tuning should be prioritized when time and computational resources allow for exhaustive hyperparameter search.

✔ **Overall, hyperparameter tuning significantly improved model accuracy and generalization.**
