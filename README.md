# Forest Fire Prediction Using Machine Learning Techniques and Background Subtraction

## Overview

Forest fires pose a significant threat to ecosystems, wildlife habitats, and human communities. Early detection of forest fires is essential to minimize environmental damage and reduce economic losses. This project presents a system for forest fire prediction using supervised machine learning techniques and background subtraction-based video analysis.

The system uses environmental and observational data to predict the likelihood of forest fires and applies image processing techniques to detect fire from video sequences.

---

# Abstract

Image processing is a powerful tool for improving both machine and human interpretation and extracting information from images for classification tasks. Forest fire detection is an important aspect of ecosystem conservation and climate change management. Fires can cause significant loss of trees and drastically increase CO₂ levels in the atmosphere.

To minimize these losses, it is important to detect forest fires quickly and accurately. This project proposes a solution using machine learning algorithms and background subtraction techniques to detect forest fires efficiently.

The system analyzes image sequences extracted from input videos and applies image processing operations to detect the presence of fire. By analyzing color patterns and motion in pixels, the system identifies changes that indicate fire occurrence and alerts relevant authorities.

---

# Technologies and Concepts Used

## Machine Learning Techniques

The following supervised machine learning models were implemented:

* Logistic Regression
* Naive Bayes
* Support Vector Machine (SVM)
* K Nearest Neighbours (KNN)
* Decision Tree
* XGBoost

These algorithms were trained and tested using different train-test ratios to evaluate prediction accuracy.

---

# Dataset

The dataset used in this project contains **13 attributes** representing environmental factors related to forest fire conditions. Data preprocessing was performed before training the machine learning models.

The dataset was split into training and testing sets using different ratios:

* 50 : 50
* 66 : 34
* 70 : 30
* 80 : 20

---

# Model Accuracy Results

| Model               | Train/Test Split | Accuracy |
| ------------------- | ---------------- | -------- |
| Logistic Regression | 50:50            | 55.21%   |
| Logistic Regression | 66:34            | 52.84%   |
| Logistic Regression | 70:30            | 51.28%   |
| Logistic Regression | 80:20            | 50.00%   |
| Naive Bayes         | 50:50            | 53.67%   |
| Naive Bayes         | 66:34            | 50.00%   |
| Naive Bayes         | 70:30            | 50.64%   |
| Naive Bayes         | 80:20            | 47.12%   |
| SVM                 | 50:50            | 54.83%   |
| SVM                 | 66:34            | 52.27%   |
| SVM                 | 70:30            | 50.64%   |
| SVM                 | 80:20            | 46.15%   |
| KNN                 | 50:50            | 50.97%   |
| KNN                 | 66:34            | 52.84%   |
| KNN                 | 70:30            | 50.00%   |
| KNN                 | 80:20            | 44.23%   |
| Decision Tree       | 50:50            | 52.51%   |
| Decision Tree       | 66:34            | 54.55%   |
| Decision Tree       | 70:30            | 52.56%   |
| Decision Tree       | 80:20            | 56.73%   |
| XGBoost             | 50:50            | 53.28%   |
| XGBoost             | 66:34            | 52.84%   |
| XGBoost             | 70:30            | 54.49%   |
| XGBoost             | 80:20            | 57.69%   |

Among all the models tested, **Decision Tree and XGBoost achieved the best performance**.

---

# Forest Fire Detection from Video

## Background Subtraction

Background subtraction is a computer vision technique used to separate foreground objects from the background in video sequences. The system compares current frames with reference background frames to detect motion or unusual changes in the scene.

This technique helps identify smoke or flames by detecting differences between frames.

---

## Motion Detection

Motion detection identifies moving objects in the video by comparing consecutive frames. Pixels that change between frames are considered moving objects and are analyzed further to determine whether they represent fire or smoke.

---

## Masking

Masking is used to isolate regions of interest in an image. It helps remove irrelevant areas such as roads or buildings and focuses on forest areas to improve detection accuracy.

---

## FGMask (Foreground Mask)

FGMask is a binary mask used to identify foreground objects in a video frame. It highlights regions that differ from the background and may represent fire or smoke.

---

## Gaussian Blur

Gaussian blur is applied to smooth images and reduce noise before further processing. This improves the accuracy of fire detection by enhancing the contrast between foreground objects and background.

---

## Threshold Erode Dilute

This process compares the brightness of smoke with surrounding clouds or background elements. If the smoke brightness exceeds a threshold, it is detected as fire.

The process includes:

* Image erosion
* Brightness adjustment
* Threshold comparison

This reduces false alarms caused by clouds or lighting changes.

---

# Results

The system successfully processes video frames and produces binary masks highlighting fire regions. The final output video clearly identifies fire locations and motion patterns associated with flames and smoke.

---

# Conclusion

Forest fire detection systems play a crucial role in preventing environmental damage and protecting human lives. Early detection allows firefighters and authorities to respond quickly and control fires before they spread extensively.

Machine learning models combined with image processing techniques provide an efficient method for detecting and predicting forest fires.

---

# Future Work

The project can be extended to include:

* Real-time fire detection systems
* Integration with satellite monitoring systems
* Detection of suspicious activities in forest areas
* Improved deep learning models for higher accuracy

---

# References

1. Mahmoud, M. A. I., & Ren, H. (2019). Forest fire detection and identification using image processing and SVM.
2. Töreyin, B. U., et al. Computer vision based method for real-time fire detection.
3. Xu, R., et al. A Forest Fire Detection System Based on Ensemble Learning.
4. Barmpoutis, P., et al. Review on Early Forest Fire Detection Systems Using Optical Remote Sensing.
5. Vipin, V. Image processing based forest fire detection.
