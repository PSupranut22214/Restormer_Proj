# Restormer Project

This project presents a **comparative study of video denoising techniques**, ranging from classical image processing methods to a modern deep learning–based approach. 
The objective is to evaluate how traditional filters perform compared to a pretrained transformer-based model, **Restormer**, when applied to noisy video data.
Rather than proposing a new model, this project focuses on **experimental design, controlled evaluation, and qualitative analysis** using real video input.

## Repo Structure
- demo.ipynb: main notebook
- (future) scripts/: helper scripts
- (future) results/: evaluation outputs (ignored in git)

## Methods
### Classical Image Processing
- **Gaussian Blur**
  - Smooths noise via convolution
  - Effective for noise reduction but blurs edges and textures

- **Median Blur**
  - Replaces pixel values with neighborhood medians
  - Preserves edges better than Gaussian blur but still removes fine details

### Deep Learning Approach
- **Restormer**
  - Transformer-based image restoration model
  - Captures long-range dependencies and global context
  - Preserves structure and textures while suppressing noise

## Metrics
- SSIM
- PSNR

## Evaluate & Result 
