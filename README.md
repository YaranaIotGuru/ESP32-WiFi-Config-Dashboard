# ESP32 WiFi Dashboard

This project provides a dynamic WiFi configuration dashboard for ESP32 using AsyncWebServer and WebSockets. Easily switch WiFi networks without re-uploading code.

## Features

- Dynamic WiFi configuration
- Web dashboard for managing WiFi networks
- Uses AsyncWebServer and WebSockets for real-time updates
- Stores WiFi credentials using Preferences library
- Reset to default WiFi credentials using the boot button

## Requirements

- ESP32 board
- Arduino IDE with ESP32 board support installed
- Required libraries:
  - WiFi
  - AsyncTCP
  - ESPAsyncWebServer
  - Preferences
  - ArduinoJson

## Pin Definitions

- `bootButtonPin` (GPIO0): Typically used for the boot button on ESP32
- `ledPin` (GPIO2): Typically has an onboard LED

## How It Works

1. **Web Dashboard**: The web dashboard displays available WiFi networks. You can select a network and enter the password to connect your ESP32 to a new WiFi network without re-uploading code.
2. **WiFi Scanning**: The ESP32 scans for available WiFi networks and sends the results to the web dashboard via WebSockets.
3. **Saving Credentials**: The selected SSID and password are saved using the Preferences library.
4. **Reset to Default**: Press the boot button for 2 seconds to reset the WiFi credentials to default values.

## Setup

1. **Install Required Libraries**:
   - Install the required libraries from the Arduino Library Manager.
2. **Upload Code**:
   - Open the `code.ino` file in Arduino IDE.
   - Select your ESP32 board and the correct COM port.
   - Upload the code to your ESP32.
3. **Connect to WiFi**:
   - Open the serial monitor to view the IP address assigned to your ESP32.
   - Open a web browser and navigate to the IP address to access the WiFi configuration dashboard.

## Usage

1. Connect to the ESP32's WiFi hotspot.
2. Open the provided IP address in a web browser.
3. Select a WiFi network from the list, enter the password, and click "Connect".
4. The ESP32 will connect to the new WiFi network and display the new IP address.

## Video Tutorial

For a detailed step-by-step guide, watch the video tutorial:

[![Change WiFi Connection Using WiFi Dashboard](https://img.youtube.com/vi/frt7MSAPuXU/0.jpg)](https://youtu.be/frt7MSAPuXU)

Click on the thumbnail above to watch the video.

---

All rights by Yarana IoT Guru
