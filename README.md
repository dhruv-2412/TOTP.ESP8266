# ESP8266 TOTP with Python MQTT Integration

## Introduction

This project demonstrates the use of an ESP8266 microcontroller to generate Time-based One-Time Passwords (TOTP) and validate them through a Python application using MQTT protocol. The ESP8266 acts as an OTP generator, while the Python application handles the validation of these OTPs.
To configure the totp you'll need two things
1] secret key(in our case its the mac id of the esp)
2] Current time (which we get throught the ntp)
The secret key can be in base32 or Hex ,as per your need you use any one of them 
As I needed the code to identify the macID of the esp itself I have written the code as per my need, you can manually add the hmac key(secret key) by editing the code slightly.


## Project Overview

The main components of this project are:
1. **ESP8266 Microcontroller**: Configured to generate TOTP.
2. **Python Application**: Subscribes to MQTT topics and validates OTPs.
3. **MQTT Broker**: Facilitates communication between the ESP8266 and the Python application.

## Features

- **TOTP Generation**: Uses the ESP8266 to generate time-based OTPs.
- **MQTT Communication**: Sends and receives OTPs through MQTT.
- **Python Validation**: Validates the received OTPs using a Python script.
- **Secure and Reliable**: Ensures secure and reliable OTP validation.

## Prerequisites

- ESP8266 Microcontroller
- ESP8266 WiFi library
- TOTP library from Luca Dentella
- PubSubClient library for MQTT connection
- Any python application
- `paho-mqtt` Python library
- MQTT Broker (e.g., MQTTX)


## Getting Started

### ESP8266 Setup

1. **Hardware Requirements**:
   - ESP8266 microcontroller
   - USB cable to connect ESP8266 to the computer

2. **Software Requirements**:
   - Arduino IDE
   - ESP8266 Board package for Arduino

3. **Installation**:
   - Install the ESP8266 board package in Arduino IDE.
   - Install necessary libraries for TOTP generation and MQTT communication(for totp library use luca dentella and for mqtt library use PubSubClient).

4. **Code**:
   - They are provided above in txt format.
  
### MQTT connection

1. **MQTT BROKER**
   - Install any MQTT broker (I have used MQTTX)
   - Use Proper username
   - Proper Password
   - Broker server ID
   - And use the proper topic


### Python Application Setup

1. **Dependencies**:
   - Install `paho-mqtt` library:
     ```sh
     pip install paho-mqtt
     ```

2. **Code**:
   Uploaded above in txt format.

## Usage

1. Power on the ESP8266 and ensure it connects to your Wi-Fi network.
2. Ensure your MQTT broker is running and accessible.
3. Run the Python application to start listening for OTPs.
4. The ESP8266 will publish OTPs to the specified MQTT topic.
5. The Python application will validate the received OTPs and log the results.

## Repository Structure

- **esp8266-code/**: Contains the Arduino sketch for the ESP8266.
- **python-app/**: Contains the Python application for OTP validation.

## Acknowledgements

- [Arduino](https://www.arduino.cc/)
- [ESP8266](https://www.espressif.com/en/products/socs/esp8266)
- [paho-mqtt](https://www.eclipse.org/paho/)
- [luca-dentella](https://www.lucadentella.it/en/totp-libreria-per-arduino/)

## Contact

For any inquiries or support, please contact [dhruvsavla03@gmail.com](mailto:dhruvsavla03@gmail.com).


