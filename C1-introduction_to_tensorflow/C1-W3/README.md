#  TensorFlow Developer Certification - Week 3

##  Week 3: Introduction to Convolutional Neural Networks (CNNs)

This directory contains my work for **Week 3** of the [Introduction to TensorFlow for AI, ML, and DL](https://www.coursera.org/learn/introduction-tensorflow) by DeepLearning.AI — part of the TensorFlow Developer Certificate Program.

---

##  Topics Covered
- Introduction to **Convolutional Neural Networks (CNNs)**
- Using `Conv2D` and `MaxPooling2D` layers
- Feature extraction through convolution
- Flattening and connecting to dense layers
- Improving image classification using spatial hierarchies

---

##  Assignment Completed

### 1. **CNN for Fashion MNIST Classification**
- Built a CNN with `Conv2D` and `MaxPooling2D` layers
- Used Fashion MNIST dataset with reshaped input (28, 28, 1)
- Compared accuracy to previous fully connected models

 **Model Architecture:**
```python
model = tf.keras.Sequential([
    tf.keras.layers.Conv2D(64, (3,3), activation='relu', input_shape=(28,28,1)),
    tf.keras.layers.MaxPooling2D(2,2),
    
    tf.keras.layers.Conv2D(64, (3,3), activation='relu'),
    tf.keras.layers.MaxPooling2D(2,2),
    
    tf.keras.layers.Flatten(),
    tf.keras.layers.Dense(128, activation='relu'),
    tf.keras.layers.Dense(10, activation='softmax')
])
