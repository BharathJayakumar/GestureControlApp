🎯 Gesture-Controlled Volume Adjustment
*Using CC3200 LaunchPad + Ultrasonic Sensor + Android App*
<hr style="border: 1px dashed #ccc" />  
📋 Table of Contents
Project Overview

Hardware Requirements

Software Setup

Installation Guide

How to Run

Code Structure

Evaluation Link

<hr style="border: 1px dashed #ccc" />  

# Section 1  
🔍 Project Overview
A smart system that:

📏 Measures hand distance using an ultrasonic sensor.

📱 Communicates with an Android app via HTTP to adjust device volume.

📊 Collects user feedback via Google Forms.

Key Components:

Hardware: CC3200 LaunchPad, HC-SR04 Ultrasonic Sensor.

Software: Energia IDE, Android Studio, Google Forms.
# Section 2
🛠️ Hardware Requirements
Component	Quantity	Notes
CC3200 LaunchPad	1	Wi-Fi enabled microcontroller.
HC-SR04 Sensor	1	For distance measurement.
Jumper Wires	4	VCC, GND, Trig, Echo.
Micro-USB Cable	1	For power and programming.
# Section 3
💻 Software Setup
1. Energia IDE (CC3200 Programming)
Download Energia IDE.

Install CC3200 board support via Tools → Board → Boards Manager.

2. Android Studio (Companion App)
Install Android Studio.

Open the provided Android_app project.

3. Google Forms (Survey)
Create a form here and link it in the Android app.
# Section 4
⚙️ Installation Guide
Step 1: Hardware Connections
Connect the HC-SR04 to the CC3200:

Sensor Pin	CC3200 Pin
VCC	3.3V
GND	GND
Trig	P2.1
Echo	P2.2
Step 2: Upload Firmware
Open ultrasonic_http.ino in Energia.

Update Wi-Fi credentials:

cpp
const char* ssid = "YOUR_WIFI";  
const char* password = "YOUR_PASSWORD";  
Upload to the CC3200 (Sketch → Upload).

Step 3: Android App Setup
Update the CC3200’s IP in MainActivity.java:

java
String url = "http://YOUR_IP_ADDRESS/sensor";  
Build and run the app.
# Section 5
🚀 How to Run
Power the CC3200 and check Serial Monitor for Wi-Fi status.

Launch the Android app and ensure it connects to the CC3200.

Wave your hand to test:

👆 Closer → Volume decreases.

✋ Farther → Volume increases.


# Section 6
📂 Code Structure
text
project-root/  
│  
├── /energia_code/            # CC3200 Firmware  
│   ├── ultrasonic_http.ino    # Main logic + HTTP server  
│  
├── /Android_app/              # Android Studio Project  
│   ├── MainActivity.java      # HTTP client for volume control  
│  
├── /docs/                     # Schematics & Datasheets  
│  
└── README.md                  # This file  


# Section 7
📊 Evaluation Link
Integrated Google Form link in the Android app:
🔗 https://docs.google.com/forms/d/e/1FAIpQLSc81LrK-BMuI_YL7YnHIu7k_sjG8p39c47EGHD46PVpbT4Fgw/viewform?usp=header
