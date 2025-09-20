# How to Open and Set Up a Raspberry Pi!!
## 1. Prepare Hardware
- Raspberry Pi board (3 / 4 / 5 or Zero)
- microSD card (16 GB or more)
- Power supply (5V 2.5A for Pi 3, 5V 3A USB-C for Pi 4/5)
- SD card reader
---
## 2. Install Raspberry Pi OS
1. Insert the microSD card into your computer.  
2. Download and install [Raspberry Pi Imager](https://www.raspberrypi.com/software/).  
3. In Raspberry Pi Imager:  
   - **Choose OS** → Raspberry Pi OS (32-bit).  
   - **Choose Storage** → your microSD card.  
   - Click **⚙️ Advanced Options** (press `Ctrl+Shift+X`):  
     - Enable **SSH**.  
     - Set **hostname** (e.g., `raspberrypi`).  
     - Set **username/password** (default: `pi` / `raspberry`).  
     - Configure **Wi-Fi** (SSID + password).  
   - Click **Write**.  
4. Insert the card into your Raspberry Pi.
---
## 3. First Boot
1. Plug in the power supply — the Pi boots automatically.  
2. Find the Pi’s IP address:  
   - On Windows/macOS/Linux terminal:  
     ```bash
     ping raspberrypi.local
     ```  
   - Or check your Wi-Fi router’s connected devices list.  
---
## 4. Connect with VNC Viewer
1. Open **VNC Viewer** on your computer.  
2. Enter your Raspberry Pi’s IP address (or `raspberrypi.local`).  
3. Login with your Pi credentials:  
   - Username: `pi`  
   - Password: `raspberry` (or the one you set in Imager).  
4. Now you’ll see the Raspberry Pi desktop on your computer! 

