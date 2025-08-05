# O2-Temperature-and-Humidity-Arduino-Sensor


This Arduino-based project collects real-time data on **oxygen concentration**, **temperature**, and **humidity**, and logs the data to a microSD card in `.csv` format for later analysis. It uses a **DFRobot Oxygen Sensor (Gravity I²C)**, a **DHT22 sensor**, and an **SD card module** for data storage.

## 🚀 Features

- Logs oxygen concentration (mg/L), humidity (%), and temperature (°C)
- Writes to an SD card in CSV format (for easy import into Excel or Python)
- Low-memory usage and lightweight code structure
- Ideal for environmental sensing, school research projects, and microclimate analysis

---

## Components Required

| Component                      | Quantity |
|-------------------------------|----------|
| Arduino Uno / Nano            | 1        |
| DFRobot Oxygen Sensor (I²C)   | 1        |
| DHT22 (Temperature & Humidity)| 1        |
| SD Card Module + MicroSD Card | 1        |
| Breadboard + Jumper Wires     | 1 set    |
| 10kΩ Resistor (for DHT22)     | 1        |

---

## Wiring Instructions
<img width="762" height="884" alt="Image" src="https://github.com/user-attachments/assets/9ed8ef73-76bf-4ed8-ac2f-0f0d3bf77755" />

### DHT22 Sensor:
- **VCC** → 5V  
- **GND** → GND  
- **DATA** → Pin 2 on Arduino  
- **10kΩ Resistor** between DATA and VCC

### DFRobot Oxygen Sensor (I²C):
- **VCC** → 5V  
- **GND** → GND  
- **SDA** → A4 (Uno/Nano)  
- **SCL** → A5 (Uno/Nano)

### SD Card Module:
- **VCC** → 5V  
- **GND** → GND  
- **MOSI** → Pin 11  
- **MISO** → Pin 12  
- **SCK**  → Pin 13  
- **CS**   → Pin 10

---

## 📥 Arduino Libraries Required

Install the following libraries via the Arduino Library Manager:

1. **DFRobot_OxygenSensor**  
   [https://github.com/DFRobot/DFRobot_OxygenSensor](https://github.com/DFRobot/DFRobot_OxygenSensor)

2. **DHT Sensor Library**  
   [https://github.com/adafruit/DHT-sensor-library](https://github.com/adafruit/DHT-sensor-library)

3. **Adafruit Unified Sensor Library** (dependency for DHT)  
   [https://github.com/adafruit/Adafruit_Sensor](https://github.com/adafruit/Adafruit_Sensor)

4. **SD** (built-in with Arduino IDE)

---

## 📄 Sample Output (SD Card: `log.csv`)

Oxygen (mg/L),Humidity (%),Temperature (C)

6.45,42.1,23.6

6.43,42.2,23.6
