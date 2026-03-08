# Sentimoji: Real-Time Emotion Recognition with Emojis

Sentimoji is an AI-powered emotion recognition application that detects facial expressions in real-time using your webcam and maps them to corresponding emojis. Built with Convolutional Neural Networks (CNN) using TensorFlow/Keras, this project combines computer vision and deep learning to create an interactive and fun emotion detection experience.

## Features

- **Real-Time Emotion Detection**: Uses OpenCV's Haar cascades to detect faces and predict emotions from live webcam feed
- **7 Emotion Categories**: Recognizes Angry, Disgusted, Fearful, Happy, Neutral, Sad, and Surprised emotions
- **Emoji Mapping**: Displays relevant emojis for each detected emotion
- **GUI Interface**: User-friendly Tkinter-based graphical interface
- **CNN Model**: Custom-trained Convolutional Neural Network for accurate emotion classification
- **Dataset Support**: Trained on the FER-2013 dataset (Facial Expression Recognition 2013)

## Installation

### Prerequisites

- Python 3.7+
- Webcam (for real-time detection)

### Dependencies

Install the required packages using pip:

```bash
pip install tensorflow opencv-python pillow numpy keras
```

For the GUI version, you'll also need Tkinter (usually included with Python).

## Usage

### Training the Model

1. Ensure you have the dataset in the `dataset/` folder with `train/` and `test/` subdirectories containing emotion folders.
2. Run the `train.ipynb` Jupyter notebook to train the model.
3. The trained model weights will be saved as `model.h5`.

### Running the Application

#### GUI Version (Recommended)
```bash
python gui.py
```

#### Real-Time Video Detection
Run the code in the `train.ipynb` notebook under the "Using openCV haarcascade xml detect the bounding boxes of face in the webcam and predict the emotions" section.

## Project Structure

```
Sentimoji/
├── gui.py                 # Tkinter GUI application
├── train.ipynb           # Jupyter notebook for training the model
├── model.h5              # Trained model weights
├── dataset/
│   ├── train/           # Training images (organized by emotion)
│   └── test/            # Test images (organized by emotion)
├── emojis/              # Emoji images for each emotion
│   ├── Angry/
│   ├── Disgusted/
│   ├── Fearful/
│   ├── Happy/
│   ├── Neutral/
│   ├── Sad/
│   └── Surprised/
└── README.md
```

## Model Architecture

The CNN model consists of:
- 4 Convolutional layers with ReLU activation
- MaxPooling and Dropout layers for regularization
- Dense layers with 1024 neurons
- Output layer with 7 neurons (one for each emotion) using softmax activation

## Dataset

The model is trained on facial expression images categorized into 7 emotions:
- Angry
- Disgusted
- Fearful
- Happy
- Neutral
- Sad
- Surprised

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- FER-2013 Dataset for training data
- OpenCV for computer vision capabilities
- TensorFlow/Keras for deep learning framework