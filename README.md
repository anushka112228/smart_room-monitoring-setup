Smart Room Monitoring and Automation System
Overview

The Smart Room Monitoring and Automation System is an embedded system project built using the Arduino platform.
The system integrates multiple sensors to monitor environmental conditions and automate room lighting based on motion and ambient light.

The system detects human motion, measures ambient light intensity, monitors temperature and humidity, and calculates the distance of nearby objects. Based on these sensor readings, the controller automatically performs actions such as turning lights ON or OFF and displaying real-time sensor data on the serial monitor.

This project demonstrates how multiple sensors can be integrated with a microcontroller to build a simple smart environment monitoring and automation system.

Hardware Components
Component	Description
Arduino Uno	Main microcontroller used for sensor interfacing and processing
PIR Motion Sensor	Detects human motion
LDR (Photoresistor)	Detects ambient light level
DHT11 Sensor	Measures temperature and humidity
Ultrasonic Sensor (HC-SR04)	Measures distance of nearby objects
LED	Used as lighting output
Breadboard	Circuit assembly
10kΩ Resistor	Used for LDR voltage divider
220Ω Resistor	LED current limiting resistor
System Working Principle

The system works by collecting environmental data from multiple sensors connected to the Arduino controller.

The PIR sensor detects motion in the room.

The LDR measures the ambient light level.

If motion is detected and the room is dark, the Arduino turns the LED ON automatically.

The DHT11 sensor continuously measures temperature and humidity.

The Ultrasonic sensor measures the distance of nearby objects.

All sensor readings are displayed on the Serial Monitor.

This demonstrates sensor integration, decision logic, and automated response in an embedded system.

System Logic / Behaviour Cases
Condition	System Response
Motion detected AND room is dark	LED turns ON
Motion detected BUT room is bright	LED remains OFF
No motion detected	LED turns OFF
Object detected by ultrasonic sensor	Distance displayed on Serial Monitor
Temperature change detected	Updated temperature displayed
Humidity change detected	Updated humidity displayed
Circuit Connections
PIR Motion Sensor

VCC → 5V
GND → GND
OUT → Digital Pin 2

LDR (Voltage Divider)

5V → LDR → A0
A0 → 10kΩ Resistor → GND

Ultrasonic Sensor (HC-SR04)

VCC → 5V
GND → GND
TRIG → Pin 7
ECHO → Pin 6

DHT11 Sensor

VCC → 5V
GND → GND
DATA → Pin 4

LED

Pin 9 → 220Ω Resistor → LED → GND

Tools Used

    Arduino IDE
    Tinkercad Circuits Simulator
    Serial Monitor

    

    
