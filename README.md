## Overview
Welcome to the Smart City Project repository! This project is a demonstration of real-time data streaming using Apache Spark and Kafka. We simulate data from a vehicle traveling from Central London to Birmingham, capturing GPS locations, weather conditions, and road incidents along the way.
![image](https://github.com/user-attachments/assets/5f0a99d7-963e-444f-ae85-fc948cae9792)

## System Architecture
Kafka and Zookeeper Setup
Zookeeper manages the Kafka broker, ensuring data consistency.
Kafka handles the ingestion and storage of streaming data.
Apache Spark Setup
Spark Master and Worker Nodes are configured to process the streaming data.

All services are orchestrated using Docker Compose.

##Data Flow
Data Generation: Simulates vehicle movement, weather conditions, and emergency incidents.
Kafka Topics: Separate topics for each data type (vehicle, GPS, traffic, weather, emergency).
Spark Structured Streaming: Reads from Kafka, processes data, and writes it to AWS S3.
Data Generation

## The project simulates the following types of data:

Vehicle Data: Speed, direction, and type of vehicle.
GPS Data: Latitude, longitude, and timestamp.
Traffic Camera Data: Simulated camera snapshots.
Weather Data: Temperature, weather conditions, wind speed, etc.
Emergency Data: Incidents like accidents or police stops.
Streaming Pipeline
Kafka Topics Setup

## Each type of data is streamed into its own Kafka topic:

vehicle_data
gps_data
traffic_camera
weather_data
emergency_data
Spark Streaming
Spark reads the data from Kafka, processes it in real-time, and writes the output to AWS S3.
AWS Integration
# S3 Data Storage
Processed data is stored in an S3 bucket for further analysis.
# AWS Glue
An AWS Glue crawler is set up to catalog the data stored in S3.
# AWS Athena
Athena is used to query the data stored in S3, making it easy to analyze.
# Data Visualization
Used AWS Athena to query the processed data.
To Visualize the results we used tool PowerBI.
# Conclusion
This project showcases a comprehensive approach to building a smart city application using real-time data streaming. The setup involves Apache Spark, Kafka, Docker, and AWS services like S3, Glue, and Athena.
