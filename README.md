# **Automated Quality Control AI System for Manufacturing**

This repository contains an AI-powered automated quality control system designed for real-time defect detection and predictive maintenance in manufacturing. By leveraging computer vision and machine learning, the system identifies defects in products and provides insights into machine performance for proactive maintenance.

## **Key Features**
- **Real-Time Defect Detection**: Utilizes Computer Vision (CV) models to identify surface defects, such as:
  - Crazing
  - Inclusion
  - Patches
  - Pitted surfaces
  - Rolled-in scale
  - Scratches
- **Predictive Maintenance**: Analyzes sensor data to predict machine failures and recommend preventive actions.
- **Edge Deployment Ready**: Supports edge devices like Raspberry Pi or NVIDIA Jetson for decentralized, real-time production line monitoring.
- **Data-Driven Insights**: Provides actionable insights and optimization strategies based on visual defect detection and sensor data analysis.
- **Interactive Dashboard**: A web-based interface for visualizing defect detection results and real-time sensor data, allowing operators to make informed decisions.

## **Tech Stack**
- **Python**: Core programming language for machine learning and system logic.
- **TensorFlow / PyTorch**: For training and deploying defect detection and predictive maintenance models.
- **OpenCV**: For capturing and processing video frames in real-time.
- **Flask**: Backend framework for serving the dashboard and handling interactions between the front end and the machine learning models.
- **HTML/CSS/JavaScript**: Used to create an interactive and user-friendly web interface (dashboard).
- **Google Cloud** (optional): For cloud deployment, real-time monitoring, and model management via Vertex AI and IoT solutions.

## **How to Use**
### **1. Defect Detection**
- Run the following command for real-time defect detection using a webcam or video feed:
  ```bash
  python test_defect_detection.py
  ```
- Customize the video input source and model parameters in the script as needed.

### **2. Predictive Maintenance**
- To analyze sensor data and predict machine failures, run:
  ```bash
  python test_predictive_maintenance.py
  ```
- Adjust the sensor data input and model configuration based on your specific manufacturing setup.

### **3. Interactive Dashboard**
- To interact with the system via a web-based dashboard, serve the `index.html` using Flask:
  ```bash
  python app.py
  ```
- Visit `http://127.0.0.1:5000` in your browser to:
  - View real-time defect detection from the video feed.
  - Analyze sensor data and predictions in the dashboard.

## **Directory Structure**
```
├── data
│   ├── images
│   │   └── NEU-DET
│   │       ├── train
│   │       │   └── images
│   │       └── validation
│   │           └── images
│   ├── sensor_data
├── models
│   └── defect_detection_model.h5
│   └── predictive_maintenance_model.pkl
├── test_defect_detection.py
├── test_predictive_maintenance.py
├── app.py
├── templates
│   └── index.html
└── README.md
```

## **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/quality_control_ai.git
   ```
2. Navigate into the project directory:
   ```bash
   cd quality_control_ai
   ```
3. Set up the virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scriptsctivate
   ```
4. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## **Future Work**
- Integrate with cloud services for distributed monitoring.
- Enhance the user interface for better visualization of the data.
- Expand support for additional types of defects and sensors.

## **Contributing**
Pull requests are welcome! For significant changes, please open an issue first to discuss what you would like to change.
