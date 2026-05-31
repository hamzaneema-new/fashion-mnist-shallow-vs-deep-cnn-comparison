# Fashion-MNIST: Shallow CNN vs Deep CNN Comparison

## Project Overview

This project presents a comparative study of two Convolutional Neural Network (CNN) architectures on the Fashion-MNIST dataset. The goal was to understand how network depth influences feature learning, classification accuracy, model complexity, and generalization performance.

Two models were developed and evaluated:

* Shallow CNN
* Deep CNN

The models were trained on the same dataset and compared using accuracy metrics, confusion matrices, prediction analysis, and model architecture characteristics.

---

## Dataset

Fashion-MNIST is a dataset of 70,000 grayscale images belonging to 10 fashion categories.

Classes:

* T-shirt/top
* Trouser
* Pullover
* Dress
* Coat
* Sandal
* Shirt
* Sneaker
* Bag
* Ankle Boot

Image Size:

```text
28 × 28 grayscale images
```

Dataset Split:

```text
Training Images: 60,000
Test Images: 10,000
```

---

## Data Preprocessing

The following preprocessing steps were applied:

* Normalized pixel values from 0–255 to 0–1
* Reshaped images for CNN input format
* Visualized sample images from all classes

Input Shape:

```text
(28, 28, 1)
```

---

## Model Architectures

### Shallow CNN

Architecture:

```text
Conv2D(32)
↓
MaxPooling2D
↓
Conv2D(64)
↓
MaxPooling2D
↓
Flatten
↓
Dense(128)
↓
Dropout(0.3)
↓
Dense(10, Softmax)
```

### Deep CNN

Architecture:

```text
Conv2D(32)
↓
Conv2D(32)
↓
MaxPooling2D
↓
Conv2D(64)
↓
Conv2D(64)
↓
MaxPooling2D
↓
Flatten
↓
Dense(128)
↓
Dropout(0.5)
↓
Dense(10, Softmax)
```

---

## Results

| Metric               | Shallow CNN | Deep CNN |
| -------------------- | ----------: | -------: |
| Training Accuracy    |      94.11% |   93.56% |
| Validation Accuracy  |      91.51% |   92.19% |
| Test Accuracy        |      91.51% |   92.19% |
| Conv Layers          |           2 |        4 |
| Trainable Parameters |     225,034 |  197,482 |

---

## Key Findings

* Both models performed well on Fashion-MNIST.
* The Deep CNN achieved the highest test accuracy.
* Visually distinct classes such as Trouser, Bag, Sandal, Sneaker, and Ankle Boot were classified accurately by both models.
* Most classification errors occurred between Shirt, T-shirt/top, Pullover, and Coat due to their visual similarity.
* The Deep CNN reduced confusion among these challenging classes.

---

## Confusion Matrix Analysis

The confusion matrices revealed that:

### Easiest Classes to Classify

* Trouser
* Bag
* Sandal
* Sneaker
* Ankle Boot

### Most Frequently Confused Classes

* Shirt
* T-shirt/top
* Pullover
* Coat

The Deep CNN showed improved performance in distinguishing these visually similar categories.

---

## What I Learned

Through this project, I gained practical experience with:

* Image preprocessing
* Convolution operations
* Pooling layers
* Feature extraction
* CNN architecture design
* Model evaluation
* Overfitting and generalization
* Confusion matrix interpretation
* Error analysis

I also learned that deeper networks can improve performance, but the improvement must justify the additional complexity.

---

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## Future Improvements

Possible enhancements include:

* Data Augmentation
* Batch Normalization
* Early Stopping
* Learning Rate Scheduling
* Hyperparameter Tuning
* Transfer Learning using pre-trained CNN architectures

---

## Author

Neema Hamza

Deep Learning | Machine Learning | Data Analytics
