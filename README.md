#ESP32 Smart Bin
An automatic smart trash bin prototype built with ESP32, an ultrasonic sensor, and a servo motor. The system detects a nearby object and automatically opens the lid, providing a simple touch-free waste disposal experience. This project was designed as a beginner-friendly embedded systems and IoT project using Arduino IDE.
#Overview
The Smart Bin is a compact prototype that demonstrates how sensors and actuators can be integrated using an ESP32 microcontroller. Instead of using a conventional trash bin, a coffee cup was used as the prototype body to simplify development while demonstrating the complete functionality.

When an object (such as a hand or trash) is detected within a specified distance, the ultrasonic sensor sends data to the ESP32. The ESP32 processes the distance measurement and rotates the servo motor to open the lid. After a short delay, the lid automatically closes.
#Learning Outcomes
This project demonstrates practical experience with:

- Embedded Systems
- ESP32 Programming
- Arduino IDE
- Sensor Integration
- Servo Motor Control
- Basic Automation
- Internet of Things (IoT) Prototyping
- Rapid Hardware Prototyping
#Technologies Used
- ESP32
- Arduino IDE
- C++
- HC-SR04 Ultrasonic Sensor
-   SG90 Servo Motor
#Features
- Automatic lid opening
- Contactless operation
- Distance detection using ultrasonic sensor
- Simple Arduino-based implementation
- Low-cost prototype
- Beginner-friendly hardware and software

#Hardware Components
| Component                  | Quantity |
| -------------------------- | -------- |
| ESP32 Development Board    | 1        |
| HC-SR04 Ultrasonic Sensor  | 1        |
| SG90 Micro Servo Motor     | 1        |
| Coffee Cup (Prototype Bin) | 1        |
| Jumper Wires               | Several  |
| Breadboard (Optional)      | 1        |
| USB Cable                  | 1        |

#System Architecture
          Object Detected
                 │
                 ▼
      HC-SR04 Ultrasonic Sensor
                 │
          Distance Measurement
                 │
                 ▼
              ESP32
      Decision Processing
                 │
      Distance < Threshold?
           Yes / No
                 │
          Yes ───┘
                 ▼
         Rotate Servo Motor
                 │
           Open Bin Lid
                 │
          Wait Few Seconds
                 │
                 ▼
          Close Bin Lid
#Circuit Connection
- Ultrasonic Sensor
  | HC-SR04 | ESP32   |
| ------- | ------- |
| VCC     | 5V      |
| GND     | GND     |
| TRIG    | GPIO 5  |
| ECHO    | GPIO 18 |

- Servo Motor
  | Servo             | ESP32   |
| ----------------- | ------- |
| Red (VCC)         | 5V      |
| Brown/Black (GND) | GND     |
| Orange (Signal)   | GPIO 13 |

#Future Improvements
- OLED display for status information
- Battery-powered operation
- Infrared sensor for improved detection
- IoT monitoring via Wi-Fi
- Mobile application integration
- Fill-level detection
- Automatic garbage level monitoring
- Buzzer notifications
- Energy-saving sleep mode
- Voice assistant integration

#Applications
- Smart homes
- Contactless waste bins
- School IoT demonstrations
- Embedded systems learning
- Automation projects
- Engineering education
