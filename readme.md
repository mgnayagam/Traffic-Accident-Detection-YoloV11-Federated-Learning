🚦 Multimodal Traffic Accident Detection using YOLOv11 & Federated Learning
📌 Project Overview

This project presents a smart traffic accident detection system that combines YOLOv11 with Federated Learning (FL) to enable real-time, privacy-preserving incident detection in smart cities.

The system is built on an Edge-Cloud architecture, leveraging containerized deployment with Kubernetes for scalability and efficient distributed processing.

🚀 Key Features
🔍 Real-Time Detection
Detects and tracks vehicles and incidents using YOLOv11 with velocity and direction estimation.
🔐 Privacy-Preserving Learning
Uses Federated Learning so that raw data remains on edge devices while only model updates are shared.
📡 Multimodal Data Integration
Supports multiple sensor inputs:
CCTV (4K video)
LiDAR
Radar
IMU sensors
📊 High Accuracy
Deep Learning Model Accuracy: 99.07%
XGBoost Model Accuracy: 99.8% (highway collision detection)
⚙️ Scalable Infrastructure
Deployed on NVIDIA Jetson NX edge devices with Kubernetes orchestration.
📊 Performance Analysis
Metric	Performance
Inference Latency	Low (Edge-optimized)
Precision / Recall	High across varied conditions
F1 Score	Strong consistency
ROC AUC	0.94

✔️ Outperforms traditional centralized CNN and YOLO-based edge systems
✔️ Robust under varying weather and lighting conditions

🛠️ System Configuration
🔁 Federated Learning Setup
Component	Configuration
FL Algorithms	FedAvg / FedProx
Edge Clients	10–50 nodes
Aggregation Server	MEC (Multi-access Edge Computing)
Communication	5G-V2X, DSRC
💻 Hardware & Software Stack

Frameworks & Libraries

PyTorch
TensorFlow
OpenCV
Ultralytics YOLO

Hardware

NVIDIA Jetson NX
Xilinx FPGA

Cloud & Communication

AWS / Azure
MQTT Brokers
📁 Repository Structure
├── EdgeComputing.ipynb     # Main notebook (training + testing)
├── weights/
│   └── best.pt             # Trained YOLOv11 model (Epoch 12)
├── dataset/
│   ├── train/
│   ├── val/
│   └── test/
▶️ How to Run
1️⃣ Environment Setup
pip install ultralytics opencv-python torch
2️⃣ Training
Epochs: 50
Image Size: 224 × 224
Early stopping enabled
3️⃣ Inference
from ultralytics import YOLO

model = YOLO('weights/best.pt')
results = model.predict(source='your_video.mp4')
🔗 Datasets
DeepAccident Dataset – (Provide link)
TADS (RGB + Optical Flow + Eye-Gaze) – (GitHub link)
TAD Bench (Highway Dataset) – (GitHub link)
🎓 Author

Dr. M. Gomathy Nayagam
Associate Professor
Department of Computer Science and Business Systems
Ramco Institute of Technology, Rajapalayam

🔮 Future Scope
Integration of Blockchain technology for enhanced security and trust
Expansion to fully autonomous traffic monitoring systems
Improved edge intelligence and adaptive learning models
