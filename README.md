# 🎯 Gesture-Controlled Volume Adjustment  
*Using CC3200 LaunchPad + Ultrasonic Sensor + Android App*  

<img width="1493" height="856" alt="image" src="https://github.com/user-attachments/assets/62d83be7-f0d1-43e6-af5f-dd29b7ee1e9c" />


---

## 📋 Table of Contents  
- [Project Overview](#-project-overview)  
- [Hardware Requirements](#-hardware-requirements)  
- [Software Setup](#-software-setup)  
- [Installation Guide](#-installation-guide)  
- [How to Run](#-how-to-run)  
- [Code Structure](#-code-structure)  

---

## 🔍 Project Overview  
A smart system that:  
- 📏 Measures hand distance using an **ultrasonic sensor**  
- 📱 Communicates with an **Android app via HTTP** to adjust device volume  
- 📊 Collects user feedback via **Google Forms**  

**Key Components**:  
| Type       | Components                          |
|------------|-------------------------------------|
| Hardware   | CC3200 LaunchPad, HC-SR04 Sensor    |
| Software   | Energia IDE, Android Studio         |

---

## 🛠️ Hardware Requirements  
| Component           | Quantity | Notes                          |  
|---------------------|----------|--------------------------------|  
| CC3200 LaunchPad    | 1        | Wi-Fi enabled microcontroller  |  
| Ultrasonic Sensor   | 1        | For distance measurement       |  
| Jumper cable        | 1        | VCC, GND, Trig, Echo           |  
| Micro-USB Cable     | 1        | For power and programming      |  

---

## 💻 Software Setup  
### 1. Energia IDE (CC3200 Programming)  
- Download [Energia IDE](http://energia.nu/download/)  
- Install CC3200 board support via **Tools → Board → Boards Manager**  

### 2. Android Studio (Companion App)  
- Install [Android Studio](https://developer.android.com/studio)  
- Open the provided `Android_app` project  

### 3. Google Forms (Survey)  
- Create your form [here]([https://forms.google.com](https://docs.google.com/forms/d/e/1FAIpQLSc81LrK-BMuI_YL7YnHIu7k_sjG8p39c47EGHD46PVpbT4Fgw/viewform?usp=header))  

---

## ⚙️ Installation Guide  
### Hardware Connections  
| Sensor Pin | CC3200 Pin |  
|------------|------------|  
| VCC        | 3.3V       |  
| GND        | GND        |  
| Trig       | P2.1       |  
| Echo       | P2.2       |  

### Firmware Setup  
1. Open `GestureContrrolApp.ino` in Energia  
2. Update Wi-Fi credentials:  
```cpp
const char* ssid = "YOUR_WIFI";  
const char* password = "YOUR_PASSWORD";
```

---

## 💻 How to Run
### 1. Power the CC3200 (check Serial Monitor for Wi-Fi status)

### 2. Launch Android app and verify connection

Gesture Control:

👆 Hand closer → Volume decreases

✋ Hand farther → Volume increases

---

## 💻 Code Structure

GestureControlApp/  
│  
├── /Energia_code/                                           # CC3200 Firmware  
│   ├── GestureContrrolApp.ino                               # Main logic + HTTP server  
│  
├── /Android_app/                                            # Android Studio Project  
│   ├── MainActivity.java                                    # HTTP client for volume control  
│  
├── /GestureControlApp_Bharath Subramaniam Jayakumar.pdf/    # Presentation  
│  
└── README.md                                                # This file  
