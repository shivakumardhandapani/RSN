# LIO-SLAM: LiDAR-Inertial Odometry SLAM with IEKF and Scan Context

This repository documents the implementation and analysis of a **LiDAR-Inertial Odometry SLAM (LIO-SLAM)** system enhanced by the **Iterative Extended Kalman Filter (IEKF)** and **Scan Context (SC)** framework. Designed as a final project for *EECE 5554: Robot Sensing and Navigation* at Northeastern University, this work focuses on enabling real-time, accurate SLAM for autonomous systems operating in complex and GPS-denied environments.

## 🚀 Project Objective

To develop and evaluate a tightly-coupled LIO-SLAM system that:
- Fuses high-frequency IMU data with high-resolution LiDAR scans
- Enhances accuracy using **IEKF** for robust state estimation
- Leverages **Scan Context** for loop closure detection and map refinement
- Integrates **GPS** data to reduce long-term drift

## 🔧 Core Components

### 📌 Sensor Fusion
- **LiDAR**: Provides spatial awareness through point clouds
- **IMU**: Offers temporal motion estimation
- **GPS** (optional): Corrects global path drift
- Sensors are synchronized and calibrated using custom pre-processing routines

### 🧠 Algorithmic Framework
- **Prediction** and **Update** steps based on IEKF to manage non-linear sensor fusion
- Loop closures detected via **ICP + Scan Context**
- Map refinement through iterative Kalman optimization
- Evaluation using **RMSE** metrics between estimated and true positions

### 📊 Evaluation Datasets
- **KITTI Odometry**
- **Livox-Horizon**
- **Ouster OS1-128**
- **KA-Urban** and **Park** datasets with GPS

## 📈 Key Results

- Demonstrated significantly reduced trajectory drift with loop closure enabled
- Achieved smoother, more accurate maps with IEKF + SC compared to baseline LIO-SAM
- Enhanced localization with GPS fusion, minimizing RMSE and improving real-time reliability
- Visualized system performance in urban environments and outdoor scenes (see figures on report)

## 📎 Figures and Visualizations

- **Page 4, Fig. 1**: Overall system framework flowchart
- **Page 4, Fig. 2**: Path visualization with/without loop closure
- **Page 5, Fig. 3**: Loop detection via Scan Context
- **Page 5, Fig. 4**: Mapping enhancement with IEKF and SC
- **Page 6, Fig. 5**: GPS fusion reducing IMU error

## 🧑‍💻 Contributors
- Palaniappan Yeagappan  
- Shiva Kumar Dhandapani  
- Sai Sreekar K S  
- Yogeshwaran Easwaran  

## 📅 Timeline
**February – April 2024**  
Course Project | EECE 5554 – Robot Sensing and Navigation  
Instructor: Prof. Thomas Consi, Northeastern University

## 📚 References
- [LIO-SAM: Tightly-coupled LiDAR-Inertial Odometry via Smoothing and Mapping](https://ieeexplore.ieee.org/document/9340839)  
- [LOAM: Lidar Odometry and Mapping in Real-Time](https://roboticsconference.org/proceedings/RSS2014/p32.pdf)  
- Additional referenced works listed on the project report
