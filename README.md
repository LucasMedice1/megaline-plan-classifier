Megaline Plan Recommendation — Classification Model
Objective

Megaline wants to recommend one of its newer plans, Smart or Ultra, to subscribers still on legacy plans, based on their monthly usage behavior (calls, minutes, messages, and data used). This project builds and compares classification models to predict the right plan (is_ultra) for a given subscriber.

Result

Three models were trained and tuned on a validation set: Decision Tree (best accuracy ~0.78 at max_depth=10), Random Forest with only n_estimators tuned (~0.78), and a fully tuned Random Forest across both max_depth and n_estimators (~0.80 accuracy, the best of the three). The tuned Random Forest was selected as the final model for its higher and more stable accuracy across hyperparameter combinations.

Tools

Python, Pandas, Scikit-learn (train_test_split, DecisionTreeClassifier, RandomForestClassifier, LogisticRegression, accuracy_score), Matplotlib.

What I learned

This project was my first hands-on comparison of multiple classification algorithms on the same problem, reinforcing how to split data into train/validation/test sets and how systematic hyperparameter tuning (looping over depth and estimator counts) can meaningfully improve model accuracy.

Possible improvements

Evaluate the final tuned model on the held-out test set (not just validation) to confirm it generalizes, and compare additional metrics beyond accuracy (such as precision, recall and F1-score), since plan recommendation errors may not be equally costly in both directions.
