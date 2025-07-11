# 🎯 Gesture-Controlled Volume Adjustment  
*Using CC3200 LaunchPad + Ultrasonic Sensor + Android App*  

![Project Banner](https://via.placeholder.com/800x200/2a2a72/FFFFFF?text=Gesture+Volume+Control+System) *(Replace with actual project image)*  

---

## 📋 Table of Contents  
- [Project Overview](#-project-overview)  
- [Hardware Requirements](#-hardware-requirements)  
- [Software Setup](#-software-setup)  
- [Installation Guide](#-installation-guide)  
- [How to Run](#-how-to-run)  
- [Code Structure](#-code-structure)  
- [Evaluation](#-evaluation)  

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
| HC-SR04 Sensor      | 1        | For distance measurement       |  
| Jumper Wires        | 4        | VCC, GND, Trig, Echo           |  
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
- Create your form [here](https://forms.google.com)  

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
1. Open `ultrasonic_http.ino` in Energia  
2. Update Wi-Fi credentials:  
```cpp
const char* ssid = "YOUR_WIFI";  
const char* password = "YOUR_PASSWORD";  
