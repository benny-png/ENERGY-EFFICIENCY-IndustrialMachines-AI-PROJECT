
---

# Energy Efficiency Industrial Machines AI Project

This project focuses on enhancing energy efficiency in industrial environments through advanced machine detection using YOLOv8. The system integrates sensors for real-time analysis and Augmented Reality (AR) for visual representation.

## Overview

The primary goal of this project is to implement a real-time machine detection system that uses YOLOv8 to monitor industrial machines. By integrating sensors and employing AR for visualization, the project aims to improve energy efficiency and operational monitoring.

### Key Components

1. **Real-Time Machine Detection**:
   - **YOLOv8 Model**: Utilizes YOLOv8 for detecting and classifying industrial machine components.
   - **Sensors Integration**: Collects real-time data on machine performance, which is used in conjunction with the detection system.

2. **Augmented Reality (AR) Visualization**:
   - **Planned AR Interface**: An interface for visualizing machine data and detection results through AR, allowing for enhanced interaction and monitoring.

## Real-Time Machine Detection

This section focuses on the real-time machine detection component of the project. It includes code files and configurations related to:

### Code Files

1. **`yolov_train.py`**:
   - **Purpose**: Contains the code for training the YOLOv8 model to detect and classify different machine components.
   - **Code Overview**:

     ```python
     from ultralytics import YOLO

     # Load the YOLOv8 model.
     model = YOLO('yolov8n.pt')

     # Train the model with the provided dataset.
     results = model.train(
         data='pothole_v8.yaml',
         imgsz=1280,
         epochs=50,
         batch=8,
         name='yolov8n_v8_50e'
     )
     ```

2. **`pyqt.py` (Future Development)**:
   - **Purpose**: Designed for developing a PyQt interface that will provide a graphical user interface (GUI) for interacting with the trained model and visualizing detection results. AR features will be integrated into this interface at a later stage.
   - **Code Overview**:

     ```python
     # pyqt.py - TEST INTERFACE a todo functionality...(later)
     val: ../valid/images
     test: ../test/images

     nc: 4
     names: ['motor', 'operador', 'plc', 'robot']
     ```

### Dataset

The dataset used for training is hosted on Roboflow and includes images for training, validation, and testing:

- **Workspace**: objectdetection-lqlxr
- **Project**: deteccion-de-objetos-r3lcr
- **Version**: 2
- **License**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- **Dataset URL**: [Roboflow Dataset](https://universe.roboflow.com/objectdetection-lqlxr/deteccion-de-objetos-r3lcr/dataset/2)

### Installation and Usage

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/ENERGY-EFFICIENCY-IndustrialMachines-AI-PROJECT.git
   cd ENERGY-EFFICIENCY-IndustrialMachines-AI-PROJECT
   ```

2. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

3. **Train the model**:

   ```python
   python yolov_train.py
   ```

4. **Develop the GUI** (Future Work):

   - Use of PYQT5 and Java app is in progress (hopefully might share) `pyqt.py` to create a testing interface for interacting with the detection results and implementing AR features.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to Ultralytics for providing YOLOv8 for object detection.
- Dataset sourced from Roboflow under CC BY 4.0.

---
