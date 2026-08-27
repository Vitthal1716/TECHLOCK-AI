🚗 TECHLOCK AI

**AI-Powered Intelligent Vehicle Security & Tracking System**

**Team Name:** KavachX
**Project Name:** TECHLOCK AI
**Domain:** Artificial Intelligence | IoT | Embedded Systems | Vehicle Security


## 📌 Overview

TECHLOCK AI is an intelligent and secure vehicle protection system designed to prevent unauthorized vehicle access and improve real-time vehicle monitoring. The system combines **fingerprint authentication, ESP32, GPS, GSM, relay-based engine control, touchscreen interface, buzzer alerts, and AI-based security intelligence** into a single integrated platform.

Unlike conventional key-based security systems, TECHLOCK AI provides **keyless biometric access**, unauthorized access detection, vehicle location tracking, and alert mechanisms.


## 🚨 Problem Statement

Traditional vehicle security systems mainly depend on mechanical keys, remote controls, or basic immobilizers. These systems may be vulnerable to lost, stolen, duplicated keys and unauthorized access.

Most conventional systems also lack integrated real-time tracking and intelligent monitoring. Therefore, there is a need for a **secure, intelligent, keyless, and connected vehicle security system** capable of authenticating users, controlling vehicle access, detecting suspicious activity, and providing location-based monitoring.


## 💡 Proposed Solution

TECHLOCK AI provides a multi-layer vehicle security solution using biometric authentication and connected embedded technology.

The system verifies the user's fingerprint before allowing vehicle access. An ESP32 acts as the main controller and communicates with the fingerprint sensor, relay, buzzer, touchscreen, and SIM868 GSM/GPS module.

If the user is authorized, the system enables vehicle access through the relay. If an unauthorized fingerprint or suspicious access attempt is detected, the system denies access and generates an alert.

GPS enables vehicle location tracking, while GSM provides remote communication and alert functionality.


## 🎯 Objectives

* Develop a secure fingerprint-based vehicle authentication system.
* Provide keyless vehicle access.
* Prevent unauthorized vehicle starting.
* Control vehicle ignition using a relay.
* Track vehicle location using GPS.
* Send security alerts using GSM.
* Provide a user-friendly touchscreen interface.
* Detect and respond to suspicious access attempts.
* Integrate AI-based intelligent security features.
* Develop a compact and reliable PCB-based prototype.


## ✨ Key Features

* 🔐 Fingerprint-based authentication
* 🚗 Keyless vehicle access
* 🧠 AI-based intelligent security
* 📍 GPS location tracking
* 📡 GSM communication
* ⚡ Relay-based engine control
* 🚨 Unauthorized access alert
* 🔊 Buzzer alarm
* 🖥️ Nextion touchscreen interface
* 🔋 Battery-powered operation
* 📊 Real-time vehicle status
* 🛡️ Multi-layer vehicle protection


# 🏗️ System Architecture

```text
                 ┌──────────────────────┐
                 │      USER            │
                 │  Fingerprint Input   │
                 └──────────┬───────────┘
                            ↓
                 ┌──────────────────────┐
                 │ FINGERPRINT SENSOR   │
                 └──────────┬───────────┘
                            ↓
                 ┌──────────────────────┐
                 │        ESP32         │
                 │   Main Controller    │
                 └──────┬─────┬─────┬───┘
                        │     │     │
              ┌─────────┘     │     └──────────┐
              ↓               ↓                ↓
       ┌────────────┐  ┌────────────┐   ┌────────────┐
       │   RELAY    │  │  NEXTION   │   │  SIM868    │
       │ Engine Ctrl│  │  DISPLAY   │   │ GPS + GSM  │
       └─────┬──────┘  └────────────┘   └─────┬──────┘
             ↓                                 ↓
       ┌────────────┐                    ┌────────────┐
       │  VEHICLE   │                    │   ALERT /  │
       │  IGNITION  │                    │  TRACKING  │
       └────────────┘                    └────────────┘
```

---

# 🔄 Working Principle

### Step 1 — System Initialization

The ESP32 initializes all connected modules including the fingerprint sensor, Nextion display, relay, buzzer, and SIM868 module.

### Step 2 — Fingerprint Detection

The user places a registered finger on the fingerprint sensor.

### Step 3 — Authentication

The fingerprint sensor compares the captured fingerprint with the stored fingerprint database.

### Step 4 — Authentication Decision

The ESP32 determines whether the user is authorized.

### Step 5 — Authorized User

If the fingerprint matches a registered user:

