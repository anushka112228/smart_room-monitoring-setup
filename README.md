# Smart Room Monitoring and Automation System

## Overview
The Smart Room Monitoring and Automation System is an Arduino-based project that integrates multiple sensors to monitor environmental conditions and automate lighting in a room.

The system detects motion, measures ambient light, monitors temperature and humidity, and calculates object distance. Based on sensor readings, the system automatically controls lighting and displays real-time data on the serial monitor.

This project demonstrates how multiple sensors can be integrated with a microcontroller to build a simple smart environment monitoring system.

---

## Features

- Motion detection using PIR sensor
- Automatic lighting control using LDR
- Temperature and humidity monitoring
- Distance measurement using ultrasonic sensor
- Real-time data display through serial monitor
- Energy-efficient lighting control

---

## Hardware Components

| Component | Description |
|-----------|-------------|
| Arduino Uno | Main microcontroller |
| PIR Motion Sensor | Detects human motion |
| LDR (Photoresistor) | Detects ambient light level |
| DHT11 Sensor | Measures temperature and humidity |
| Ultrasonic Sensor HC-SR04 | Measures distance of nearby objects |
| LED | Lighting output indicator |
| Breadboard | Circuit assembly |
| Resistors | Voltage divider and current limiting |

---

## System Working Principle

The system works by collecting data from different sensors connected to the Arduino controller.

1. PIR sensor detects motion in the room.
2. LDR measures ambient light intensity.
3. If motion is detected and the room is dark, the LED automatically turns ON.
4. DHT11 sensor measures temperature and humidity of the room.
5. Ultrasonic sensor measures the distance of nearby objects.
6. All sensor data is displayed on the Arduino Serial Monitor.

---

## System Logic

| Condition | System Response |
|----------|----------------|
| Motion detected + Dark room | LED turns ON |
| Motion detected + Bright room | LED remains OFF |
| No motion detected | LED turns OFF |
| Object detected near ultrasonic sensor | Distance displayed |
| Temperature/Humidity changes | Updated on serial monitor |

---

## Circuit Connections

### PIR Sensor
VCC → 5V  
GND → GND  
OUT → Digital Pin 2  

### LDR (Voltage Divider)
5V → LDR → A0  
A0 → 10kΩ resistor → GND  

### Ultrasonic Sensor HC-SR04
VCC → 5V  
GND → GND  
TRIG → Pin 7  
ECHO → Pin 6  

### DHT11 Sensor
VCC → 5V  
GND → GND  
DATA → Pin 4  

### LED
Pin 9 → 220Ω Resistor → LED → GND  

---

## Project Structure
