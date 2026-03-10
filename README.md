# MNIST Handwritten Digit Classification using Dense Neural Network

## 📌 Project Overview

This project implements a **Dense Neural Network (Fully Connected Neural Network)** to classify handwritten digits from the **MNIST dataset**.

The goal of this project is to understand the fundamentals of neural networks including:

* Data preprocessing
* Neural network architecture design
* Regularization techniques
* Model training and evaluation
* Bias–Variance analysis
* Prediction visualization

The model takes **28×28 grayscale images of handwritten digits (0–9)** and predicts the correct digit class.

---

## 📊 Dataset

This project uses the **MNIST dataset**, which contains images of handwritten digits.

Dataset characteristics:

* **70,000 images total**
* **60,000 training images**
* **10,000 testing images**
* Image size: **28 × 28 pixels**
* Classes: **Digits 0–9**

Each image is grayscale and represented as pixel values ranging from **0 to 255**.

---

## ⚙️ Data Preprocessing

Before training the neural network, the following preprocessing steps were applied:

1. **Normalization**

Pixel values were scaled from:

```
0–255 → 0–1
```

This helps neural networks train faster and more efficiently.

2. **Flattening Images**

Each image:

```
28 × 28
```

was converted into a **784-dimensional vector**:

```
28 × 28 → 784
```

This is required because Dense layers expect **1D input vectors**.

3. **Train / Validation Split**

The training data was split into:

* **Training Set**
* **Validation Set**

This allows monitoring of model generalization during training.

---

## 🧠 Model Architecture

The neural network is implemented using **TensorFlow / Keras**.

Architecture:

```
Input Layer: 784 neurons (flattened image)

Hidden Layer 1
Dense(25 units, ReLU activation)
L2 Regularization

Hidden Layer 2
Dense(15 units, ReLU activation)
L2 Regularization

Output Layer
Dense(10 units, Softmax activation)
```

Explanation:

* **ReLU Activation** introduces non-linearity.
* **L2 Regularization** helps reduce overfitting by penalizing large weights.
* **Softmax** outputs probability distribution over the 10 digit classes.

---

## 📈 Model Training

The model was trained using:

* **Optimizer:** Adam
* **Loss Function:** Sparse Categorical Crossentropy
* **Batch Size:** 32
* **Epochs:** 50

Training and validation accuracy were monitored during the training process.

---

## 📊 Results

Final performance on the test dataset:

**Test Accuracy:**

```
96.6%
```

This indicates that the neural network correctly classifies most handwritten digits.

---

## 🔍 Bias–Variance Analysis

Model performance was analyzed using training and validation accuracy.

| Metric              | Observation                |
| ------------------- | -------------------------- |
| Training Accuracy   | High                       |
| Validation Accuracy | Close to training accuracy |

This indicates **good generalization** with minimal overfitting.

L2 regularization helped prevent large weights and reduced model variance.

---

## 📉 Error Analysis

Misclassified examples were analyzed to understand model limitations.

Common confusions include:

* **Digit 4 vs 9**
* **Digit 3 vs 5**
* **Digit 7 vs 1**

These errors occur due to visual similarity in handwritten digits.

---

## 🛠 Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Scikit-learn
* Google Colab

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository

```
git clone https://github.com/mohdrizwan11/mnist-dense-neural-network.git
```

### 2️⃣ Install Dependencies

```
pip install -r requirements.txt
```

### 3️⃣ Run the Notebook

Open the notebook:

```
mnist_dense_model.ipynb
```

You can run it locally or in **Google Colab**.

---

## 📌 Future Improvements

Possible extensions for this project:

* Implement **Convolutional Neural Networks (CNN)** for improved accuracy
* Add **Dropout Regularization**
* Build **interactive prediction visualization**
* Deploy the model as a **web application**

---

## 📚 Learning Outcome

This project helped build a strong understanding of:

* Neural network fundamentals
* Model training workflow
* Regularization techniques
* Bias–variance tradeoff
* Model evaluation and diagnostics

---

## 👨‍💻 Author

**K Mohammad Rizwan**

GitHub:
https://github.com/mohdrizwan11

LinkedIn:
https://www.linkedin.com/in/mohdrizwan11/
