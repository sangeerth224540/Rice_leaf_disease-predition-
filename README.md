Project Overview

This project aims to develop an accurate and automated system to detect and classify rice leaf diseases using deep learning techniques. By leveraging convolutional neural networks (CNNs), the model can identify common rice plant diseases from leaf images, assisting farmers and agronomists in early detection and effective disease management.

Objectives

-Detect and classify common rice leaf diseases.

-Build a deep learning model (CNN) capable of learning from image data.

-Evaluate model performance using accuracy and visual metrics.

-Demonstrate predictions with sample leaf images.


## 🧠 Model Details

- **Framework**: TensorFlow / Keras
- **Architecture**:
- Input layer (128x128x3)
- 3 Convolutional Layers + MaxPooling
- Output Layer: Softmax (4 Classes)
- **Optimizer**: Adam
- **Loss Function**: Categorical Crossentropy
- **Metrics**: Accuracy

## 📊 Evaluation

- Final Model Accuracy: **~95%**
- Used Confusion Matrix and Classification Report
- Plotted training and validation accuracy/loss curves

