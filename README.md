# Student Loan Risk with Deep Learning

This project develops a machine learning model to predict the likelihood of student loan repayment.


* Data Source: https://static.bc-edx.com/ai/ail-v-1-0/m18/lms/datasets/student-loans.csv


## Steps:

### 1. Prepare the data to be used on a neural network model
1. Using the preprocessed data, create the features (`X`) and target (`y`) datasets. The target dataset should be defined by the preprocessed DataFrame column “credit_ranking”. The remaining columns should define the features dataset.
2. Split the features and target sets into training and testing datasets.
3. Use scikit-learn's `StandardScaler` to scale the features data.
### 2. Compile and Evaluate a Model Using a Neural Network
1. Create a deep neural network by assigning the number of input features, the number of layers, and the number of neurons on each layer using Tensorflow’s Keras.
2. Compile and fit the model using the `binary_crossentropy` loss function, the `adam` optimizer, and the `accuracy` evaluation metric.
3. Evaluate the model using the test data to determine the model’s loss and accuracy.
4. Save and export the model to a keras file, and name the file `student_loans.keras`.
### 3. Predict Loan Repayment Success by Using the Neural Network Model
1. Reload the saved model.
2. Make predictions on the testing data and save the predictions to a DataFrame.
3. Display a classification report with the y test data and predictions
### Answered the Following Questions:
1. Describe the data that you would need to collect to build a recommendation system to recommend student loan options for students. Explain why this data would be relevant and appropriate.
2. Based on the data you chose to use in this recommendation system, would your model be using collaborative filtering, content-based filtering, or context-based filtering? Justify why the data you selected would be suitable for your choice of filtering method.
3. Describe two real-world challenges that you would take into consideration while building a recommendation system for student loans. Explain why these challenges would be of concern for a student loan recommendation system.
#
**1. To build a student loan recommendation system, you would need to collect two main categories of data: Student Data and Loan Option Data.**
  **Academic and financial information (student data) determines the amount needed and the student's financial standing. Loan option data provides the details of available loans.**
#
**2. The data described above would be most suitable for a content-based filtering method.** 
  **This Method would be suitable becuase the core of the recommendation would be driven by matching the content of the student's needs and eligibility with the content of the loan offerings.**
#
**3. Data Scarcity/Cold Start and Ethical Considerations/Bias are two real world chellenges to take into account.**
  **Data Scarcity/Cold Start: Obtaining comprehensive and accurate financial data from students can be challenging due to privacy concerns and reluctance to share sensitive information, could also be limited data on new students or new loan options leading to the system struggling to make relevant suggestions.**

  **Ethical Considerations/Bias: Student loan recommendations can have significant financial implications for individuals' futures. The system could inadvertently perpetuate existing biases present in the data or make recommendations that prioritize certain lenders or loan types over others without clear justification.**


* Imports:
    - import pandas as pd
    - import tensorflow as tf
    - from tensorflow.keras.layers import Dense
    - from tensorflow.keras.models import Sequential
    - from sklearn.model_selection import train_test_split
    - from sklearn.preprocessing import StandardScaler
    - from sklearn.metrics import classification_report
    - from pathlib import Path