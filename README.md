# 🤖🔥 Arduino Fire Fighting Robot Project

Welcome to the **Arduino-based Fire-Fighting Robot** repository!  
This project is all about building a robot that can **detect fire**, **move towards it**, and **extinguish it**—all by itself! 🚗💦

---

## ✨ Features

- 🔥 **Fire Detection:** Uses multiple flame sensors to locate fire in the right, front, and left directions.
- 🚙 **Autonomous Movement:** Controls DC motors via an L293D driver to navigate towards danger.
- 💦 **Fire Extinguishing:** Activates a water pump and sweeps the water using a servo motor to douse the flames.

---

## 🛠️ Hardware Requirements

- 🟦 Arduino Board (Uno, Mega, Nano, etc.)
- 🧰 L293D Motor Driver Module
- 🔥 3 x Flame Sensors (Analog)
- 🔄 Servo Motor (for water spray direction)
- ⚡ Relay Module (to switch the water pump)
- 💧 Water Pump
- 🛞 DC Motors & Wheels
- 🪛 Chassis, Wires, Power Supply

---

## ⚡ Pin Configuration

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

---

## 📝 Code Overview

The main Arduino sketch does the following:

- **Setup:** Initializes all sensors, motors, servo, and relay.
- **Loop:** Reads sensor values, prints them via Serial Monitor, and:
  - ➡️ Moves the robot toward fire.
  - 💧 Activates water pump & sweeps with servo when fire detected.
  - ⏹️ Stops or reverses if no fire or to avoid obstacles.

**Key Functions:**
- `moveForward()`, `moveBackward()`, `turnRight()`, `turnLeft()`, `stopRobot()` – Robot movement
- `handleFireDetection()`, `sweepServo()` – Fire extinguishing
- `activatePump()`, `deactivatePump()` – Pump control

---

## 🚦 Getting Started

1. **Connect hardware** as per the pin configuration above. 🔌
2. **Upload the code** from `Code/#include Servo.h.txt` to your Arduino board. 📥
3. **Power up** and **test** by bringing a small flame (like a lighter or matchstick) near the sensors. The robot should chase and extinguish it! 🧯

---

## 📂 Folder Structure

```
Code/
  └── #include Servo.h.txt    # Main Arduino sketch
```

---

## 👤 Author

- [tanmoykdas](https://github.com/tanmoykdas)

---
