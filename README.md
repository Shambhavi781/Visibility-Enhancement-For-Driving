# Visibility Enhancement for Driving Using Dark Channel Prior (DCP)

## 📌 Project Overview

Visibility Enhancement for Driving is an image dehazing project designed to improve the clarity and contrast of road images affected by haze or fog. Poor visibility can make it difficult to identify vehicles, pedestrians, road signs, and lane markings.

This project uses the **Dark Channel Prior (DCP)** technique and Guided Filtering to estimate and remove haze from images. The system is developed using Python and image-processing libraries, with potential applications in Advanced Driver Assistance Systems (ADAS) and autonomous driving.

## 🎯 Objectives

- Improve the visibility of hazy road images.
- Enhance image clarity and contrast.
- Estimate haze using the Dark Channel Prior technique.
- Refine the transmission map using Guided Filtering.
- Evaluate image quality using PSNR and SSIM.

## 🛠️ Technologies Used

- **Python** – Algorithm development and implementation
- **OpenCV** – Image processing and image manipulation
- **NumPy** – Numerical computations and array operations
- **KITTI Dataset** – Driving-scene images for testing and evaluation
- **PSNR and SSIM** – Image quality evaluation metrics

## ⚙️ Project Workflow

1. **Input Image:** Load a road image from the KITTI dataset.
2. **Dark Channel Prior:** Estimate haze using dark pixel information.
3. **Atmospheric Light Estimation:** Estimate the atmospheric light in the image.
4. **Transmission Map Estimation:** Estimate the amount of scene light reaching the camera.
5. **Guided Filtering:** Refine the transmission map while preserving image edges.
6. **Image Recovery:** Recover a clearer image using the estimated atmospheric light and transmission map.
7. **Performance Evaluation:** Compare the recovered image with a suitable clear reference image using PSNR and SSIM.

## 🧠 Methodology

The project follows the atmospheric scattering model:

\[
I(x)=J(x)t(x)+A(1-t(x))
\]

Where:

- **I(x):** Input hazy image
- **J(x):** Recovered scene image
- **t(x):** Transmission map
- **A:** Atmospheric light

The estimated atmospheric light and refined transmission map are used to recover the scene and reduce the effect of haze.

## 📊 Performance Evaluation

### PSNR (Peak Signal-to-Noise Ratio)
Measures pixel-level reconstruction error between the recovered image and a clear reference image. A higher value generally indicates lower reconstruction error.

### SSIM (Structural Similarity Index Measure)
Measures structural similarity between the recovered image and a clear reference image. Values closer to 1 generally indicate greater structural similarity.

**Note:** Reference-based PSNR and SSIM require a corresponding clear reference image. For synthetic haze experiments, the original clear image can be used as the reference.

## 🚗 Applications

- Advanced Driver Assistance Systems (ADAS)
- Autonomous driving systems
- Vehicle and obstacle detection
- Lane detection
- Traffic sign recognition
- Road-scene image enhancement
- Outdoor surveillance in hazy conditions

## ▶️ Installation and Execution

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd <your-project-folder>
```

### 2. Install Dependencies

```bash
pip install numpy opencv-python
```

Install any additional dependencies required by your implementation.

### 3. Prepare the Dataset

Download or access the KITTI dataset and place the required road images in the appropriate project directory.

### 4. Run the Project

Run the main Python script:

```bash
python main.py
```

Replace `main.py` with your actual Python entry-point filename if it is different.

## 📁 Project Structure

```text
Visibility-Enhancement-for-Driving/
│
├── dataset/           # Input road images
├── output/            # Recovered images
├── main.py            # Main Python program
├── requirements.txt   # Project dependencies
└── README.md          # Project documentation
```

*Update the folder and file names to match your actual repository structure.*

## 🔮 Future Enhancements

- Extend testing to different weather conditions, including fog and snow.
- Optimize the algorithm for real-time image processing.
- Integrate the dehazing system with object-detection models.
- Explore deployment in ADAS and autonomous-driving pipelines.

## 👩‍💻 Project Information

**Project Title:** Visibility Enhancement for Driving Using Dark Channel Prior and Guided Filtering

**Domain:** Image Processing and Computer Vision

**Primary Language:** Python

**Libraries:** OpenCV and NumPy

---

**Disclaimer:** This project focuses on image dehazing and visibility enhancement. Improved image clarity alone does not guarantee better object detection or road safety.

