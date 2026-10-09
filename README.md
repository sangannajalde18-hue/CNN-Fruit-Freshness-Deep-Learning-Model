# CNN Fruit Freshness Deep Learning Model

A deep learning application that classifies fruit images as fresh or rotten using a Convolutional Neural Network (CNN) and MobileNetV2 transfer learning. The project includes a Streamlit web app that lets users upload fruit images and receive real-time freshness predictions.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9%2B-blue" alt="Python 3.9+" />
  <img src="https://img.shields.io/badge/TensorFlow-2.x-orange" alt="TensorFlow 2.x" />
  <img src="https://img.shields.io/badge/Streamlit-App-red" alt="Streamlit App" />
  <img src="https://img.shields.io/badge/Status-Working-success" alt="Working Status" />
</p>

## Overview

This project focuses on automated fruit quality assessment using computer vision. By training a CNN on fruit images, the system can distinguish between fresh and rotten produce across multiple fruit categories such as apples, bananas, oranges, peaches, pomegranates, and strawberries.

The repository includes:

- a trained MobileNetV2 model (`fruit_freshness_mobilenetv2.h5`)
- a Streamlit application for inference (`app.py`)
- a Jupyter notebook used for training and experimentation
- sample prediction and model evaluation outputs

## Features

- Fresh vs. rotten fruit classification
- Supports multiple fruit categories
- MobileNetV2 transfer learning for faster and accurate predictions
- User-friendly web interface built with Streamlit
- Image upload support for `.jpg`, `.jpeg`, and `.png` files
- Confidence score for each prediction

## Tech Stack

- Python 3.9+
- TensorFlow / Keras
- Streamlit
- NumPy
- Pillow
- Jupyter Notebook

## Project Structure

```text
CNN-Fruit-Freshness-Deep-Learning-Model/
├── app.py                              # Streamlit app for fruit prediction
├── fruit_freshness_cnn (1).ipynb       # Training notebook
├── fruit_freshness_mobilenetv2.h5      # Trained CNN model
├── requirements.txt                    # Python dependencies
├── README.md                           # Project documentation
├── outputs_baseline_cnn_curves (1).png # Training curves
├── outputs_class_distribution.png      # Class distribution chart
├── outputs_confusion_matrix.png         # Confusion matrix
├── outputs_mobilenetv2_(fine-tuned)_curves.png
├── outputs_sample_images.png            # Sample fruit images
├── outputs_sample_predictions.png       # Sample predictions
├── .gitignore                          # Git ignore rules
└── LICENSE (if present in your repo)   # Add if applicable
```

## Model Details

The model is based on a transfer learning approach using MobileNetV2, which is lightweight and effective for image classification tasks. The network is fine-tuned for fruit freshness classification and predicts one of several fruit-condition classes such as:

- fresh apples
- fresh bananas
- fresh oranges
- fresh peaches
- fresh pomegranates
- fresh strawberries
- rotten apples
- rotten bananas
- rotten oranges
- rotten peaches
- rotten pomegranates
- rotten strawberries

## Installation

1. Clone the repository

```bash
git clone https://github.com/sangannajalde18-hue/CNN-Fruit-Freshness-Deep-Learning-Model.git
cd CNN-Fruit-Freshness-Deep-Learning-Model
```

2. Create a virtual environment

```bash
python -m venv venv
```

On Windows:

```bash
venv\Scripts\activate
```

On macOS/Linux:

```bash
source venv/bin/activate
```

3. Install dependencies

```bash
pip install -r requirements.txt
```

## Run the App

Start the Streamlit application:

```bash
streamlit run app.py
```

Then open the local URL displayed in the terminal (usually `http://localhost:8501`).

## How to Use

1. Upload a fruit image in JPG, JPEG, or PNG format.
2. Click the "Predict Freshness" button.
3. The model will detect the fruit type and predict whether it is fresh or rotten.
4. The app displays the uploaded image, the predicted class, and the confidence score.

## Sample Outputs

This repository includes evaluation plots and sample visualizations to understand model performance:

- Training curves for model convergence
- Class distribution of the dataset
- Confusion matrix
- Sample predictions
- Example input images

## Training Notebook

The notebook `fruit_freshness_cnn (1).ipynb` contains the model development workflow, including:

- dataset preparation
- image preprocessing
- CNN model design
- training and validation
- performance evaluation
- visualization of results

## Requirements

The project dependencies are listed in `requirements.txt`:

```txt
streamlit
tensorflow
numpy
pillow
```

## Notes

- The trained model file is large and should be kept in the project root for the app to load correctly.
- For best results, upload clear fruit images with good lighting.
- The model is designed for fruit images similar to the dataset used during training.

## License

This project does not currently include a license file. If you plan to share or distribute it publicly, consider adding an appropriate open-source license such as MIT or Apache 2.0.

## Acknowledgements

This project demonstrates the use of deep learning and computer vision for food quality assessment and can be extended with:

- larger datasets
- additional fruit types
- mobile deployment
- real-time camera inference
- e-commerce and agriculture use cases

## Contact

If you want to contribute, improve the model, or use this project for further development, feel free to reach out or open an issue in the repository.

---

Made with Python, TensorFlow, and Streamlit for fruit freshness detection.
