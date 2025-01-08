

# 🚗💤 Drowsiness Detection System

## 📖 Overview  
This project showcases a **real-time drowsiness detection system** built with **Python**, **OpenCV**, and a **Convolutional Neural Network (CNN)**. The system monitors a driver’s eyes via a webcam feed and triggers an alarm if drowsiness is detected, aiming to reduce accident risks caused by fatigue.

---

## ✨ Features  
- 🎥 Real-time video feed analysis using OpenCV.  
- 👀 Face and eye detection with Haar cascade classifiers.  
- 🤖 High-accuracy eye status classification using a CNN.  
- 🔊 Alarm triggered after sustained eye closure.  
- 📊 Live FPS calculation and visualization for a smooth user experience.  

---

## 🛠️ Technologies Used  

### 📚 Libraries and Tools  
- **Python**: The core programming language for the project.  
- **OpenCV**: A powerful library for image processing and computer vision, enabling face and eye detection.  
- **TensorFlow/Keras**: Frameworks for building and training the CNN model.  
- **NumPy**: For efficient numerical computations.  
- **Matplotlib**: To visualize training and validation metrics.  
- **Haar Cascade Classifiers**: Pre-trained XML models for detecting faces and eyes.  
- **Threading**: Ensures smooth alarm playback without interrupting the main application.  

---

## 🔍 What We Used  

### 🧠 **Convolutional Neural Networks (CNNs)**  
CNNs are specialized deep learning architectures designed to process and analyze visual data. By applying convolutional and pooling layers, CNNs effectively extract and learn hierarchical features, making them ideal for classifying images (e.g., open vs. closed eyes).  

### 📷 **OpenCV**  
OpenCV is an open-source library for real-time computer vision. It uses Haar cascades for efficient face and eye detection, enabling the system to isolate relevant regions for further analysis.  

---

## 📁 Project Structure  
```
project-folder
├── data
    ├── no_yawn
    ├── yawn
    ├── closed
    ├── open
│   ├── alarm.mp3                # Alarm sound file 🔊
│   ├── haarcascade_frontalface_default.xml
│   ├── haarcascade_lefteye_2splits.xml
│   └── haarcascade_righteye_2splits.xml
├── drowsiness_detection.py      # Main Python script 🐍
├── drowiness_new2.h5            # Pre-trained CNN model 🤖
└── README.md                    # Project documentation 📄
```

---

## 🗂️ Dataset  
The custom dataset contains images of **open eyes** and **closed eyes**. Preprocessing steps include:  
1. Resizing images to 145x145 pixels.  
2. Normalizing pixel values to [0, 1].  

---

## 🧑‍💻 Installation  

1. Clone the repository:  
   ```bash  
   git clone https://github.com/kamalkolisetty/kamal-DriverDrowsiness-Detection  
   ```  

2. Navigate to the project directory:  
   ```bash  
   cd detect_drowsiness
   ```  
 

---

## 🚀 Usage  

1. **Run the script**:  
   ```bash  
   python detect_drowsiness.py  
   ```  

2. **Webcam feed**: The system captures frames, processes them, and displays the live feed with FPS, eye status, and drowsiness alerts.  

3. **Quit**: Press `q` or `ESC` to exit.  

---

## 📊 Results  
- **Training Accuracy**: High accuracy achieved on training and validation datasets.  
- **Performance**: Real-time detection with minimal latency.  
- **Effectiveness**: Timely alarm system alerts when drowsiness is detected.  

---

## 🎥 Demo  
- Real-time face and eye detection via webcam.  
- Eye classification as **Open** or **Closed**.  
- FPS display and drowsiness alerts.  
- Alarm plays when drowsiness is detected.
# Demo Video

[![Watch the demo video](/kdd.png)](https://drive.google.com/file/d/1W9Oyf1kwmvn6Qv5ZZ5iNLp-aVyiCdj7M/view?usp=sharing)


---

## 🚀 Future Enhancements  
- Support for detecting multiple faces.  
- Yawning detection as an additional fatigue indicator.  
- Deployment on devices like Raspberry Pi for portability.  

---

## 🤝 Contributing  
We welcome contributions! Fork the repository, create a feature branch, and submit a pull request.  

---

## ⚖️ License  
This project is licensed under the MIT License. Refer to the `LICENSE` file for details.  

---

## 💌 Contact  
For questions or feedback, reach out:  
📧 **Email**: kamalkumarkolisetty@gmail.com  

