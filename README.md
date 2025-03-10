# analog-and-NN-CNN-and-GNN
Amrutha V,Snigdhatanu Acharya


An AI-powered prosthetic hand with real-time feedback for improved grip control



# EMG Signal Classification using CNN

## Description
This project aims to classify EMG signals using a Convolutional Neural Network (CNN). The model is trained on synthetic EMG data representing three classes: 'rest', 'fist', and 'open'.

## Dataset Setup
The dataset is organized into directories for each class:
- `dataset/rest/`
- `dataset/fist/`
- `dataset/open/`

Each directory contains images of spectrograms generated from synthetic EMG signals.

## Model Overview
The CNN model consists of the following layers:
- Convolutional layers for feature extraction
- MaxPooling layers for down-sampling
- Dense layers for classification

## Training Instructions
To train the model, run the `CNN_model1.py` script. You can adjust the number of epochs and batch size as needed.

## Running the Model
After training, the model can be used to make predictions on new data. Load the trained model using TensorFlow/Keras and use the `predict` method.

## Results Visualization
The training results, including accuracy and loss plots, are generated during training. A confusion matrix is also created to evaluate model performance.

## Dependencies
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Seaborn
- SciPy
