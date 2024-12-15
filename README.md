# Raspberry Pi Pico W as a Rubber Ducky

## Overview

### Raspberry Pi Pico W
The Raspberry Pi Pico W is a microcontroller board based on the RP2040 chip, with built-in WiFi support. It's lightweight, affordable, and perfect for DIY projects and automation.

### Rubber Ducky
A Rubber Ducky is a USB device that acts like a keyboard to execute pre-written scripts (Ducky Scripts) on a target device, automating tasks or running payloads.

---

## Setup Guide
Follow these 5 simple steps to turn your **Raspberry Pi Pico W** into a Rubber Ducky:

### Step 1: Reset the Raspberry Pi Pico W
1. Connect the Raspberry Pi Pico W to your PC in setup mode:
   - Hold the **BOOTSEL button** while plugging it into the PC.
2. Open the `01 NUKE IT` folder.
3. Copy and paste the `flash_nuke.uf2` file onto the Pico W.
   - This will reset the board automatically.

---

### Step 2: Install CircuitPython
1. Open the `Step 1` folder.
2. Copy and paste the `adafruit-circuitpython-raspberry_pi_pico_w-en_GB-9.2.1.uf2` file onto the Pico W.
   - This installs CircuitPython.
3. After installation, the device name will change from **RPI-RP2** to **CIRCUITPY**.

---

### Step 3: Add Required Libraries
1. Open the `Step 2/Lib folder paste` folder.
2. Copy the following files:
   - `adafruit_hid`
   - `adafruit_wsgi`
   - `asyncio`
   - `adafruit_debouncer.mpy`
   - `adafruit_ticks.mpy`
3. Paste these files into the **`lib`** folder on the **CIRCUITPY** drive.

---

### Step 4: Copy Root Files
1. Open the `Step 3/Root folder paste` folder.
2. Copy the following files:
   - `boot.py`
   - `code.py`
   - `duckyinpython.py`
   - `secrets.py`
   - `webapp.py`
   - `wsgiserver.py`
3. Paste these files into the **root folder** of the **CIRCUITPY** drive.
   - **Note:** Do not modify any other files in the root folder.

---

### Step 5: Add Payload
1. Open the `Step 4/Add payload.dd file` folder.
2. Copy your `payload.dd` file to the root folder of the **CIRCUITPY** drive.
   - **Payload.dd:** This file contains the Ducky Script that will execute on the target device.
   - You can create your own Ducky Script by referring to the [Hak5 Documentation](https://docs.hak5.org/hak5-usb-rubber-ducky/duckyscript-tm-quick-reference).
   - Alternatively, use example payloads from the `Step 5 (Example Payloads)` folder.

---

## Final Step: Test Your Rubber Ducky
1. Plug the Raspberry Pi Pico W into the target device.
2. The Rubber Ducky script will execute automatically.

---

## Disclaimer
This project is for **educational purposes only**. Use responsibly and ensure you have permission to test devices.

---

### Happy Hacking!
