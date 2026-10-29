# Final Project: Emotion Detection Application

## Project Overview

This project demonstrates an Emotion Detection application using Natural Language Processing (NLP) and the IBM Watson Emotion Prediction service.

The application analyzes text entered by a user and identifies five emotions: anger, disgust, fear, joy, and sadness. It also determines the dominant emotion in the given text.

The application is developed using Python and Flask, with a web interface that allows users to enter text and view the emotion analysis results.

## Project Objectives

- Build an emotion detection function using the IBM Watson NLP service.
- Identify five emotions from the submitted text.
- Determine the dominant emotion.
- Create a Flask web application for text input and emotion analysis.
- Handle blank input and HTTP error responses.
- Test the application using Python unit tests.
- Perform static code analysis using Pylint.

## Features

- **Emotion Detection:** Identifies anger, disgust, fear, joy, and sadness.
- **Dominant Emotion:** Determines the emotion with the highest score.
- **Flask Web Interface:** Allows users to submit text for analysis.
- **Input Validation:** Handles blank text input.
- **Error Handling:** Handles HTTP 400 responses and service errors.
- **Unit Testing:** Tests the emotion detection function.
- **Static Code Analysis:** Uses Pylint to check code quality.

## Technologies Used

- Python
- Flask
- IBM Watson NLP Emotion Prediction service
- Requests
- HTML
- JavaScript
- Unittest
- Pylint
- Git and GitHub

## Project Structure

```text
oaqjp-final-project-emb-ai/
├── EmotionDetection/
│   ├── __init__.py
│   └── emotion_detection.py
├── static/
│   └── mywebscript.js
├── templates/
│   └── index.html
├── test_emotion_detection.py
├── server.py
└── README.md
```

## Emotion Detection Function

The `emotion_detector()` function sends the input text to the IBM Watson NLP Emotion Prediction service and processes the returned emotion scores.

The function returns a dictionary containing:

- `anger`
- `disgust`
- `fear`
- `joy`
- `sadness`
- `dominant_emotion`

The dominant emotion is the emotion with the highest score. Error responses and invalid inputs should be handled according to the application's error-handling logic.

## Flask Web Application

The Flask application is implemented in `server.py`.

It provides two routes:

- `/` — Displays the emotion detection web page.
- `/emotionDetector` — Receives submitted text and returns the emotion analysis results.

The application validates blank input and displays an appropriate error message when the input is empty or the emotion analysis service is unavailable.

## Unit Testing

Unit tests are implemented in `test_emotion_detection.py` using Python's `unittest` framework.

Run the unit tests using:

```bash
python3 test_emotion_detection.py
```

## Static Code Analysis

Pylint is used to analyze the Flask server code for coding standards and potential issues.

Run the analysis using:

```bash
python3 -m pylint server.py
```

## How to Run the Application

### 1. Install the required packages

```bash
python3 -m pip install Flask requests pylint
```

### 2. Start the Flask server

```bash
python3 server.py
```

### 3. Open the application

Open the following address in your web browser:

http://127.0.0.1:5000

Enter text into the input field and run the emotion analysis.

**Note:** Successful live emotion predictions require the IBM Watson NLP service endpoint to be accessible.

## Conclusion

This project demonstrates the development of an NLP-based emotion detection application using Python, Flask, and the IBM Watson Emotion Prediction service. It includes input validation, error handling, unit testing, and static code analysis.