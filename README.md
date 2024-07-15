# Smart-Vaccum-Cleaner
The smart vacuum cleaner is an autonomous robotic device designed to clean floors by navigating around obstacles using sensors and motors controlled by an Arduino microcontroller. This README file provides detailed information on the components used, how to set up the project, and how to operate and troubleshoot the vacuum cleaner.

# Components
## 1)Arduino Microcontroller 
**Model:** Arduino Uno (or equivalent)

**Function:** Processes input from sensors and controls the motors.

## 2)Motor Driver Shield
**Model:** L298N Motor Driver Shield (or equivalent)

**Function:** Amplifies control signals from the Arduino to drive the motors.

## 3)DC Motors (4)
**Model:** Generic DC motors with gearboxes

**Function:** Provide movement by driving the wheels.

## 4)Battery Pack
**Model:** Lithium-ion battery pack (4 cells)

**Function:** Powers the entire circuit

## 5)Ultrasonic Sensor
**Model:** HC-SR04 Ultrasonic Distance Sensor

**Function:** Measures distance to obstacles for navigation.

## 6)Servo Motor
**Model:** Generic SG90 Servo Motor

**Function:** Adjusts orientation or specific components of the vacuum cleaner.

## 7)DC Motor
**Model:** MorningVale EB-TOY-MTR

**Function:** To rotate the fan.

# Circuit Diagram and Connections
![Circuit Diagram](Circuit%20Diagram.jpg)
## 1.Power Connections:
### Motor Driver Shield to Arduino:
  - Connect the power pins (usually labeled VCC and GND) on the motor driver shield to the corresponding 5V and GND pins on the Arduino.
## 2.Control Pins:
### Arduino Digital Pins to Motor Driver Shield:
  - Connect Arduino digital pins to the control inputs (typically labeled IN1, IN2, IN3, IN4) on the motor driver shield. These pins control the direction and speed of the motors connected to the shield.
## 3.Motor Driver Shield to Motors:
### M1, M2, M3, M4 Pins on Motor Driver Shield:
  - Connect the motors to these output pins on the motor driver shield. Ensure each motor is connected to its corresponding pins (M1 for Motor 1, M2 for Motor 2, and so on).
## 4.Ultrasonic Sensor:
### VCC and GND:
  - Connect the VCC pin of the ultrasonic sensor to the 5V pin on the Arduino.
  - Connect the GND pin of the ultrasonic sensor to the GND pin on the Arduino.
### Trigger and Echo Pins:
  - Connect the Trigger pin of the ultrasonic sensor to a specific digital pin on the Arduino (e.g., pin 9).
  - Connect the Echo pin of the ultrasonic sensor to another specific digital pin on the Arduino (e.g., pin 10).
## 5.Servo Motor:
### Control Wire:
  - Connect the control wire (usually colored yellow or white) of the servo motor to a PWM (Pulse Width Modulation) capable pin on the Arduino (e.g., pin 11).
### Power and Ground Wires:
  - Connect the power wire (usually red) of the servo motor to the 5V pin on the Arduino.
  - Connect the ground wire (usually black or brown) of the servo motor to the GND pin on the Arduino.
## 6.Battery Connections:
### Powering the Motor Driver Shield:
  - Connect a battery pack (e.g., Lithium Ion batteries) to the motor driver shield’s power input pins (usually labeled VCC and GND) to provide sufficient power for the motors.

# Operation
## 1.Power On:
  -Insert the batteries into the battery pack.
  -Turn on the power switch (if available).
## 2.Initialization:
  -The Arduino initializes the motors and sensors.
  -The servo motor moves to its initial position.
## 3.Obstacle Detection:
  -The ultrasonic sensor continuously measures the distance to obstacles.
  -If an obstacle is detected within a certain range, the Arduino processes this information.
## 4.Movement Control:
  - Based on sensor data, the Arduino controls the motors to move forward, stop, or turn to avoid obstacles.
  - The servo motor may adjust to help with navigation.
## 5.Continuous Operation:
  - The vacuum cleaner continues to navigate and clean the area until turned off or the batteries are depleted.
# Conclusion
  This smart vacuum cleaner project demonstrates the integration of various electronic components to create an autonomous cleaning device. By following this documentation, you can replicate the project and understand its workings.

