# Udacity Data Science Capstone Project
## Dog Breed Classifier

This project uses CNNs and Transfer Learning to predict dog breeds in images.

### Contents

[Packages](#Packages)

[Project Description](#Description)

[Files](#Files)

[Key Findings](#Findings)


## Packages <a name="Packages"></a>

The following libraries were used in this project

- numpy
- sklearn
- keras
- glob
- random
- cv2
- matplotlib
- tqdm
- PIL
- IPython

## Project Description <a name="Description"></a>

This project is part of the Udacity Data Science Nanodegree. The goal is to use CNNs and transfer learning to

1. Detect either a dog or human with an image input
2. Classify the closest resembling dog breed

## Files <a name="Files"></a>

- `README.md`: Read me file (being read by you now)

- `Images/`: Image files used for analysis after training

- `saved_models/weights.best.from_scratch.hdf5`: Best weights from CNN from scratch
- `saved_models/weights.best.Resnet50.hdf5`: Best weights using Resnet50 bottleneck features 
- `saved_models/weights.best.VGG16.hdf5`: Best weights using VGG16 bottleneck features 

- `extract_bottleneck_features.py`: script to extract bottleneck features for transfer learning

- `dog_app.ipynb`: Notebook

NOTE: The bottleneck features files were too large to add here
  
## Key Findings <a name="Key Findings"></a>


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

