# Lightweight CNN for Dog Cardiomegaly Detection

This repository contains the implementation of a lightweight and efficient Convolutional Neural Network (CNN) for detecting dog cardiomegaly (heart enlargement) from X-ray images. The model, referred to as **DCNN**, is designed to balance accuracy, computational efficiency, and interpretability, making it ideal for real-time deployment in resource-constrained environments, such as veterinary clinics.

---

## **Table of Contents**
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training Details](#training-details)
- [Results](#results)
- [Paper](#paper)

---

## **Introduction**
Cardiac disease is one of the leading causes of death in dogs, with cardiomegaly being a critical condition requiring early detection. Traditional methods, such as the Vertebral Heart Scale (VHS), are manual and prone to error. This project presents a lightweight CNN model to automate cardiomegaly detection from X-ray images, offering a practical, real-time diagnostic solution.

---

## **Dataset**
The dataset used consists of lateral X-ray images of dog hearts categorized into three classes:
- **Small hearts**: VHS < 8.2
- **Normal hearts**: 8.2 ≤ VHS ≤ 10.0
- **Large hearts**: VHS > 10.0

**Citation for Dataset**: Dharani Goalla. *Dog Cardiomegaly Detection Using a Simplified CNN Architecture*. [ResearchGate](https://www.researchgate.net/publication/382109652), 2024.

---

## **Model Architecture**
The **DCNN** architecture consists of:
- Convolutional layers with a $7 \times 7$ kernel.
- Three stages of residual blocks with increasing filter sizes.
- Global average pooling, dropout, and a fully connected layer for classification.

The model is lightweight, making it suitable for deployment on devices with limited computational resources.

---

## **Training Details**
- **Optimizer**: Adam
- **Learning Rate**: 0.001
- **Batch Size**: 32
- **Epochs**: 50
- **Hardware**: NVIDIA GPU

---

## **Results**
The DCNN model achieved the following results:
- **Test Accuracy**: 71.5%
- **Inference Efficiency**: Faster than traditional models (e.g., VGG16, RVT).
- **Model Size**: Compact and deployable in real-world scenarios.

| Model   | Test Accuracy (%) | Inference Time | Model Size   |
|---------|--------------------|----------------|--------------|
| DCNN    | 71.5              | Fast           | Compact      |
| VGG16   | 75.0              | Moderate       | Large        |
| RVT     | 85.0              | Slow           | Very Large   |

---

## **Paper**
https://www.researchgate.net/publication/386021250_Lightweight_CNN_for_Dog_Cardiomegaly_Detection

---

## **Contributions**
Feel free to submit issues or pull requests if you'd like to contribute to this project!

---

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.
