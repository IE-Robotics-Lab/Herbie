# Herbie: The Autonomous Plant

Herbie is an autonomous plant system designed to sustain itself for long periods, potentially even for its entire life. Herbie is equipped with several sensors and is mounted on a platform capable of omnidirectional movement. This README file provides an overview of the components and instructions for setting up and running Herbie.

## Components

### Arduino Code

The Arduino board is connected to the motors and wheels, making it responsible for Herbie's movement. The basic commands for controlling the Arduino board to move in various directions are provided in the code. Additionally, there is an option for connecting the Arduino board directly to a Wi-Fi network, allowing control via the OYOSHO app.

#### Arduino Wi-Fi Setup

1. **Network Configuration**: Enter your network SSID and password in the designated section of the Arduino code.
2. **Run the Code**: Upload the code to the Arduino board. Once connected to the network, the IP address will be displayed.
3. **OYOSHO App Control**: Open the OYOSHO app and enter the IP address to control the Arduino board.

#### OYOSHO App Commands

- **Pause**: Stop
- **Top Arrow**: Move forward
- **Bottom Arrow**: Move backwards
- **Left Arrow**: Move left
- **Right Arrow**: Move right
- **Obstacle**: Move sideways to the right
- **Tracking**: Move sideways to the left
- **F1**: Move forward diagonally from left to right
- **F6**: Move backward diagonally from left to right
- **F3**: Move forward diagonally from right to left
- **F4**: Move backward diagonally from right to left

### light-to-movement.py

This Python script is designed to fetch data from the Xiaomi MiFlora sensor using Bluetooth. It collects information on moisture, fertility, temperature, and light intensity. When the sensor detects light levels below 140 lux, the script sends a signal to the Arduino to move Herbie to a location with better light.

#### Script Functionality

1. **Initialize Serial Communication**: Set up communication between the Raspberry Pi and Arduino.
2. **Read Sensor Data**: Implement a function to read data from the light sensor.
3. **Control Movement**: Based on the sensor data, send commands to the Arduino to control Herbie's movement.
4. **Handle Reconnection**: Ensure the script can handle disconnections and attempt to reconnect.

## Setup Instructions

### Hardware Setup
