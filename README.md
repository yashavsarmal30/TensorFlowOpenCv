
# Teachable Machine Image Classifier

This repository demonstrates a Keras-based image classifier trained using Google’s Teachable Machine. It uses a pre-trained model to classify images captured via a webcam into categories such as Identity Cards, Calculators, and Mobile Phones.


## Features
- **Real-Time Classification**: Classify images in real-time using your webcam.
- **Custom Labels**: Train the model with your own dataset and labels using Teachable Machine.
- **Confidence Scores**: Displays the confidence percentage of the prediction.
- **Pre-Trained Model**: Includes a pre-trained model ready for use.

---

## Prerequisites
Ensure the following tools and libraries are installed:
- Python 3.7 or higher
- TensorFlow (`tensorflow`)
- OpenCV (`opencv-python`)
- NumPy (`numpy`)

---

## Installation

### 1. Clone the Repository
Clone the repository to your local machine:
```bash
git clone https://github.com/your-username/converted_keras.git
cd converted_keras
```

### 2. Install Dependencies
Install the required Python packages:
```bash
pip install tensorflow opencv-python numpy
```

### 3. Add Model and Label Files
Ensure the following files are in the project directory:
- **`keras_Model.h5`**: Pre-trained Keras model file.
- **`labels.txt`**: Text file containing class names, one per line.

### 4. Add the Example Image
Save the provided `image.png` file in the root directory of the project.

---

## Usage

### Run the Script
Start the webcam-based classifier:
```bash
python classify.py
```

### What Happens:
1. The webcam captures images in real-time.
2. Each frame is resized, normalized, and fed into the model for prediction.
3. The script displays:
   - The predicted class.
   - The confidence score.
4. Exit the webcam feed by pressing the `ESC` key.

### Example Output:
Terminal output might look like this:
```
Class: Calculator
Confidence Score: 96 %
```

---

## Code Breakdown

### Loading the Model and Labels
The script loads a pre-trained Keras model (`keras_Model.h5`) and reads the class names from `labels.txt`.

### Image Processing
Captured images are resized to **224x224** pixels and normalized to fit the model's input requirements.

### Prediction
The model predicts the class of the processed image, calculates confidence scores, and outputs the results.

---

## Training Information

The model was trained using Google’s [Teachable Machine](https://teachablemachine.withgoogle.com/) with the following parameters:
- **Number of Classes**: 3
- **Categories**: Identity Card, Calculator, Mobile Phone
- **Training Settings**:
  - Epochs: 52
  - Batch Size: 16
  - Learning Rate: 0.00101

### Dataset Summary
The training dataset contains:
- **277** images of Identity Cards.
- **174** images of Calculators.
- **359** images of Mobile Phones.

---

## Example Dataset
Here’s a preview of the dataset categories used for training:

- **Identity Card**: Images of various identity cards.
- **Calculator**: Different types of calculators.
- **Mobile Phone**: Images of mobile phones and similar devices.

---

## Preview

Below is a sample screenshot of the Teachable Machine interface during training:



## Acknowledgments
- [Teachable Machine](https://teachablemachine.withgoogle.com/) by Google for making the training process simple and intuitive.
- [TensorFlow](https://www.tensorflow.org/) and [Keras](https://keras.io/) for their powerful machine learning frameworks.
- [OpenCV](https://opencv.org/) for webcam integration and image processing.

```
