# Object Detection with YOLOv3

## Introduction
This Python script leverages the YOLOv3 object detection model to identify and highlight various objects within a video stream. It's designed to be a versatile tool for a range of applications, from security surveillance to automated systems.

---

## Prerequisites
Before running the script, ensure you have the following installed:

- **OpenCV**: A popular computer vision library.
- **NumPy**: A fundamental library for numerical operations in Python.
- **YOLOv3 Model**: The pre-trained YOLOv3 model and its configuration file.
- **COCO Names**: A text file containing the names of the 80 object classes that YOLOv3 can detect.

---

## Installation

### Install Required Libraries:
```bash
pip install opencv-python numpy
```

### Download YOLOv3 Model and COCO Names:
You can download the YOLOv3 model and COCO names from the official YOLO website or other reliable sources. Place them in the same directory as the script.

---

## How to Run

### Place Files:
Ensure the following files are in the same directory as the script:

- `yolov3.weights`
- `yolov3.cfg`
- `coco.names`

### Execute the Script:
```bash
python object_detection.py
```

---

## How it Works

### Video Capture:
The script initializes a video capture object to access the default camera.

### Object Detection:

1. **Image Preprocessing**: The current frame from the video is resized and converted into a suitable format for YOLOv3.
2. **YOLOv3 Forward Pass**: The preprocessed image is fed into the YOLOv3 network to generate bounding boxes and class probabilities for detected objects.
3. **Non-Maximum Suppression (NMS)**: NMS is applied to filter out overlapping bounding boxes with lower confidence scores.
4. **Drawing Bounding Boxes**: The remaining bounding boxes are drawn on the image, along with their corresponding class labels.

### Display:
The processed image with detected objects is displayed in a window.

---

## Customization

1. **Model**: You can experiment with different YOLO models or fine-tune the existing one for specific object detection tasks.
2. **Confidence Threshold**: Adjust the confidence threshold to control the sensitivity of the detector.
3. **NMS Threshold**: Modify the NMS threshold to balance precision and recall.
4. **Video Source**: Change the video capture source to process video files or other camera streams.

---

## Potential Applications

- **Security Surveillance**: Monitor for suspicious activities or intruders.
- **Autonomous Vehicles**: Detect obstacles and pedestrians.
- **Retail Analytics**: Analyze customer behavior and inventory management.
- **Quality Control**: Inspect products for defects.

---
