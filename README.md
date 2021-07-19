# Machine Learning Challenge
Dave Wisinski
----
July 2021
----
----

## Purpose/Process

The purpose of this project is demonstrate a number of machine learning concepts via testing various models on an example dataset of NASA Kepler space telescope data.

## Model Performance

**Logistic Regression**: 0.8798 (87.98%) accuracy on test data.

The logistic regression model was tested and subsequently tuned using GridSearchCV (cross-validated grid-search) to adjust the model's available hyperparameters. The "tuned" model did perform slightly better (about 2.1%) in terms of overall accuracy on the test data.

**Random Forest**: 0.8758 (87.58%) accuracy on test data.

The random forest model was tested and subsequently re-tested after implementing significant feature selection using the [feature importance technique](https://scikit-learn.org/stable/auto_examples/ensemble/plot_forest_importances.html). Feature importance was used to improve the model's performance by removing those features which scored with an importance score of less than 1%. Doing so however only improved the model's accuracy negligibly (about 0.2% improvement on test data). The resulting model was subsequently tuned further using GridSearchCV, however the final model performance was ultimately slightly lower than the initial run.

Given additional time, more parameter tuning (including criterion adjustment, number of estimators, etc.) would be required on the random forest model in order to potentially yield better performance.

**Deep Learning**: 0.8919 (89.19%) accuracy on test data.

The deep learning model (using TensorFlow/Keras) scored the highest of the three models tested, without any additional tuning. Additional layers could be added to this model for potential improved performance at the cost of additional required computing resources.

## Final Observations

Given more time, additional models including KNN (K-Nearest Neighbors) and SVM (Support Vector Machine) models would also be tested for comparison against the performance of the models noted above. Additionally train/test splits would be modified for each to better gauge performance of models on final testing.

Choosing the "best" model for a given dataset will depend on a number of factors, including the breadth/size of the dataset itself, the available time and computing resources, etc.

For the purposes of this project all three of the tested models performed relatively comparably in terms of both time and final accuracy.

## Notes

Source data .csv is located in the /source_data folder.

The Logistic Regression and Random Forest models are saved in the main repository as .sav files, and the Deep Learning model is saved in the same location as an .h5 file.
