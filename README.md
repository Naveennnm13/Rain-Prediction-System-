# Rain-Prediction-System-
# IoT and Wireless Sensor Network (WSN) Based Data Logger System with Rain Prediction using Machine Learning

## Project Overview
This project presents an intelligent, scalable, and cost-effective solution for real-time monitoring in agriculture using an IoT-enabled Wireless Sensor Network (WSN). The system collects environmental data, stores it in the cloud, and applies machine learning tree based algorithms to predict rainfall, enabling optimized irrigation planning.

## Features
- Wireless Sensor Network for real-time environmental data collection
- Battery-powered and solar-rechargeable sensor nodes
- **ESP-NOW** and **UART** protocols for efficient communication
- Real-time data storage using **Google Firebase**
- Rainfall prediction using **Tree Based algorithms**
- Modular architecture allowing plug-and-play sensor integration
- End-to-end system tested with complete ML pipeline

## Tech Stack
### Hardware
- NodeMCU ESP8266 (Sensor Node)
- ESP32 (Master Node)
- DHT11 (Temperature and Humidity Sensor)
- Soil Moisture Sensor
- Rain Sensor
- TP4056 Battery Management

### Software
- Arduino IDE (Embedded Programming)
- Python (ML Processing)
- Firebase (Cloud Database and Hosting)
- Python Libraries: pandas, numpy, matplotlib, scikit-learn

## Architecture
1. **Sensor Nodes**: Collect data using DHT11, soil moisture, and rain sensors.
2. **Sink Node (ESP8266)**: Gathers data from multiple sensor nodes via ESP-NOW.
3. **Master Node (ESP32)**: Sends data to Firebase over Wi-Fi using HTTP.
4. **Firebase**: Stores and visualizes real-time data.
5. **ML Model (Python)**: Uses multivariate linear regression to predict rainfall.

## Project Modules
### 1. Sensor Node
- Collects environmental data
- Transmits using ESP-NOW

### 2. Sink Node
- Acts as a gateway
- Forwards data to master node

### 3. Master Node
- Pushes data to Firebase in real-time

### 4. ML Rain Prediction
- Uses a dataset to train a linear regression model
- Predicts rainfall based on real-time input

## How to Run
### Hardware Setup
- Flash microcontrollers using Arduino IDE with provided code
- Power sensor nodes using 3.7V lithium-ion batteries

### Firebase Setup
- Create Firebase project
- Enable Real-Time Database
- Add API key and user credentials in ESP32 code

### Machine Learning
```bash
# Install dependencies
pip install pandas numpy matplotlib scikit-learn

# Run prediction script
python rain_prediction.py
```

## Repository Structure
```
IoT-WSN-Rain-Predictor/
├── arduino_code/
│   ├── sensor_node.ino
│   ├── sink_node.ino
│   └── master_node.ino
├── ml_model/
│   ├── rain_prediction.py
│   └── dataset.csv
├── documentation/
│   └── project_report.pdf
├── firebase_config/
│   └── firebase_setup.json
└── README.md
```

## Results
- Real-time monitoring dashboard
- Rain prediction with ~85% accuracy
- System validated on agricultural test beds

## Applications
- Precision agriculture
- Smart irrigation
- Climate-aware farming

## Future Work
- Integration with automated drip irrigation
- Solar power optimization
- Support for additional crops and soil types
- Mobile app for field-level monitoring

## Contributors
- Aakarsh Satyam
- Lavanya R
- M. V. Narasimha Prasad
- Naveen N. N. M

## Academic Details
- Institution: Dayananda Sagar Academy of Technology and Management
- Department: Electronics and Communication Engineering
- Year: 2021-2022
