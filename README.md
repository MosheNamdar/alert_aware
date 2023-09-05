# Alert_aware Project

**Alert_aware** is a project designed to detect signs of fatigue by monitoring individuals' eyes through image analysis.
It employs computer vision techniques to capture images from a camera, processes these images to extract eye crops,
and then applies a deep learning model to classify the eyes as "Open" or "Closed."
If fatigue is detected, it sends an alert message.

## Table of Contents

- [Usage](#usage)
- [Components](#components)
- [Contributing](#contributing)


## Usage

To run the **Alert_aware** project, follow these steps:

1. Start the camera and data processing:
   python controller.py

2. The project will continuously capture images, process them, and classify eye status. If fatigue is detected, an alert message will be sent.

3. To monitor the server status, you can access the `/sanity` endpoint of the Flask server.

## Components

The **Alert_aware** project consists of several components:

- **camera.py**: Captures images from a camera and saves them to the "resources" directory.

- **eyes_recognition.py**: Processes captured images, detects eyes, crops and saves the eye regions, and deletes the original images.

- **fatigue_detection.py**: Uses a deep learning model to classify eye status as "Open" or "Closed" to detect signs of fatigue.

- **run_model_on_crops.py**: Loads cropped eye images and classifies them. If fatigue is detected, it sends an alert message.

- **scan_to_csv.py**: Scans the "train" directory and creates a CSV file with image paths and labels for training.

- **telegram_server.py**: Sets up a Flask server to send alert messages via Telegram when fatigue is detected.

## Contributing

Contributions to **Alert_aware** are welcome! If you'd like to contribute to this project, please follow these guidelines:

- Fork the repository.

- Create a new branch for your feature or bug fix.

- Make your changes and test thoroughly.

- Submit a pull request with a clear description of your changes and why they are beneficial.

