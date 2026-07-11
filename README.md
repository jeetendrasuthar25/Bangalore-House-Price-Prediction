# Bangalore House Price Prediction

An end-to-end data science project that predicts real estate prices in Bangalore based on location, square footage, number of bedrooms (BHK), and bathrooms. First step would be build a model using sklearn and linear regression using bangalore home prices dataset from kaggle.com. Second step would be to write a python flask server that uses the saved model to serve http requests.Third component is the website build in html, css and javascript that allows user to enter home square ft area, bedrooms etc and it will call python flask server to retrieve the predicted price. During model building, I cover all data science concepts such as data loading and cleaning, outlier detection and removal, feature engineering, dimensionality reduction, gridsearchcv for hyperparameter tunning, k fold cross validation etc.

## Overview

This project walks through building a real estate price prediction web app in three stages:

1. *Model Building* — Cleaning the Bangalore home prices dataset (Kaggle) and training a regression model using scikit-learn.
2. *Backend Server* — A Python Flask server that loads the trained model and serves predictions via HTTP.
3. *Frontend Client* — An HTML/CSS/JavaScript UI where users enter square footage, BHK, bathrooms, and location to get an estimated price.

## Tech Stack

- *Language:* Python
- *Data Processing:* NumPy, Pandas
- *Visualization:* Matplotlib
- *Modeling:* Scikit-learn (Linear Regression)
- *Backend:* Flask
- *Frontend:* HTML, CSS, JavaScript
- *IDE/Tools:* Jupyter Notebook, VS Code, PyCharm

## Project Structure

Bangalore-House-Price-Prediction/
├── model/       # Jupyter notebook: data cleaning, feature engineering, model training
├── server/      # Flask server that serves the trained model
├── client/      # Frontend (HTML/CSS/JS) to interact with the server
├── .idea/
├── .vscode/
└── README.md

## Key Data Science Steps

- Data loading and cleaning
- Outlier detection and removal
- Feature engineering (e.g., converting total_sqft ranges to numeric, price per sqft)
- Dimensionality reduction (grouping rare locations into an "other" category)
- Hyperparameter tuning using GridSearchCV
- Model evaluation using K-Fold cross-validation

## Getting Started

### Prerequisites
- Python 3.11.0
- pip

### Installation
git clone https://github.com/jeetendrasuthar25/Bangalore-House-Price-Prediction.git
cd Bangalore-House-Price-Prediction

### Run the Model Notebook
cd model
jupyter notebook

### Run the Server
cd server
pip install -r requirements.txt
python server.py

### Run the Client
Open client/index.html in your browser (or serve it via a local server), and ensure the Flask server is running so it can respond to prediction requests.

## How It Works

1. User enters square footage, BHK, number of bathrooms, and location on the web UI.
2. The client sends this data to the Flask server via an HTTP request.
3. The server loads the pre-trained regression model and returns a predicted price.
4. The predicted price is displayed on the UI.

## Future Improvements

- Deploy the app on a cloud platform (Heroku, AWS, Render)
- Add more features (amenities, property age, floor number)
- Experiment with advanced models (Random Forest, XGBoost) and compare performance
- Add unit tests for the Flask API