* Access is granted.
* Relay is activated.
* Vehicle ignition can be enabled.
* Vehicle status is displayed on the Nextion screen.

### Step 6 — Unauthorized User

If the fingerprint does not match:

* Vehicle access remains blocked.
* Buzzer can be activated.
* Unauthorized access event is recorded.
* GSM alert functionality can be triggered.

### Step 7 — GPS Tracking

The SIM868 module obtains the vehicle's location using GPS.

### Step 8 — GSM Communication

The GSM module can communicate vehicle status and security alerts to the authorized user.

---

# 🔄 System Flowchart

```text
                 START
                   ↓
          Initialize System
                   ↓
        Scan Fingerprint
                   ↓
       Verify Fingerprint
                   ↓
             ┌───────────┐
             │ Authorized│
             │    ?      │
             └─────┬─────┘
                YES│       │NO
                   ↓       ↓
              Access     Access
               Granted   Denied
                   ↓       ↓
              Relay ON   Buzzer
                   ↓       ↓
             Vehicle ON  GSM Alert
                   ↓
              GPS Tracking
                   ↓
            Vehicle Monitoring
                   ↓
                  END
```

---

# 🔌 Hardware Components

| Component             | Purpose                            |
| --------------------- | ---------------------------------- |
| ESP32                 | Main controller                    |
| Fingerprint Sensor    | Biometric authentication           |
| Nextion NX3224T028    | Touchscreen user interface         |
| SIM868                | GSM communication and GPS tracking |
| Relay Module          | Vehicle ignition control           |
| 5V Passive Buzzer     | Security alert                     |
| LM2596 Buck Converter | Voltage regulation                 |
| TP4056                | Li-ion battery charging            |
| Li-ion Battery        | Power supply                       |

---

# 🧠 AI Module

The AI layer is designed to improve the intelligence of the security system.

Potential AI-based functions include:

* Unauthorized access pattern detection
* Suspicious activity detection
* Repeated failed authentication analysis
* Abnormal vehicle activity detection
* Intelligent security event classification
* Future theft-risk prediction

The AI module can be integrated with the embedded security layer to provide smarter decision-making and adaptive vehicle protection.

---

# 📍 GPS & GSM Module

The SIM868 module provides both GPS and GSM functionality.

### GPS Functions

* Vehicle location acquisition
* Latitude and longitude information
* Location monitoring
* Future geofencing support

### GSM Functions

* Security alerts
* Vehicle status messages
* Remote communication
* Future remote-control functionality

---

# 🖥️ User Interface

The Nextion NX3224T028 touchscreen provides a simple interface for displaying:

* Vehicle status
* Authentication status
* Fingerprint registration
* GPS status
* GSM status
* Security alerts
* System information

---

# 🔐 Security Layers

TECHLOCK AI uses multiple security layers:

```text
        ┌──────────────────────────┐
        │   Fingerprint Layer      │
        └────────────┬─────────────┘
                     ↓
        ┌──────────────────────────┐
        │ Authentication Layer     │
        └────────────┬─────────────┘
                     ↓
        ┌──────────────────────────┐
        │ Vehicle Control Layer    │
        └────────────┬─────────────┘
                     ↓
        ┌──────────────────────────┐
        │ GPS Tracking Layer       │
        └────────────┬─────────────┘
                     ↓
        ┌──────────────────────────┐
        │ GSM Alert Layer          │
        └────────────┬─────────────┘
                     ↓
        ┌──────────────────────────┐
        │ AI Intelligence Layer    │
        └──────────────────────────┘
```

---

# 🟩 PCB Design

The TECHLOCK AI hardware can be integrated into a custom PCB designed using **KiCad**.

The PCB integrates:

* ESP32 controller
* Power regulation
* Fingerprint interface
* Relay control
* GSM/GPS interface
* Buzzer connection
* Display interface
* Battery/power connections

### PCB Files

The repository contains:

* KiCad schematic
* PCB layout

---

# 🔧 Hardware Prototype

The final prototype integrates the major hardware components into a compact vehicle-security unit.

The prototype demonstrates:

* Fingerprint authentication
* Vehicle access control
* Security alerts
* GPS tracking
* GSM communication
* Touchscreen interaction

---

# 📊 System Advantages

* Improved vehicle security
* Keyless authentication
* Reduced dependency on conventional keys
* Real-time location tracking
* Unauthorized access detection
* Remote alert capability
* Modular architecture
* Expandable AI functionality
* Suitable for cars and two-wheelers
* Can be integrated with IoT platforms

---

# 🚗 Applications

