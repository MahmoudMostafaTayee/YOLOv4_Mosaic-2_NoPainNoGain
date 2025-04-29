# YOLOv4 Mask Detection

This repository demonstrates the implementation of **YOLOv4** (You Only Look Once) for detecting people wearing masks versus those without. This work was done using **Google Colab** with **GPU** enabled for fast training and real-time inference.

![Mask Detection Demo](https://github.com/MahmoudMostafaTayee/YoloV4/blob/main/Mask%20vs%20No%20mask.gif)

## 🧠 Overview

**YOLOv4** is an advanced object detection algorithm based on **Convolutional Neural Networks (CNN)**. This model operates in real-time, making it suitable for applications like surveillance, security, and public health monitoring.

The system is trained using a custom dataset that includes labeled mask-wearing and non-mask-wearing individuals, and the training process is optimized using **batch size** and **data augmentation** techniques.

### 🔍 Key Contributions:
- **Batch Size Optimization**: Explores the effect of batch size on model training. Smaller batch sizes (e.g., 32) provided better training results than the original YOLOv4 configuration (batch size 64).
- **Mosaic2 Data Augmentation**: Enhances YOLOv4's data augmentation by applying the mosaic technique twice (Mosaic2). This results in better model generalization, as it introduces more diverse object scenarios, including smaller objects and partial object views, simulating real-world conditions.

![YOLOv4 vs Other Models](https://github.com/MahmoudMostafaTayee/YoloV4/blob/main/Comparison%20of%20the%20proposed%20YOLOv4%20and%20other%20SOTA%20ODs.png)

## 📚 Methodology

The following methodology was used in this project:

### A. **Batch Size Optimization**
The batch size plays an important role in the performance of deep learning models. We experimented with different batch sizes to optimize training:
- **Batch Size 32** outperformed the default **Batch Size 64** used in YOLOv4, providing better accuracy and reduced inference cost.

### B. **Mosaic2 Data Augmentation**
The **Mosaic2** technique is an extension of the original mosaic used in YOLOv4. By applying mosaic twice (instead of once), we achieved:
- **More challenging and generalizable images**: The model is trained on more complex and varied images, improving its ability to detect objects in different conditions.
- **Better detection of small objects and partial objects**: The model became more robust by learning to detect even partially visible objects (e.g., faces with masks, partially cropped objects).
- **Handling diverse poses**: The enhanced mosaic augmentation allowed the model to better handle unusual poses and angles, common in surveillance scenarios.

## 📊 Dataset

The dataset used for training can be found on Kaggle:
- [Labeled Mask Dataset - YOLO Darknet](https://www.kaggle.com/datasets/techzizou/labeled-mask-dataset-yolo-darknet)

For further reading, refer to the official **YOLOv4** paper:
- [YOLOv4: Optimal Speed and Accuracy of Object Detection](https://arxiv.org/pdf/2004.10934.pdf)

## 🖥️ Setup & Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/MahmoudMostafaTayee/YoloV4.git
    ```
2. Follow the instructions in the **Google Colab Notebook** to set up and train the model with GPU acceleration enabled.
3. Ensure you have **TensorFlow** and **OpenCV** installed for testing and inference.

## 📹 Demo

For a demonstration of the model in action, you can watch the demo video here:
- [🔗 Watch Demo](https://nileuniversity-my.sharepoint.com/:v:/g/personal/mamostafa_nu_edu_eg/EUmxBzr0ThpMkBM9sn7TTzsBpVeDA_SGMLlk-X8_MAWu6Q?e=ghdJTa)

---

## 📜 References
- [YOLOv4: Optimal Speed and Accuracy of Object Detection (Paper)](https://arxiv.org/pdf/2004.10934.pdf)
