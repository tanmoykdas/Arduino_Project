# Arduino Fire Fighting Robot Project

This repository contains the code and resources for an **Arduino-based fire-fighting robot**. The robot is designed to detect fire using flame sensors, move towards the detected fire source, and extinguish it using a water pump controlled by a relay and a servo mechanism.

## Features

- **Fire Detection:** Uses multiple flame sensors to locate fire in different directions (right, front, left).
- **Autonomous Movement:** Controls DC motors via an L293D motor driver to navigate towards the fire.
- **Fire Extinguishing:** Activates a water pump and sweeps the water spray using a servo motor to cover a range of angles.

## Hardware Requirements

- Arduino Board (e.g., Uno, Mega, Nano)
- L293D Motor Driver Module
- 3 Flame Sensors (Analog)
- Servo Motor (for water nozzle movement)
- Relay Module (to switch the water pump)
- Water Pump
- DC Motors & Wheels
- Chassis, Wires, Power Supply

## Pin Configuration

| Component        | Arduino Pin | Description                        |
|------------------|-------------|------------------------------------|
| Motor IN1        | 9           | L293D Motor Driver IN1             |
| Motor IN2        | 8           | L293D Motor Driver IN2             |
| Motor IN3        | 7           | L293D Motor Driver IN3             |
| Motor IN4        | 6           | L293D Motor Driver IN4             |
| Flame Sensor R   | A0          | Right flame sensor (analog)        |
| Flame Sensor F   | A1          | Front flame sensor (analog)        |
| Flame Sensor L   | A2          | Left flame sensor (analog)         |
| Servo Control    | A4          | Servo signal pin                   |
| Relay Control    | A5          | Relay for water pump               |

> **Note:** Common ground is required for all modules.

## Code Overview

The main Arduino sketch implements:

- **Setup:** Initializes all sensors, motors, servo, and relay.
- **Loop:** Reads sensor values, prints them to serial, and applies logic to:
  - Move robot toward the fire.
  - Activate water pump and sweep with servo when fire is detected.
  - Stop or reverse if no fire or to avoid obstacles.

Key functions include:
- `moveForward()`, `moveBackward()`, `turnRight()`, `turnLeft()`, `stopRobot()` for robot movement.
- `handleFireDetection()` and `sweepServo()` for extinguishing fire.
- `activatePump()` and `deactivatePump()` for pump control.

## Getting Started

1. **Connect hardware** as per the pin configuration.
2. **Upload the code** from the `Code/#include Servo.h.txt` file to your Arduino board.
3. **Power up** the system and test fire detection and extinguishing with a flame (e.g., lighter or matchstick).

## Folder Structure

- `Code/`
  - `#include Servo.h.txt` – Main Arduino sketch with motor, sensor, and pump control logic.

## Author

- [tanmoykdas](https://github.com/tanmoykdas)
