Read this!!!!

# This page includes different file (coding) function, so you won't use the wrong file!

- **led+timing** →  Control LEDs with RTC (turn on between 8:00–20:00)
  
- **led_shify register** →  Control LEDs with the 74HC595 shift register (More like a testing program for led+timing)
  
- **plant.watering** → Automatic watering using soil moisture sensor. When the soil moistture percent is below a number, it will automaticlly open the watering system.
  
- **watering.testing** →Testing your watering system (ONLY water pump)
  
- **APDS-9960.data** →Collecting data (RBG) to create an algorithm

- **APDS-9960** →Allow APDS-9960 to check the plant health condition by using RGB

(I'm not combining the program together because you can decide how many Arduino Uno you are using)

For my project, I use 2 Arduino barod: The first one is controlling watering system and APDS-9960. The second one is controlling the led system with RTC
