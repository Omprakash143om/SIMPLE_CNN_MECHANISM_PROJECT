# SIMPLE_CNN_MECHANISM_PROJECT

# 🧠 Simple Dense Neural Network with TensorFlow (Regression Demo)

This project demonstrates how to build a **simple fully connected neural network** using **TensorFlow/Keras** to perform a basic regression task.

---

## 📌 About the Project

This is a toy example to understand how multiple dense layers work in a neural network model. The model is trained on a small dataset:

- Input: `x = [1, 2, 3, 4, 5]`
- Output: `y = [3, 4, 5, 6, 7]`

The model learns a basic linear relationship and is tested by predicting the output for a new input value.

---

## 🧠 Model Architecture

The model is built using `tf.keras.Sequential` and contains 9 stacked `Dense` layers:

- Dense(units=4, input_dim=1)
- Dense(units=32)
- Dense(units=32)
- Dense(units=64)
- Dense(units=64)
- Dense(units=128)
- Dense(units=64)
- Dense(units=64)
- Dense(units=1) → Final output layer

Despite the dataset being very small, this structure demonstrates how to construct deep models in TensorFlow.

---

## ⚙️ Model Summary

- **Optimizer:** Adam
- **Loss Function:** Mean Squared Error
- **Metrics:** Mean Squared Error
- **Epochs Trained:** 10

---

## 🔍 Prediction Example

After training, the model was asked to predict the value for `x = 16`.  
The output was: Prediction for input 16: 17.127695

---

Which is very close to the expected value of ~18 (based on the pattern `y = x + 2`).

---

## 🚀 How to Run

1. Make sure TensorFlow is installed:
    ```bash
    pip install tensorflow
    ```

2. Run the script or notebook with the code:
    ```python
    import tensorflow as tf
    import numpy as np

    x = np.array([1,2,3,4,5])
    y = np.array([3,4,5,6,7])

    # Model definition
    model = tf.keras.Sequential([
        tf.keras.layers.Dense(4, input_dim=1),
        tf.keras.layers.Dense(32),
        tf.keras.layers.Dense(32),
        tf.keras.layers.Dense(64),
        tf.keras.layers.Dense(64),
        tf.keras.layers.Dense(128),
        tf.keras.layers.Dense(64),
        tf.keras.layers.Dense(64),
        tf.keras.layers.Dense(1)
    ])

    model.compile(optimizer='adam', loss='mean_squared_error', metrics=['mean_squared_error'])

    # Train the model
    model.fit(x, y, epochs=10)

    # Make prediction
    prediction = model.predict(np.array([16]))
    print("Prediction:", prediction)
    ```

---

## 🎯 Educational Value

This project is ideal for:
- Beginners learning **TensorFlow/Keras**
- Understanding how layers stack in neural networks
- Exploring basic regression using deep learning

---

## 🙋‍♂️ Author

**Anantha Omprakash**  
For learning and demonstration purposes.

---

## 📄 License

This project is intended for educational use only.



