# Face Recognition Project

## Overview

This repository contains a face recognition pipeline developed in April 2023 as a university project. It includes two Jupyter notebooks:

- **`CNN.ipynb`**: Implements a Convolutional Neural Network (CNN)–based classifier for face recognition.
- **`SVM.ipynb`**: Implements a Support Vector Machine (SVM)–based classifier for face recognition.

Both notebooks share the following workflow:

1. **Dataset extraction**: Unzip `data.zip` into `data/`.
2. **Face detection**: Use OpenCV’s Haar Cascade to locate and crop faces from images.
3. **Preprocessing**: Resize and normalize face patches.
4. **Feature extraction**:
   - For the CNN notebook: prepare torch `Dataset` and `DataLoader`.
   - For the SVM notebook: flatten extracted face patches into feature vectors.
5. **Model training**:
   - **CNN**: Train a simple CNN architecture with PyTorch.
   - **SVM**: Train an SVM classifier with scikit-learn.
6. **Evaluation**: Report accuracy on held-out test data.
7. **Inference**: Code snippets demonstrate how to predict a face class on a new image.

## Project Structure

```text
/
├── data.zip               # Zipped dataset of labeled face images
├── data/                  # (After extraction) directory with subfolders per subject
│   ├── subject1/
│   │   ├── img1.jpg
│   │   ├── img2.jpg
│   │   └── ...
│   ├── subject2/
│   │   ├── img1.jpg
│   │   └── ...
│   └── ...
├── CNN.ipynb         # Jupyter notebook for CNN-based training & evaluation
├── SVM.ipynb          # Jupyter notebook for SVM-based training & evaluation
```
