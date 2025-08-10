# COVAS – Collision Avoidance and Vehicle Automation System
**COVAS** is a full-stack embedded vehicle safety solution built with STM32F407 microcontrollers, CAN protocol, and standard automotive sensors. Designed for modular deployment, it uses a two-node CAN network where a Transmitter Node collects sensor data (ultrasonic distance, rain status, temperature) and sends it to a Receiver Node that handles automatic braking and driver alerts in real-time.

---
## Overview

COVAS implements an **Automatic Braking System (ABS)** with environmental monitoring to enhance driver safety. The Transmitter Node detects obstacles, rain, and temperature; the Receiver Node processes this data to trigger braking, alerts, and visual indicators. The system is scalable for integration into modern automotive safety platforms.

## Features

- **Automatic Braking:** Stops the motor when an obstacle is detected within a threshold distance.
- **CAN-Based Communication:** High-speed, reliable data exchange between nodes.
- **Environmental Monitoring:** Real-time rain detection and temperature monitoring.
- **Driver Alerts:** LED and buzzer warnings for rain, high/low temperature, and obstacle detection.
- **Modular & Scalable:** CAN bus supports adding more sensors or nodes.

---

##  Tech & Infrastructure

### **Embedded Hardware**
- **MCUs:** 2× STM32F407 Discovery Boards (Cortex-M4, 168 MHz, 1 MB Flash)
- **CAN Transceivers:** MCP2551 (ISO-11898 compliant)
- **Motor Control:** L298N Motor Driver
- **Sensors:**
  - HC-SR04 Ultrasonic Sensor (obstacle detection)
  - LM35 Temperature Sensor
  - Rain Sensor Module (LM393-based)
- **Actuators:** DC motor, buzzer
- **Interface:** UART (CP2102) for debug/monitoring

### **Software**
- **Language:** Embedded C (STM32 HAL)
- **IDE:** STM32CubeIDE 1.18.0
- **Protocols & Interfaces:** CAN (11-bit standard frame), GPIO, UART, ADC, PWM, TIM

---
##  System Architecture

**Transmitter Node (TX):**
- Measures **distance**, **rain status**, and **temperature**
- Sends packaged data over CAN bus

**Receiver Node (RX):**
- Receives CAN messages
- Controls **braking motor** and **alerts** based on received data

---



# Video

https://github.com/user-attachments/assets/2dd8c873-0ebc-4af8-bd4b-ef24635d2ddc

---


# Photo
![COVAS](https://github.com/user-attachments/assets/cd1ded88-4478-42e4-b477-3780012d2ae3)
![COVAS-1](https://github.com/user-attachments/assets/0f05d4e4-977a-4a3d-ad8f-31c37a424af9)