* Personal cars
* Motorcycles and scooters
* Commercial vehicles
* Rental vehicles
* Delivery vehicles
* Fleet management
* Family vehicles
* Security-sensitive vehicles

---

# ⚠️ Limitations

* GPS availability depends on satellite signal.
* GSM functionality depends on network availability.
* Fingerprint recognition may be affected by sensor/environment conditions.
* Vehicle wiring must be performed carefully for safe installation.
* AI features require suitable training data for reliable prediction.

---

# 🔮 Future Scope

Future versions of TECHLOCK AI can include:

* 📱 Dedicated mobile application
* ☁️ Cloud-based vehicle monitoring
* 📍 Geofencing
* 🧠 AI-based theft prediction
* 👤 Face recognition
* 🎙️ Voice authentication
* 📷 Camera-based monitoring
* 🔔 Push notifications
* 🌐 IoT dashboard
* 🔒 Multi-user authentication
* 🚘 Remote vehicle control
* 📊 Security analytics dashboard

---

# 🧪 Testing

The system can be tested under the following conditions:

| Test                     | Expected Result          |
| ------------------------ | ------------------------ |
| Registered fingerprint   | Vehicle access granted   |
| Unregistered fingerprint | Vehicle access denied    |
| Multiple failed attempts | Security alert           |
| Relay activation         | Vehicle control enabled  |
| GPS request              | Location obtained        |
| GSM communication        | Alert/status transmitted |
| Touchscreen interaction  | Correct status displayed |

---

# 📁 Project Structure


TECHLOCK-AI/
│
├── README.md
│
├── docs/
│   ├── abstract.md
│   ├── problem-statement.md
│   ├── objectives.md
│   ├── methodology.md
│   ├── system-architecture.png
│   ├── flowchart.png
│   └── circuit-diagram.png
│
├── hardware/
│   ├── components.md
│   ├── circuit/
│   └── pcb/
│
├── software/
│   ├── esp32/
│   ├── fingerprint/
│   ├── gps-gsm/
│   
│
├── images/
│   ├── prototype/
│   ├── pcb/
│   └── ui/
│
├── demo/
│   └── demo-video.md
│
└── references/
    └── references.md
```

#  Installation & Setup

### Hardware Setup

1. Connect the fingerprint sensor to the ESP32.
2. Connect the SIM868 GSM/GPS module.
3. Connect the relay module.
4. Connect the buzzer.
5. Connect the power regulation circuit.
6. Connect the battery and charging circuit.
7. Verify all common-ground connections.
8. Upload the ESP32 firmware.
9. Test the system before vehicle installation.

### Software Setup

Required tools:

* Arduino IDE
* ESP32 Board Package
* KiCad
* Required ESP32 libraries


# 📸 Project Images

## Prototype


## PCB
<img width="524" height="433" alt="image" src="https://github.com/user-attachments/assets/dfcc53c3-dc64-4389-8203-2d45936153e9" />

## User Interface
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/c59a5129-1d97-4ca6-a2ac-4aad1247a2d2" />


# 🎥 Demo

The demonstration video will show:

* Fingerprint registration
* Fingerprint authentication
* Authorized vehicle access
* Unauthorized access attempt
* Relay operation
* Buzzer alert
* GPS tracking
* GSM alert
* Nextion interface

**Demo Video:** https://drive.google.com/file/d/1D4W0jJVReStrp9ZEKo5Y4yoR6H1GpQTH/view?usp=drivesdk


# 📚 References

1. Espressif Systems — ESP32 Technical Documentation.
2. SIMCom — SIM868 Hardware and Software Documentation.
3. Nextion — Intelligent Display Documentation.
4. Fingerprint Sensor Module Documentation.
5. KiCad Documentation.
6. Relevant IEEE research papers on vehicle security, biometric authentication, IoT and AI-based security systems.


# 👥 Team

## Team Name

**KavachX**

## Project

**TECHLOCK AI**

### Team Members

1. **[Modhave Aditti Raju ]**
2. **[Koli Vitthal Haribhau **
3. **[Phadale Tanuja Narendra ]**
4. **[Mohite Saloni Jalindar ]**

### Institution

**[Jaihind College of Engineering, Kuran Junnar ]**


# 🏆 Project Vision

> **“Making every vehicle smarter, safer and harder to steal.”**

TECHLOCK AI aims to transform conventional vehicle security into an intelligent, biometric, connected and future-ready security platform.


## ⭐ TECHLOCK AI

**Secure. Intelligent. Connected.**

**AI-Powered Vehicle Security for the Next Generation.**
****
