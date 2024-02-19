# UdacityDSCapstone
# Udacity Data Science Project 2
## Disaster Response ML Pipeline

This project uses Figure Eight message data to train message classification system. This would be useful to filter our unimportant messages and direct messages to the right people. The trained model can be accessed through a provided web app, instructions will follow.

### Contents

[Packages](#Packages)

[Project Description](#Description)

[Files](#Files)

[Key Findings](#Findings)


## Packages <a name="Packages"></a>

The following libraries were used in this project

- sys
- pandas

## Project Description <a name="Description"></a>

This project is part of the Udacity Data Science Nanodegree. The goal is to use CNNs and transfer learning to

1. Detect either a dog or human with an image input
2. Classify the closest resembling dog breed

## Files <a name="Files"></a>

- `README.md`: Read me file (being read by you now)

- `data/process_data.py`: Python script to process data, containing ETL pipeline
- `data/DisasterResponse.db`: Disaster Response Database
- `data/disaster_categories.csv`: categories csv file
- `data/disaster_messages.csv`: messages csv file

- `models/train_classifier.py`: Python script to load data, create gridsearch to train model and store model
- `models/classifier.pkl` (EXCLUDED SINCE FILE IS TOO LARGE): Optimal model in wider parameter space 
- `models/classifier_balanced.pkl` (EXCLUDED SINCE FILE IS TOO LARGE): Optimal Random forest classifier with class frequency taken into account
- `models/classifier_balanced_low.pkl` (EXCLUDED SINCE FILE IS TOO LARGE): Alternative Random forest classifier with class frequency taken into account

- `app/templates/`: HTML Templates to be used for web app
- `app/run.py`: Python script to launch web app
  
## Instructions <a name="Instructions"></a>

To use the web app, download the `data`, `models` and `app` folders.

If you'd like to process the data, store this in a database and train a model run the following commands in the root directory:
1. `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
2. `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

You can then run the app by opening the apps directory and running the python script as follows:
1. `cd app`
2. `python run.py`

The current default uses the prebuilt classifier `models/classifier_balanced_low.pkl`, this can be modified to use your classifier, just replace with `models/YOURCLASSIFIERNAME`.
Once the web app has been loaded you can try out any prompt! If you're not sure what to use, try this as your starting point:
"This is an emergency, I need help. Water is building up in my livingroom, I think it's because of the rain."

