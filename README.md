# GFP Nuclear Translocation Image Analysis Pipeline

[![Python 3.6+](https://img.shields.io/badge/Python-3.6%2B-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Python-based pipeline to analyze fluorescence microscopy images for **GFP nuclear vs cytoplasmic localization**. Built for the [BBBC013_v1](https://bbbc.broadinstitute.org/BBBC013) dataset but easily adaptable to similar high-content screening experiments.

## Features
- Dual-channel image processing (GFP + DNA stain)
- Custom thresholding for nucleus/cytoplasm separation
- Watershed segmentation + regionprops
- Per-cell GFP intensity quantification (nucleus, cytoplasm, ratio)
- Dose-response analysis and statistical comparisons
- Export to CSV for downstream visualization

## Requirements
```bash
pip install numpy pandas matplotlib seaborn scikit-image scipy statsmodels
