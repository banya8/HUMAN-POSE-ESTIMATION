
# 🤸‍♀️  Human Pose Estimation Using OpenCV DNN and OpenPose MobileNet


A real-time **Human Pose Estimation System** that uses **OpenCV DNN and OpenPose MobileNet** to detect and visualize human body keypoints and skeletal structures in static images and live video streams. It leverages deep learning and computer vision to analyze human posture and movement, with applications in fitness monitoring, gesture recognition, and activity analysis.

![alt text](output.jpeg)

## 🌟 Features

- **Image-Based Pose Estimation:** Detect and visualize human body keypoints and skeleton connections from static images using OpenCV's DNN module.

- **Skeleton Visualization:** Draw connecting lines between detected joints to represent the human body's skeletal structure.
- **Keypoint Visualization:** Highlight detected body joints with red dots for clear and intuitive pose visualization.
- **Deep Learning Powered:** Use a pretrained OpenPose MobileNet model to perform human pose estimation through OpenCV's Deep Neural Network (DNN) module.

## 🛠️ Tech Stack

- **Programming Language:** Python 3.x
- **Computer Vision:** OpenCV
- **Deep Learning Inference:** OpenCV DNN
- **Pose Estimation Model:** OpenPose MobileNet
- **Development Environment:** Jupyter Notebook

## 🚀 Getting Started

### Prerequisites

Ensure Python is installed on your system. It is recommended to create a virtual environment before installing dependencies.

```bash
python -m venv venv
```

Activate the environment:

```bash
# Windows
venv\Scripts\activate

# Linux / macOS
source venv/bin/activate
```

### Installation

1. Install the required dependencies:

   ```bash
   pip install opencv-python 
   ```
   ```bash
   pip install matplotlib
   ```
2. Download or obtain the pretrained OpenPose MobileNet model files required by your implementation.

3. Configure the model paths, input dimensions, confidence threshold, body-part mapping, and skeleton connection pairs in your Python code.

4. Load a test image and pass it to the pose-estimation function.

## 🖥️ Usage

### 1. Static Image Pose Estimation

Load an image using OpenCV and pass it to the pose-estimation function.

```python
import cv2 as cv

img = cv.imread("posenew.jpg")

estimated_img = pose_estimation(img)

cv.imshow("Human Pose Estimation", estimated_img)
cv.waitKey(0)
```

- **Input:** A static image containing a person.
- **Detection:** The model predicts body keypoints using heatmaps.
- **Filtering:** Keypoints are accepted based on the confidence threshold.
- **Visualization:** Detected joints are marked with red dots, and valid skeletal connections are drawn using green lines.
- **Output:** An image displaying the estimated human pose.

### 2. Confidence Threshold Adjustment

Adjust the `thr` parameter to control which keypoints are displayed.

- A higher threshold filters out more uncertain predictions.
- A lower threshold may reveal additional keypoints but can introduce incorrect detections.

### 3. Inference Time Measurement

The implementation uses OpenCV's performance profiling functions to measure the neural network's inference time and display it on the output image.

## 📊 Keypoints Detected

The model is configured to identify 18 human body keypoints:

- **Head:** Nose, right eye, left eye, right ear, left ear
- **Upper Body:** Neck, right shoulder, left shoulder, right elbow, left elbow, right wrist, left wrist
- **Lower Body:** Right hip, left hip, right knee, left knee, right ankle, left ankle

The detected keypoints are connected according to predefined skeleton pairs to visualize the estimated body posture.

## 📁 Project Structure

```text
.
├── pose_estimation.ipynb  # Jupyter notebook containing pose estimation code
├── posenew.jpg              # Sample input image
├── output.jpg             # Example processed image (optional)
├── model/                 # Pretrained model files (if stored separately)
└── README.md              # Project documentation
```

*Note: Update the filenames and folder structure to match your actual repository.*

## 🎯 Applications

- Human posture visualization
- Body-joint localization
- Basic pose analysis
- Computer vision learning and experimentation
- A foundation for future gesture recognition and human activity analysis

## 🔮 Future Enhancements

- Real-time pose estimation using a webcam
- Video-based pose tracking
- Interactive confidence-threshold controls
- Multi-person pose estimation
- Integration with a web-based interface using Streamlit
- Pose-based activity recognition and movement analysis

## 📌 Conclusion

This project demonstrates human pose estimation using OpenPose MobileNet and OpenCV DNN. By extracting body keypoints from model-generated heatmaps and visualizing their skeletal connections, the system provides an accessible foundation for exploring deep learning-based human pose detection.
