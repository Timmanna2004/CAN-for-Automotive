# CAN-for-Automotive

# 🚗 CAN-Based Node Communication for Automotive

## 📌 Project Overview

The **CAN-Based Node Communication for Automotive** project demonstrates communication between multiple Electronic Control Units (ECUs) using the Controller Area Network (CAN) protocol.

The system consists of three PIC18F4580 microcontroller-based ECU nodes. ECU1 and ECU2 transmit vehicle-related parameters, while ECU3 receives the transmitted data and displays the information on a 16×2 Character LCD.

This project simulates a basic automotive dashboard system, demonstrating how different vehicle parameters can be exchanged between multiple ECUs through a common CAN bus.

## 🎯 Objectives

- To implement CAN-based communication between multiple ECUs.
- To understand CAN protocol and message transmission.
- To transmit and receive vehicle parameters.
- To display real-time vehicle information on a dashboard.
- To understand the role of distributed ECUs in automotive applications.

## 🔧 Hardware Requirements

- PIC18F4580 Microcontrollers – 3
- CAN Transceiver Modules
- 16×2 Character LCD
- ADC-based Potentiometer
- Digital Keypad / Switches
- LEDs
- Connecting Wires
- Power Supply

## 💻 Software Requirements

- MPLAB X IDE
- MPLAB XC8 Compiler
- Embedded C
- PIC18F4580 Microcontroller
- CAN Communication Protocol
- Tera Term (for UART debugging)

## 🏗️ System Architecture

The project consists of three ECU nodes:

### 🚘 ECU1 – Vehicle Speed and Gear Control
- Reads vehicle speed using an ADC-based potentiometer.
- Controls gear selection using digital switches.
- Transmits speed and gear information through CAN.

### ⚙️ ECU2 – Engine and Indicator Control
- Reads engine RPM using an ADC input.
- Reads engine temperature using an ADC input.
- Controls left and right indicator LEDs using switches.
- Transmits RPM, engine temperature, and indicator status through CAN.

### 📟 ECU3 – Dashboard / Receiver
- Receives CAN messages from ECU1 and ECU2.
- Processes the received vehicle parameters.
- Displays vehicle information on a 16×2 Character LCD.
- Controls dashboard indicator LEDs based on received indicator status.

## 📨 CAN Message IDs

| Parameter | CAN Message ID |
|---|---|
| 🚗 Speed | `0x10` |
| ⚙️ Gear | `0x20` |
| 🔄 RPM | `0x30` |
| 🌡️ Engine Temperature | `0x40` |
| 💡 Indicator | `0x50` |

## 🔄 Working Principle

1. ECU1 reads the speed and gear values from the input devices.
2. ECU2 reads engine RPM and temperature and processes indicator switch inputs.
3. Both ECUs transmit their respective data using CAN messages.
4. ECU3 receives the messages through the CAN bus.
5. The received data is decoded based on CAN message IDs.
6. The dashboard displays the vehicle parameters on the LCD.
7. The indicator status is reflected through the dashboard LEDs.

## 📡 Communication Protocol – CAN

Controller Area Network (CAN) is a serial communication protocol widely used in automotive applications. It allows multiple ECUs to communicate with each other over a shared bus without requiring a central controller.

**Important CAN Features:**
- 🔹 Multi-master communication.
- 🔹 Message-based communication.
- 🔹 Priority-based arbitration.
- 🔹 Error detection and handling.
- 🔹 Reliable communication between multiple nodes.

## 🌍 Applications

- 🚘 Automotive Electronic Control Units.
- 📊 Vehicle Dashboard Systems.
- ⚙️ Engine Monitoring Systems.
- 🔌 Automotive Sensor Networks.
- 🚗 Vehicle Control and Monitoring Systems.

## 📚 Learning Outcomes

- Practical implementation of CAN communication.
- Understanding multi-node communication.
- Interfacing PIC18F4580 with CAN transceivers.
- ADC and digital input interfacing.
- UART-based debugging.
- LCD interfacing and real-time data display.
- Understanding automotive embedded systems.

## 🚀 Future Enhancements

- Integration of additional automotive sensors.
- Implementation of fault detection and diagnostics.
- Development of a more advanced vehicle dashboard.
- Integration of vehicle speed and engine monitoring features.

## 👨‍💻 Author

**Timmanna Kulagod**

🎓 Embedded Systems Trainee

- **Domain:** Automotive Embedded Systems
- **Microcontroller:** PIC18F4580
- **Programming Language:** Embedded C
- **Communication Protocol:** CAN

---
