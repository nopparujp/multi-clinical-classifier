# Multi Clinical Classification

## Exploratory data analysis (EDA)
- The dataset includes 26 anonymized clinical features (A-Z) and an ordinal class label
- Each feature has approximately 20% missing data
- Significant missing data in the 'class' column of the training set

## Data preprocessing
- Remove rows with missing 'class' values
- Fill missing value with mean of each feature

## Model selection
- Using Support Vector Classifier(SVC)
- SVC is effective in high-dimentional spaces, making it ideal for 26-feature dataset

## Model training
- Utilized Scikit-learn to train the SVC model

## Hyperparameter tuning
- Applied GridSearchCV for comprehensive hyperparameter optimization
- experimenting with different configurations for 'decision_function_shape', choosing between 'ovr' and 'ovo'

## Evaluation
- Macro f1 score 
  - We achieved a notable macro F1 score of 0.836
  - Indicating a strong balance between precision and recall across all classes
- confusion matrix
  - plot confusion matrix to inspect model's performance across difference classes

## Error analysis
The model misclassify instances of a particular class(e.g., 0.0) becauseof limted data available for this category. We can improve it by reblancing the dataset or add more training data for underrepresented classes.