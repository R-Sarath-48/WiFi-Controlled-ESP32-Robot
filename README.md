# WiFi-Controlled-ESP32-Surveillance-Robot

## Introduction

The ESP32 WiFi-Controlled Robotic Platform is an embedded robotics project designed for real-time wireless navigation and interactive robotic behavior. The system uses an ESP32 microcontroller to host an embedded HTTP web server, allowing the robot to be controlled directly from a mobile device through WiFi.

The robot integrates motor control and OLED-based animated eye rendering to create an interactive robotic system. The project demonstrates concepts in embedded systems, IoT communication, wireless robotics, graphical display rendering, and non-blocking firmware architecture.

## Components Used
Component	Purpose
ESP32 Development Board	Main controller and WiFi communication
L298N Motor Driver	Controls DC motors
DC Motors	Robot movement
SH1106 OLED Display	Animated robotic eye display
Robot Chassis	Mechanical structure
Battery Pack	Power supply
Jumper Wires	Circuit connections
System Architecture
Hardware Architecture
ESP32 acts as the central controller.
L298N motor driver interfaces the ESP32 with the DC motors.
OLED display is connected using I2C communication.
Mobile devices communicate wirelessly with the ESP32 through WiFi.
Battery powers the complete robotic system.

## Software Architecture
ESP32 hosts an embedded HTTP web server.
Web interface sends movement commands through HTTP requests.
Firmware processes commands and controls motors in real time.
OLED animation engine continuously updates the robotic eye.
Non-blocking timing using millis() enables simultaneous multitasking.

## Web Control Interface
The robot includes a browser-based control interface hosted directly on the ESP32.

### Features
Mobile responsive design
Real-time directional control
Touch-based navigation buttons

### Wireless communication
Low-latency command execution
Available Controls
Forward
Backward
Left
Right
Stop
The interface can be accessed by connecting to the ESP32 WiFi network and opening the ESP32 IP address in a browser.

## Working
The ESP32 initializes the WiFi Access Point and starts an embedded HTTP web server.
A mobile device connects to the ESP32 WiFi network.
The user opens the hosted control webpage through a browser.
When a control button is pressed, the webpage sends an HTTP request to the ESP32.
The ESP32 processes the received command and controls the motor driver accordingly.
The L298N motor driver drives the DC motors for robot navigation.
Simultaneously, the OLED display renders an animated robotic eye.
The pupil animation continuously moves left and right using non-blocking timing logic based on millis().
The entire system operates in real time while maintaining stable WiFi communication and smooth OLED animation rendering.
