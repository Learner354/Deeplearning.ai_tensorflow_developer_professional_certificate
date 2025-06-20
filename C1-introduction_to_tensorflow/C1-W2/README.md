# TensorFlow Developer Certification - Week 2

## Week 2: Training Optimization with Callbacks

This repository contains my work for **Week 2** of the [Introduction to TensorFlow for AI, ML, and DL](https://www.coursera.org/learn/introduction-tensorflow) by DeepLearning.AI — part of the TensorFlow Developer Certificate Program.

---

## Topics Covered
- Improving training with callbacks
- Writing custom callbacks using `tf.keras.callbacks.Callback`
- Automatically stopping training when accuracy threshold is reached
- Understanding the importance of early stopping to reduce overfitting and save compute resources

---

## Assignment Completed

### 1. **Custom Callback Implementation**
- Built a simple feedforward neural network using Fashion MNIST
- Implemented a custom callback that stops training when accuracy reaches **>99%**
- Demonstrated model optimization with fewer epochs

📌 **Custom Callback Code:**
```python
class myCallback(tf.keras.callbacks.Callback):
    def on_epoch_end(self, epoch, logs={}):
        if logs.get('accuracy') > 0.99:
            print("\nReached 99% accuracy, stopping training!")
            self.model.stop_training = True
