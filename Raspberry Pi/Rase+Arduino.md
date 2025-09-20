# 🌱 Raspberry Pi + Arduino → LINE Notification Guide

This guide explains how to connect an Arduino to a Raspberry Pi, collect sensor data, and send updates directly to your phone using **LINE Notify**.

---

## 1. Hardware Needed
- Raspberry Pi (3 / 4 / 5 or Zero W)  
- Arduino (Uno / Nano / Mega)  
- USB cable (to connect Arduino to Raspberry Pi)  
- Sensor (example: soil moisture, temperature, etc.)  
- Internet connection (Raspberry Pi with Wi-Fi or Ethernet)  
- Smartphone with **LINE** app installed  

---

## 2. Arduino Setup
Upload this code to your Arduino (reads from sensor pin A0):

```cpp
void setup() {
  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(A0);  // Example: soil moisture
  Serial.println(sensorValue);
  delay(2000);
}
