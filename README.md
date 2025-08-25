# 🌫️ Air Quality Monitoring System (ESP32 + MQ135 + Blynk)

An **IoT-enabled air quality monitor** built using **ESP32** and the **MQ135 gas sensor** to measure **CO₂ and Benzene levels** in the environment.  
The system automatically **calibrates the sensor**, determines air quality status, and uploads data to the **Blynk IoT cloud** for real-time monitoring.

---

## 📌 Features
- 🏭 **Air quality monitoring** using MQ135 gas sensor.  
- 🌡️ Calculates **CO₂ concentration (PPM)** and **Benzene (PPM)**.  
- 🛠️ **Automatic sensor calibration** in clean air.  
- 📊 Shows **Good / Moderate / Poor** air quality levels.  
- 📲 **Blynk IoT Integration** → View readings on smartphone in real time.  
- 🔬 Serial Monitor debugging with detailed logs.  

---

## 🛠 Components Used
| Component              | Quantity |
|------------------------|----------|
| ESP32 Dev Board        | 1        |
| MQ135 Gas Sensor       | 1        |
| Jumper Wires           | As needed |
| Breadboard             | 1        |
| Power Supply (USB/5V)  | 1        |

---

## 🔌 Circuit Diagram / Pin Configuration
- **MQ135 Sensor Output (Analog)** → **GPIO34 (D34)**  
- **VCC** → **3.3V**  
- **GND** → **GND**  

---

## 📜 Arduino Code
- Initializes **MQ135 sensor** on ESP32.  
- Automatically calibrates `Ro` in clean air.  
- Calculates **Rs, CO₂ PPM, and Benzene concentration**.  
- Displays results via Serial and sends to **Blynk Cloud**.  

📂 File: [`air_quality_monitor.ino`](https://github.com/alex22022005/Air-Quality-Monitor-MQ135-ESP32/blob/main/AirQuality_Monitor.ino)

---

## 🚀 Getting Started
1. Install **Arduino IDE** (with ESP32 board support).  
2. Install the required libraries from **Library Manager**:  
   - `WiFi.h`  
   - `BlynkSimpleEsp32.h`  
   - `MQ135.h`  
3. Open the code and update your WiFi & Blynk credentials:  
4. Upload the code to your **ESP32**.  
5. Open the **Serial Monitor (115200 baud)** to view logs.  
6. Launch the **Blynk App** → Add widgets → Connect to virtual pins:  
- **V0** → CO₂ PPM  
- **V1** → Benzene PPM  
- **V2** → Air Quality Status (Good / Moderate / Poor)  

---

## 📲 Air Quality Status Levels
| CO₂ (PPM) Range | Status     |
|-----------------|------------|
| **0 – 100**     | ✅ Good     |
| **101 – 300**   | ⚠️ Moderate |
| **301+**        | ❌ Poor     |

---

## 📌 Applications
- 🏠 Indoor Air Quality Monitoring (Homes & Offices).  
- 🏭 Industrial Gas Monitoring.  
- 🌍 Pollution Tracking & Environmental Projects.  
- 🚗 Air Quality Monitoring inside vehicles.  

---

## 📄 License
This project is licensed under the **MIT License** – free to use, modify, and distribute.  

---

## ✨ Author
Developed by **Antony Alex**  
🌐 GitHub: [alex22022005](https://github.com/alex22022005)  
🚀 IoT | Embedded Systems | Smart Automation  

---
