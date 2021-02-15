# Neural_Network_Charity_Analysis
Analysis on whether applicants will be successful when funded by Alphabet Soup

## Overview of the Analysis
Alphabet Soup is a non-profit, philanthropic foundation that helps different organizations help the environment, improve people's well-being and unify the world.  Not all donations have been effective or impactul.  Therefore Alphabet Soup's data science team aims to create a model that predicts which organizations are worth donating to, and which are not.

## Results
- Data Processing
    - The target variable is the column "IS_SUCCESSFUL".
    - The feature varaibles are the columns "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATION", and "ASK_AMT".
    - Columns that are neither target or feature, and therefore have been removed as 1st step of preprocessing, are:  "EIN" and "NAME".

- Compiling, Training, and Evaluating the Model
    - Two hidden layers were used, with 80 neurons in the first, and 30 neurons for the second.  80 neurons were used in the first hidden layer since it is ideal to have two to three times the amount of neurons in the hidden layer as the number of inputs \(in this case, about 40 input variables\).  The second layer helps boost the first layer's perfomance.  The "relu" activation function was used, which is the most commonly used activation function.  It is ideal for looking at positive nonlinear input data for classification or regression.\
    ![alt text](?raw=True)
    - The target model performance is 75%.  The first pass of the model achieved a 72% accuracy.\
    ![alt text](?raw=True)
    - The following are the step I took to try and increase model performance:
        - Drop "SPECIAL_CONSIDERATIONS" column\
        ![alt text](?raw=True)
        - Add a a third hidden layer with 10 neurons\
        ![alt text](?raw=True)
        - Add 100 more epochs to the training regimen, now with a total of 200 epochs.\
        ![alt text](?raw=True) 

## Summary
Overall, the deep learning neural netork only achieves a maximum of 73% accuracy on predicting whether or not the donations of Alphabet Soup to a specific organization is impactful.

Using a different model may achieve a more desirable model performance.  I would recommend to try using an ensemble learning model.  Ensemble learning models combines multiple algortihms to improve the accuracy and decrease variance of the model, and ultimately increase its overall performance.  Using boosting algorithms with an ensemble learning method may help increase perfomance as well.