# FitCheck – Virtual Clothing Try-On System

A computer vision-based virtual try-on system that overlays selected garments onto a user's body image or live camera feed.

## Overview

FitCheck allows users to virtually try on clothing by aligning garments realistically with body pose, size, and orientation — without physically wearing them.

## Pipeline
Pose Estimation → Body Segmentation → Garment Overlay
## Features

- **Pose Estimation** – Uses MediaPipe Pose to extract 9 body keypoints for garment alignment and body measurement computation
- **Body Segmentation** – U2Net (rembg) with GrabCut fallback to isolate the user's body
- **Garment Overlay** – Affine warping and Poisson seamless blending via OpenCV for realistic garment fitting

## Tech Stack

- Python
- MediaPipe
- OpenCV
- rembg (U2Net)
- NumPy
- Pillow

## Setup

```bash
# Create environment
conda env create -f environment.yml
conda activate fitcheck

# Run
python tryon.py
```

