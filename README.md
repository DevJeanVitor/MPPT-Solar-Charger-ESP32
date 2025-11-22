<div align="center">
  <img src="https://github.com/user-attachments/assets/4a215133-4790-4ad6-b44a-9a3aff4274eb" alt="MPPT Solar Charge Controller Banner" width="100%">
  <br>
  <h1>MPPT Solar Charge Controller for EVs</h1>
  <p>
    <b>High-efficiency energy optimization system for Electric Vehicle charging using ESP32, IoT Integration, and Custom Power Electronics.</b>
  </p>
</div>

## Project Overview
This project focuses on the development of a smart **Solar Charge Controller** designed to optimize the charging process of Electric Vehicles (EVs) directly from photovoltaic panels.
The system integrates **IoT connectivity** with the system hardware for more efficient monitoring. It implements the **MPPT (Maximum Power Point Tracking)** algorithm on an **ESP32** to maximize energy extraction and synchronizes real-time telemetry data with **Google Firebase**, enabling remote monitoring through a customized **mobile application**.

### Key Results
* **High efficiency:** Maximized energy transfer using MPPT algorithms.
* **IoT connectivity:** Real-time data logging in the cloud.
* **Remote monitoring:** Mobile app for status and security tracking.
* **Hardware:** Power electronics design capable of handling high currents.

## Technologies and tools

Technologies used:

**Firmware:** C++, MPPT algorithms.
**Hardware:** ESP32 (SoC), MOSFETs, power sensors (voltage/current), PCB design.
**Connectivity:** WiFi (station mode), Google Firebase (real-time database).
**Mobile app:** Android, secure authentication, real-time dashboard.
**Tools:** Arduino IDE, EasyEDA.

## System architecture (how it works)

The system operates in a continuous cycle to ensure optimal charging and data transparency:

1.  **Detection:** Sensors monitor photovoltaic voltage, battery current, and temperature.
2.  **Processing (ESP32):** The microcontroller executes the **MPPT algorithm** to calculate the optimal duty cycle.
3.  **Actuator:** The PWM signal adjusts the DC-DC converter (Buck/Boost) to match the impedance.
4.  **Communication:** The ESP32 connects to WiFi and sends JSON data to **Firebase**.
5.  **Visualization:** The **mobile app** fetches data from the cloud and updates the user dashboard instantly.

## Implementation details

### Firmware and control
Developed in **C++**, with a focus on performance and low-level hardware manipulation.
* **MPPT logic:** Implementation of “Perturb and Observe” (P&O) to track the power curve.
* **Safety:** Routines for overvoltage/overcurrent protection.

### Hardware layer
* **Schematic design:** Circuit optimized for energy efficiency and thermal management.
* **Assembly:** Integration of the ESP32 logic unit with power drivers and MOSFETs.

### IoT and mobile device integration
A complete ecosystem has been built to enable remote supervision of the charging process.

**1. Cloud Integration (Firebase):**
The system acts as an IoT node, sending critical data packets every few seconds.
* **Data Points:** PV Voltage (V), Charging Current (A), Power (W), and System Status.

**2. Mobile Application Features:**
* **User Authentication:** Secure login screen with Password Recovery functionality.
* **Real-time Dashboard:** Visual interface displaying:
    * Input Voltage & Output Current.
    * Current Charging Mode (MPPT, Bulk, Absorption, Float).
* **System Status:** Visual indicators for connection status and error alerts.

## Academic Context

* **Institution:** Instituto Federal de Educação, Ciência e Tecnologia de Alagoas (IFAL)
* **Research topic:** Development of a Charge Controller for Photovoltaic Panels in MPPT Configuration, Controlled by Arduino for Charging Electric Cars.
* **Program:** PIBITI (Research and Technological Development)
* **Period:** Sep 2024 - Aug 2025
* **Advisor:** MSc Paulo César do Nascimento Cunha
