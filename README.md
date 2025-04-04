# Face Condition Detection App

A real-time Flutter application that detects a user's facial condition (e.g. happy, sad, stressed, tired) using a custom machine learning model, even under varying lighting environments. This project was completed as part of the **GSoC 2025 Take-Home Qualification Task** for CCExtractor.

## 🧠 Features

- Real-time facial condition analysis
- Works in different lighting conditions (bright, dim, etc.)
- On-device inference using TensorFlow Lite
- Built using Flutter for cross-platform support (Android & iOS)

## 🚀 How It Works

1. **Model Training**  
   The facial expression recognition model was trained using [Google Teachable Machine](https://teachablemachine.withgoogle.com/). It was then exported and converted to **TensorFlow Lite** format.

2. **Camera Input**  
   The `camera` package streams live video from the device's front camera.

3. **Inference Engine**  
   Each frame is processed and passed through the TFLite model using the `tflite_flutter` package.

4. **Result Display**  
   The app displays the predicted facial condition in real-time.

## 📦 Packages Used

- `camera`: Access and display live camera feed  
- `tflite_flutter`: Run the TFLite model on-device  
- `image`: Preprocess image frames before inference  
- `path_provider`: Load model assets from local storage

## 📂 Directory Structure

lib/  
├── main.dart  
├── home.dart 
assets/  
└── model.tflite

## 📱 Screenshots

![image](https://github.com/user-attachments/assets/0abb4316-428e-4cfa-9611-f08b6caec8e3)
![image](https://github.com/user-attachments/assets/4b60f135-e699-4ee6-a48e-7589148f3aaf)



## 🛠️ Getting Started

1. **Clone the repository**  
   `git clone https://github.com/your-username/face-condition-detector.git`  
   `cd face-condition-detector`

2. **Install dependencies**  
   `flutter pub get`

3. **Add the TFLite model**  
   - Place your `model.tflite` file in the `assets/` directory.  
   - Update `pubspec.yaml` to include:
     ```
     assets:
       - assets/model.tflite
     ```

4. **Run the app**  
   `flutter run`

## ✅ Completed As

This project was developed as part of the **GSoC 2025 Take-Home Qualification Task** under **CCExtractor** to demonstrate real-time face detection and analysis capabilities using Flutter and on-device ML.
