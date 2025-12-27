# Restormer Project

This project presents a **comparative study of video denoising techniques**, ranging from classical image processing methods to a modern deep learning–based approach. 
The objective is to evaluate how traditional filters perform compared to a pretrained transformer-based model, **Restormer**, when applied to noisy video data.
Rather than proposing a new model, this project focuses on **experimental design, controlled evaluation, and qualitative analysis** using real video input.

# Pipeline Overview
1. Input clean video
2. Extract frames
3. Inject Gaussian noise
4. Apply classical denoising methods
5. Apply Restormer denoising
6. Align frames across methods
7. Reconstruct comparison video
8. Perform qualitative and quantitative evaluation

# References 
- Zamir, S. W., et al., *Restormer: Efficient Transformer for High-Resolution Image Restoration*, CVPR 2022.
- Restormer Official GitHub Repository: https://github.com/swz30/Restormer
  - The Restormer source code and the pretrained denoising weights
    (`gaussian_color_denoising_blind.pth`) were downloaded from the official GitHub repository
    released by the original authors. The pretrained model was used strictly for inference
    without any training or fine-tuning.
# Methods
This project compares **classical image processing techniques** with a **deep learning–based restoration model** under a controlled video denoising pipeline. All methods are applied to the same noisy video frames to ensure a fair and consistent comparison.

### Classical Image Processing
Classical denoising methods are used as baseline approaches due to their simplicity,
interpretability, and widespread adoption in traditional image processing.

- **Gaussian Blur**
  - Smooths noise via convolution with a Gaussian kernel
  - Effective for reducing Gaussian noise but causes edge and texture blurring
  - **Strengths:** Simple, fast, computationally efficient  
  - **Limitations:** Loss of fine details and edge sharpness

- **Median Blur**
  - Replaces pixel values with the median of neighboring pixels
  - Preserves edges better than Gaussian blur
  - **Strengths:** Robust to impulse noise and outliers  
  - **Limitations:** Removes fine textures and small details


### Deep Learning Approach
- **Restormer**
  - Transformer-based image restoration model
  - Captures long-range dependencies and global contextual information
  - Effectively suppresses noise while preserving structural details and textures
  - Used with **pretrained weights** and applied **only in inference mode**
  - **Strengths:** High perceptual quality and strong texture preservation  
  - **Limitations:** Requires pretrained models and higher computational resources


### Implementation Details
- Video frames are processed on a frame-by-frame basis.
- Gaussian noise is synthetically added to simulate realistic degradation.
- Classical filters use fixed parameters across all frames.
- Restormer is applied using pretrained weights without training or fine-tuning.
- All outputs are aligned by frame index to ensure fair visual comparison.


### Method Comparison Rationale
Classical image processing methods rely on fixed mathematical rules and local
operations, whereas Restormer adopts a data-driven approach that learns complex
spatial and contextual relationships from data. This contrast enables a clear
comparison between rule-based and deep learning–based denoising techniques.


# Evaluation Metrics
- **SSIM (Structural Similarity Index)**
  - Measures the ratio between the maximum possible signal power and the noise power.
    Higher PSNR indicates better noise suppression but does not always correlate with
    human visual perception.
- **PSNR (Peak Signal-to-Noise Ratio)**
  - Evaluates perceptual image quality by comparing luminance, contrast, and structural
    information. SSIM aligns better with human visual perception than PSNR.
    
- Both metrics are reported to provide complementary perspectives: PSNR focuses on
  pixel-wise fidelity, while SSIM emphasizes structural and perceptual similarity.


# Evaluate & Result 
