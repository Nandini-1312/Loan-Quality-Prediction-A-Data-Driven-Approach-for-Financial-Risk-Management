# Loan Repayment Prediction Analysis

This project addresses the critical challenge of predicting loan repayment success or default risk in the financial sector using advanced data science techniques.

**Objective:**
To predict whether a loan will be repaid successfully or is at risk of default using a supervised machine learning approach. This project tackled challenges such as class imbalance, dimensionality reduction, and model performance evaluation.

**Real-World Applications in Finance**
  •	Classifies loans as either successful or at default risk to minimize defaults and improve resource allocation..
  

**Implementation**	
  1. Data Preprocessing

     •	Label Encoding: Converted categorical labels (e.g., "default risk" and "successful") into numeric binary values for compatibility with the model.
     
     •	Variable Transformation: Encoded categorical features into numerical values to maintain interpretability and enable machine learning.
     
     •	Scaling: Standardized the dataset to ensure consistent feature magnitudes for PCA and logistic regression.
     
  
  2. Feature Engineering

     •  Dimensionality Reduction: Applied Principal Component Analysis (PCA) to reduce the number of predictors while retaining 87% of the variance. This step ensured computational efficiency and     reduced overfitting risks.

  
  3. Handling Class Imbalance
     

     •	Initial Model (Imbalanced Dataset):
     
          o	Trained a logistic regression model, which exhibited poor performance on the minority class (default risk) due to severe class imbalance.
       
          o	Accuracy: 99.44%, but with significant misclassifications of default risk loans.

     •	Synthetic Minority Oversampling Technique (SMOTE):

          o	Applied SMOTE to balance the dataset by creating synthetic samples of the minority class.
       
          o	Reapplied PCA to maintain reduced dimensionality and prevent overfitting.
     
  4. Modeling and Evaluation

     •	Logistic Regression:

         o	Post-SMOTE logistic regression achieved 72.64% accuracy, providing more balanced predictions for both successful repayment and default risk loans.
     
     •	Evaluation Metrics:

         o	Accuracy alone was insufficient for imbalanced data. Hence ROC curve was used to measure performance:

      
      ![image](https://github.com/user-attachments/assets/37074b7e-42de-43de-8fee-c88d7d072c29)


         The sharp rise in the ROC curve suggests that the model is effectively capturing true positives (i.e., identifying successful loans). The curve remains relatively low along the x-axis, indicating minimal false positives (misclassifying default risk loans as successful loans), which is critical for effective risk assessment.

     
  6. Insights and Adjustments

     •	The ROC curve indicates that the model is well-calibrated and effective in distinguishing between successful loans and those at default risk, making it a reliable tool for loan repayment prediction.
     
     •	The balanced model improved the classification of default risk loans, highlighting the importance of addressing class imbalance in supervised learning.
     
     •	SMOTE effectively increased minority class representation but introduced a trade-off in overall accuracy.
     
     •	PCA was critical in managing computational complexity and avoiding overfitting, especially in high-dimensional data.
     
        
**Power BI Visualizations**

    
  
  ![image](https://github.com/user-attachments/assets/73a48e01-d893-47b0-a8f1-122c54d4f7b3)
  

  ![image](https://github.com/user-attachments/assets/4c8f36bc-1570-4a8d-bb6b-8aebb9f79d78)


**Prerequisites**

  • R programming language, Power BI

  • Required R packages: readxl, dplyr, ggplot2, corrplot, DMwR2, smotefamily, ROCR

