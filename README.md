# Dog Breed Classification

Deep learning based dog breed classification project using TensorFlow and ResNet50V2. The model identifies different dog breeds from images using transfer learning, image preprocessing, and CNN techniques.

## Overview

The Dog Breed Identifier uses a pre-trained ResNet50V2 model to classify dog images into their respective breeds. The model is fine-tuned and trained on a labeled dataset of dog images stored in the `train` folder and described in `labels.csv`.

## How It Works

- **Data Preparation:**
  - Reads breed labels from `labels.csv`.
  - Resizes and preprocesses images from the `train` folder.
  - Splits the dataset into training and testing sets.
- **Data Augmentation:**
  - Applies image augmentation to improve model performance.
- **Model Training:**
  - Uses a ResNet50V2 model pre-trained on ImageNet.
  - Adds custom top layers for dog breed classification.
  - Trains with callbacks for learning-rate reduction and early stopping.
- **Prediction:**
  - Classifies a dog image and outputs the predicted breed.

## Files Included

- `dog-breed-identification.py`: Main Python script for data preparation, model training, and prediction.
- `labels.csv`: CSV file mapping image IDs to breed names.
- `model`: Folder containing saved model files.
- `test`: Folder containing test images.
- `train`: Folder containing training images.

## Requirements

- TensorFlow 2.2 or higher
- Keras, if using a TensorFlow version below 2.2
- OpenCV
- Scikit-learn
- NumPy
- Pandas
- Matplotlib

## Running the Program

Install the required libraries, then run:

```bash
python dog-breed-identification.py
```

The program trains the model and predicts the breed of the configured dog image. You can change the image path in the code to test different images.

Example output:

```python
Predicted Breed for this Dog is : ['leonberg']
```
