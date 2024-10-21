# Face Recognition System

A Python-based facial recognition system that can detect, train, and recognize faces using OpenCV. This project implements Local Binary Pattern Histograms (LBPH) for face recognition and includes features like real-time face detection and web page redirection upon successful authentication.

## Features

- Real-time face detection using webcam
- Face data collection and training
- Face recognition with confidence scoring
- Automatic web page redirection upon successful authentication
- User-friendly interface with visual feedback

## Prerequisites

Before running this project, make sure you have the following installed:
- Python 3.6 or higher
- OpenCV (`cv2`)
- NumPy
- A webcam

## Installation

1. Clone this repository:
```bash
git clone https://github.com/YourUsername/face-recognition-system.git
cd face-recognition-system
```

2. Install required packages:
```bash
pip install opencv-python numpy
```

3. Download the Haar Cascade classifier file and place it in the project directory:
   - `haarcascade_frontalface_default.xml`

## Project Structure

```
face-recognition/
│
├── haarcascade_frontalface_default.xml
├── face-recognition.ipynb
├── training-data/
│   └── (training images will be stored here)
└── test-page.html
```

## Usage

1. **Data Collection**
   - Run the first cell in the notebook to capture face data
   - The system will capture 100 images of your face for training
   - Images are saved in the `training-data` directory

2. **Training**
   - Run the second cell to train the model
   - The system will use the captured images to train the LBPH face recognizer

3. **Recognition**
   - After training, the system will start face recognition
   - A confidence score will be displayed on the screen
   - If confidence is above 85%, it will recognize the user and redirect to a specified webpage

## How It Works

1. **Face Detection**: Uses Haar Cascade Classifier to detect faces in real-time
2. **Data Collection**: Captures and processes multiple images of the face
3. **Training**: Uses LBPH algorithm to train on the collected face data
4. **Recognition**: Compares live feed with trained data to recognize faces
5. **Authentication**: Provides access based on recognition confidence level

## Code Features

- Real-time face detection and tracking
- Automatic image capture and processing
- Confidence-based authentication
- Visual feedback with rectangle drawing around detected faces
- Status display (Locked/Unlocked)
- Browser integration for successful authentication

## Error Handling

The system includes error handling for:
- No face detected in frame
- Low confidence matches
- Invalid input handling

## Contributing

Feel free to fork this project and submit pull requests. You can also open issues for bugs or feature suggestions.
