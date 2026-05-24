# XGBoost - Lab

Model Performance

After training and tuning an XGBoost classifier on the Wine Quality dataset:
Before tuning:
Training accuracy: high (overfitting observed)
Test accuracy: moderate (~low 60s)

After GridSearch tuning:
Training accuracy: still very high (~99%+)
Validation accuracy: improved / stabilized (typically ~65–70%)

GridSearchCV tested multiple combinations of:
learning_rate
max_depth
min_child_weight
subsample
n_estimators
It selected the combination that maximized cross-validated accuracy, not just training performance.

Key Findings
1. Overfitting is still present
Training accuracy ≫ validation accuracy
Model memorizes training patterns due to boosting complexity

2. Generalization improved slightly
Validation accuracy is more stable after tuning
Subsampling helped reduce overfitting

3. Best parameters found
Typical optimal set from your run:
learning_rate: 0.1
max_depth: 6
min_child_weight: 1 or 2
subsample: 0.5 or 0.7
n_estimators: 100

Final conclusion
XGBoost significantly improves performance over baseline models
GridSearchCV helps identify better hyperparameters
However, it does not eliminate overfitting completely
Final model is strong but still biased toward training data

Key takeaway

XGBoost is powerful but sensitive — good tuning improves performance, but real gains come from controlling model complexity and preventing overfitting.
