
# GreenSense – IoT Smart Garden System 🌱

GreenSense is an intelligent IoT-based smart garden system designed to automate plant monitoring and irrigation using real-time sensor data, mobile control, and AI-powered plant analysis.

The system helps reduce manual plant care by monitoring soil moisture, detecting light conditions, controlling a water pump automatically, sending alerts through Blynk, and supporting AI-based plant identification and health analysis.

---

## 📌 Project Overview

Traditional gardening often depends on manual watering and guesswork. This can lead to:

- Overwatering
- Underwatering
- Poor plant growth
- Delayed disease detection
- Plant damage when users are away

GreenSense solves this problem by using an ESP8266 microcontroller, sensors, automation logic, and a mobile dashboard to monitor and manage plant care more efficiently.

---

## 🎯 Aim

To develop a low-cost smart garden system that can monitor soil conditions, automate irrigation, notify users, and provide AI-powered plant insights.

---

## ✅ Key Features

### 🌱 Smart Monitoring
- Soil moisture monitoring
- Light condition detection using LDR
- Real-time data display through Blynk

### 💧 Automated Irrigation
- Automatically turns the water pump ON/OFF based on soil moisture
- Uses threshold-based watering logic
- Prevents unnecessary watering

### ☀️ Climate-Aware Logic
- Detects bright and dark conditions
- Supports smarter watering decisions based on environmental conditions

Example logic:

```text
Dry Soil + Bright Condition = Water plant
Dry Soil + Dark Condition = Delay watering
Wet Soil = Stop pump
Sensor failure = Stop pump for safety


System Architecture

Soil Moisture Sensor ─┐
                      ├──> ESP8266 NodeMCU ───> Relay Module ───> Water Pump
LDR Sensor ───────────┘
                              │
                              ▼
                         Blynk IoT App
                              │
                              ▼
                    Alerts, Monitoring & Control
