# 🤖 Dual Car Robotics Projects: ESP32-CAM Web Controlled Car & Arduino Line Follower

This repository contains two exciting embedded systems projects:

1. **ESP32-CAM Based WiFi Car with Live Camera and Web Controls**
2. **Arduino Line Following Robot using IR Sensors**

---

## 📸 Project 1: ESP32-CAM Web Controlled Car

### 🚗 Features
- Live video stream from ESP32-CAM
- Web-based user interface for:
  - Car movement (forward, backward, left, right, stop)
  - Speed control
  - Headlight brightness control
  - Camera pan/tilt using servo motors

### 🔧 Hardware Required
- ESP32-CAM module
- 2 DC motors (left & right wheels)
- L298N or similar motor driver module
- 2 servo motors (for pan and tilt)
- Light (LED)
- Power source (battery or USB)
- Jumper wires, breadboard or chassis

### 📶 How It Works
- ESP32 creates its own WiFi hotspot:  
  **SSID:** `For the love of PHYSICS`  
  **Password:** `12345678`
- User connects to this WiFi via phone/laptop and visits the IP shown in the serial monitor (`192.168.4.1`)
- Web interface is loaded, allowing live view and control

### 📁 File
- `esp32_camera_car.ino` - Full ESP32 sketch with WebSockets, HTML UI, motor, light, and servo control.

---

## ⚫ Project 2: Arduino Line Following Car

### 🤖 Features
- Robot follows a black line on a white surface using IR sensors
- Automatically moves forward, turns left/right, or stops based on sensor input

### 🔧 Hardware Required
- Arduino Uno
- L293D Motor Driver Shield (AFMotor)
- 4 DC motors
- 2 IR sensors
- Power source (battery)
- Chassis, wheels, jumper wires

### 🧠 Logic
- **Both sensors detect black:** Move forward
- **Left sensor on black, right off:** Turn left
- **Right sensor on black, left off:** Turn right
- **Both sensors off:** Stop

### 📁 File
- `line_follower.ino` - Arduino sketch using AFMotor library

> ⚠️ Make sure to install the **AFMotor** library for the Arduino project.  
Go to **Sketch > Include Library > Add .ZIP Library** in the Arduino IDE.

---



## 🛠 Installation Notes

### ESP32 Setup
- Use **Arduino IDE**
- Select Board: `AI Thinker ESP32-CAM`
- Install libraries:
  - `ESPAsyncWebServer`
  - `ESPAsyncTCP`
  - `ESP32Servo`
- Upload the code, open serial monitor, and connect to the AP

### Arduino Setup
- Use **Arduino IDE**
- Install `AFMotor` library
- Upload to Arduino Uno

---

## 💡 Future Improvements
- Add obstacle detection to both bots
- Integrate both features in one robot (manual + auto)
- Control via Android app instead of web

---



---


