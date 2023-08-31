# Module-20---Supervised-Learning --- Credit Risk Classification 

For this challenge, various techniques will be used to train and evaluate a model based on loan risk. The dataset used in this challenge is from historical lending activity from a peer to peer lending services company and will be used to build a model taht can help identify the creditworthiness of borrowers. 

There will be 3 parts to this challenges: 

1) Split the data into training and testing sets
2) Create a Logistic Regression Model with the Original Data.
3) Write a Credit Risk Analysis Report


Part 1. Split the Data into Training and Testing Sets. 
  1. Read the lending_data.csv data into a Pandas DataFrame.
    

![image](https://github.com/AnnLy2023/Module-20---Supervised-Learning/assets/129100456/7ca9a545-cdf6-40ee-9b0c-8512ebe652a7)

  2. Create the labels set (y) from the loan_status column, then create the features X Dataframe from the remaining columns.
     
![image](https://github.com/AnnLy2023/Module-20---Supervised-Learning/assets/129100456/6fa32ba6-2305-40ce-9124-ac84750f4bdc)
  3. Split the data into training adn testing datasets by using train_test_split.
  ![image](https://github.com/AnnLy2023/Module-20---Supervised-Learning/assets/129100456/c069e35b-d225-4cd1-a737-00836d4be968)


Part 2. Create a Logistic Regression Model with the Original Data. 
  1. Fit a logistic regression model by using the training data X_train and y_train.
  ![image](https://github.com/AnnLy2023/Module-20---Supervised-Learning/assets/129100456/ed9242d5-d03d-4e11-928d-12c5f467ba7e)
  2. Save teh predictions for teh testing data labels by using the testing feature data (X_test) and the fitted model.
  ![image](https://github.com/AnnLy2023/Module-20---Supervised-Learning/assets/129100456/75a70705-8e15-48f9-ae8b-cfe342fc9187)
  3. Evaluate teh model's performance by generate a confusion matrix and print the classification report.
     ![image](https://github.com/AnnLy2023/Module-20---Supervised-Learning/assets/129100456/5a716fd9-3414-4d14-8952-641beed50b4f)
     ![image](https://github.com/AnnLy2023/Module-20---Supervised-Learning/assets/129100456/41d8b314-7477-4886-ac8f-9e1dc115f99d)
  4. How well does the logistic regression model predict both the O(healthy loan) and 1(high risk loan) labels?

     The precision for the Logistic regression model for the testing data was great at detecting healthy loans (1) and a little less accurate at detecting high risk loan (.85) In terms of the recall, the testing model is great at detecting healthy loan (.99) and a little less accurate at detecting high risk loan (.91). For F1 score, the testing model is great at detecting healthy loan (1) but not so good at detecting high risk one (.88).

Part 3. Credit Risk Analysis Report

  The purpose of this analysis is to predicting the creditworthiness of the borrowers based on a dataset collected from historical lending activity from a peer to peer lending services company. A model will be build with the intention to identify if the loan status is a healthy one (0) or a high risk one (1). 
  - Precision: The precision for both the original and testing models are pretty high at predicting outcome for healthy loan, with both score at 1. However, for high risk loan, the original data scored .86, a little higher than the testing model which is at .85. The accuracy for testing and original models is only accurate for predicting healthy loan, less accurate in predicting outcome for high risk one.
  - Recall: In term of recall, both original and testing models scored pretty high on accuracy in predicting the outcome for "healthy loan" with a score of 1 vs. .99. However, on the predictions of high risk loan, original data scored only .9 vs testing model's recall of .91. Again, this models are good at predicting healthy loan but not high risk loan status.
  - F1 score: Both the model (training and testing) are good at detecting healthy loans, both has 1 as the score. However, both of the models are not doing so good at detecting high risk loan status, both came in with a score of .88.

    The correlations columns that helps determines whether a loan is healthy or highrisk depends highly on the interest rate, borrower's income, total debt, loan size, and the number of accounts. The columns that have little or no affect in determining the outcome of the loan whether it is a healthy or high risk are debt to income and derogatory marks. 
    I would recommend to use other more complicated models to use the testing data on, it would provide a more higher accuracy in predicting the outcome for both healthy and especially at predicting high risk loans such as XGB, GB, ADA and KNN, all have high accuracy in predicting outcome for healthy loans, and scored precision .84, recall .99 and F1 at .91. These numbers are higher than the LR model. I would not recommend using DT, or RF models. Both are good with predicting healthy loans outcome, but not with high risk. All the precisions/recalls and F1 scores for DT and RF models in predicting outcome for high risk loan are lower than LR.




     

 
   


