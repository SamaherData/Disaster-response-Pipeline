# Disaster-response-Pipeline

*Project Overview:*

In this project, we will use data set provided by Figure Eight containing real messages which was sent during disasters events  . There are 36 pre-defined categories.  The project aim is to build  basic ETL , Machine Learning pipeline  and web application that extracts data from the sqlite database to create data visualizations and use the model to classify new messages in various categories on a real time basis. 

*File Descriptions:*

- Project workspace App folder including the templates folder and "run.py" for the web application that enables the user to enter a disaster message, and then view the categories of the message.
- Project workspace Data folder containing "DisasterResponse.db", "disaster_categories.csv", "disaster_messages.csv" and "process_data.py" for data preparation.
- Project workspace Models folder including "classifier.pkl" and "train_classifier.py" for the Machine Learning model.

*File Details:*

*ETL Pipeline*: process_data.py file contain the script to create ETL pipline which:

- Loads  and merge the messages and categories datasets
- Merges the two datasets
- Cleans the data and stores it in a SQLite database

*ML Pipeline*: train_classifier.py file contain the script to create ML pipline which:

- Loads data from the SQLite database and split it  into training and test sets.
- Builds a text processing , machine learning pipeline Trains and tunes a model using GridSearchCV.
- Outputs results on the test set and exports the final model as a pickle file for later use.

*Instructions:*

To execute the app follow the instructions:

1- Run the following commands in the project's root directory to set up your database and model.

*      To run ETL pipeline that cleans data and stores in database 

*      python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db

*      To run ML pipeline that trains classifier and saves 

*      python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl

2- Run the following command in the app's directory to run your web app. python run.py

*      Go to http://0.0.0.0:3001/
