## CAT DOG CLASSIFICATION USING CNN 
This project trains a convolutional neural network (CNN) model to classify images of cats and dogs.

### Overview
The dataset contains 23,000 total images of cats and dogs from the Kaggle Dogs vs Cats competition.
A convolutional neural network model is built and trained on this dataset to classify cat vs dog images.
The trained model is serialized and can be loaded to make predictions on new images.

### Data
- The original dataset consists of 25,000 images of dogs and cats.
- Images are rescaled to 60x60 grayscale and pixel values normalized between 0-1.
- The training dataset contains 23,000 images split into 12,500 cat images and 10,500 dog images.
- 2000 validation images are held out from training for model evaluation.
  
### Model Architecture
1. Input layer 60x60x1 for grayscale images followed by:
2. 3 Convolutional layers with 64 3x3 filters and ReLU activation
3. 2x2 MaxPooling layers for downsampling after Conv layers
4. Fully connected hidden layer with 128 units
5. Output layer with softmax activation to classify 2 categories
   
### Training
- Model compiled with Adam optimizer, sparse categorical cross-entropy loss
- Trained for 8 epochs with a batch size of 32
- Best validation accuracy achieved: 83%

### Usage
- The trained model is serialized and saved as catdog.model file.
- It can be loaded and used to classify new cat/dog images:

## Notebooks
The data processing, model training and usage examples are in the following notebooks:

1. CatsVsDogs.ipynb: Dataset loading and preprocessing
2. Training model.ipynb: Model definition, training and serialization
3. using model to predict.ipynb: Loading saved model and making predictions
