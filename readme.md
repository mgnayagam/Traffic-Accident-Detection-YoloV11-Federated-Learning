**Multimodal Live Streaming Data for Traffic Accident Detection using YoloV11 based Federated Learning in Edge Computing**
📌 Project Overview
This research presents a novel methodology for enhancing smart city safety through advanced traffic accident detection. By integrating YoloV11 with Federated Learning (FL), the system enables real-time processing and identification of incidents while preserving data privacy.
The system is designed for Edge-Cloud Architecture, utilizing Kubernetes-based containerized computing for superior scalability compared to conventional systems.
🚀 Key Features
•	Real-Time Detection: Uses YoloV11 to identify, categorize, and track moving objects, including velocity and direction calculations.
•	Privacy-Preserving: Federated Learning ensures that only model weights are shared with the central MEC server, keeping raw data local to the edge clients.
•	Multimodal Integration: Supports data from CCTV (4K), LIDAR, Radar, and IMU sensors.
•	High Accuracy: The Deep Learning system achieved 99.07% accuracy, while the XGBoost model recorded 99.8% accuracy for highway collisions.
•	Scalable Infrastructure: Implemented using NVIDIA Jetson NX edge nodes and Kubernetes for orchestration.
📊 Performance Analysis
The proposed framework outperforms traditional centralized models in several key areas:
•	Inference Latency: Significantly lower latency compared to centralized CNNs and YOLOv8 Edge implementations.
•	Robustness: High precision and F1-scores across varying environmental conditions like weather and illumination.
•	ROC Curve: Demonstrates strong reliability with an Area Under the Curve (AUC) of 0.94.
🛠️ System Configuration
Federated Learning Setup
Aspect	Configuration
FL Algorithm	FedAvg / FedProx 
Edge Clients	10–50 nodes 
Aggregation Server	Multi-access Edge Computing (MEC) 
Communication	5G-V2X, DSRC 
Hardware & Software Stack
•	Deep Learning: PyTorch, TensorFlow, OpenCV.
•	Hardware: NVIDIA Jetson NX, Xilinx FPGA.
•	Cloud/Edge: AWS, Azure, MQTT Brokers.
📁 Repository Structure
•	EdgeComputing.ipynb: The primary notebook containing data preprocessing, YoloV11 classification training, and testing logic.
•	weights/best.pt: The trained YoloV11 model weights (saved from Epoch 12).
•	dataset/: Folder structure for train, val, and test data (Accident vs. Non-Accident classes).
📖 How to Run
1.	Environment Setup: Install the necessary requirements:
Bash
pip install ultralytics opencv-python torch
2.	Training: The model was trained for 50 epochs with an image size of 224x224 and early stopping enabled.
3.	Inference:
Python
from ultralytics import YOLO
model = YOLO('best.pt')
results = model.predict(source='your_video.mp4')
🔗 Data Sources
The model was trained and validated using the following datasets:
•	DeepAccident Dataset: Download Link 
•	TADS (RGB + Optical Flow + Eye-gaze): GitHub 
•	TAD Bench (Large-scale Highway): GitHub 
🎓 Author
Dr. M. Gomathy Nayagam Associate Professor, Department of Computer Science and Business Systems
Ramco Institute of Technology, Rajapalayam.
🔮 Future Scope
Future iterations of this project will incorporate a Blockchain model to further enhance security and privacy for real-time traffic applications.

