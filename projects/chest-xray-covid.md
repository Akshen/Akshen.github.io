---
layout: default
title: Chest X-Ray COVID-19 Classification
---

[← Back to Portfolio](/)

# Chest X-Ray COVID-19 Classification

![Status](https://img.shields.io/badge/Status-Completed-success)
![Research](https://img.shields.io/badge/Type-Research-blue)
![ML](https://img.shields.io/badge/ML-Deep%20Learning-orange)

**Master's Thesis Project | National College of Ireland (2021)**

## 🎯 Overview

Deep learning ensemble system for automated classification of chest X-ray images into COVID-19, pneumonia, and normal categories. This research addresses the critical need for rapid, accurate diagnostic tools during the COVID-19 pandemic.

## 📊 Problem Statement

During the COVID-19 pandemic, rapid and accurate diagnosis became crucial for:
- Efficient patient triage and resource allocation
- Reducing burden on radiologists
- Early detection and isolation of COVID-19 cases
- Managing overlapping symptoms with pneumonia

Traditional diagnosis methods were time-consuming and required expert radiologists, creating bottlenecks in healthcare systems worldwide.

## 💡 Solution

Developed an ensemble deep learning system combining multiple convolutional neural network architectures to achieve robust, accurate classification of chest X-rays.

### Key Innovation: Ensemble Approach

Instead of relying on a single model, I combined multiple architectures through:
- **Hard Voting:** Multiple models vote on the final classification
- **Soft Voting:** Weighted probability averaging across models
- **Transfer Learning:** Leveraging pre-trained models (AlexNet, ResNet variants)

## 🏗️ Architecture
```
Input: Chest X-Ray Image
       ↓
Preprocessing Pipeline:
  - Normalization
  - Histogram Equalization
  - Data Augmentation
       ↓
Ensemble Models:
  - AlexNet (Transfer Learning)
  - ResNet-18 (Transfer Learning)
  - ResNet-50 (Transfer Learning)
  - Custom CNN Architecture
       ↓
Voting Mechanism:
  - Hard Voting (Majority)
  - Soft Voting (Probability)
       ↓
Output: COVID-19 / Pneumonia / Normal
```

## 🛠️ Technical Implementation

### Preprocessing Pipeline

1. **Image Normalization:** Standardize pixel values for consistent model input
2. **Histogram Equalization:** Enhance contrast in medical images
3. **Data Augmentation:** Address class imbalance through strategic augmentation
   - Rotation, flipping, scaling
   - Brightness and contrast adjustments
   - Elastic transformations

### Model Architecture

**Base Models with Transfer Learning:**
- **AlexNet:** 8-layer deep CNN, pre-trained on ImageNet
- **ResNet-18:** 18-layer residual network with skip connections
- **ResNet-50:** Deeper 50-layer architecture for complex features
- **Custom CNN:** Task-specific architecture for medical imaging

**Ensemble Strategy:**
- Hard voting for interpretability
- Soft voting for improved accuracy
- Cross-validation for model selection

### Training Strategy

- **Dataset Split:** 70% training, 15% validation, 15% testing
- **Cross-Validation:** 5-fold stratified cross-validation
- **Class Balancing:** SMOTE and weighted loss functions
- **Optimization:** Adam optimizer with learning rate scheduling
- **Regularization:** Dropout, L2 regularization, early stopping

## 📈 Results

### Classification Performance

| Metric | COVID-19 | Pneumonia | Normal | Overall |
|--------|----------|-----------|--------|---------|
| Accuracy | 88% | 87% | 90% | **85-90%** |
| Precision | 86% | 84% | 92% | 87% |
| Recall | 89% | 86% | 88% | 88% |
| F1-Score | 87.5% | 85% | 90% | 87.5% |

### Key Achievements

✅ **Balanced performance** across all three classes (addressing class imbalance)  
✅ **High precision** minimizing false positives (critical in medical diagnosis)  
✅ **Robust generalization** through ensemble methods  
✅ **Clinically relevant** accuracy suitable for screening tools

## 🧠 Challenges & Solutions

### Challenge 1: Class Imbalance
**Problem:** Unequal distribution of COVID-19, pneumonia, and normal cases  
**Solution:** Strategic data augmentation, SMOTE oversampling, and weighted loss functions

### Challenge 2: Model Overfitting
**Problem:** High variance on small medical imaging datasets  
**Solution:** Transfer learning, aggressive regularization, and ensemble methods

### Challenge 3: Feature Extraction
**Problem:** Subtle differences between COVID-19 and pneumonia patterns  
**Solution:** Multi-scale feature extraction through ResNet architectures and ensemble voting

### Challenge 4: Computational Resources
**Problem:** Training multiple deep networks requires significant GPU resources  
**Solution:** Transfer learning reduced training time, efficient data pipelines, mixed precision training

## 🔬 Research Contributions

1. **Ensemble Methodology:** Demonstrated effectiveness of combining multiple architectures
2. **Transfer Learning Application:** Showed ImageNet pre-training benefits medical imaging
3. **Class Imbalance Solutions:** Developed strategies for balanced medical dataset classification
4. **Clinical Relevance:** Achieved accuracy suitable for real-world screening applications

## 📚 Technologies Used

**Programming & Frameworks:**
- Python 3.8
- TensorFlow 2.x / PyTorch 1.x
- Keras (high-level API)
- NumPy, Pandas for data manipulation

**Computer Vision:**
- OpenCV for image preprocessing
- PIL/Pillow for image handling
- Scikit-image for advanced transformations

**ML Tools:**
- Scikit-learn for metrics and validation
- Matplotlib/Seaborn for visualization
- TensorBoard for training monitoring

**Development:**
- Jupyter Notebooks for experimentation
- Git for version control
- Google Colab / AWS for GPU training

## 📖 Dataset

**Source:** Public COVID-19 chest X-ray datasets
- COVID-19 Radiography Database
- Kaggle COVID-19 datasets
- NIH Chest X-Ray dataset (normal cases)

**Size:** 
- COVID-19: ~1,000 images
- Pneumonia: ~1,200 images
- Normal: ~1,500 images

## 🚀 Future Work

- [ ] Integration with DICOM medical imaging standards
- [ ] Real-time inference API for clinical deployment
- [ ] Explainable AI (Grad-CAM) for interpretability
- [ ] Multi-modal learning (X-rays + clinical data)
- [ ] Federated learning for privacy-preserving training

## 📄 Publication

**Title:** Chest X-Ray COVID-19 Classification Using Ensemble Deep Learning  
**Institution:** National College of Ireland  
**Year:** 2021  
**Supervisor:** [Rashmi Gupta]

## 🔗 Resources

- [GitHub Repository](https://github.com/Akshen/NIC-Project)
- [Research Paper](https://norma.ncirl.ie/7623/)

## 💭 Reflections

This project taught me the critical importance of:
- **Medical AI ethics:** High stakes require high accuracy and interpretability
- **Domain expertise:** Collaboration with radiologists improves model design
- **Robust evaluation:** Medical applications need comprehensive testing
- **Real-world deployment:** Accuracy alone isn't enough - explainability matters

The COVID-19 pandemic highlighted the potential of AI in healthcare, but also the responsibility that comes with deploying such systems. This research reinforced my commitment to building AI solutions that are not just technically sound, but clinically relevant and ethically deployed.

---

**Questions or collaboration opportunities?** Connect with me on [LinkedIn](https://linkedin.com/in/akshen)
