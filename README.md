
# POD Analysis Project

## Project Overview
The POD Analysis Project focuses on extracting and analyzing frames from video data to explore the effectiveness of various denoising techniques. With the advent of advanced imaging technologies, handling and processing large volumes of video data has become increasingly important. Noise in video frames can significantly degrade the quality of the data, making it difficult to analyze and extract meaningful information. This project aims to address this challenge by systematically adding different types of noise to video frames and then applying various denoising algorithms to assess their performance.

### Objectives
- **Frame Extraction**: Extract frames from a video at specific intervals to create a dataset for analysis.
- **Noise Addition**: Introduce different types of noise (Gaussian and Salt-and-Pepper) to the extracted frames to simulate real-world conditions.
- **Denoising**: Apply denoising techniques such as Gaussian Blur and Non-local Means (NLM) Denoising to the noisy frames.
- **SVD Analysis**: Use Singular Value Decomposition (SVD) to analyze the energy distribution in the image data and understand the impact of denoising.

### Importance
Video data is ubiquitous in various fields such as surveillance, medical imaging, remote sensing, and entertainment. Ensuring the quality and integrity of this data is crucial for accurate analysis and decision-making. By improving denoising techniques, this project contributes to the development of more robust and efficient methods for handling noisy video data, which can be beneficial for:
- **Surveillance Systems**: Enhancing the quality of footage for better identification and monitoring.
- **Medical Imaging**: Reducing noise in medical scans to improve diagnosis and treatment planning.
- **Remote Sensing**: Enhancing satellite imagery for better environmental monitoring and disaster management.
- **Entertainment**: Improving the quality of video content in film and media production.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Frame Extraction](#frame-extraction)
- [Adding Noise](#adding-noise)
- [Denoising Techniques](#denoising-techniques)
- [SVD Analysis](#svd-analysis)
- [Results](#results)
- [Report](#report)
- [License](#license)
- [Contact](#contact)

## Installation
1. Clone the repository:
   \`\`\`bash
   git clone https://github.com/username/POD_Analysis_Project.git
   cd POD_Analysis_Project
   \`\`\`

2. Install the required dependencies:
   \`\`\`bash
   pip install -r requirements.txt
   \`\`\`

## Usage
1. Ensure you have your video file in the specified path.

2. Run the script to extract frames, add noise, and perform denoising.

   \`\`\`bash
   python pod_analysis.py
   \`\`\`

## Frame Extraction
The \`frames\` function extracts frames from a video at specified intervals.

\`\`\`python
def frames(video_path, folder, interval_seconds, color_scale):
    # function implementation
\`\`\`
- **Parameters**:
  - \`video_path\`: Path to the video file.
  - \`folder\`: Directory to save extracted frames.
  - \`interval_seconds\`: Time interval between frames.
  - \`color_scale\`: Color scale of the frames ('RGB' or 'Grayscale').

## Adding Noise
The project explores two types of noise: Gaussian and Salt-and-Pepper.

### Gaussian Noise
\`\`\`python
def add_gaussian_noise(image, magnitude):
    # function implementation
\`\`\`

### Salt-and-Pepper Noise
\`\`\`python
def add_salt_and_pepper_noise(image, salt_percent, pepper_percent):
    # function implementation
\`\`\`

## Denoising Techniques
Two denoising techniques are applied:

### Gaussian Blur
\`\`\`python
def denoise_with_gaussian_blur(images, kernel_size=(5, 5), sigma_x=0):
    # function implementation
\`\`\`

### Non-local Means Denoising
\`\`\`python
def denoise_with_nlm(images, h=10, templateWindowSize=7, searchWindowSize=21):
    # function implementation
\`\`\`

## SVD Analysis
Singular Value Decomposition (SVD) is used to analyze the energy distribution of the images.

\`\`\`python
def perform_svd(data_matrix):
    U, S, Vt = np.linalg.svd(data_matrix, full_matrices=False)
    return U, S, Vt
\`\`\`

## Results
- Energy contribution of different modes
- Reconstruction of images using SVD
- Cumulative variance to determine the number of modes required to retain a certain percentage of energy

## Report
A detailed analysis and results are documented in the [POD Analysis Report](./POD_Analysis_Report.pdf).

## License
This project is licensed under the MIT License.

## Contact
For any questions or contributions, please contact [your_email@example.com].
