# Disaster Response Pipeline Project


### Motivation:
The purpose of the project is to build a model for an API that classifies disaster messages. Using the web app an emergency worker ould use during a disaster event (e.g. an earthquake or hurricane) and can input a new message and get classification results in several categories so to have an idea what kind of help is needed ("water", "shelter", "food", etc.) or to send to the appropiate aid agency. 

The web app also displays visualizations of the data.

### File Description:

#### process_data.py: 
This code takes as its input csv files containing message data and message categories (labels), and creates an SQLite database containing a merged and cleaned version of this data.
#### train_classifier.py: 
This code takes the SQLite database produced by process_data.py as an input and uses the data contained within it to train and tune a ML model for categorizing messages. The output is a pickle file containing the fitted model. Test evaluation metrics are also printed as part of the training process.
 
You can find all of the files necessary to run and render the web app in the folder app

### Screenshots

![image](https://user-images.githubusercontent.com/46485715/106393125-93a2f600-63f5-11eb-900b-3575e443f255.png)


![image](https://user-images.githubusercontent.com/46485715/106393413-4031a780-63f7-11eb-9ae4-2509538982e6.png)




### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
