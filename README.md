

# Driver Drowsiness Detection System

## Introduction
This project implements a driver drowsiness detection system using computer vision techniques and deep learning. The system analyzes facial features, particularly the eyes, in real-time through a webcam feed to detect signs of drowsiness in drivers. When drowsiness is detected, the system alerts the driver to prevent potential accidents.

## Training the Model
### Dataset Preparation
- The model was trained using a dataset containing images of drivers with various eye states, including open and closed eyes.
- Data augmentation techniques such as image rotation, flipping, and zooming were employed to increase dataset diversity.

## The Dataset

The dataset used is a subset of a dataset from [Kaggle](https://www.kaggle.com/datasets/dheerajperumandla/drowsiness-dataset). It includes the following folders:
1. `Closed_eyes` - containing 726 pictures
2. `Open_eyes` - containing 726 pictures
3. `Yawn` - containing 725 pictures
4. `no_yawn` - containing 723 pictures
.
### Model Training
- The dataset was split into training and validation sets.
- Hyperparameters such as learning rate, batch size, and number of epochs were fine-tuned for optimal performance.
- The model's performance was evaluated using metrics such as accuracy, precision, recall, and F1-score.

## Building the Model
### Model Architecture
- The model architecture utilized convolutional neural network (CNN) layers followed by fully connected layers.
- ReLU activation function was used in the convolutional layers, while Softmax activation was used in the output layer for multi-class classification.

### Regularization
- Dropout regularization was employed to prevent overfitting.

### Loss Function
- Categorical Crossentropy loss function was used for multi-class classification.

## Libraries Used
- **OpenCV**: Used for image processing and webcam access.
- **TensorFlow/Keras**: Utilized for building, training, and evaluating the deep learning model.
- **NumPy**: Employed for numerical computations and data manipulation.
- **Playsound**: Utilized for playing audio alerts when drowsiness is detected.

## Model API
- TensorFlow/Keras API was used for building and training the model.

## Seed Used
- A seed value (42) was used for reproducibility and ensuring consistent randomization.

 ## User Interaction for Termination
 - Users can terminate the application by pressing the "q" key or the ESC button, exiting the while loop and releasing the webcam feed.

