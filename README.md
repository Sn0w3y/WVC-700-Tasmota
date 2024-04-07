# ESP8266 Tasmota Scripting Guide

This README provides a comprehensive guide on flashing Tasmota firmware onto an ESP8266, configuring WiFi settings, uploading and enabling a script, setting device commands, and configuring module pins.

## Prerequisites

Before you begin, ensure you have the following:
- An ESP8266 device.
- A computer with a USB port.
- A Serial-to-USB adapter (if your ESP8266 does not have a USB port).
- The Tasmota firmware file (`tasmota-scriptserial160mhz2MB.bin`).
- A flashing tool such as Tasmotizer.

## 1. Flashing Firmware onto ESP8266

1. **Download Firmware**: Obtain the `tasmota-scriptserial160mhz2MB.bin` from the Tasmota GitHub releases page.
2. **Prepare Device**: Connect the ESP8266 to your computer using a USB cable or via a Serial-to-USB adapter.
3. **Flash Firmware**: Open your flashing tool, select the correct COM port, load the downloaded firmware file, and initiate the flashing process. Wait for completion.

## 2. Configure WiFi

After flashing, the ESP8266 will create a WiFi access point (AP). Connect to this AP from a computer or mobile device to configure your WiFi settings.

1. Connect to the `tasmota-XXXX` network.
2. Open a web browser and navigate to `http://192.168.4.1`.
3. Enter your WiFi SSID and password to connect the device to your local network.

## 3. Configure the Script

To upload and enable a script on your Tasmota device:

1. Access the Tasmota device web interface by entering its IP address in a web browser.
2. Navigate to **Scripts**.
3. Paste the contents of your `script_file.script` into the text area.
4. Save the script and ensure it's enabled.

## 4. Device Configuration Commands

Execute the following commands in the Tasmota console to configure your device further:

```plaintext
ledstate 7
so65 1
```
These commands adjust LED behaviors and set other device-specific options.

## 5. Module Configuration
Configure the GPIO pins via the module configuration:

1. In the Tasmota web interface, go to Configuration -> Configure Module.
2. Assign GPIO 5 to Led.
3. Save your configuration.

## 6. Have Fun!
Your ESP8266 with Tasmota firmware is now ready. Enjoy exploring the vast features and capabilities of your device!
