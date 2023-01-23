# Preparations

# Creating the Rubber Ducky

### Connect the Raspberry Pi
Hold the button on Raspberry Pi and connect it to your computer using the USB cable. The Pi should show up as RPI-RP2. 

### Adding CircuitPython
Put the file from CircuitPython into the root directory of the Raspberry Pi Pico. The Pi will reboot, connect again and appear as CIRCUITPY. 

### Adding Adafruit Bundle
Copy files/folders into the lib directory on the Pico from the Adafruit Bundle. The files are located in the lib folder of the Adafruit folder.
Following items need to be copied: 
- add adafruit_hid
- copy adafruit_debouncer.mpy
- copy adafruit_ticks.mpy
- copy asyncio

### Adding files from Git
Put boot.py into the root directory and overwrite code.py with code.py retrieved from the git.
From now on the Pico needs to be put into setup/arming mode, otherwise the device will execute scripts. 

### Adding scripts/payloads
Save scripts as payload.dd om the root directory of the Pico.
You can save up to six scripts: payload.dd, payload2.dd, etc., payload6.dd

# Usage

### Setup/Arming Mode

### Selecting the Payload

### Stealth Mode

### Change Keyboard Layout
