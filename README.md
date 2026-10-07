# Smart Diagnostics: COVID Detection using AI

Science Fair 2023–2024 project by **Reyansh Gupta**

## Problem Statement

COVID tests like the RT-PCR test can be time-consuming and resource-intensive, resulting in long wait times for diagnosis. To address this, this project builds an AI (deep learning) system that predicts whether a patient has COVID-19 by identifying patterns in chest X-ray images.

## Solution Approach

1. Learn the specific tools and techniques needed
2. Acquire and load the dataset (chest X-ray images)
3. Train a convolutional neural network model
4. Analyze the model's performance
5. Tune the model for higher performance
6. Deploy the model for general use

## Dataset

The dataset used is the [Chest X-ray (COVID-19 & Pneumonia) dataset](https://www.kaggle.com/datasets/prashant268/chest-xray-covid19-pneumonia) from Kaggle, which contains labeled chest X-ray images across three classes:

- Normal
- Viral Pneumonia
- COVID-19

## Model

Built with **TensorFlow/Keras**. The notebook ([Main Model.ipynb](Main%20Model.ipynb)) walks through:

- Building and training an initial CNN classifier
- Evaluating performance on training/testing data
- Tuning the model with image augmentation and an improved architecture
- Saving the final model for deployment

## Results

The tuned model was evaluated on a balanced test set of 300 images (100 per class):

**Overall Accuracy: 94.0%**

| Class | Precision | Recall | F1 Score |
|---|---|---|---|
| Normal | 88.4% | 99.0% | 93.4% |
| Viral Pneumonia | 95.6% | 86.0% | 90.5% |
| COVID-19 | 98.0% | 97.0% | 97.5% |

The model performs strongest on COVID-19 detection but shows some confusion between Normal and Viral Pneumonia cases, with Viral Pneumonia having the lowest recall (86%).

## Getting Started

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/prashant268/chest-xray-covid19-pneumonia) and place it in the project directory.
2. Install the required Python packages: `pip install -r requirements.txt`
3. Open `Main Model.ipynb` in Jupyter and run the cells in order.

## Credits

Created for the **Science and Engineering Fair of Houston**.
