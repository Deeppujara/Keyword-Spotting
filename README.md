# Keyword Spotting on Arduino Nano 33 BLE Sense

This project focuses on a Keyword Spotting system developed using Edge Impulse and deployed on an Arduino Nano 33 BLE Sense. The model is trained to recognize specific keywords and operates efficiently on embedded hardware.

## Project Overview

- **Keywords**: "Go", "Stop", "Up", "Down", "Unknown", and "Noise"
- **Data**: 1-second audio data samples for each keyword
- **Feature Extraction**: MFCC (Mel Frequency Cepstral Coefficients) with 13 coefficients and 256 FFT lengths
- **Model Architecture**:
  - 1D Convolutional Layer with 64 neurons
  - Dropout Layer (25% dropout)
  - 1D Convolutional Layer with 32 neurons
  - Dropout Layer (25% dropout)
  - 1D Convolutional Layer with 8 neurons
  - Dropout Layer (25% dropout)
  - Flattened Layer for classification into 6 features
- **Accuracy**: 
  - Training Accuracy: 85.4%
  - Test Accuracy: 78.63%
- **Deployment**: The model was converted to TensorFlow Lite and deployed on the Arduino Nano 33 BLE Sense for real-time testing.

## Installation Instructions

To use this project on your Arduino Nano 33 BLE Sense, follow the steps below:

1. **Add the Library**:
   - Open the Arduino IDE.
   - Navigate to `Sketch > Include Library > Add .ZIP Library...`.
   - Select the `.zip` file of the model library provided.

2. **Run the Example**:
   - After adding the library, navigate to `File > Examples > Speech_Recognition_6_Classes_inferencing` in the Arduino IDE.
   - Upload the example code to your Arduino Nano 33 BLE Sense and start the live testing.

## Project Highlights for Resume

- Developed and deployed a Keyword Spotting model using Edge Impulse on an Arduino Nano 33 BLE Sense with an accuracy of 85.4% (training) and 78.63% (testing).
- Utilized MFCC coefficients (13 coefficients, 256 FFT lengths) and a 1D CNN architecture with dropout layers to enhance model performance.
- Successfully converted the model to TensorFlow Lite and integrated it into an Arduino-based embedded system for real-time keyword detection.