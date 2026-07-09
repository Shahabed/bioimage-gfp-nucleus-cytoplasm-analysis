# Bioimage Analysis: GFP Nuclear vs Cytoplasmic Quantification

This project implements an automated image analysis pipeline to quantify GFP (Green Fluorescent Protein) intensity in the nucleus versus the cytoplasm of cells. It is designed for high-content screening assays, particularly nuclear translocation studies.

## Project Overview

The goal is to measure the ratio of fluorescence intensity between the nucleus and cytoplasm, which is a common readout in cell biology for studying protein translocation, signaling pathways, and drug effects.

The pipeline processes microscopy images from the **BBBC013 dataset** (Broad Bioimage Benchmark Collection) and performs:

- Cell and nucleus segmentation
- Intensity quantification in nuclear and cytoplasmic regions
- Calculation of nuclear-to-cytoplasmic (N/C) ratio
- Dose-response analysis across different compound concentrations

## Key Features

- Automated segmentation using **Watershed algorithm** and **Sobel edge detection**
- Region-based intensity measurements using `skimage.measure.regionprops`
- Statistical analysis and visualization of results
- Support for multi-well plate data processing

## Technologies Used

- **Python**
- **scikit-image** (segmentation and feature extraction)
- **pandas** & **numpy** (data handling)
- **matplotlib** & **seaborn** (visualization)
- Statistical testing (t-test, correlation analysis)

## Pipeline Steps

1. **Image Preprocessing**: Load and normalize fluorescence images
2. **Segmentation**: Detect nuclei and cell boundaries using watershed
3. **Quantification**: Measure GFP intensity in nucleus and cytoplasm
4. **Analysis**: Compute N/C ratios and perform statistical tests
5. **Visualization**: Generate plots and summary statistics

## Skills Demonstrated

- Image processing and computer vision
- Quantitative biology / high-content screening analysis
- Data analysis and statistical modeling
- Automated pipeline development for biological assays


## Results

The pipeline successfully quantifies GFP nuclear translocation and generates:
- Per-cell and per-well intensity measurements
- Nuclear-to-cytoplasmic ratios
- Dose-response curves
- Statistical comparisons between treatment groups

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/analysis.ipynb
