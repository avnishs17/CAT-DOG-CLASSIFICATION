# CAT-DOG-CLASSIFICATION
## CAT DOG CLASSIFICATION USING CNN 
This project trains a convolutional neural network (CNN) model to classify images of cats and dogs.

## Data
The dataset contains 23,000 images of cats and dogs (12,500 cat images and 10,500 dog images) from the Kaggle Dogs vs Cats dataset.

The images are 60x60 grayscale and normalized between 0-1.

## Model
The model is a basic CNN with the following architecture:
- 3x Convolutional layers with 64 filters and ReLU activation
- MaxPooling layers for downsampling
- Fully connected dense layer
- Output layer with softmax activation
. The model is trained for 8 epochs with adam optimizer and sparse categorical crossentropy loss.

## Usage
The model is serialized as a  file catdog.model. It can be loaded and used to make predictions on new images.

## Notebooks
The data processing, model training and usage examples are in the following notebooks:

1. CatsVsDogs.ipynb: Dataset loading and preprocessing
2. Training model.ipynb: Model definition, training and serialization
3. using model to predict.ipynb: Loading saved model and making predictions
