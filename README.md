# IoT Environmental Monitoring & Anomaly Detection System

## About the Project

This project is a Python-based environmental monitoring system that analyzes temperature, humidity, and AQI (Air Quality Index) data.

I built this project to understand how sensor data from an IoT system can be collected, organized, analyzed, and used to identify unusual environmental conditions.

For the current version, I used simulated sensor readings instead of physical sensors. The project can later be connected to an ESP32 and real environmental sensors.

## What the Project Does

The system:

- Generates simulated temperature, humidity, and AQI readings
- Stores the readings using Python
- Converts the data into a Pandas DataFrame
- Analyzes the collected sensor data
- Detects anomalies using predefined threshold values
- Classifies each reading as `Normal` or `Hazardous`
- Calculates the percentage of normal and hazardous readings
- Visualizes temperature, humidity, and AQI readings
- Saves the processed data as a CSV file
- Identifies the readings classified as hazardous

## Anomaly Detection

The current version uses simple threshold-based detection.

A reading is considered anomalous when:

| Parameter | Threshold |
|-----------|-----------|
| Temperature | > 35°C |
| Humidity | > 80% |
| AQI | > 100 |

If any one of these parameters crosses its threshold, the overall environmental status for that reading is marked as **Hazardous**.

Otherwise, it is classified as **Normal**.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Google Colab
- CSV

## Project Workflow

```text
Simulated Sensor Data
        ↓
    Pandas DataFrame
        ↓
   Data Exploration
        ↓
 Threshold-based
 Anomaly Detection
        ↓
 Normal / Hazardous
 Classification
        ↓
 Data Visualization
        ↓
 CSV Export & Analysis
