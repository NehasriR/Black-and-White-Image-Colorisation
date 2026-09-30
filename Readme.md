# Black-and-White Image Colorization using U-Net

## 📌 Project Overview

Black-and-white images contain only intensity information and do not contain color information. This project uses a **deep learning-based U-Net model** to automatically add colors to grayscale images.

The model is trained using the **CIFAR-10 dataset**. RGB images are converted into the **LAB color space**, where the **L channel represents lightness** and the **A and B channels represent color information**.

The U-Net model takes the L channel as input and learns to predict the A and B channels. The predicted color channels are then combined with the L channel to generate the final colorized image.

---

## 🎯 Objectives

- Automatically colorize black-and-white images.
- Use deep learning for image-to-image translation.
- Understand the LAB color space for image colorization.
- Implement a lightweight U-Net architecture.
- Predict color information from grayscale information.
- Generate a colorized RGB image from a grayscale input.

---

## 🧠 Technologies Used

- Python
- Google Colab
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib
- U-Net
- CIFAR-10 Dataset

---

## 🏗️ Model Architecture

The project uses a **lightweight U-Net architecture** consisting of:

- Encoder
- Bottleneck
- Decoder
- Skip connections

### Model Flow

```text
Black-and-White Image
        ↓
   L Channel
        ↓
   U-Net Model
        ↓
Predicted A + B Channels
        ↓
Combine L + A + B
        ↓
    LAB → RGB
        ↓
Colorized Image
