# palmprint-recognition-contactless
A palmprint biometric recognition project based on the SYEnet CNN architecture, implemented with PyTorch.

The project focuses on palm region preprocessing, feature extraction, and few-shot palmprint recognition.

---

## Overview

Palmprint recognition is a biometric identification technique that uses distinctive patterns and structural features of the human palm.

This project implements a complete recognition pipeline including:

- Palm image preprocessing
- Hand segmentation and alignment
- Palm ROI extraction
- Multi-patch feature extraction
- CNN-based feature learning
- Feature embedding generation
- Few-shot recognition using Collaborative Representation Classification (CRC)

---

## Preprocessing Pipeline

The input palm image is processed to extract the Region of Interest (ROI).  
The ROI is then divided into nine overlapping patches before being passed to the CNN.

Base
<img width="1245" height="230" alt="image" src="https://github.com/user-attachments/assets/a0ce254e-bb87-44da-8826-0eb3fe119daa" />

ROI Extract
<img width="1194" height="259" alt="image" src="https://github.com/user-attachments/assets/8979d914-ab09-46d6-8cfc-fcec11bb525b" />

---

## Model

The recognition model is based on the SYEnet CNN architecture.

The network processes palm patches and generates an 84-dimensional feature embedding used to represent the biometric characteristics of each palm.

These embeddings can then be used for palmprint identification and few-shot recognition.

Patches
<img width="882" height="642" alt="image" src="https://github.com/user-attachments/assets/b36c0f70-40a7-4d79-a510-640126497d1c" />

---

## Technologies

- Python
- PyTorch
- OpenCV
- NumPy
- Pandas
- Scikit-learn
- Pillow

---

## Dataset

The project supports two public palmprint datasets:

### CASIA Palmprint Dataset

CASIA contains original palm images that require preprocessing and ROI extraction before being passed to the recognition model.

### Tongji Palmprint Dataset

Tongji provides palm ROI images that can be directly processed by the feature extraction pipeline.

> Dataset files are not included in this repository.  
> Users should download the datasets separately and update the dataset paths in the notebook configuration.

---

## Project Structure

```text
syenet-palmprint-recognition/
│
├── SYEnet_Palmprint_Recognition_GitHub.ipynb
├── README.md
├── .gitignore
│
├── assets/
│   └── roi_pipeline.png
│
└── data/
    ├── CASIA/
    └── Tongji/
