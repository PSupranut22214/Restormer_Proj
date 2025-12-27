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

## Evaluation Metrics
- **SSIM (Structural Similarity Index)**
  - Measures the ratio between the maximum possible signal power and the noise power.
    Higher PSNR indicates better noise suppression but does not always correlate with
    human visual perception.
- **PSNR (Peak Signal-to-Noise Ratio)**
  - Evaluates perceptual image quality by comparing luminance, contrast, and structural
    information. SSIM aligns better with human visual perception than PSNR.
    
- Both metrics are reported to provide complementary perspectives: PSNR focuses on
  pixel-wise fidelity, while SSIM emphasizes structural and perceptual similarity.


## Evaluate & Result 
