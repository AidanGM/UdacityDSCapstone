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

- `extract_bottleneck_features.py`: Script to extract bottleneck features for transfer learning

- `dog_app.ipynb`: Notebook 

NOTE: The bottleneck features files were too large to add here
  
## Key Findings <a name="Findings"></a>

The findings are highlighted in this [blog](https://medium.com/@aidangmassaromlp/what-dog-are-you-using-convolutional-neural-networks-and-transfer-learning-to-predict-dog-breeds-83785e15903a) and in the `dog_app.ipynb` notebook. Just to summarize here are some results:

- The best model which used Transfer LEarning with ResNet50 Bottleneck features had 78% predictive accuracy
- The relatively small CNN built from scratch only had just over 1% predicitve accuracy
- Predicted probability distributions for hummans typically had a significantly higher entropy score than those for dogs
- This could potentially be extended to predict which dog breeds mixed-breed dogs are made up of
