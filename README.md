# AI-ML-Task4

1. Import Libraries:
   
          The code imports essential libraries:
               > pandas for data handling
               > sklearn for model building and evaluation
               > matplotlib.pyplot for plotting the ROC curve
  
3. Load and Clean the Dataset:

               > Loads the Breast Cancer dataset from CSV.
               > Drops the 'id' column if present (not useful for prediction).
               Converts the 'diagnosis' column:
                    > 'M' (Malignant) → 1
                    > 'B' (Benign) → 0
               > Replaces zero values in important features with NaN.
               > Fills NaN with the median of each column to fix missing values.

5. Split and Scale the Data:

              Splits the dataset into:
                    > Training data (80%) for learning
                    > Test data (20%) for evaluation
              > Uses StandardScaler to normalize the feature values for better model performance.

7. Train the Model:
   
              > Fits a Logistic Regression model on the scaled training data.

9. Predict and Evaluate:
   
              > Predicts the class (0 or 1) on the test set.
               Prints:
                    > Confusion Matrix: shows counts of TP, TN, FP, FN.
                    > Classification Report: includes accuracy, precision, recall, and F1-score.

11. ROC Curve and AUC:
    
               > Calculates the predicted probabilities for the positive class.
               > Plots the ROC Curve, which shows the trade-off between true positive and false positive rates.
               > Calculates AUC (Area Under Curve) — higher AUC means better model performance.

13.  Threshold Tuning:
    
               > Sets a custom classification threshold (0.4 instead of default 0.5).
               > Predicts new labels using the threshold.
               > Prints a new classification report to observe how changing the threshold affects performance (e.g., higher recall, possibly lower precision).
