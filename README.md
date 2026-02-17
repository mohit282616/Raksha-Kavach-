# Raksha Kavach: The Ultimate Self-Charging Safety Guard

**Innovation for Women Empowerment & Safety**
*Made with passion by Mohit, Krish, Gautam, and Prashant (ITI SCVR Dheerpur).*

**Topics/Tags:** `edge-ai` `esp32` `womens-safety` `wearable-tech` `tiny-ml` `energy-harvesting`

---

## Overview
Raksha Kavach is a next-generation safety wearable designed to bridge the gap between hardware autonomy and predictive intelligence. Unlike standard safety bands that rely on manual triggers and constant charging, Raksha Kavach is camouflaged as a premium woven friendship band and utilizes Edge AI to proactively detect danger before the user even presses a button.

## Key Features
* **Dual Energy Harvesting:** Self-charging system utilizing Thermoelectric Generators (TEG) for body heat and flexible micro-solar strips.
* **Predictive Edge AI:** Autonomously detects panic signatures (rapid heart rate and erratic shaking) using an MPU6050 and pulse sensor.
* **Premium Stealth Design:** Camouflaged as standard jewelry with a hidden SOS trigger bead to remain completely unnoticeable to attackers.
* **Autonomous Emergency Response:** Locks GPS coordinates and broadcasts SMS/Voice alerts via an integrated GSM module.
* **Industrial Resilience:** IP69 rated for extreme sweat, corrosion, and high-pressure water resistance.

## Hardware Architecture
The device uses a unique internal layering system to maintain a slim profile:
* **Core Microcontroller:** ESP32 
* **Sensors:** MPU6050 (Accelerometer/Gyroscope), Analog Pulse Sensor
* **Communication:** Neo-6M GPS Module, SIM800L GSM Module
* **Power:** Li-Po Battery, TEG modules, Flexible Solar Panels

## Software Integration
This repository contains the master firmware that handles both the manual SOS trigger and the continuous 50Hz AI inference loop. 

**Required Arduino Libraries:**
* `HardwareSerial.h`
* `TinyGPS++.h` (by Mikal Hart)
* `Wire.h`
* `Adafruit_MPU6050.h`
* `Adafruit_Sensor.h`
* Custom `Edge Impulse` Inferencing Library for Raksha Kavach

## Usage and Deployment
1. Clone this repository and open `RakshaKavach_Master.ino` in the Arduino IDE.
2. Install the required libraries via the Arduino Library Manager.
3. Import the trained Edge Impulse `.zip` library into the IDE (Sketch > Include Library > Add .ZIP Library).
4. Update the `EMERGENCY_PHONE` variable in the code with the designated family or police contact number.
5. Compile and flash the code to the ESP32. 
6. The device will run autonomously, triggering alerts either via the hidden physical button or automatically when the AI detects an attack profile.

---
*"True safety is technology that is always alert, even when you aren't."*
