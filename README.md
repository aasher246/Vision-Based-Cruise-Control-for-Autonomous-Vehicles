# Vision-Based Cruise Control for Autonomous Vehicles

## Overview
This project focuses on developing an AI-driven **vision-based cruise control system** capable of lane detection, object recognition, and imitation learning for autonomous navigation.  
It was designed as a Bachelor’s final-year research project, combining **computer vision**, **deep learning**, and **simulation environments** to emulate real-world autonomous driving systems.

The project implements multiple object detection architectures, culminating in **YOLOv4**, integrated with Unity ML Agents for behavioral learning and real-time steering control.

---

## Objectives
- Implement a robust lane detection system using image processing and Hough Transform.  
- Evaluate multiple object detection algorithms and deploy the YOLOv4 model for real-time inference.  
- Develop imitation learning workflows using Unity’s ML-Agents toolkit.  
- Integrate lane and object detection modules to simulate autonomous cruise control in a virtual environment.  

---

## Tools and Technologies
- **Languages:** Python, C# (for Unity integration)  
- **Libraries & Frameworks:** OpenCV, TensorFlow, YOLOv3/YOLOv4, NumPy, Matplotlib  
- **Simulation Platform:** Unity ML-Agents Toolkit  
- **Hardware:** GPU-enabled workstation for model training  
- **Core Techniques:**  
  - Canny Edge Detection, Hough Line Transform  
  - Deep Learning–based object detection (YOLO)  
  - Behavioral Cloning (Imitation Learning)

---

## System Architecture
1. **Image Acquisition & Preprocessing**  
   - Frames captured from a front-mounted camera feed (or simulation feed).  
   - Gaussian blurring and Canny edge detection applied for noise reduction.  

2. **Lane Detection Pipeline**  
   - Edge-based lane marking detection using **Hough Line Transform**.  
   - Steering angle derived from the slope of the central virtual lane line.  

3. **Object Detection**  
   - Comparative analysis of R-CNN, Fast R-CNN, SSD, and YOLO architectures.  
   - YOLOv4 selected for optimal trade-off between accuracy and speed.  
   - Implemented multi-object detection for vehicles, pedestrians, and signals.  

4. **Imitation Learning in Unity**  
   - Configured a Unity-based driving environment for reinforcement and imitation learning.  
   - “Teacher” and “Student” neural networks trained through behavioral cloning to replicate driving behavior.  
   - Integrated with Python via `socket.io` for real-time control communication.  

---

## Results
- Achieved **93% accuracy** in object detection using the YOLOv4 model.  
- Lane detection system successfully calculated steering corrections with <0.4s latency per frame.  
- Integrated model demonstrated reliable navigation in Unity simulations, avoiding lane drift and obstacles.  
- YOLOv4 outperformed previous versions by **10% mAP improvement** and **12% higher FPS** during inference.  

---

## Challenges and Limitations
- Real-time model performance constrained by GPU memory during multi-object tracking.  
- Integration between Unity ML and Python required custom socket communication to overcome environment incompatibility.  
- Limited availability of high-quality labeled datasets for simulation-to-reality testing.  

---

## Future Work
- Implement real-world testing using Raspberry Pi or NVIDIA Jetson for edge deployment.  
- Expand the model to handle dynamic environments with pedestrians and complex traffic scenarios.  
- Integrate LiDAR and radar inputs for multimodal sensor fusion.  
- Explore reinforcement learning for adaptive path planning and decision-making.  

---

## Author
**Aashika Chakravarty**  
Bachelor of Engineering, Electronics and Communication  
PES Institute of Technology, Bangalore, India  
Email: aashikachakravarty@gmail.com  
LinkedIn: [linkedin.com/in/aashikachakravarty](https://www.linkedin.com/in/aashikachakravarty)
