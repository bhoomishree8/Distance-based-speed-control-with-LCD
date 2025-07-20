#  Distance-Based Speed Control with LCD

A hardware-software integrated project using **Arduino Uno boards** and **ROS2 (Robot Operating System)** to control speed and display proximity-based status messages.  

## Project Overview

This system uses two Arduinos and ROS2 to measure distance and display proximity feedback:

- One Arduino connects to an **ultrasonic sensor (HC-SR04)** and sends distance data to ROS2 via serial communication.
- ROS2 runs two nodes:
  - `distance_publisher`: Reads serial input and publishes distance to the `/distance` topic.
  - `status_subscriber`: Subscribes to `/distance`, generates a status message, and sends it to the second Arduino.
- The second Arduino displays the received status on a **16x2 LCD**.
- Optionally, a motor driver can be added to control speed based on the measured distance.
- ROS2 provides the backbone for inter-node communication, while Arduino handles low-level sensor reading and LCD display.


## Components Used

| Component               | Quantity | Purpose                                |
|------------------------|----------|----------------------------------------|
| Arduino Uno            | 2        | One for sensor, one for LCD            |
| Ultrasonic Sensor (HC-SR04) | 1   | Measures distance to obstacle          |
| 16x2 LCD Display        | 1        | Displays proximity status              |
| Motor Driver (L298N)   | 1 (optional) | Controls motor speed/direction     |
| DC Motor               | 1–2      | For physical movement                  |
| USB Cables             | 2        | Serial communication to ROS2 host      |
| Breadboard & Jumper Wires | –     | Circuit connections                    |
| Power Supply           | –        | To power Arduino and motors            |


##  How It Works
1. Upload `distance_sensor.ino` to Arduino-1 (with HC-SR04)
2. Upload `lcd_display.ino` to Arduino-2 (with LCD)
3. Launch ROS2 nodes


