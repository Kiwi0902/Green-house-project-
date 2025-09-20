# This guide explains how to connect multiple common sensors to Arduino.  
Arduino collects the data → sends it via USB → Raspberry Pi reads the values → data goes to your phone (LINE Notify).  

--- 
## 1. Soil Moisture Sensor (Analog Type)
- Measures soil water level (0 = wet, 1023 = dry).

| Sensor Pin | Arduino Connection |
|------------|--------------------|
| **VCC**    | 5V                 |
| **GND**    | GND                |
| **A0**     | A0 (Analog Input)  |
--- 
## 2. DHT11 / DHT22 (Temperature & Humidity)

| Sensor Pin | Arduino Connection |
| ---------- | ------------------ |
| **VCC**    | 5V                 |
| **GND**    | GND                |
| **DATA**   | D2 (Digital Pin)   |
--- 
## 3.LDR (Light Sensor with Resistor)

| Component     | Arduino Connection       |
| ------------- | ------------------------ |
| **LDR leg 1** | 5V                       |
| **LDR leg 2** | A1 + 10kΩ resistor → GND |
--- 
## 4. APDS-9960 (Color & Gesture Sensor, I²C)

| Sensor Pin | Arduino Connection |
| ---------- | ------------------ |
| **VCC**    | 3.3V               |
| **GND**    | GND                |
| **SDA**    | A4 (SDA)           |
| **SCL**    | A5 (SCL)           |
--- 
## 5. RTC

| Sensor Pin | Arduino Connection |
| ---------- | ------------------ |
| **VCC**    | 5V                 |
| **GND**    | GND                |
| **SDA**    | A4 (SDA)           |
| **SCL**    | A5 (SCL)           |
