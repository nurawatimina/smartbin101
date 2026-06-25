# 🗑️ ESP32 Smart Bin

![Arduino](https://img.shields.io/badge/Arduino-IDE-blue?logo=arduino)
![ESP32](https://img.shields.io/badge/ESP32-IoT-red)
![Language](https://img.shields.io/badge/Language-C%2B%2B-blue)
![Platform](https://img.shields.io/badge/Platform-Arduino-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

A compact **touchless smart trash bin** prototype powered by an **ESP32**, **HC-SR04 Ultrasonic Sensor**, and **SG90 Servo Motor**. The system automatically opens the lid when an object is detected nearby, providing a simple demonstration of embedded systems, automation, and IoT concepts.

> **Prototype:** Coffee cup used as the trash bin for rapid prototyping.

---

## 📖 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Hardware Components](#hardware-components)
- [System Workflow](#system-workflow)
- [Circuit Connections](#circuit-connections)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Demo](#demo)
- [Future Improvements](#future-improvements)
- [Learning Outcomes](#learning-outcomes)
- [License](#license)

---

# Overview

The ESP32 Smart Bin is an automation project designed to demonstrate how sensors and actuators interact within an embedded system.

The ultrasonic sensor continuously measures the distance to nearby objects. When a hand or piece of trash is detected within a predefined threshold, the ESP32 commands the servo motor to open the lid automatically. After a short delay, the lid closes again.

This project emphasizes simplicity while introducing fundamental IoT and embedded programming concepts.

---

# Features

- ✅ Automatic lid opening
- ✅ Contactless waste disposal
- ✅ Ultrasonic distance detection
- ✅ Servo-controlled lid
- ✅ ESP32 microcontroller
- ✅ Easy Arduino IDE implementation
- ✅ Beginner-friendly project

---

# Hardware Components

| Component | Quantity |
|-----------|----------|
| ESP32 Dev Board | 1 |
| HC-SR04 Ultrasonic Sensor | 1 |
| SG90 Servo Motor | 1 |
| Coffee Cup (Prototype Bin) | 1 |
| Jumper Wires | Several |
| Breadboard (Optional) | 1 |
| USB Cable | 1 |

---

# System Workflow

```text
        Object Detected
               │
               ▼
     HC-SR04 Measures Distance
               │
               ▼
            ESP32
               │
   Distance < Threshold ?
         │          │
        Yes         No
         │          │
         ▼          ▼
  Rotate Servo     Wait
         │
         ▼
     Open Lid
         │
         ▼
      Delay
         │
         ▼
     Close Lid
```

---

# Circuit Connections

## Ultrasonic Sensor

| HC-SR04 | ESP32 |
|----------|--------|
| VCC | 5V |
| GND | GND |
| TRIG | GPIO 5 |
| ECHO | GPIO 18 |

---

## Servo Motor

| Servo | ESP32 |
|--------|--------|
| VCC | 5V |
| GND | GND |
| Signal | GPIO 13 |

> GPIO pins may be modified in the source code.

---

# Project Structure

```text
ESP32-Smart-Bin
│
├── SmartBin.ino
├── README.md
│
├── images
│   ├── prototype.jpg
│   ├── wiring.jpg
│   └── demo.gif
│
└── diagrams
    ├── circuit.png
    └── flowchart.png
```

---

# Installation

## Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/ESP32-Smart-Bin.git
```

---

## Open Arduino IDE

Install the ESP32 Board Package:

```
Tools
→ Board
→ Board Manager
→ Search "ESP32"
→ Install
```

---

## Install Library

Install:

```
ESP32Servo
```

---

## Upload Program

Select

```
Board:
ESP32 Dev Module
```

Choose the correct COM port and upload the sketch.

---

# Usage

1. Power the ESP32.
2. Place an object within approximately **15 cm** of the ultrasonic sensor.
3. The servo rotates to open the lid.
4. After several seconds, the lid automatically closes.

---

# Example Code

```cpp
if(distance <= 15){
    servo.write(90);
    delay(3000);
    servo.write(0);
}
```

---

# Demo

## Prototype

Coffee cup prototype

```
          _________
         /         \
        /           \
       |   COFFEE    |
       |     CUP     |
       |-------------|
       |             |
       | SMART  BIN  |
       |             |
       |_____________|

      Ultrasonic Sensor

             ESP32
               │
         Servo Motor
```

---

## Serial Monitor Output

```
Distance : 42 cm
Distance : 25 cm
Distance : 13 cm

Opening Lid...

Closing Lid...

Distance : 40 cm
```

---

# Future Improvements

- OLED Display
- Battery Operation
- Wi-Fi Monitoring
- Mobile Application
- Fill Level Detection
- Firebase Integration
- Telegram Notification
- Voice Assistant Support
- Energy Saving Mode
- Smart Waste Classification

---

# Learning Outcomes

This project demonstrates knowledge of:

- Embedded Systems
- ESP32 Programming
- Arduino IDE
- C++
- Sensor Integration
- Servo Motor Control
- Automation
- IoT Prototyping

---

# Technologies

- ESP32
- Arduino IDE
- C++
- HC-SR04
- SG90 Servo

---

# Repository Contents

```
📦 ESP32-Smart-Bin
 ┣ 📂images
 ┣ 📂diagrams
 ┣ 📜SmartBin.ino
 ┣ 📜README.md
 ┗ 📜LICENSE
```

---

# License

This project is licensed under the **MIT License**.

---

# Author

**Nurawati Mina**

Master of Information Technology

- AI
- IoT
- Embedded Systems
- Educational Technology

---

⭐ If you found this project useful, consider giving it a star!
