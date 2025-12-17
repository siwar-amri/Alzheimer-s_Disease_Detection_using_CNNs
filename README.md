# Alzheimer’s Disease Detection using CNNs

This repository presents a deep learning approach for the automatic detection and classification of Alzheimer’s disease stages from brain MRI scans. The project explores both 2D and 3D convolutional neural networks (CNNs) to improve early diagnosis accuracy using the OASIS-1 dataset.

##  Project Overview

Alzheimer’s disease is a progressive neurodegenerative disorder where early diagnosis remains challenging. This project aims to leverage CNN-based models to classify different stages of the disease by analyzing structural MRI data.

The study compares lightweight custom models with well-known pretrained architectures and 3D volumetric networks, evaluating their performance and trade-offs in terms of accuracy, robustness, and architectural complexity.

##  Dataset

* **Dataset**: OASIS-1 (Open Access Series of Imaging Studies)
* **Modality**: T1-weighted brain MRI scans
* **Classes**:

  * Cognitively Normal
  * Very Mild Alzheimer’s Disease
  * Mild to Moderate Alzheimer’s Disease

Data preprocessing differs for 2D and 3D models:

* **2D CNNs**: MRI volumes are sliced into informative axial views, resized, and augmented.
* **3D CNNs**: Volumetric data is preprocessed using Clinica, with a focus on the right hippocampus.

##  Models Implemented

### 2D CNN Models

* BrainNet2D (custom lightweight CNN)
* VGG16
* DenseNet121
* InceptionV3

### 3D CNN Models

* BrainNet3D (baseline and modified versions)
* 3D ResNet
* 3D DenseNet

Hybrid and deeper architectures are explored to capture subtle structural changes in early-stage Alzheimer’s disease.

##  Evaluation Metrics

Models are evaluated using:

* Accuracy
* Balanced Accuracy
* Sensitivity (Recall)
* Specificity
* ROC-AUC (One-vs-Rest)
* Confusion Matrices

These metrics provide a balanced assessment, especially in the presence of class imbalance.

##  Key Results

* Pretrained 2D CNNs (especially **DenseNet121** and **VGG16**) outperform lightweight custom models.
* 3D CNNs demonstrate strong potential in capturing volumetric patterns, particularly in moderate stages.
* Early-stage (very mild) Alzheimer’s remains the most challenging to classify due to subtle MRI changes.

##  Future Work

* Explore hybrid CNN architectures combining lightweight and pretrained models
* Integrate CNN-LSTM models for sequential slice learning
* Apply self-supervised or multimodal learning approaches
* Validate models on larger and more diverse datasets

##  Tools & Technologies

* Python
* PyTorch / TensorFlow
* Google Colab
* Clinica (neuroimaging preprocessing)
* NumPy, OpenCV, Scikit-learn

##  References

* OASIS Dataset
* BrainNet2D / BrainNet3D
* ResNet, DenseNet, VGG architectures

##  Authors

* **Amri Siwar**
* **Ellefi Alaa**

##  License

This project is intended for academic and research purposes only.
