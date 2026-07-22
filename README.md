Smart Irrigation System using ESP32

Overview

This project is an IoT-based Smart Irrigation System built using ESP32. It monitors temperature, humidity, soil moisture, and motion detection while allowing remote water pump control using the Blynk IoT platform.

Features
🌱 Soil Moisture Monitoring
🌡 Temperature Monitoring
💧 Humidity Monitoring
🚰 Water Pump Control
📱 Blynk Mobile Dashboard
📟 LCD Display
🚶 PIR Motion Detection
☁ Real-Time IoT Monitoring

Hardware Used
ESP32
DHT11 Sensor
Soil Moisture Sensor
PIR Motion Sensor
Relay Module
Water Pump
LCD 16x2 I2C
Jumper Wires
Breadboard
Software Used
Arduino IDE
ESP32 Board Package
Blynk IoT
C++
WiFi
Working

The ESP32 continuously reads:

Temperature
Humidity
Soil Moisture

These values are displayed on the LCD and uploaded to Blynk Cloud.

The user can remotely control the water pump using the Blynk App.

The PIR sensor detects motion and sends an event notification.

Future Improvements
Automatic Pump Control
Weather API Integration
Data Logging
AI-based Irrigation Prediction




## Project Architecture
```text
                +----------------------+
                |     Blynk Mobile     |
                |     Application      |
                +----------+-----------+
                           |
                     Wi-Fi / Internet
                           |
                +----------v-----------+
                |      Blynk Cloud     |
                +----------+-----------+
                           |
                     Wi-Fi Connection
                           |
                +----------v-----------+
                |        ESP32         |
                |   Main Controller    |
                +---+----+----+----+---+
                    |    |    |    |
        +-----------+    |    |    +-----------+
        |                |    |                |
+-------v------+  +------v------+  +----------v---------+
| DHT11 Sensor |  | Soil Sensor |  |   PIR Sensor       |
| Temp/Humidity|  |  Moisture   |  | Motion Detection   |
+-------+------+  +------+------+
        |                |
        +--------+-------+
                 |
        Sensor Data Processing
                 |
        +--------+--------+
        |                 |
+-------v------+   +------v------+
|  I2C LCD     |   | Relay Module|
| Display Data |   | Pump Control|
+--------------+   +------+------+
                         |
                   +-----v-----+
                   | Water Pump|
                   +-----------+
```
