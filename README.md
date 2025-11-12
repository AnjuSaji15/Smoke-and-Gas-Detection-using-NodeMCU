Smoke and Gas Detection Using NodeMCU8266
📘 Overview

This project, “Smoke and Gas Detection Using NodeMCU8266”, is an IoT-based fire and smoke monitoring system designed to detect potential fire hazards in real time.
It utilizes NodeMCU (ESP8266) as the central controller, interfacing with a Flame Sensor, MQ2 Smoke Sensor, OLED Display, and Buzzer.

When smoke or flames are detected, the system triggers an audible alarm and displays real-time alerts on the OLED screen.
It is powered directly via USB connection from a laptop, eliminating the need for batteries.

🎯 Aim

To design and implement an IoT-based fire and smoke detection system using NodeMCU that detects hazards in real time and alerts users through an alarm and OLED display.

🧠 Objectives

To detect fire and smoke using NodeMCU-based sensors.

To replace traditional LCD with an OLED display for clearer visualization.

To power the system via laptop USB, ensuring portability and simplicity.

To activate an audible alarm whenever fire or smoke is detected.
| Sno | Component Name      | Quantity    | Description                                     |
| --- | ------------------- | ----------- | ----------------------------------------------- |
| 1   | NodeMCU (ESP8266)   | 1           | Central microcontroller with built-in Wi-Fi     |
| 2   | Flame Sensor Module | 1           | Detects infrared light emitted by flames        |
| 3   | Smoke Sensor (MQ2)  | 1           | Detects smoke and gas concentration             |
| 4   | OLED Display        | 1           | Displays sensor readings and alerts             |
| 5   | Buzzer              | 1           | Produces audible alarm when fire/smoke detected |
| 6   | Mini Breadboard     | 1           | For assembling components                       |
| 7   | Jumper Wires        | As required | For interconnections                            |
| 8   | USB Cable           | 1           | To power the system via laptop                  |
Component Details
🧠 NodeMCU (ESP8266)

A low-cost open-source IoT platform based on the ESP8266 Wi-Fi module.
It has multiple GPIO pins for interfacing sensors and output devices and is programmed using Arduino IDE.
It serves as the main controller that reads sensor data, processes it, and controls display and alarm outputs.

🔥 Flame Sensor Module

Detects infrared radiation from flames and outputs a digital signal to the NodeMCU when fire is detected.

💨 Smoke Sensor (MQ2)

Senses smoke and gas concentrations in the air, providing an analog signal proportional to the detected gas density.

💡 OLED Display

Displays real-time readings and alert messages.
Offers better contrast, lower power consumption, and faster response than LCDs.

🔔 Buzzer

Produces a loud alarm sound when hazardous conditions are detected.

🔌 Breadboard and Jumper Wires

Used to build and test the circuit without soldering.

🧭 Block Diagram

Central Controller: NodeMCU (ESP8266)

Reads sensor data

Processes input

Controls output devices

Optionally sends alerts over Wi-Fi

Input (Sensing Layer):

Flame Sensor – Digital Input (D2 - GPIO4)

Smoke Sensor (MQ2) – Analog Input (A0)

Output (Actuation Layer):

OLED Display – I2C Interface (D1 - SCL, D2 - SDA)

Buzzer – Digital Output (D5 - GPIO14)

Power Supply: Laptop USB (5V)

⚙️ Working of the System

The system is powered through the laptop’s USB port, initializing all components.

Flame Sensor continuously monitors infrared radiation to detect fire.

MQ2 Sensor reads smoke/gas concentration and sends analog signals to NodeMCU.

The NodeMCU processes the sensor data, comparing it with safety thresholds.

If fire or smoke levels exceed safe limits:

The buzzer activates to provide an audible alert.

The OLED display shows a warning message like “🔥 Fire Detected” or “💨 Smoke Detected”.

Optionally, NodeMCU’s Wi-Fi can be configured to send remote notifications for IoT-based monitoring.

This continuous monitoring ensures early fire detection, improving safety and response time.

🧪 Prototype Output

The OLED display shows “System Ready” during normal operation.

On detection:

Fire Alert: “🔥 Fire Detected!” displayed.

Smoke Alert: “💨 Smoke Detected!” displayed.

The buzzer produces a continuous sound to alert users.

🧰 Learning Outcomes

Learned interfacing of Flame and MQ2 sensors with NodeMCU.

Gained hands-on experience programming NodeMCU using Arduino IDE.

Understood real-time data acquisition and threshold-based decision-making.

Implemented OLED-based system status visualization.

Developed a functional IoT-based alert system integrating hardware and software.

📂 Project Structure
Smoke-Gas-Detection-NodeMCU/
│
├── code/
│   └── smoke_gas_detection.ino
│
├── hardware/
│   ├── circuit_diagram.png
│   └── component_images/
│
├── report/
│   └── project_report.docx
│
├── README.md
└── LICENSE

🧑‍💻 Author

Anju Susan Saji
MCA (Artificial Intelligence & Machine Learning)
UID: 24MCI10019
Section: 24MAM–1B
Subject: Internet of Things (24CAH-723)
Date: 12-11-2025
Guided by: Faculty, Chandigarh University

🚀 Future Enhancements

Enable Wi-Fi-based real-time alerts via mobile notifications.

Integrate with cloud IoT platforms (like Blynk or ThingSpeak).

Add temperature and humidity sensors for more comprehensive fire risk detection.

Power system with rechargeable battery for portability.

Develop a mobile app for live monitoring and history logs.
