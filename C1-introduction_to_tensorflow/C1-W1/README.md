# TensorFlow Developer Certification - Week 1

## Week 1: Introduction to TensorFlow for Machine Learning

This repository contains my work for **Week 1** of the [Introduction to TensorFlow for AI, ML and DL](https://www.coursera.org/learn/introduction-tensorflow) by DeepLearning.AI — part of the TensorFlow Developer Certificate Program.

---

## Topics Covered
- What is TensorFlow?
- Tensors and basic operations
- TensorFlow Sequential API
- Model building and compilation
- Training with `.fit()` and evaluation with `.evaluate()`
- Introduction to callbacks (e.g., `EarlyStopping`)

---

## Assignments Completed
### 1. **Fashion MNIST Classifier**
- Built a neural network using the Keras Sequential API
- Trained on Fashion MNIST dataset
- Achieved >90% accuracy with minimal layers
- Used callbacks to stop training early when accuracy crossed a threshold

📊 **Model Architecture:**
```python
model = tf.keras.Sequential([
    tf.keras.layers.Flatten(input_shape=(28, 28)),
    tf.keras.layers.Dense(128, activation='relu'),
    tf.keras.layers.Dense(10, activation='softmax')
])
