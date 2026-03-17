# Smart Rehabilitation Walker System

A proof-of-concept smart walker platform designed to enhance rehabilitation through real-time biofeedback, fall detection, and data-driven progress tracking. This system integrates embedded hardware, a mobile application, and a cloud-based web dashboard to provide users and clinicians with actionable insights into mobility and recovery.

## Overview

This project transforms a standard walker into an intelligent rehabilitation device by measuring user-applied pressure, detecting instability, and tracking activity over time. Data flows seamlessly from embedded sensors to a mobile app and into a cloud backend, where it can be visualized and analyzed.

### Key Features
- **Pressure Monitoring:** Measures bilateral handle force to assess user reliance and asymmetry  
- **Fall Detection & Alerts:** Detects instability and provides haptic feedback
- **Real-Time Data Streaming:** BLE communication from embedded system to mobile app  
- **Cloud Integration:** REST API pipeline for data storage and retrieval  
- **Progress Visualization:** Web dashboard displaying trends and rehabilitation metrics  

---

## System Architecture

```
[Pressure Sensors]
↓
[ESP32 (Embedded System)]
↓ (BLE)
[Mobile App]
↓ (REST API)
[Cloud Backend + Database]
↓
[Web Dashboard]
```

---

## Repositories

### 1. Embedded System (MCU)
**Repo:** [`Handles`](https://github.com/CPE-Walker-Capstone-25-26/Handles)

Firmware for the ESP32-based smart walker handles.

**Responsibilities:**
- Read and process pressure sensor data  
- Detect instability and trigger haptic feedback  
- Transmit real-time data via Bluetooth Low Energy (BLE)  

**Technologies:**
- ESP32  
- Embedded C/C++  
- BLE (Bluetooth Low Energy)  

---

### 2. Mobile Application
**Repo:** [`Mobile-App`](https://github.com/CPE-Walker-Capstone-25-26/Mobile-App)

Mobile interface for real-time monitoring and data transmission.

**Responsibilities:**
- Connect to ESP32 via BLE  
- Display live pressure and activity data  
- Send collected data to backend via REST API  
- Notify users of instability events  

**Technologies:**
- BLE integration  
- REST API communication  
- Swift

---

### 3. Web Server & Dashboard
**Repo:** [`Web-Server`](https://github.com/CPE-Walker-Capstone-25-26/Web-Server)

Backend services and web dashboard for data storage and visualization.

**Responsibilities:**
- Provide REST API endpoints for data ingestion  
- Store sensor and activity data in cloud database  
- Serve a web dashboard for graphical visualization  

**Technologies:**
- REST APIs  
- Cloud database (MongoDB)  
- Web framework (Node.js, Express.js)

---

## Data Flow

1. Pressure sensors collect force data from walker handles  
2. ESP32 processes and transmits data via BLE  
3. Mobile app receives and forwards data through REST endpoints  
4. Backend stores data in the cloud database  
5. Web dashboard visualizes user progress and trends  

---

## Goals

- Improve rehabilitation outcomes through measurable feedback  
- Enhance user safety with real-time fall detection  
- Provide clinicians with actionable recovery data  
- Create a scalable, adaptable system for various mobility needs  

---

## Contributors

Senior Capstone Project – Cal Poly  
In collaboration with stroke survivor advocate Carl Sloan  

---

## Future Work

- Advanced analytics for rehabilitation insights  
- Machine learning for fall prediction  
- Expanded compatibility with assistive devices  
- Improved accessibility and UI/UX for diverse users  
