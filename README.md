# AWS_SageMaker_Fraud_Detection
Using AWS SageMaker to optimize training of an XGBoost model that detects fraudulent credit card transactions in an extremely imbalanced dataset.  

## Motivation
This project was completed for a Cloud Computing class at the George Washington University.  For this project, we were tasked with using multiple AWS services to work with a large dataset and analyze it.  My group chose to work on a credit card fraud detection dataset from Kaggle.  

## Personal Contribution
I was tasked with using AWS SageMaker to classify the fraudulent transactions with a model of my choosing by optimizing precision and recall.  I also performed the EDA and did extensive research on SageMaker on behalf of my group.  

## Other Team Members Contributions
Aside from the SageMaker work, our team also used IAM, VPC, and S3 services.  Another team member also put together a web app with R Shiny to present our results to the class. 

## Data Source
https://www.kaggle.com/mlg-ulb/creditcardfraud.  The data was stored in a S3 bucket and accessed from that bucket in SageMaker. 

## Using the Notebooks
- XGBoost_EDA.ipynb shows how I read the data from the S3 bucket and perform some EDA using plotly.
- XGBoost_HyperparameterTuning.ipynb shows the training and hyperparameter tuning setup used for our XGBoost model.  The code also shows how to monitor training jobs in the notebook once they are started.
- XGBoost_GetPredictions.ipynb shows how to get predictions from a trained XGBoost model with the optimal hyperparameters.  I also created precision and recall curves with plotly here.  The model achieved precision and recall scores of 85.2%.

## Other Files
- Sagemaker_PPT_V2.pptx was used for our presentation of the project and shows how the SageMaker notebook kicks off jobs that can be inspected in the AWS console.
- Figures folder contains all of the interactive plotly visuals I created for the project as HTML files.