This code is based off the code from [dbisu](https://github.com/dbisu/pico-ducky). The main change of this code were made to host up to six payloads, instead of the original four.

# Preparations
- Raspberry Pi Pico
- CircuitPython 7.X.X from [here](https://circuitpython.org/board/raspberry_pi_pico/)
- [adafruit-circuitpython-bundle](https://github.com/adafruit/Adafruit_CircuitPython_Bundle/releases/latest); extract it outside of the Pico
- the code from here

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
To prevent the execution of payloads connect pin GPIO 0 to Ground.

### Selecting the Payload
To select the payload, connect folowwing GPIO Pins to Ground.
- Payload 1: GPIO 4
- Payload 2: GPIO 5
- Payload 3: GPIO 10
- Payload 4: GPIO 11 
- Payload 5: GPIO 14
- Payload 6: GPIO 15

### Stealth Mode
When the stealth mode is activated, the Pi will not show up as a USB device, if you connect it to a computer. For this connect GPIO 16 to Ground.

### Change Keyboard Layout
The original keyboard layout is set to US English. To change the language, download the keyboard layouts from [here](https://github.com/Neradoc/Circuitpython_Keyboard_Layouts/releases/tag/20221209).<br>
Put the keyboard layout into the lib folder on the Pi and change the imports in code.
