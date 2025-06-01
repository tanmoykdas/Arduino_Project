# Arduino Fire-Fighting Robot Project

This repository documents the design and implementation of an **autonomous Arduino-based fire-fighting robot** capable of detecting fires, navigating toward them, and extinguishing flames automatically.

---

## Features

- **Fire Detection:** Utilizes multiple flame sensors to identify fire sources in front, left, and right directions.
- **Autonomous Navigation:** Employs DC motors and an L293D driver to approach detected fires.
- **Active Fire Extinguishing:** Controls a water pump and a servo mechanism to direct and disperse water over the fire.

---

## Hardware Requirements

- Arduino Board (Uno, Mega, Nano, etc.)
- L293D Motor Driver Module
- 3 Analog Flame Sensors (Right, Front, Left)
- Servo Motor (for directional water spraying)
- Relay Module (to control the pump)
- Water Pump
- DC Motors and Wheels
- Robot chassis, jumper wires, and a suitable power supply

---

## Pin Configuration

| Component         | Arduino Pin | Description                      |
|-------------------|-------------|----------------------------------|
| Motor IN1         | 9           | L293D Motor Driver IN1           |
| Motor IN2         | 8           | L293D Motor Driver IN2           |
| Motor IN3         | 7           | L293D Motor Driver IN3           |
| Motor IN4         | 6           | L293D Motor Driver IN4           |
| Flame Sensor Right| A0          | Analog input for right sensor    |
| Flame Sensor Front| A1          | Analog input for front sensor    |
| Flame Sensor Left | A2          | Analog input for left sensor     |
| Servo Control     | A4          | Servo signal control             |
| Relay Control     | A5          | Relay for water pump             |

---

## Code Overview

The main Arduino sketch (`Code/#include Servo.h.txt`) handles:

- **Initialization:** Setting up sensors, motors, servo, and relay controls.
- **Main Loop:** Continuously reads flame sensor data, prints values to Serial Monitor, and:
  - Directs the robot to approach detected fire.
  - Activates the water pump and uses the servo to sweep water when fire is present.
  - Stops or maneuvers to avoid obstacles when no fire is detected.

**Core Functions:**
- `moveForward()`, `moveBackward()`, `turnRight()`, `turnLeft()`, `stopRobot()` – Robot mobility
- `handleFireDetection()`, `sweepServo()` – Fire detection and extinguishing process
- `activatePump()`, `deactivatePump()` – Water pump control

---

## Getting Started

1. **Assemble hardware** according to the pin configuration table.
2. **Upload the code** from `Code/#include Servo.h.txt` to your Arduino.
3. **Power the robot** and test its operation by introducing a controlled flame near the sensors—the robot should automatically move toward and extinguish the fire.

---

## Folder Structure

```
Code/
  └── #include Servo.h.txt    # Main Arduino sketch
```

---

## Author

- [tanmoykdas](https://github.com/tanmoykdas)

---

Thank you for exploring this project!
