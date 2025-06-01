Rice Leaf Disease Detection using Deep Learning

1. Introduction
  Rice is a staple food for more than half the global population. However, rice crops are susceptible to various leaf diseases that significantly reduce yield. Manual identification of such diseases is time-consuming and error-prone. This project aims to automate the detection and classification of rice leaf diseases using Convolutional Neural Networks (CNNs) in TensorFlow/Keras, providing fast and accurate results from leaf images.

2. Problem Statement
   The goal is to build a multi-class image classifier capable of identifying three major rice leaf diseases and distinguishing them from healthy leaves using image data.

3. Dataset Description
Source: Rice Leaf Disease Dataset from Kaggle

Categories:

  -Bacterial Leaf Blight

  -Brown Spot

  -Leaf Smut

Image Format: RGB .jpg images

Preprocessing:

Resized all images to 512x512 pixels

Normalized pixel values (0 to 1 range)

One-hot encoded class labels

Data Split:

Training Set

Validation Set

Test Set

4. Data Augmentation
  To improve generalization and avoid overfitting, the following data augmentation techniques were applied:

Rotation

Zoom

Horizontal/Vertical Flipping

Width/Height Shift

Shear

These augmentations were performed using Keras’s ImageDataGenerator.

5. Model Architecture
Framework: TensorFlow & Keras

Input Shape: 512x512x3

Model Layers:

3 Convolutional Layers (ReLU activation)

MaxPooling Layers after each Conv layer

Flatten Layer

Dense Layer with Dropout

Output Layer with Softmax activation for 3 classes

Optimizer: Adam

Loss Function: Categorical Crossentropy

Evaluation Metric: Accuracy

6. Training & Evaluation
Epochs: 30

Batch Size: 32

Early Stopping was used to prevent overfitting.

Results:
Training Accuracy: ~99.88%

Test Accuracy: ~98.36%

Evaluation Metrics:
Confusion Matrix

Classification Report:

Precision, Recall, F1-Score for each class

7. Prediction Demo
  The model was tested on new images of rice leaves downloaded from the internet. Images were resized to 512x512 and preprocessed before prediction. Sample prediction:

text
Copy
Edit
Predicted Class: Brown Spot
Visualizations of predictions on test data were also displayed with correct/incorrect predictions highlighted using color-coded titles.

8. Image Augmentation Visualization
  The notebook also demonstrates how an input image is augmented using ImageDataGenerator, showcasing 6 variations for a single image to highlight how the model learns from diverse data.

9. Tools & Technologies
Python

TensorFlow / Keras

OpenCV

NumPy, Pandas

Scikit-learn

Matplotlib, Seaborn

10. Conclusion
  The CNN-based deep learning model achieved high accuracy in identifying three common rice leaf diseases. With image augmentation, early stopping, and validation strategies, the model generalized well to unseen data and could serve as a foundation for real-world agricultural disease detection systems.

11. Future Work
Extend to more diseases and real-field noisy data

Deploy as a web or mobile app using Flask, Streamlit, or TensorFlow Lite

Integrate drone or mobile camera input for real-time prediction
