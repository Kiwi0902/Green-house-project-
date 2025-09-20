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
```
---
## 3. Get LINE Token
- Visit 👉 https://notify-bot.line.me/en/
- Log in with your LINE account.
- Go to My Page → Generate Token.
- Name it (e.g., PlantProject) and choose 1-on-1 chat.
- Copy the token (a long string like AbCdEf...).
---
### 4. Arduino Code
Upload this to your Arduino using Arduino IDE:
```cpp
void setup() {
  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(A0);   // read sensor
  Serial.println(sensorValue);        // send to Pi
  delay(2000);
}
```
---
## 5. Get LINE Token
- Go to your home folder (or create a project folder):
```cpp
  cd ~
# or make a folder for this project
mkdir ~/PlantProject && cd ~/PlantProject
```
- Create the file:
```
nano send_to_line.py
```
- Paste the following code inside Nano:
```cpp
import serial, time, requests

ser = serial.Serial('/dev/ttyACM0', 9600, timeout=1)
time.sleep(2)

LINE_TOKEN = "YOUR_LINE_TOKEN"   # paste your token here
LINE_URL = "https://notify-api.line.me/api/notify"
HEADERS = {"Authorization": f"Bearer {LINE_TOKEN}"}

def send_line(message):
    requests.post(LINE_URL, headers=HEADERS, data={"message": message})

while True:
    if ser.in_waiting > 0:
        data = ser.readline().decode().rstrip()
        print("Sensor:", data)
        send_line(f"🌱 Sensor Value: {data}")
        time.sleep(10)  # send every 10 seconds
```
- Save and exit Nano:
  Press CTRL + O → Enter (save)
  Press CTRL + X (exit)
- Now the file send_to_line.py is created in your folder.
---
## 6. Get LINE Token
Run the Program
Run on Raspberry Pi: 
```cpp
python3 send_to_line.py
```
You should now receive sensor values directly in your LINE chat.
