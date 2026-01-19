# 🍓 Raspberry Pi Pico Mini-Projects Collection

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![Language](https://img.shields.io/badge/language-CircuitPython-purple.svg) ![Status](https://img.shields.io/badge/status-active-green.svg)

A collection of practical **CircuitPython** projects for the Raspberry Pi Pico, demonstrating integration with various sensors, displays, and actuators.

![Pico Pinout](https://github.com/user-attachments/assets/ab6dae48-6632-4d50-85aa-125d3403c244)

---

## 🌡️ 1. Temperature & Humidity Monitor

A real-time environmental monitor that alerts users when conditions go beyond comfortable limits.

![Temp Monitor](https://github.com/user-attachments/assets/1bd40e2e-4f84-4e8c-8478-6f6daea0d11d)

### 📝 Overview
Displays real-time temperature and humidity readings on an OLED screen. If the temperature exceeds **28°C** or humidity exceeds **58%**, a buzzer alerts the user.

### 🛠️ Components
*   Raspberry Pi Pico
*   OLED Display (128x32)
*   DHT11 Sensor
*   Buzzer

### 🔌 Wiring Diagram
![Temp Wiring](https://github.com/user-attachments/assets/f6d01ea4-e9c1-41b9-8faa-11be9143ea10)

| Component | Pin | Pico GPIO |
| :--- | :--- | :--- |
| **OLED** | SDA | GP0 |
| | SCK | GP1 |
| **DHT11** | OUT | GP2 |
| **Buzzer** | + | GP3 |

---

## 🔒 2. Safe Lock System

An infrared-based security system that detects unauthorized access to a safe.

| Safe Locked | Safe Violated |
| :---: | :---: |
| ![Locked](https://github.com/user-attachments/assets/c9a2965e-9945-4fcd-9a71-5edf5309c378) | ![Violated](https://github.com/user-attachments/assets/512e0dbd-7925-4636-992e-f79976b2ede9) |

### 📝 Overview
Monitors the safe door using an IR sensor. When the door is opened, the system triggers an alarm and increments an "intrusion counter" displayed on the OLED screen.

### 🛠️ Components
*   Raspberry Pi Pico
*   OLED Display (128x32)
*   IR (Infrared) Obstacle Sensor
*   Buzzer

### 🔌 Wiring Diagram
![Safe Wiring](https://github.com/user-attachments/assets/960f4449-8ac0-4d33-8de8-437ceb0b992e)

| Component | Pin | Pico GPIO |
| :--- | :--- | :--- |
| **OLED** | SDA | GP0 |
| | SCK | GP1 |
| **IR Sensor**| OUT | GP2 |
| **Buzzer** | + | GP3 |

---

## 🚪 3. Smart Door Control System

An automated entry system offering hands-free operation and feedback.

![Door Control](https://github.com/user-attachments/assets/e442b466-8074-44e9-89f9-21f36a09531d)

### 📝 Overview
Uses an ultrasonic sensor to detect presence at the door.
1.  **Detection**: If someone is in range -> Buzzer beeps & OLED shows "Someone Outside".
2.  **Action**: Press the button to open the door (Servo rotates 90°).
3.  **Auto-Close**: Door closes automatically after 5 seconds.

### 🛠️ Components
*   Raspberry Pi Pico
*   OLED Display (128x32)
*   HC-SR04 Ultrasonic Sensor
*   Servo Motor (SG90)
*   Push Button
*   Buzzer

### 🔌 Wiring Diagram
![Door Wiring](https://github.com/user-attachments/assets/9cf77b1f-dbc7-4380-ae88-7b5ad4020c2c)

| Component | Pin | Pico GPIO |
| :--- | :--- | :--- |
| **OLED** | SDA | GP0 |
| | SCK | GP1 |
| **Button** | OUT | GP2 |
| **Buzzer** | + | GP3 |
| **Servo** | SIG | GP4 |
| **Ultrasonic**| ECHO | GP20 |
| | TRIG | GP21 |

---

## 🚀 Getting Started

### Prerequisites
1.  **CircuitPython Firmware**: Install the latest CircuitPython [uf2](cci:7://file:///c:/Users/Myduino/Downloads/newbackup/newbackup/repo_analysis_pico/adafruit-circuitpython-raspberry_pi_pico_w-en_US-9.2.0.uf2:0:0-0:0) on your Pico.
2.  **Libraries**: Copy the `lib` folder from this repository to your Pico's `lib` folder. This contains essential drivers for the OLED, DHT11, and Servo.

### Installation
1.  Clone this repository.
2.  Choose a project script (e.g., `Door Control System.py`).
3.  Rename the chosen script to `code.py` and copy it to the root of your Pico.
4.  The project will start automatically!

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License
This project is open-source.
