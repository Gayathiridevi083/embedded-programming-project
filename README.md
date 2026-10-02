# AI-Enabled Smart Cold Chain Logistics Tracker

## 📌 Project Overview

The **AI-Enabled Smart Cold Chain Logistics Tracker** is an ESP32-based IoT monitoring system designed to monitor the environmental and physical conditions of temperature-sensitive products during transportation and storage.

Cold-chain products such as medicines, vaccines, biological samples, food products, and other temperature-sensitive materials can be affected by improper temperature conditions and physical shocks during transportation. Traditional monitoring methods may depend on manual inspection or monitor only a single parameter.

This project addresses this problem by combining **temperature monitoring, humidity monitoring, acceleration/shock detection, local display, and real-time alert indications** into a compact embedded system.

The prototype uses an **ESP32** as the central controller, a **DHT22 sensor** for temperature and humidity measurement, and an **MPU6050 sensor** for acceleration and shock detection. A **16×2 I²C LCD** displays sensor information, while LEDs and a buzzer provide immediate local alerts.

---

## 🎯 Objectives

* Monitor temperature continuously during cold-chain operation.
* Monitor humidity conditions using the DHT22 sensor.
* Detect sudden physical shocks or excessive acceleration.
* Display sensor readings locally using a 16×2 I²C LCD.
* Provide visual warning indications using LEDs.
* Provide an audible alert when a shock condition is detected.
* Reduce dependence on manual monitoring.
* Provide a foundation for future IoT, GPS, AI/ML, and automated cooling features.

---

## ✨ Features

### 🌡️ Temperature Monitoring

The DHT22 sensor continuously measures the surrounding temperature. A prototype threshold of **15°C** is used for demonstration and testing.

### 💧 Humidity Monitoring

The DHT22 also measures relative humidity and displays the measured value through the system.

### 📳 Shock Detection

The MPU6050 accelerometer monitors acceleration along multiple axes. The system calculates the acceleration magnitude and identifies a shock condition when it exceeds the prototype threshold of **20 m/s²**.

### 📟 LCD Display

A 16×2 I²C LCD provides local information about sensor readings and system status.

### 🟢 Safe Indication

The green LED indicates that the monitored temperature is within the configured prototype range and no shock condition has been detected.

### 🔴 Warning Indication

The red LED is activated when the temperature exceeds the configured threshold or when a shock condition is detected.

### 🔊 Audible Shock Alert

The buzzer provides an immediate audible warning when the detected acceleration exceeds the configured shock threshold.

### ⚡ ESP32 Processing

The ESP32 collects sensor readings, processes the values, applies the monitoring logic, and controls the display and alert devices.

---

## 🧩 Hardware Components

| Component               | Purpose                                    |
| ----------------------- | ------------------------------------------ |
| ESP32 Development Board | Main controller and sensor data processing |
| DHT22                   | Temperature and humidity measurement       |
| MPU6050                 | Acceleration and shock detection           |
| 16×2 I²C LCD            | Display sensor readings and system status  |
| Green LED               | Safe-condition indication                  |
| Red LED                 | Warning indication                         |
| Buzzer                  | Audible shock alert                        |
| Resistors               | LED current limiting                       |
| Breadboard              | Prototype circuit assembly                 |
| Jumper Wires            | Electrical connections                     |
| USB Cable               | ESP32 programming and power                |

---

## 🔌 Pin Configuration

| Component   | ESP32 Pin |
| ----------- | --------- |
| DHT22 Data  | GPIO 15   |
| MPU6050 SDA | GPIO 21   |
| MPU6050 SCL | GPIO 22   |
| I²C LCD SDA | GPIO 21   |
| I²C LCD SCL | GPIO 22   |
| Red LED     | GPIO 25   |
| Green LED   | GPIO 26   |
| Buzzer      | GPIO 4    |

### I²C Addresses

| Device | I²C Address |
| ------ | ----------- |
