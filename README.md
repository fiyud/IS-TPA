# IS-TPA: Intelligent System for Traffic Police Action Recognition

**Spatial-Temporal Dynamics Skeletal Graph-Based Human Action Recognition for Vietnamese Traffic Police Gestures**

## 📋 Overview

This repository contains the implementation of a skeletal graph-based human action recognition system specifically designed for recognizing Vietnamese traffic police gestures. The system utilizes spatial-temporal dynamics to analyze skeleton data captured from Microsoft Kinect v2 sensor for accurate gesture classification.

In this research, we proposed the **International School - Traffic Police Action (IS-TPA) dataset**, a novel benchmark specifically designed for Human Action Recognition (HAR) of Vietnamese traffic police gestures during traffic direction scenarios. The IS-TPA dataset addresses the unique challenges of recognizing standardized traffic control gestures, which exhibit distinct spatiotemporal patterns compared to general human actions. Our dataset consists of eight distinct action classes representing fundamental traffic control gestures commonly employed by Vietnamese traffic police officers.

## 🎯 Dataset

### Dataset Information
- **Dataset Name**: IS-TPA (International School - Traffic Police Action)
- **Sensor**: Microsoft Kinect v2
- **Total Classes**: 8 action classes
- **Joints per Skeleton**: 25 joints
- **Frame Rate**: 30 FPS

### IS-TPA Dataset Action Class Descriptions

The dataset comprises 8 distinct traffic police gesture classes representing fundamental traffic control gestures commonly employed by Vietnamese traffic police officers:

## **Class 0: Stop Signal**
## **Class 1: Go/Proceed Signal**
## **Class 2: Turn Left Signal**
## **Class 3: Turn Right Signal**
## **Class 4: Slow Down Signal**
## **Class 5: Speed Up Signal**
## **Class 6: Pull Over Signal**
## **Class 7: U-Turn Signal**

### Dataset Structure

```
Dataset/
├── 0/              # Class 0 samples (Stop Signal)
│   ├── class_0_0000.json
│   ├── class_0_0001.json
│   └── ...
├── 1/              # Class 1 samples (Go/Proceed Signal)
│   ├── class_1_0000.json
│   └── ...
├── 2/              # Class 2 samples (Turn Left Signal)
├── 3/              # Class 3 samples (Turn Right Signal)
├── 4/              # Class 4 samples (Slow Down Signal)
├── 5/              # Class 5 samples (Speed Up Signal)
├── 6/              # Class 6 samples (Pull Over Signal)
└── 7/              # Class 7 samples (U-Turn Signal)
```

### Skeleton Joint Information

Each skeleton frame contains 25 joints tracked by Kinect v2:

**Torso**: SpineBase, SpineMid, SpineShoulder, Neck, Head  
**Left Arm**: ShoulderLeft, ElbowLeft, WristLeft, HandLeft, HandTipLeft, ThumbLeft  
**Right Arm**: ShoulderRight, ElbowRight, WristRight, HandRight, HandTipRight, ThumbRight  
**Left Leg**: HipLeft, KneeLeft, AnkleLeft, FootLeft  
**Right Leg**: HipRight, KneeRight, AnkleRight, FootRight

### Coordinate System
- **X-axis**: Horizontal (left-right)
- **Y-axis**: Vertical (up-down)
- **Z-axis**: Depth (distance from sensor)

### Tracking States
- **0**: NotTracked
- **1**: Inferred
- **2**: Tracked

## 🚀 Getting Started

### Prerequisites

```bash
# Python 3.8+
# Required libraries (example)
pip install numpy
pip install torch
pip install scikit-learn
```

### Installation

```bash
git clone https://github.com/fiyud/IS-TPA.git
cd IS-TPA
```

## 💻 Usage

```python
# Example usage will be added here
# Load dataset, train model, and perform inference
```

## 📊 Results

Performance metrics and experimental results will be documented here.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📧 Contact

For questions or collaboration opportunities, please open an issue in this repository.

## 🙏 Acknowledgments

- Vietnamese Traffic Police for gesture specifications
- Microsoft Kinect v2 for skeleton tracking technology
- Research team members and contributors

## 📚 Citation

If you use this dataset or code in your research, please cite:

```bibtex
@inproceedings{istpa2025,
  title={IS-TPA: Spatial-Temporal Dynamics Skeletal Graph-Based Human Action Recognition for Vietnamese Traffic Police Gestures},
  author={Quang-Anh N.D., Mai-Hanh Nguyen Thi, Tien Dat Nguyen, Quoc Bao Doan,Ha Phuong Vu, Kieu Oanh Do Thi, Truong Linh Nguyen Thanh, Manh-Hung Ha},
  booktitle = {2nd Asia Meeting on Environment and Electrical Engineering},
  year={2025},
  publisher={IEEE},
}
```