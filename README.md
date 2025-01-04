# Project---ML-Based-Laser-Tracking-Security-System
In this project I have created a computer vision-driven security system that uses pose detection to track and respond to human presence. The system combines MediaPipe pose detection with Arduino-controlled laser tracking, creating an intelligent security solution that can follow targets and respond to proximity alerts.

## Features
- Real-time pose detection and tracking using MediaPipe
- Distance-adaptive tracking with dynamic position adjustment
- Multi-threaded processing for optimal performance
- Integrated alarm system with ultrasonic sensor detection
- Remote control capabilities via IR sensor

## Technologies Used
- Python 3.10
- Arduino
- MediaPipe
- OpenCV
- Serial Communication
- Hardware Components:
  - Arduino Uno
  - 2x MG9964 Servo Motors
  - Ultrasonic Sensor
  - IR Receiver
  - Laser Module
  - LED & Buzzer
  - Power supply module
  - 5V DC wall adapter

## Setup
- Connect all the sensors and parts to the breadboard using mtm wires
  - Connect arduino to breadboard 5v and ground rails
  - Led with resistor and buzzer to arduino pin and ground
  - Laser diode inside a tube (I used a pen) connected to wires with a resistor to power
  - Ultrasonic sensor connected to power, ground, and an echo and trigger pins connected to arduino
  - IR sensor connected to power, ground, and arduino pin
  - 2 servos set up one for x-axis movement one for y-axis movement, connected to power, ground, and arduino pins
  - Power the power supply module with a 5V dc wall adapter
- Mount the bottom servo somewhere stable, and the top servo on its side ontop of the bottom servo, and connect the laser tube to the wheel of the top servo
- Point out the ultrasonic sensor in direction of where you want the tripwire to be

## Hardware Requirements
- Computer powerful enough to use ML algorithm effectively and communicate to arduino
- Decent webcam (at least 480p)

## Dependencies
- Arduino IDE
- Python, I used Pycharm

## Usage
- Upload the arduino code to the arduino using a data cable
- Run the Python code
- Click the button on IR remote to arm the device, then once you cross the ultrasonic sensor, it will trigger the device
- Once the device is triggered it will set off the alarm, blink the led, turn on the laser and activate the servos to track you using the ML algorithm

## Future Improvements
- If someone is detected it will record video and send to phone
- Eventually make it entirely embedded with Nvidia Jetson Nano, and a bigger power supply
- Implement multiple target tracking
- Add remote monitoring features
