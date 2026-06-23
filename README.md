# 🧠 Brain Tumor Detection using Deep Learning

A Deep Learning-based Brain Tumor Detection system built using **Python**, **TensorFlow**, and **Keras**. This project uses a **Convolutional Neural Network (CNN)** to classify MRI brain scan images and determine whether a tumor is present or not.

The model leverages **real-time image augmentation**, **Dropout regularization**, and **binary classification** to achieve reliable performance while reducing overfitting.

---

## 🚀 Features

* MRI-based Brain Tumor Detection
* Custom CNN Architecture
* Binary Classification (`Yes` / `No`)
* Real-time Data Augmentation
* Dropout Regularization for Better Generalization
* Easy-to-use Jupyter Notebook Implementation
* Prediction on Custom MRI Images

---

## 📂 Repository Structure

Ensure your project directory is organized as follows:

```text
brain-tumor-detection/
│
├── train/
│   ├── yes/                 # Training images with tumors
│   └── no/                  # Training images without tumors
│
├── test/
│   ├── yes/                 # Validation images with tumors
│   └── no/                  # Validation images without tumors
│
├── prediction/
│   └── yes3.jpg             # Image used for final prediction
│
├── brain_tumor_detection.ipynb
└── README.md
```

---

## 🧠 Model Architecture

The CNN processes MRI images resized to **224 × 224 RGB** format.

### Architecture Overview

1. **Conv2D**

   * Filters: 224
   * Kernel Size: 3×3
   * Activation: ReLU

2. **MaxPooling2D**

   * Pool Size: 2×2
   * Stride: 2

3. **Conv2D**

   * Filters: 224
   * Kernel Size: 3×3
   * Activation: ReLU

4. **MaxPooling2D**

   * Pool Size: 2×2
   * Stride: 2

5. **Dropout**

   * Rate: 0.5

6. **Flatten**

7. **Dense Layer**

   * Units: 128
   * Activation: ReLU

8. **Output Layer**

   * Units: 1
   * Activation: Sigmoid

### Training Configuration

| Parameter           | Value               |
| ------------------- | ------------------- |
| Optimizer           | Adam                |
| Loss Function       | Binary Crossentropy |
| Epochs              | 10                  |
| Image Size          | 224 × 224           |
| Classification Type | Binary              |

---

## ⚙️ Installation

### Prerequisites

* Python 3.x
* Jupyter Notebook / Google Colab

### Install Required Libraries

```bash
pip install numpy tensorflow keras
```

---

## 📊 Dataset

The dataset should contain MRI brain scan images divided into two classes:

* **yes** → Brain Tumor Present
* **no** → No Brain Tumor

Place the images inside the appropriate folders shown in the repository structure.

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/brain-tumor-detection.git
cd brain-tumor-detection
```

### 2. Prepare Dataset

Populate the following directories with MRI images:

```text
train/yes
train/no
test/yes
test/no
```

### 3. Open the Notebook

Launch:

```bash
jupyter notebook
```

Open:

```text
brain_tumor_detection.ipynb
```

### 4. Train the Model

Run all notebook cells sequentially.

The model will train for **10 epochs** using the training dataset.

### 5. Make Predictions

Place a test MRI image inside:

```text
prediction/
```

Update the image path if required and run the final prediction cell.

The model outputs:

```text
yes
```

or

```text
no
```

depending on whether a brain tumor is detected.

---

## 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Jupyter Notebook

---

## 📈 Future Improvements

* Increase dataset size for improved accuracy
* Implement Transfer Learning (VGG16, ResNet50)
* Deploy using Streamlit or Flask
* Add Grad-CAM visualization for model interpretability
* Support multi-class tumor classification

---

## 👨‍💻 Author

**Dipak Choudhary**

B.Tech CSE Student
Passionate about Artificial Intelligence, Machine Learning, and Deep Learning.

---

## ⭐ Support

If you found this project useful, consider giving the repository a ⭐ on GitHub.
