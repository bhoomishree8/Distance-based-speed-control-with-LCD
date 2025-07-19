# Distance-Based Speed Control with LCD 

Project Type: Hardware and Software Integration (Arduino + ROS2)  

## Project Overview

The project uses two Arduinos connected via USB to a computer running ROS2. One Arduino measures distance using an ultrasonic sensor and sends the data to the ROS2 node via serial. The second Arduino, connected to an LCD, receives the proximity information from a ROS2 subscriber node and displays context-specific messages.
The distance_publisher node reads serial input from the sensor Arduino and publishes it to the /distance topic. The status_subscriber node listens to this topic and sends formatted messages to the LCD Arduino via another serial connection.
ROS2 provides the backbone for inter-node communication, while Arduino handles low-level sensor reading and LCD display.


## Components Used

    • Arduino Uno (x2): One for ultrasonic sensor and another for LCD interfacing
    • Ultrasonic Sensor (HC-SR04): For measuring distance to obstacles
    • LCD Display (16x2): For displaying distance status
    • Motor Driver and DC Motors: To control motor actions
    • USB Serial Connections: For communication between Arduino and ROS2
    • Jumper Wires and Breadboards
    • Power Supply

