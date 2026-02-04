# Multi-Object Tracking: Pedestrian Detection & Tracking

A comprehensive multi-object tracking (MOT) system that detects and tracks pedestrians in crowded scenes using three different approaches: Naive IOU-based tracking, Kalman Filter with Hungarian algorithm, and deep learning-based YOLO tracking.

##  Project Overview

This project implements and compares three tracking approaches on the MOT17 Challenge dataset:
- **Naive Baseline**: Simple IOU-based frame-to-frame matching
- **Classical ML**: Kalman Filter for motion prediction + Hungarian algorithm for data association
- **Deep Learning**: YOLOv8 detector with ByteTrack algorithm (and a finetuned YOLO)

##  Key Features

- Real-time pedestrian detection and tracking
- Motion prediction using Kalman filtering
- Comparative analysis of tracking algorithms
- Comprehensive evaluation metrics (MOTA, Precision, Recall, ID Switches)

##  Results Summary

| Model | Total Tracks | Precision | Recall | ID Switches | Avg IDs/GT |
|-------|-------------|-----------|--------|-------------|------------|
| Naive | 262 | 91.09% | 15.95% | 251 | 4.23 |
| Kalman | 199 | 91.09% | 15.95% | 279 | 3.21 |
| YOLO | 90 | 81.89% | 21.49% | 45 | 1.45 |

### Evaluation Metrics Used:
- **Precision**: Ratio of correct detections to all detections
- **Recall**: Ratio of correct detections to ground truth objects
- **ID Switches**: Number of identity changes per track
- **MOTA**: Multiple Object Tracking Accuracy
- **Avg IDs per GT**: Average number of predicted IDs per ground truth track

**Winner**: YOLO achieves best recall, fewest ID switches, and superior track continuity.

##  Installation
```bash
# Clone repository
git clone [https://github.com/SharmilNK/Pedestrian-Tracking-MOT.git]
cd Pedestrian-Tracking-MOT

# Install dependencies
pip install -r requirements.txt

# Download MOT17 dataset
wget https://motchallenge.net/data/MOT17.zip
unzip MOT17.zip
```

##  Technologies Used

- **Python 3.8+**
- **PyTorch**: Deep learning framework
- **Ultralytics YOLOv8**: Object detection
- **FilterPy**: Kalman Filter implementation
- **OpenCV**: Image processing and visualization
- **NumPy, Pandas**: Data manipulation
- **Matplotlib**: Plotting and visualization


⭐ If you find this project helpful, please consider giving it a star!
