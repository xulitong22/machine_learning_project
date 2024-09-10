## My end to end machine learning project

### Overview
This project is designed to predict a student's math score based on their information using a machine learning model. The project follows a structured approach with data ingestion, transformation, model training, and prediction pipeline. The final prediction is served via a Flask application that accepts student information as input and returns the predicted math score.

### Installation
You can install the project and its dependencies by running: pip install .

### Requirements
The project requires the following Python libraries:
numpy, 
pandas, 
seaborn, 
matplotlib, 
scikit-learn, 
dill, 
Flask

### Usage
Once installed, you can start the Flask web application by running: python app.py

### Steps
1. Data Ingestion
The data_ingestion.py module loads the raw dataset, performs basic data cleaning, and saves the cleaned data as cleaned_data.csv in the data folder. It utilizes logging from the logger.py file to track progress.

2. Data Transformation
The data_transformation.py module is responsible for feature engineering and preparing the data for model training. It scales and encodes the features and splits the data into training and testing sets. This module also logs each transformation step for traceability.

3. Model Training
In model_trainer.py, multiple machine learning models are trained and evaluated. The best-performing model is selected based on accuracy and other metrics, then saved as best_model.pkl in the model folder. Logs are recorded during the training process to track the performance of different models.

4. Prediction Pipeline
The predict_pipeline.py module is responsible for loading the saved best_model.pkl and predicting new inputs. This module is integrated into the Flask application for serving real-time predictions.

5. Flask App
The Flask app (app.py) provides a web interface where users can input student information to get a predicted math score. It uses the prediction pipeline to make predictions and displays the results in the web browser.
