# Drowsiness Detection System

## Overview
This project demonstrates a **real-time drowsiness detection system** using **Python**, **OpenCV**, and a **Convolutional Neural Network (CNN)**. The system monitors a driver’s eyes using a webcam feed and triggers an alarm if drowsiness is detected, reducing the risk of accidents caused by fatigue.

---

## Features
- Real-time video feed analysis using OpenCV.
- Face and eye detection with Haar cascade classifiers.
- CNN model for classifying open and closed eyes with high accuracy.
- Alarm system triggered after detecting closed eyes for a sustained period.
- FPS calculation and live display for smooth visualization.

---

## Technologies Used
### Languages and Libraries:
- **Python**
- **OpenCV**: For image processing and face/eye detection.
- **TensorFlow/Keras**: For building and training the CNN model.
- **NumPy**: For numerical computations.
- **Matplotlib**: For plotting training/validation metrics.

### Tools:
- Haar Cascade Classifiers: Pre-trained models for face and eye detection.
- ImageDataGenerator: Data augmentation for training.
- Threading: For handling the alarm playback.

---

## Project Structure
```
project-folder
├── data
    ├── no_yawn
    ├── yawn
    ├── closed
    ├── open
│   ├── alarm.mp3                # Alarm sound file
│   ├── haarcascade_frontalface_default.xml
│   ├── haarcascade_lefteye_2splits.xml
│   └── haarcascade_righteye_2splits.xml
├── drowsiness_detection.py      # Main Python script
├── drowiness_new2.h5            # Pre-trained CNN model
└── README.md                    # Project documentation
```

---

## Dataset
The model was trained on a custom dataset containing images of **open eyes** and **closed eyes**. The dataset was preprocessed to:
1. Resize images to 145x145 pixels.
2. Normalize pixel values to the range [0, 1].

---

## Model Architecture
The CNN model was built using the Keras **Sequential API** with the following layers:
1. **Convolutional Layers**: Extract features from input images.
2. **Batch Normalization**: Normalize activations to stabilize training.
3. **Max Pooling Layers**: Reduce spatial dimensions.
4. **Dropout Layers**: Prevent overfitting by randomly dropping neurons.
5. **Fully Connected Layers**: Classify images into two categories (open/closed eyes).
6. **Softmax Activation**: Output probabilities for each class.

**Optimizer:** Adam  
**Loss Function:** Categorical Crossentropy  
**Metrics:** Accuracy

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.comkamalkolisetty/kamal-DriverDrowsiness-Detection
   ```
2. Navigate to the project directory:
   ```bash
   cd drowsiness-detection
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage
1. **Run the script:**
   ```bash
   python drowsiness_detection.py
   ```
2. **Webcam feed:** The system will capture frames from your webcam and display the processed feed with FPS, eye status, and drowsiness alerts.
3. **Quit:** Press `q` or `ESC` to exit the program.

---

## Code Walkthrough
### Import Libraries
The script begins by importing essential libraries for deep learning, image processing, and threading.

### Loading Haar Cascades
Haar cascade XML files are loaded to detect faces and eyes in the video feed.

### Real-Time Video Capture
Using OpenCV’s `VideoCapture`, frames are captured from the webcam and processed in grayscale.

### Eye Classification
Eye regions are extracted and resized to the model’s input dimensions (145x145). These are passed to the trained CNN model to classify them as **open** or **closed**.

### Alarm Mechanism
If closed eyes are detected for a sustained period (3 consecutive frames), an alarm is triggered using a separate thread to ensure smooth execution.

---

## Results
1. **Training Metrics:**
   - Accuracy: Achieved high accuracy on both training and validation datasets.
   - Loss: Smooth convergence during training.

2. **Performance:**
   - Real-time detection with minimal latency.
   - Effective alarm system for drowsiness alerts.

---

## Demo
1. The system processes real-time video feed and highlights detected face and eyes.
2. The model identifies eye status as "Open" or "Closed."
3. FPS and drowsiness status are displayed on the video feed.
4. Alarm sound plays when drowsiness is detected.

---

## Future Enhancements
- Add support for multiple faces.
- Extend detection to include yawning as a sign of fatigue.
- Deploy the system on embedded devices like Raspberry Pi.

---

## Contributing
Contributions are welcome! Feel free to fork this repository, create a feature branch, and submit a pull request.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## Acknowledgments
- OpenCV documentation
- TensorFlow/Keras tutorials
- Dataset contributors

---

## Contact
For questions or feedback, feel free to reach out:
- **Email:** kamalkumarkolisetty@gmail.com
