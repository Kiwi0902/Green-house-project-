Green-house-project
# OVERVIEW 📖

This project uses an Arduino Uno and a Raspberry Pi 3B to build an automated plant care system.
  
  -Arduino Board: manages the hardware components: water pump, color sensor, soil moisture sensor, and LED grow lights  
  -Raspberry Pi 3B:communicates with the Arduino, receives sensor data, and uploads it online for monitoring 

# How the system will work ⚙️

Soil Moisture Sensor: Measures how dry or wet the soil is. If the soil is too dry, the Arduino turns on the water pump to water the plant
Color Sensor: Monitors the color of the leaves. By detecting changes in leaf color, the system can guess whether the plant is healthy or stressed
LED Grow Lights: Turn on during a set time window (for example, 8:00 AM to 8:00 PM) to make sure the plant gets enough light
Raspberry Pi:Collects all the data from the Arduino and sends it online. Later, this can be used for logging, creating graphs, or building a dashboard

# Hardware List 🛠
1. Arduino Uno
2. Raspberry Pi 3B
3. Water pump + relay
4. Soil moisture sensor
5. APDS-9960 color sensor (or similar)
6. RTC module (Real-Time Clock for scheduling)
7. LED grow lights

# The purpose of the project
The project combines electronics, coding, and plant care. It allows me to practice my skills in Arduino programming (C++) and working with different sensors. At the same time, I am learning Raspberry Pi programming (Python) on my own. This system demonstrates how hardware and software can work together to create a practical solution.
It is especially useful for people who want to take care of plants but do not always have the time to water them or check their condition.

# The progress and future

Meanwhile, I am working on enabling the Raspberry Pi to upload sensor data to the cloud. In the future, I plan to design a plastic enclosure to improve the structure and durability of the greenhouse, while also adding more functions such as temperature and humidity sensors. Since many parts of my code can still be improved, this project also serves as a way for me to practice and grow my coding skills in both Arduino (C++) and Raspberry Pi (Python).


