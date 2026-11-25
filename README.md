# 🐾 Smart Pet Feeder

An Arduino-based automatic pet feeder that dispenses food using a motor, measures the portion by weight, monitors the remaining food level, and alerts the owner when the container runs low.

---

## Overview

Keeping a regular feeding schedule is hard when you are away from home. This project automates it: the feeder dispenses a measured portion, tracks how much food is left, and signals the owner when a refill is needed.

## Features

- **Automated dispensing:** a motor-driven mechanism releases food on demand.
- **Weight-based portioning:** a load cell checks the amount dispensed into the bowl.
- **Food level monitoring:** a distance sensor measures how much food remains in the container.
- **Low-food notification:** alerts the owner when the container is nearly empty.
- **Feeding-time sound cue:** plays a sound at feeding time to call the pet.

## Hardware Required

| Component | Purpose | Qty |
|---|---|---|
| Arduino-compatible board (`[Uno / ESP32 / etc.]`) | Main controller | 1 |
| DC / servo / stepper motor (`[specify]`) | Dispensing mechanism | 1 |
| Load cell + HX711 amplifier (`[confirm]`) | Measure food weight | 1 |
| Ultrasonic sensor (`[HC-SR04, confirm]`) | Measure food level | 2 |
| Buzzer / speaker module (`[confirm]`) | Feeding-time sound | 1 |
| Power supply (`[voltage / current]`) | Power the system | 1 |
| Jumper wires, breadboard / PCB | Connections | — |


## Repository Structure

| File | Description |
|---|---|
| `mainCODE.ino` | Main program integrating all modules |
| `NEWMAIN.ino` | Updated version of the main program |
| `motor.ino` | Standalone test for the dispensing motor |
| `weight.ino` | Standalone test for the load cell |
| `distance.ino` | Standalone test for the food-level sensor |
| `sound_with_time.ino` | Feeding-time sound logic |
| `FoodLevelNotify.ino` | Low-food level notification logic |



## How It Works

1. At the scheduled time, the feeder plays a sound cue.
2. The motor dispenses food into the bowl.
3. The load cell monitors weight until the target portion is reached, then the motor stops.
4. The distance sensor checks the food level in the container.
5. If the level is low, a notification is triggered so the owner can refill.

## Future Improvements

- [ ] Mobile app control and scheduling
- [ ] Wi-Fi / cloud logging of feeding history
- [ ] Adjustable portion sizes per pet
- [ ] Camera for remote viewing
- [ ] 3D-printed enclosure

## Author

**Sanjida Hossain Eva**
GitHub: [SanjidaHossainEva](https://github.com/SanjidaHossainEva)
