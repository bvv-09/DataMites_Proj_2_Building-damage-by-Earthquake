# DataMites_Proj_2_Building-damage-by-Earthquake


## Project description 
Machine learning project to predict earthquake damage grades/levels on buildings using building structure, geographical, and ownership features. Includes EDA, feature engineering, encoding strategies, and model comparison using Random Forest and LightGBM with cross-validation.

## Objective
- Predicting earthquake damage levels on buildings
- Classify damage into 3 categories (1, 2, 3)(clearly a multi class classification task)
- Building a robust ML pipeline with proper preprocessing and evaluation

## Dataset Information
- Source: https://www.drivendata.org/competitions/57/nepal-earthquake/page/136/
- Number of rows / features : I has approx 260601 rows and 40 columns
- Target variable: damage_grade (3 classes)
- Key feature groups: Geo features, Structural features(especially roof, and land's)

## Data Preprocessing
- Handling categorical variables using one-hot encoding
- Frequency encoding for geographical features
- Log transformation for skewed features (age, area_percentage)
- Missing values & duplicates handling 
- Train-test split with stratification

## Exploratory Data Analysis (EDA)
- Class imbalance observed in target variable
- Geographical features show strong influence on damage levels
- Skewed distributions in numerical features
- Relationship between structural attributes and damage severity

## Models Used
- Random Forest Classifier (baseline)
- LightGBM Classifier (final model)
-- LightGBM showed better performance and stability compared to Random Forest.

## Evaluation Metrics used
- Macro F1 Score (primary metric due to class imbalance)
- Accuracy (secondary metric)
- Confusion Matrix
- Stratified 5-Fold Cross Validation

## Results:
- Random Forest: Macro F1: ~0.62

- LightGBM: Macro F1: ~0.66

- Cross Validation (LightGBM): Mean Macro F1: ~0.665, Std: ~0.0019

## Key Insights
- Geographical features are the most influential predictors
- LightGBM significantly improves performance over baseline
- Model shows stable performance across cross-validation folds
- Frequency encoding did not significantly improve results

## Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- LightGBM
- Matplotlib / Seaborn

## Future Work
- Hyperparameter tuning of LightGBM
- Experiment with CatBoost / XGBoost
- Advanced geo-spatial feature engineering
- Ensemble modeling
- Feature selection optimization
