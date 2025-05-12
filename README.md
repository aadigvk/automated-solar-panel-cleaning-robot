# automated-solar-panel-cleaning-robot

**Automated Solar Panel Cleaning Robot** designed to maintain solar panel efficiency by regularly removing dust. The robot autonomously navigates on solar panels, detects obstacles, and activates a cleaning mechanism to ensure optimal solar energy production.

---

## Features

- **Automatic Movement:** Navigates solar panel surfaces using DC geared motors.
- **Obstacle Detection:** Uses an ultrasonic sensor to detect obstacles and panel edges.
- **Automated Cleaning:** Activates a cleaning mechanism (e.g., water pump) via a relay.
- **Microcontroller-Based:** Powered by an ESP32 for control, logic, and future IoT expansion.
- **Efficient Power Management:** Utilizes LM2576S and AMS1117 voltage regulators for stable operation.
- **User Feedback:** Includes status LEDs and a buzzer for alerts.

---

## Hardware Used

- **ESP32-WROOM-32** microcontroller
- **2 × 12V DC Geared Motors**
- **TB6612FNG or L293D Motor Driver IC**
- **12V Relay Module (with BC547 transistor)**
- **Ultrasonic Sensor (HC-SR04)**
- **LM2576S Step-Down Regulator**
- **AMS1117 3.3V Regulator**
- **Metal Chassis**
- **Wheels and Mounting Hardware**
- **Water Pump or Cleaning Actuator**
- **Li-ion Battery (7.4V)**
- **LEDs, Buzzer, Connectors, etc.**

---

## Getting Started

### 1. **Clone the Repository**
```bash
git clone https://github.com/aadigvk/automated-solar-panel-cleaning-robot.git
```

### 2. **Hardware Setup**
- Assemble the chassis, mount the motors, ESP32, sensors, relay, and cleaning actuator as per the hardware images and schematic.
- Connect all components following the provided circuit diagram.

### 3. **Upload the Code**
- Open the code in the Arduino IDE or PlatformIO.
- Select the correct ESP32 board and port.
- Upload the code from the `code/` directory.

### 4. **Power Up**
- Connect the 7.4V battery.
- The robot will start moving, detect obstacles, and activate the cleaning mechanism automatically.

---

## How It Works

1. **Movement:** The ESP32 controls the motors via the motor driver, moving the robot forward or turning as needed.
2. **Obstacle Detection:** The ultrasonic sensor measures distance; if an obstacle or edge is detected, the robot stops and turns.
3. **Cleaning:** The relay, controlled via a BC547 transistor, switches the cleaning actuator on/off during operation.
4. **Power Management:** LM2576S and AMS1117 regulators provide stable voltages for motors and logic.

---

## Testing

- **Movement and Navigation:** Tested on flat and inclined solar panels (up to 15°).
- **Obstacle Avoidance:** Verified with various obstacles and panel edges.
- **Cleaning Efficiency:** Compared panel output before and after cleaning.
- **Power Consumption:** Measured average current draw (~1.4–1.5A during operation).

---

## Future Improvements

- Add edge detection sensors for improved safety.
- Implement IoT features for remote monitoring and scheduling.
- Enhance cleaning mechanism for sticky contaminants.
- Improve weatherproofing for outdoor use.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Acknowledgements

- Inspired by open-source robotics and solar maintenance research.
- Uses ESP32 and open hardware components.
