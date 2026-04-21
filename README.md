# TinyVGG on Food-101 — PyTorch Project

A complete **end-to-end deep learning pipeline** built using **PyTorch**, where a TinyVGG-style CNN is trained on a custom-structured subset of the Food-101 dataset and used for real-world image inference.

---

##  Project Overview

This repository walks through the **full lifecycle of a computer vision model**:

-  Dataset downloading & structuring  
- Model building & training (TinyVGG)  
- Inference on custom images  

Built with a focus on **understanding core PyTorch concepts without abstraction layers**.

---

##  Project Structure

```
├── 06_PyTorch_Download_Custom_Dataset.ipynb
├── 07_PyTorch_Train_Tiny_VGG.ipynb
├── 08_PyTorch_Model_Inference.ipynb
├── structured_data.zip
├── tiny_vgg_model.pth
├── Ice_cream.jpg
└── README.md
```

---

##  Workflow

### 1. Dataset Preparation  
**06_PyTorch_Download_Custom_Dataset.ipynb**

- Downloads Food-101 dataset  
- Converts into PyTorch-friendly structure:
  ```
  train/
  test/
    └── class_name/
  ```
- Saves as `structured_data.zip`  

---

### 2. Model Training  
**07_PyTorch_Train_Tiny_VGG.ipynb**

- Implements TinyVGG from scratch  
- Includes:
  - Model architecture  
  - Loss & optimizer  
  - Training loop  
  - Evaluation  
- Saves trained model:
  ```
  tiny_vgg_model.pth
  ```

---

### 3. Model Inference  
**08_PyTorch_Model_Inference.ipynb**

- Loads saved model  
- Runs inference on:
  ```
  Ice_cream.jpg
  ```
- Outputs predicted class  

---

##  Model Architecture

TinyVGG (inspired by VGG):

- Conv → ReLU → Conv → ReLU → MaxPool  
- Repeated blocks  
- Fully connected classifier  

Lightweight and beginner-friendly.

---

## Example Inference

**Input:**  
`Ice_cream.jpg`

**Output:**  
```
Predicted Class: Ice Cream 
Confidence: 59%
```

---

##  Key Learnings

- Building CNNs from scratch in PyTorch  
- Structuring custom datasets  
- Writing training loops manually  
- Saving & loading models  
- Performing inference on new data  

---

##  Tech Stack

- Python  
- PyTorch  
- Torchvision  
- Matplotlib  

---

##  How to Run

```bash
git clone https://github.com/ashutosh-kedar/pytorch_cv_food_101_tiny_vgg.git
cd pytorch_cv_food_101_tiny_vgg
```

Run notebooks in order:

```
06 → 07 → 08
```

---

##  Highlights

- Pure PyTorch (no high-level frameworks)  
- Clear pipeline: Data → Training → Inference  
- Easy to understand & extend  

---

##  Notes

- Use GPU for faster training  
- You can test your own images by replacing `Ice_cream.jpg`  





