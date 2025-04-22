# smart-kitchen-iot-using-esp32
# 🌬️ IoT Smart Air Monitoring System with ESP32

This project is an IoT-based Air Quality and Motion Detection System built using **ESP32**, integrated with **ThingSpeak** for real-time monitoring. It features local display on an **I2C LCD** and alerts using a **buzzer** and **LED**.

---

## 📦 Components Used

- ESP32 Dev Board  
- DHT11 – Temperature & Humidity Sensor  
- MQ135 – Gas Sensor  
- IR Sensor – Motion Detection  
- Buzzer  
- LED  
- 16x2 LCD with I2C Module  
- WiFi (ESP32 Built-in)  
- ThingSpeak (Cloud Platform)

---

## 🔧 Features

- 🌡️ Displays **temperature** and **humidity** on LCD
- 💨 Detects **gas leakage** using MQ135
- 🚶 Detects **motion** via IR sensor
- 🔔 **Alerts** with buzzer and LED on detection
- ☁️ Sends sensor data to **ThingSpeak** every 20 seconds
- 📊 Monitor environment remotely via ThingSpeak dashboard

---

## 🧠 How It Works

- ESP32 reads data from DHT11, MQ135, and IR sensors.
- Displays readings on LCD in real-time.
- Triggers **buzzer** if gas is detected.
- Triggers **LED** if motion is detected.
- Connects to WiFi and sends data to ThingSpeak every 20 seconds.

---

## 🖥️ Circuit Diagram

> *Coming soon – will include Fritzing or schematic image here*

---

## 📲 ThingSpeak Setup

1. Go to [ThingSpeak](https://thingspeak.com/)
2. Create a new channel with 4 fields:
   - Field 1: Temperature
   - Field 2: Humidity
   - Field 3: Gas Level (0 or 1)
   - Field 4: Motion Detected (0 or 1)
3. Copy your **Write API Key** into the code.

---

## 📁 Code Snippet (Setup)

```cpp
const char* ssid = "Your_SSID";
const char* password = "Your_PASSWORD";

unsigned long myChannelNumber = 1;
const char * myWriteAPIKey = "Your_API_Key";
