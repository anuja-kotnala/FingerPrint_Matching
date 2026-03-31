## Fingerprint Matching using ORB Feature Descriptor

A biometric verification system that determines whether two fingerprint images belong to the same person, built using OpenCV's ORB (Oriented FAST and Rotated BRIEF) feature detector and Brute Force Matcher.

## Overview

Fingerprint matching is a core problem in biometric authentication systems. This project implements a classical feature-based approach to verify fingerprint identity by extracting and comparing keypoints across two fingerprint images.

## Methodology

1. **Preprocessing** — Load fingerprint images in grayscale
2. **Feature Extraction** — Detect keypoints and compute descriptors using ORB
3. **Feature Matching** — Match descriptors using Brute Force Matcher with Hamming distance
4. **Decision** — Classify as genuine (same person) or impostor (different person) based on the number of good matches against a threshold

## Dataset

[FVC2002](http://bias.csr.unibo.it/fvc2002/) (Fingerprint Verification Competition 2002) — a standard benchmark dataset for fingerprint verification research, containing multiple databases of fingerprint images captured using different sensors.

## Results

- Correctly identifies genuine pairs (same person, different impressions)
- Correctly rejects impostor pairs (different people)
- Evaluated using accuracy score and confusion matrix across multiple genuine and impostor pairs

## Tech Stack
- Python
- OpenCV
- NumPy
- Scikit-learn
- Matplotlib

## Files

| File | Description |
|------|-------------|
| `fingerprint_matching.ipynb` | Main notebook with full implementation |
| `README.md` | Project documentation |

## How to Run

1. Open `fingerprint_matching.ipynb` in Google Colab
2. Upload FVC2002 dataset as a zip file when prompted
3. Run all cells sequentially
