![Python](https://img.shields.io/badge/Python-3.x-blue)
![AI](https://img.shields.io/badge/AI-GAN-red)
![Model](https://img.shields.io/badge/Model-PCA%20%2B%20GAN-orange)
![Medical](https://img.shields.io/badge/Domain-Medical%20Imaging-green)
![Metrics](https://img.shields.io/badge/Metrics-PSNR%20%7C%20SSIM-yellow)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

A PCA-guided generative framework for reconstructing incomplete MRI images using GAN-based feature refinement and inverse PCA reconstruction.

# PCA-Guided Multimodal GAN for MRI Image Reconstruction

## Overview

This project presents a robust deep learning framework for reconstructing incomplete or corrupted Magnetic Resonance Imaging (MRI) data using a hybrid approach that combines **Principal Component Analysis (PCA)** and **Generative Adversarial Networks (GANs)**.

MRI scans often suffer from missing modalities, motion artifacts, or acquisition limitations, which can reduce diagnostic reliability. Traditional reconstruction techniques fail to capture complex anatomical structures, especially under severe corruption.

To address this, the proposed system leverages:

* PCA for efficient feature extraction and dimensionality reduction
* GANs as a generative AI component for refining latent representations
* Inverse PCA for reconstructing high-quality MRI images

---

## Problem Statement

MRI datasets frequently contain incomplete or degraded information due to:

* Motion artifacts
* Hardware limitations
* Incomplete acquisition

Existing reconstruction methods:

* Fail to preserve fine anatomical details
* Cannot effectively utilize multimodal relationships
* May produce unrealistic outputs (in case of standard GANs)

This creates a need for a **reliable and anatomically consistent reconstruction framework**.

---

## Proposed Approach

The model follows a structured pipeline:

**PCA → GAN (Generative AI) → Inverse PCA**

### 1. PCA (Feature Extraction)

* Reduces high-dimensional MRI data
* Retains maximum variance
* Removes redundancy and noise

### 2. GAN (Feature Refinement)

* Generator reconstructs missing or corrupted regions
* Discriminator enforces realism
* Learns non-linear anatomical structures

### 3. Inverse PCA (Reconstruction)

* Maps refined latent features back to image space
* Produces final reconstructed MRI images

---

## Dataset

The model is trained on brain MRI datasets containing multimodal scans such as:

* T1
* T2
* FLAIR

The data is:

* Preprocessed (normalized, resized, skull-stripped)
* Structured for deep learning applications

---

## Methodology

1. MRI data collection from standard datasets
2. Data preprocessing (normalization, resizing, noise removal)
3. Simulation of missing or corrupted regions
4. PCA-based feature extraction
5. GAN training (Generator + Discriminator)
6. Reconstruction using refined latent features
7. Inverse PCA transformation
8. Performance evaluation using quantitative metrics

---

## Evaluation Metrics

The model performance is evaluated using:

* **PSNR (Peak Signal-to-Noise Ratio)**
  Measures reconstruction quality

* **SSIM (Structural Similarity Index)**
  Measures structural similarity with ground truth

These metrics ensure both **visual quality and anatomical consistency**.

---

## Results

The model demonstrates strong reconstruction performance:

* High PSNR values indicating low reconstruction error
* High SSIM values indicating preserved structural integrity
* Accurate reconstruction of missing MRI regions

### Visual Outputs

* Reconstructed MRI images
* Error heatmaps
* PSNR and SSIM distributions
* Reconstruction error analysis

---

## Repository Structure

```plaintext
project/
│
├── MRI_Reconstruction_Code.ipynb   # Model implementation
├── results/                        # Output visualizations
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

* Hybrid PCA + GAN architecture for medical image reconstruction
* Integration of dimensionality reduction with generative modeling
* Improved reconstruction quality for incomplete MRI data
* Quantitative evaluation using PSNR and SSIM

---

## Applications

* Medical image reconstruction
* Clinical decision support systems
* Radiology and diagnostic imaging
* AI-assisted healthcare systems

---

## Conclusion

This project presents a reliable and efficient framework for reconstructing incomplete MRI data using a combination of PCA and GAN-based learning.

By integrating statistical feature extraction with generative AI, the model achieves:

* High-quality reconstruction
* Preservation of anatomical structures
* Improved robustness over traditional methods

This approach highlights the potential of combining classical techniques with deep learning for advanced medical imaging applications.

---
