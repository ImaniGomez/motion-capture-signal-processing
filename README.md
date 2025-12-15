# Motion Capture Signal Processing

This repository contains the code and experimental pipeline for the paper:

**“Signal Processing and Uses in Motion Capture: A Comparative Analysis of Common Algorithm Performance”**

The project evaluates common signal processing algorithms applied to motion capture data, with a focus on accuracy, smoothness, and robustness under real-world capture conditions. Motion data was recorded using a marker-based optical motion capture system and analyzed using multiple filtering techniques.

---

## Overview

Motion capture systems are widely used in film, gaming, sports, and medical rehabilitation, but captured data often contains noise, occlusions, and artifacts. Signal processing algorithms are commonly applied to improve data quality before analysis or animation.

This project compares the performance of:
- **Kalman Filter**
- **Butterworth Filter**
- **Gaussian Filter**

using real marker-based motion capture recordings.

---

## Data Collection

- Motion data was captured in a marker-based studio using **40 Vicon cameras**
- Skeletal data was recorded in `.fbx` format using **Vicon Shōgun**
- A wearable suit with **25 degrees of freedom (DOFs)** was calibrated using a wand-based procedure
- Two 90-second motion sequences were recorded, including:
  - Running
  - Kicking
  - Jumping
  - Dancing
- Additional recordings captured failure cases when the performer exited the calibrated capture volume

---

## Data Extraction

Captured `.fbx` files were imported into **Unity**, where individual joint position data was extracted using a custom **C# script**. The extracted joint data was exported as CSV files for further signal processing and analysis.

---

## Methods

The extracted joint position data was filtered using three common signal processing algorithms:

- **Kalman Filter** — optimal estimation algorithm used for tracking noisy dynamic systems
- **Butterworth Filter** — frequency-domain low-pass filtering for noise reduction
- **Gaussian Filter** — smoothing via convolution with a Gaussian kernel

Each method was evaluated based on smoothness, distortion, and preservation of motion characteristics.

---

## Citation

If you use this code or data in academic work, please cit: 

@article{motion_capture_signal_processing,
  title={Signal Processing and Uses in Motion Capture: A Comparative Analysis of Common Algorithm Performance},
  author={Your Name},
  year={2025}
}

