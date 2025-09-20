#  Raspberry Pi Camera Setup Guide

This guide explains how to connect, enable, and use a camera with Raspberry Pi.

---

## 1. What You Need
- Raspberry Pi board (3 / 4 / 5 or Zero W)  
- Raspberry Pi Camera Module (v2 / v3) **or** a USB webcam  
- Camera ribbon cable (if using the Pi Camera Module)  

---

## 2. Connect the Camera
### For Raspberry Pi Camera Module:
1. Power off your Pi.  
2. Locate the **CSI camera port** (between the HDMI and audio jack on Pi 4).  
3. Gently lift the plastic clip and insert the ribbon cable (blue side facing the Ethernet/USB ports).  
4. Push the clip back down to secure the cable.  

### For USB Webcam:
- Plug the webcam into a USB port on your Raspberry Pi.  

---

## 3. Enable the Camera
Open a terminal and run:

```bash
sudo raspi-config
