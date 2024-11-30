# Loan-Quality-Prediction-A-Data-Driven-Approach-for-Financial-Risk-Management
This project addresses the critical challenge of predicting loan quality in the financial sector using advanced data science techniques.


**Objective:**
To predict the quality of loans (Good or Bad) using a supervised machine learning approach. This project tackled various challenges, including class imbalance, dimensionality reduction, and evaluation of model performance.

**Real-World Applications in Finance**
  •	Loan Quality Prediction: Classifies loans as Good or Bad to minimize defaults and improve resource allocation.
  
  •	Credit Card Fraud Detection: Identifies fraudulent transactions by detecting anomalies in transaction patterns.
  
  •	Insurance Risk Assessment: Predicts claim risks and customer defaults, aiding in underwriting and policy pricing.
  
  •	Portfolio Risk Management: Flags risky assets in investment portfolios based on historical performance and trends.
  
  •	Regulatory Compliance: Ensures adherence to financial regulations like Basel III through robust risk assessment models.
  

**Implementation**	
  1. Data Preprocessing

     •	Label Encoding: Converted categorical labels (values like G, B) into numeric binary values for compatibility with the model.
     
     •	Variable Transformation: Encoded categorical features into numerical values to maintain interpretability and enable machine learning.
     
     •	Scaling: Standardized the dataset to ensure consistent feature magnitudes for PCA and logistic regression.
     
  
  2. Feature Engineering

     •  Dimensionality Reduction: Applied Principal Component Analysis (PCA) to reduce the number of predictors while retaining 87% of the variance. This step ensured computational efficiency and     reduced overfitting risks.

  
  3. Handling Class Imbalance
     

     •	Initial Model (Imbalanced Dataset):
     
          o	Trained a logistic regression model, which exhibited poor performance on the minority class due to severe class imbalance.
       
          o	Accuracy: 99.44%, but with significant misclassifications of Bad Loans.

     •	Synthetic Minority Oversampling Technique (SMOTE):

          o	Applied SMOTE to balance the dataset by creating synthetic samples of the minority class.
       
          o	Reapplied PCA to maintain reduced dimensionality and prevent overfitting.
     
  4. Modeling and Evaluation

     •	Logistic Regression:

         o	Post-SMOTE logistic regression achieved an accuracy of 72.64%. While lower than the imbalanced model's accuracy, it provided more balanced predictions for both classes.
    
     •	Evaluation Metrics:

         o	Accuracy alone was insufficient for imbalanced data. Hence ROC curve was used to measure performance:


      ![image](https://github.com/user-attachments/assets/37074b7e-42de-43de-8fee-c88d7d072c29)


         The sharp rise in the curve suggests that the model is effectively capturing true positives early on (i.e., it's good at identifying "Good Loans"). The curve remains relatively low along the x-axis, showing that false positives (misclassifying "Bad Loans" as "Good Loans") are minimal, which is important for risk assessment.

     
  6. Insights and Adjustments

     •	The ROC curve indicates that the model is well-calibrated, the model appears effective in distinguishing between "Good" and "Bad" loans, making it a reliable tool for loan quality prediction.
     
     •	The balanced model improved the ability to classify Bad Loans, highlighting the importance of addressing class imbalance in supervised learning.
     
     •	SMOTE effectively increased minority class representation but introduced a trade-off in overall accuracy.
     
     •	PCA was critical in managing computational complexity and avoiding overfitting, especially in the presence of high-dimensional data.
      
      
**Prerequisites**

  • R programming language

  • Required R packages: readxl, dplyr, ggplot2, corrplot, DMwR2, smotefamily, ROCR

