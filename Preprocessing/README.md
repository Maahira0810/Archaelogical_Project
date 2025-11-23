---

# 🌱 Dataset Preprocessing Pipeline – Soil Detection & Vegetation Segmentation

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Ready-orange?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-Enabled-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)
![Preprocessing](https://img.shields.io/badge/Preprocessing-Automated-purple?style=flat-square)

---

## 📌 Overview

This repository contains a complete preprocessing pipeline used for two computer vision datasets:

* **Soil Detection**
* **Vegetation Segmentation**

The workflow is executed in **Google Colab** and includes color enhancement, augmentation, normalization, resizing, and strong error handling.

The goal is to prepare high-quality, consistent images for training deep learning models such as **YOLO**.

---

## 📊 1. Exploratory Data Analysis (EDA)

Before preprocessing, the pipeline performs light EDA:

* Displays **5 random images**
* Verifies image shape and file count
* Observes color, lighting, and contrast
* Checks dataset quality and consistency

Example used:

```python
sample_imgs = random.sample(os.listdir(img_folder), 5)
```

EDA helps ensure the raw dataset is visually understood before applying transformations.

---

## ⚙️ 2. Preprocessing Pipeline

Each image undergoes the following steps:

### 🔧 **Color Enhancements**

* **Histogram Equalization** to improve contrast
* **Random Brightness Adjustment** (safe from overflow)
* **Sharpening Filter** to highlight texture and edges

### 🔁 **Augmentation**

* Random Horizontal Flip
* Random Rotation
  Adds variability to improve model generalization.

### 📐 **Standardization**

* Uniform resizing
* Pixel normalization to **0–1** range

These ensure compatibility with YOLO training requirements.

---

## 🛡 3. Error Handling & Safety

The pipeline is designed to be *fully robust*:

* Skips unreadable/corrupt images
* Supports multiple extensions:
  `.jpg`, `.jpeg`, `.png`, uppercase variations
* Uses `try/except` so errors do not interrupt execution
* Avoids NumPy overflow issues

This ensures smooth preprocessing for large datasets.

---

## 🚀 4. Google Colab Execution

The entire workflow runs seamlessly in **Google Colab**:

* Execute cells in sequence
* Processed images appear instantly in the file explorer
* No manual file organization required

The process is automated from start to finish.

---

## ⭐ 5. Benefits of This Preprocessing

This pipeline ensures:

* Cleaner and sharper images
* More balanced brightness and contrast
* Augmented dataset diversity
* Smaller risk of model overfitting
* Consistent input dimensions
* Stable training performance

It is ideal for object detection, segmentation, and classification tasks.

---

## 📚 6. Future Enhancements

Planned upgrades:

* CLAHE (Adaptive Histogram Equalization)
* Gamma correction
* Hue/Saturation/Color jittering
* Adding Gaussian blur augmentation
* Multiple augmentation variants per image
* tqdm progress bar for visual execution tracking

---

## 📌 Summary

This preprocessing pipeline standardizes and enhances two visually different datasets — soil textures and vegetation — into high-quality, model-ready inputs suitable for deep learning workflows.

---

Just let me know!

