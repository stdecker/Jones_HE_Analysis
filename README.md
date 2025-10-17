# Jones H&E Analysis
Pipeline for automated Jones Silver H&E segmentation and analysis

## Overview

This repository provides a **Google Colab–based deep-learning pipeline** for automated segmentation and morphometric analysis of **Jones’ Silver and H&E–stained kidney sections**.  
The workflow performs **GPU-accelerated segmentation**, **color deconvolution**, and **GBM-focused quantification** to extract key renal histopathology metrics, including **glomerular basement membrane (GBM) thickness**, **Bowman’s space area**, and **tubular morphology**.

Developed by **Stephen T. Decker, Ph.D.** (University of Utah, *Utah Nephron Energetics & Pathophysiology Lab*), this notebook delivers a fully reproducible and open-access approach to structural renal histology analysis using free Colab GPU resources.

---

## 🔬 Features

- **Colab-native pipeline** — runs entirely in the cloud (no installation)
- **GPU-accelerated inference** (T4 / A100)
- **Deep learning segmentation** using U-Net / Cellpose / MONAI-compatible models  
- **Dual-stain normalization** for Jones & H&E images  
- **Quantitative GBM analysis** with adaptive edge detection and thickness estimation  
- **Bowman’s space, tuft, and tubular metrics** (area, circularity, lumen fraction)  
- **Batch mode** for processing entire slide sets automatically  
- **CSV + QC overlay outputs** ready for statistical analysis in R or Python  
- **Creative Commons BY 4.0 license** — free and open reuse with attribution  

---

## ⚙️ Requirements

This pipeline runs directly in **Google Colab** — no setup required.

### Automatically installed dependencies
- Python ≥ 3.10  
- PyTorch / MONAI / OpenCV / NumPy / scikit-image  
- OpenSlide-Python for WSI handling  
- Pandas / Matplotlib for summaries and visualization  

---

## 🚀 Getting Started

1. **Open the Colab notebook**  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/USERNAME/JONES_HE_PIPELINE/blob/main/Jones_HE_Analysis.ipynb)

2. **Upload input data**
   - Jones’ Silver or H&E WSIs (`.tif`, `.svs`, `.ndpi`)  
   - Optional segmentation masks (`.png`, `.tif`) from U-Net / Labkit / DeepImageJ  

3. **Run all cells**
   - Colab automatically installs dependencies and detects GPU hardware.  
   - Results (masks, overlays, CSVs) are saved to your Google Drive.  

4. **Download outputs**
   - Each WSI yields a `*_summary.csv` and `QC_overlay.png`.  

---

## 📊 Quantitative Metrics
Structure	Metric	Units
Glomerulus	Total area, tuft area, Bowman’s space area	µm²
GBM	Mean thickness, SD thickness, perimeter	µm
Tubules	Lumen fraction, cytoplasmic fraction, circularity	µm² / %
Whole tissue	Fibrotic area %, nuclei count	% / n

---

##🧠 Applications

Measurement of GBM thickening and splitting in X-Linked Alport Syndrome (XLAS) models

Quantification of glomerular hypertrophy, tubular dilation, and fibrosis

Comparative analysis between Jones’ Silver and H&E staining modalities

Generation of labeled datasets for deep-learning model training

Standardized morphometry aligned with AJP-Renal and Kidney International methods

---

## 🧾 Citation

If you use this pipeline in your research, please cite:

Decker, S. T. (2025).
Jones’ Silver + H&E Segmentation & Quantitative Histopathology Pipeline (Colab).
Utah Nephron Energetics & Pathophysiology Lab, University of Utah.
https://github.com/stdecker/JONES_HE_PIPELINE

---

## 📜 License

This repository is licensed under the
Creative Commons Attribution 4.0 International License (CC BY 4.0).
You are free to share, adapt, and redistribute this material in any medium or format, provided appropriate credit is given.

---
🤝 Contributing

Pull requests are welcome.
Potential contributions include:

New stain vector or color deconvolution methods

Enhanced GBM measurement algorithms

Integration with other deep-learning frameworks (MONAI, Segment Anything, etc.)
