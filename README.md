# Brain Tumor Detection Using Deep Learning

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/Brain-Tumor-Detection.git
cd Brain-Tumor-Detection
```
---


## Overview

This project implements a Brain Tumor Detection System using Deep Learning and Transfer Learning techniques. The model classifies MRI brain scan images into two categories:

* Tumor
* No Tumor

The project uses MobileNetV2 as a pretrained convolutional neural network and achieves high classification performance on the MRI image dataset.

---

## Dataset

The dataset contains MRI brain scan images organized into two classes:

```text
BrainTumor/
│
├── yes/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
└── no/
    ├── image1.jpg
    ├── image2.jpg
    └── ...
```

### Dataset Statistics

| Class    | Images |
| -------- | ------ |
| Tumor    | 155    |
| No Tumor | 98     |
| Total    | 253    |

---

## Technologies Used

* Python
* TensorFlow
* Keras
* MobileNetV2
* NumPy
* Matplotlib
* Scikit-Learn
* Seaborn

---

## Project Workflow

1. Load MRI image dataset
2. Resize images to 224 × 224 pixels
3. Apply data augmentation
4. Split dataset into Training, Validation, and Test sets
5. Train MobileNetV2 transfer learning model
6. Evaluate model performance
7. Generate predictions on unseen MRI images

---

## Model Architecture

The project uses MobileNetV2 as a pretrained feature extractor.

### Layers

* Data Augmentation
* Rescaling Layer
* MobileNetV2 (Pretrained on ImageNet)
* Global Average Pooling Layer
* Dense Layer (128 neurons, ReLU)
* Dropout Layer (0.3)
* Output Layer (Sigmoid)

---

## Results

### Confusion Matrix

```text
[[17  0]
 [ 1 27]]
```

### Performance Metrics

| Metric    | Score   |
| --------- | ------- |
| Accuracy  | 97.78%  |
| Precision | 100.00% |
| Recall    | 96.43%  |
| F1-Score  | 98.18%  |
| ROC-AUC   | 1.00    |

---

## Visualizations

The project includes:

* Training Accuracy Curve
* Validation Accuracy Curve
* Training Loss Curve
* Validation Loss Curve
* Confusion Matrix Heatmap
* ROC Curve

---

## Model Saving

The trained model is saved as:

```python
model.save("brain_tumor_model.keras")
```

To load the model:

```python
from tensorflow.keras.models import load_model

model = load_model("brain_tumor_model.keras")
```

---

## Requirements

```text
tensorflow
numpy
matplotlib
scikit-learn
seaborn
opencv-python
pandas
```

---

## Future Improvements

* Increase dataset size
* Fine-tune MobileNetV2 layers
* Add Grad-CAM visualization
* Deploy using Streamlit or Flask
* Evaluate on larger medical imaging datasets

---
