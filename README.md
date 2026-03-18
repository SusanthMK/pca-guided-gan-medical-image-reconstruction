![Python](https://img.shields.io/badge/Python-3.x-blue)
![AI](https://img.shields.io/badge/AI-GAN-red)
![Model](https://img.shields.io/badge/Model-PCA%20%2B%20GAN-orange)
![Medical](https://img.shields.io/badge/Domain-Medical%20Imaging-green)
![Metrics](https://img.shields.io/badge/Metrics-PSNR%20%7C%20SSIM-yellow)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

A PCA-guided generative framework for reconstructing incomplete MRI images using GAN-based feature refinement and inverse PCA reconstruction.

# PCA-Guided Multimodal GAN for MRI Image Reconstruction

---

## Overview

This project presents a deep learning-based framework for reconstructing incomplete or corrupted MRI images using a hybrid approach that combines **Principal Component Analysis (PCA)** and **Generative Adversarial Networks (GANs)**.

MRI images often suffer from missing modalities, motion artifacts, and acquisition limitations. Traditional reconstruction techniques fail to recover fine anatomical structures and cannot effectively utilize multimodal relationships.

To address this, the proposed system integrates:

* PCA for dimensionality reduction and feature extraction
* GAN (Generative AI) for feature refinement and reconstruction
* Inverse PCA for restoring high-quality MRI images

---

## Problem Statement

MRI datasets frequently contain missing or corrupted data due to:

* Motion artifacts
* Incomplete acquisition
* Hardware limitations

Existing methods:

* Fail to preserve anatomical accuracy
* Cannot handle multimodal dependencies effectively
* May generate unrealistic outputs

This motivates the need for a **reliable and anatomically consistent reconstruction framework**.

---

## Architecture

**PCA → GAN (Generative AI) → Inverse PCA**

### PCA (Feature Extraction)

* Reduces dimensionality while preserving variance
* Extracts important structural information

### GAN (Feature Refinement)

* Generator reconstructs missing or corrupted regions
* Discriminator enforces realism
* Learns complex non-linear anatomical structures

### Inverse PCA (Reconstruction)

* Maps refined features back to image space
* Produces final reconstructed MRI

---

## Dataset

The model is trained using **Brain MRI datasets (BraTS 2021)** 

### Dataset Details

* Multimodal MRI scans:

  * T1
  * T1-contrast (T1ce)
  * T2
  * FLAIR

* Data characteristics:

  * Collected from multiple hospitals and MRI scanners
  * Expert-annotated for clinical reliability
  * Provided in **NIfTI format**

### Preprocessing Steps

* Image normalization
* Resizing to standard resolution
* Skull stripping
* Noise removal

### Why Multimodal Data?

Each modality provides complementary information:

* T1 → anatomical structure
* T2 → fluid detection
* FLAIR → lesion highlighting

---

## Methodology

1. MRI data collection from standard datasets
2. Data preprocessing and normalization
3. Simulation of missing or corrupted regions
4. PCA-based feature extraction
5. GAN training (Generator + Discriminator)
6. Feature refinement using GAN
7. Inverse PCA reconstruction
8. Evaluation using PSNR and SSIM

---

## Evaluation Metrics

* **PSNR (Peak Signal-to-Noise Ratio)**
  Measures reconstruction quality

* **SSIM (Structural Similarity Index)**
  Measures structural similarity and perceptual quality

---

## Results

The model demonstrates:

* High PSNR values (low reconstruction error)
* High SSIM values (strong structural preservation)
* Accurate reconstruction of missing MRI regions

### Outputs

* MRI reconstruction images
* Error heatmaps
* PSNR distribution
* SSIM distribution
* Reconstruction error per image

---

## Repository Structure

```plaintext
project/
│
├── MRI_Reconstruction_Code.ipynb
│
├── results/
│   ├── MRI_RECON.png
│   ├── Output.png
│   ├── HeatMap.png
│   ├── RE_per_image.png
│   ├── PSNR_Distribution.png
│   ├── SSIM_Distribution.png
│   └── Accuracy(PSNR&SSIM).png
│
└── README.md
```

---

## Technologies Used

* Python
* NumPy
* Scikit-learn (PCA)
* TensorFlow / PyTorch
* Matplotlib

---

## Key Contributions

* Hybrid PCA + GAN framework for MRI reconstruction
* Integration of statistical and deep learning approaches
* Improved reconstruction accuracy for incomplete MRI data
* Quantitative validation using PSNR and SSIM

---

## Applications

* Medical image reconstruction
* Radiology and diagnostics
* Clinical decision support systems
* AI-assisted healthcare

---

## Conclusion

This project presents a reliable and efficient framework for reconstructing incomplete MRI images using a combination of PCA and GAN-based learning.

By integrating dimensionality reduction with generative AI, the system achieves:

* High-quality reconstruction
* Preservation of anatomical structures
* Improved robustness over traditional methods

---
