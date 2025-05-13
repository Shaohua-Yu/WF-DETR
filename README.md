
# WF-DETR: Real-Time Fruit Quality Detection with Wavelet Transform and Parallel Perception


## 📖 Project Overview
This repository is the official implementation of the paper *"Research on Data-Driven Fruit Quality Detection Algorithm"*. We propose **WF-DETR** (Wavelet-Frequency DETR), an enhanced real-time end-to-end detection framework optimized for fruit quality inspection under challenging conditions, including complex illumination, multi-scale defects, and occlusions. Key innovations include:
- **Wavelet Transform Convolution Module (WTConv)**: Enhances high-frequency texture features and improves robustness to lighting variations.
- **Parallel Perception Intra-scale Feature Interaction (PIFI)**: Dual-branch architecture fuses local details and global semantics.
- **Dynamic Occlusion Augmentation & MPDIoU Localization**: Optimizes bounding box regression for irregular targets.

Trained on the **Fruit-Quality-10** dataset (10 fruit categories, 34,500 images), WF-DETR achieves **84.2 mAP50** at **16.8 FPS**, outperforming state-of-the-art detectors.

---

##📁 Dataset Preparation

Fruit-Quality-10: Download from GitHub Release(https://github.com/Wenyi0829/fruit_datasets) and extract to ./datasets. The 'Single' folder means a single-target dataset, and the 'Multi' folder means a multi-target dataset. You can merge them manually.

Modify yamls/alldata.yaml to ensure correct paths:

train: ./datasets/train

val: ./datasets/val

---

## 🛠️ Environment Setup
### Dependencies
- **OS**: Windows/Linux
- **Python**: 3.10+
- **PyTorch**: 1.13.0+ (CUDA 11.6)
- **GPU**: NVIDIA GPU (RTX 4090 recommended)


### Clone repository
git clone https://github.com/Shaohua-Yu/WF-DETR.git
cd WF-DETR

### Install dependencies

pip install -r requirements.txt


---

##🚀 Training & Inference

###Quick Start:

python maintrain.py

###Key Parameters (modifiable in code):

- data_yaml: Dataset config path (default: yamls/alldata.yaml)

- imgsz: Input image size (default: 640)

- epochs: Training epochs (default: 200)

- batch_size: Batch size (default: 16)

- device: Training device (default: GPU 0)

###Hyperparameters
- Learning Rate: lr0=0.001

- Weight Decay: weight_decay=0.0001

- Data Augmentation: Enabled (horizontal flip, brightness adjustment via augment=True)


---

##📧 Contact 
Author: Wenyi Shen, Shaohua Yu, Mengchu Tian, Qiyun Zhou

Email: shen_wenyi@njust.edu.cn, shaohua.yu@njust.edu.cn, 2759910264@qq.com, tianmengchu@njust.edu.cn




