# Emotion Prediction Model for Children with Autism

This repository contains the code and documentation for the thesis project focused on the training and creation of a model capable of predicting emotions through the correct identification of micro-expressions in children with autism.

## Project Overview

This project is divided into several stages, each contributing to the development of a robust model for emotion prediction. Below is a summary of the activities and stages involved in this project:

### 1. Topic Selection
The project focuses on training and creating a model that can predict emotions by correctly identifying micro-expressions in children with autism.

### 2. Database Review
An exhaustive study of available databases pertinent to the topic was conducted, focusing on images of faces showing micro-expressions, preferably labeled. The Chinese Academy of Sciences Micro Expressions database was identified and usage rights were obtained.

### 3. Data Cleaning and Exploration
The database was cleaned and explored, selecting suitable images for training the model and verifying that they were correctly labeled.

### 4. Initial Model Training
Using the Teachable Machine platform, which allows training pre-existing models without the need for programming from scratch, the model training began. After multiple tests with different types of emotions and quantities of images, three models were selected. An article about these models was presented at the ARTIIS 2023 conference and published in its journal.

### 5. Field Analysis
Visits were made to the Pro Autismo school to directly analyze the target audience that would be worked with at the end of the model training.

### 6. Model Evaluation and Improvement
The models trained with Teachable Machine did not provide satisfactory results with new images. Therefore, new models were developed from scratch using Python and machine learning libraries such as TensorFlow, Keras, and scikit-learn. Although these models showed slight improvement, they were not accurate enough for field tests.

### 7. Change of Approach
The focus of the image classification model was changed to one based on facial meshes and coordinates instead of pixel analysis alone. This new model required identifying key facial points to determine the type of expression shown.

### 8. Facial Points Identification
A tool called blendshapes was used, which identifies 52 facial sections and determines their activation degree from 0 to 1, using a neutral face as a reference.

### 9. Final Results
This tool was used to process the images, identifying the facial sections with the highest activation according to the expressed emotion. Five basic emotions were identified: fear, anger, sadness, joy, and disgust.

## Repository Structure

- `data/`: Contains the cleaned and processed datasets used for model training.
- `notebooks/`: Jupyter notebooks used for data exploration, model training, and evaluation.


## Installation

To run the code in this repository, you need to have Python installed. It's recommended to create a virtual environment and install the required dependencies using the following commands:

```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt
