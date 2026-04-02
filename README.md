# Airbnb Price Prediction using MLflow & AWS S3

## Project Overview

This project aims to build a machine learning pipeline to predict Airbnb
listing prices based on various features such as location, availability,
and property attributes.

The workflow integrates: - AWS S3 → dataset storage\
- MLflow → experiment tracking\
- Scikit-learn → model training

------------------------------------------------------------------------

## Objectives

-   Retrieve dataset from AWS S3\
-   Perform preprocessing\
-   Train multiple models\
-   Track experiments using MLflow\
-   Register best model

------------------------------------------------------------------------

## Setup Instructions

### Clone Repository

    git clone <your-repo-link>
    cd <repo-name>

### Create Virtual Environment

    python -m venv venv

### Activate Environment (Windows)

    venv\Scripts\activate

### Install Dependencies

    pip install -r requirements.txt

------------------------------------------------------------------------

## AWS S3

### Create Bucket

    aws s3 mb s3://your-bucket-name

    ![Make new bucket](../images/make_new_bucket.png)

### Upload Dataset

    aws s3 cp AB_NYC_2019.csv s3://your-bucket-name/

------------------------------------------------------------------------

## MLflow

### Start UI

    mlflow ui

### Run Project

    python download_data.ipynb

------------------------------------------------------------------------

## Models

-   Linear Regression\
-   Random Forest (Best)\
-   Gradient Boosting

------------------------------------------------------------------------

## Results

  Model               RMSE    R2 Score
  ------------------- ------- ----------
  Linear Regression   0.427   0.58
  Random Forest       0.395   0.64
  Gradient Boosting   0.406   0.61

------------------------------------------------------------------------

## Best Model

Random Forest performed best with highest R² and lowest RMSE.

------------------------------------------------------------------------

## Structure

    .
    ├── images/
    ├── download_data.ipynb/
    ├── mlruns/
    ├── requirements.txt
    └── README.md

------------------------------------------------------------------------

## Workflow

1.  Upload data to S3\
2.  Load data\
3.  Preprocess\
4.  Train models\
5.  Track in MLflow\
6.  Compare & register

------------------------------------------------------------------------

## Insights

-   Tree models outperform linear models\
-   Random Forest handles non-linearity well\
-   MLflow simplifies tracking

------------------------------------------------------------------------

## Future Work

-   Hyperparameter tuning\
-   Deployment API\
-   Feature engineering improvements
