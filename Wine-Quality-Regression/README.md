## 📊 Data Source

This project uses the Wine Quality datasets from the UCI Machine Learning Repository.

> **Citation**  
P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis (2009).  
*Modeling wine preferences by data mining from physicochemical properties*.  
Decision Support Systems, 47(4):547–553.  
[https://doi.org/10.1016/j.dss.2009.05.016](https://doi.org/10.1016/j.dss.2009.05.016)

Dataset available at: [https://archive.ics.uci.edu/ml/datasets/wine+quality](https://archive.ics.uci.edu/ml/datasets/wine+quality)

-------------------------------------------------------------

## 🍷 Wine Quality Prediction with Machine Learning
1. Introduction

Wine quality is traditionally assessed by expert tasters, but such evaluations are subjective, costly, and time-consuming. This project aims to build a machine learning model that predicts wine quality using physicochemical features. By automating quality prediction, wineries can improve consistency, reduce costs, and enhance consumer satisfaction.

---------------------------------------------

2. Dataset Description

* Source: UCI Wine Quality Dataset

* Samples: ~4,898 white wines or ~1,599 red wines (depending on subset)

* Features: 11 physicochemical variables, including:

    * Fixed acidity

    * Volatile acidity

    * Citric acid

    * Residual sugar

    *  Chlorides

    * Free sulfur dioxide

    * Total sulfur dioxide

    * Density

    * pH

    * Sulphates

    * Alcohol

* Target Variable: Wine quality score (0–10, integer).

* Class Imbalance: Most wines fall in the middle scores (5–7), with relatively few at the extremes. This imbalance motivates the use of resampling techniques and balanced evaluation metrics.

-----------------------------------------

3. Methodology

The machine learning workflow is organized into a pipeline for reproducibility and clarity:

* Preprocessing

    * Missing values imputed using median strategy.

    * Features scaled with MinMaxScaler to ensure comparable ranges.

* Handling Imbalance

    * Applied SMOTE (Synthetic Minority Over-sampling Technique) to balance underrepresented quality classes.

* Dimensionality Reduction

    * Used Recursive Feature Elimination (RFE) and Principal Component Analysis (PCA) to identify the most relevant features and reduce dimensionality.

* Model Selection

    * Chose Logistic Regression (solver = saga, max_iter=5000) as the baseline classifier.

    * Hyperparameter optimization performed with HalvingRandomSearchCV combined with StratifiedKFold cross-validation for efficient and robust model tuning.

* Evaluation

    * Metrics: Accuracy, Balanced Accuracy, Macro F1.

    * Visualizations: Confusion Matrix and ROC curves.

--------------------------------------------------

4. Evaluation Strategy

Since the dataset is imbalanced, raw accuracy can be misleading (a model predicting only the majority class would score high). To account for this, the following metrics were prioritized:

* Accuracy – overall proportion of correct predictions.

* Balanced Accuracy – averages recall across all classes, giving equal weight to minority labels.

* Macro F1 – harmonic mean of precision and recall, calculated equally for all classes.

* Confusion Matrix – illustrates true vs. predicted class distributions.

-----------------------------------------

5. Results Summary

* Without SMOTE: Logistic Regression achieved high raw accuracy (~93%) but performed poorly on minority classes.

* With SMOTE: Overall accuracy decreased (~55%), but balanced accuracy and macro F1 improved, reflecting fairer treatment of all classes.

This highlights the trade-off between maximizing raw accuracy versus building a model that generalizes better across all quality levels.

6. Conclusion

Machine learning provides a promising approach for predicting wine quality from physicochemical features. While baseline logistic regression achieved high accuracy, imbalanced class distributions strongly affected fairness across classes. The use of SMOTE improved representation of minority classes, at the cost of raw accuracy.

Future Directions:

* Explore ensemble methods such as Random Forest, XGBoost, or Gradient Boosting.

* Compare with regression approaches predicting the exact quality score.

* Integrate sensory or textual data (e.g., tasting notes) to complement physicochemical features.
