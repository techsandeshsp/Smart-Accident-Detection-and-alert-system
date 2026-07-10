# 🚨 Smart Accident Detection and Alert System

An IoT-based **Smart Accident Detection and Alert System** that detects vehicle accidents using a vibration/impact sensor and instantly sends a **WhatsApp alert** with the vehicle's live GPS location. The project is built using **NodeMCU (ESP8266)**, **GPS Module (Neo-6M)**, and the **UltraMsg WhatsApp API** to provide quick emergency notifications.

---

## 📖 Overview

Road accidents often require immediate medical assistance. This project automatically detects a possible accident by monitoring sudden impacts through a sensor. Once an accident is detected, the system retrieves the current GPS coordinates and sends an emergency WhatsApp message containing the live location to a predefined contact.

If GPS is unavailable, the system still notifies the emergency contact that an accident has been detected.

---

## ✨ Features

* 🚗 Automatic accident detection using an impact/vibration sensor
* 📍 Real-time GPS location tracking
* 💬 Instant WhatsApp emergency alerts
* 🌐 Google Maps location link included in the message
* 📶 Wi-Fi-based communication
* ⚡ Low-cost and portable IoT solution
* 🔁 Prevents repeated alerts using a configurable delay timer

---

## 🛠 Hardware Requirements

* NodeMCU ESP8266
* Neo-6M GPS Module
* Vibration/Impact Sensor
* Breadboard
* Jumper Wires
* USB Cable
* Power Supply

---

## 💻 Software Requirements

* Arduino IDE
* ESP8266 Board Package
* UltraMsg WhatsApp API Account
* Wi-Fi Connection

---

## 📚 Libraries Used

* ESP8266WiFi
* ESP8266HTTPClient
* WiFiClientSecure
* TinyGPS++
* SoftwareSerial

---

## ⚙ Working Principle

1. The NodeMCU connects to the Wi-Fi network.
2. GPS continuously updates the current location.
3. The vibration sensor monitors sudden impacts.
4. When the sensor value exceeds the predefined threshold:

   * The system detects a possible accident.
   * Current GPS coordinates are obtained.
   * A Google Maps location link is generated.
   * An emergency WhatsApp message is sent to the registered contact using the UltraMsg API.
5. A timer prevents duplicate messages from being sent repeatedly.

---

## 📱 WhatsApp Integration

This project uses the **UltraMsg WhatsApp API** to send emergency messages.

### Example Alert Message

```text
🚨 ACCIDENT DETECTED!

Latitude: 15.849125
Longitude: 74.497632

Location:
https://maps.google.com/?q=15.849125,74.497632
```

---

## 🌍 Technologies Used

* Embedded C
* Arduino IDE
* ESP8266
* IoT
* GPS Technology
* HTTP API
* WhatsApp Messaging
* Google Maps

---

## 📂 Project Structure

```text
Smart-Accident-Detection-System/
│
├── Smart_Accident_Detection.ino
├── README.md
├── circuit_diagram.png
├── images/
└── docs/
```

---

## 🔧 Configuration

Before uploading the code, update the following parameters:

### Wi-Fi Credentials

```cpp
const char* ssid = "YOUR_WIFI_NAME";
const char* password = "YOUR_WIFI_PASSWORD";
```

### UltraMsg Configuration

```cpp
String phone = "YOUR_PHONE_NUMBER";
String token = "YOUR_ULTRAMSG_TOKEN";
String instance = "YOUR_INSTANCE_ID";
```

---

## 🚀 Installation

1. Clone this repository.

```bash
git clone https://github.com/yourusername/Smart-Accident-Detection-System.git
```

2. Open the project in Arduino IDE.

3. Install all required libraries.

4. Update:

   * Wi-Fi credentials
   * UltraMsg API details
   * Phone number

5. Select the ESP8266 board.

6. Upload the code.

7. Power the NodeMCU.

---

## 📷 Project Workflow

```text
Impact Detected
       │
       ▼
Read Sensor Value
       │
       ▼
Threshold Exceeded?
       │
      Yes
       │
       ▼
Read GPS Coordinates
       │
       ▼
Generate Google Maps Link
       │
       ▼
Send WhatsApp Alert
       │
       ▼
Emergency Contact Receives Notification
```

---

## 🔮 Future Enhancements

* Android application
* Cloud database integration
* Accident history logging
* AI-based accident severity detection
* Automatic call to emergency services
* Vehicle speed monitoring
* Buzzer and LCD display
* Integration with Blynk or ThingsBoard dashboard

---

## 🎯 Applications

* Smart Vehicle Safety
* Emergency Response Systems
* Fleet Management
* Public Transportation
* School and College Vehicles
* Personal Vehicle Safety

---

## 👨‍💻 Author

**Sandesh Sandeep Pujeri**

Electronics and Communication Engineering

Interested in IoT, Embedded Systems, Robotics, and Smart Automation Projects.

---

## ⭐ Support

If you found this project helpful, please consider giving it a ⭐ on GitHub. Your support helps improve and share this project with others.
