# Depth Segmentation with MiDaS

This project showcases depth segmentation using the MiDaS model. It takes an input image and generates a depth map to estimate the distance of various objects in the scene.

## Project Overview

This project utilizes MiDaS, a deep learning model developed by Intel, to perform depth estimation on images. The primary objective is to estimate the depth of each pixel in an input image. MiDaS works on monocular images (images taken from a single camera) and is widely applicable in robotics, 3D reconstruction, augmented reality, and more.

## Features

- **Depth Segmentation**: Generate depth maps from monocular images.
- **MiDaS model integration**: Using state-of-the-art pre-trained models for accurate depth estimation.
- **Supports GPU acceleration**: Optimized for both CPU and GPU (CUDA or Apple’s MPS for macOS users).
- **Grayscale Visualization**: Changed from regular RGB depth output to a normalized greyscale image for better differentiation.

## Installation

To use this project, clone the repository and install the required dependencies:

```bash
git clone https://github.com/yourusername/depth-segmentation.git
cd depth-segmentation
pip install -r requirements.txt
```
## Usage

1. Prepare your environment: Ensure you have a proper Python environment set up with the required dependencies.
2. Run Depth Segmentation: Open the Jupyter notebook and follow the steps provided to run the depth segmentation on your images.
```python
# Import the required functions and libraries
from utils import run_midas

# Define the image path
img_path = "path_to_your_image.jpg"

# Run MiDaS for depth segmentation
run_midas(img_path, title="Depth Segmentation", device="cuda", input_mode="bilinear")
```
3. Apple Silicon Users:
If you're using an Apple device with an M1 or M2 chip, ensure you set the device to "mps".

## Some Comparisions
Images for these examples are included in the repo

![depth-seg](https://github.com/user-attachments/assets/17058b8a-cde7-427d-a38d-5a1fb874daeb)



## Notes

- If you're using a macOS device with an Apple Silicon GPU (M1, M2), use "mps" as the device setting.
- On other systems, "cuda" is recommended for GPU acceleration.
- Ensure that the input mode is compatible with your device. For Apple M1, use "bilinear" mode for interpolation as "bicubic" may not be supported.
