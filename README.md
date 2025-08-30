
# Obstacle Avoidance Robot

An Arduino-based autonomous obstacle avoidance robot that uses an **ultrasonic sensor**, **IR sensor**, **servo motor**, and an **I2C LCD display** to navigate its surroundings. The robot moves forward until it detects an obstacle, then decides whether to turn left or right based on distance readings.

---

## Features

* Obstacle detection using **HC-SR04 Ultrasonic Sensor**
* IR sensor for additional obstacle sensing
* **Servo-mounted ultrasonic scanner** for left/right distance measurement
* **L298N motor driver** for bidirectional motor control
* **I2C LCD display** showing turn count in real-time
* Push button to start/stop robot operation

---

## Components Used

* Arduino Uno / Nano
* Ultrasonic Sensor (HC-SR04)
* IR Sensor Module
* Servo Motor (SG90 / MG90S)
* L298N Motor Driver
* I2C 16x2 LCD Display
* Push Button
* DC Motors + Wheels + Chassis
* Power Supply (Li-ion/LiPo or batteries)

---

## Working Principle

1. The ultrasonic sensor continuously measures distance ahead.
2. If an obstacle is detected within 15 cm:
   * The servo rotates left and right to measure distances.
   * The robot chooses the side with more space and turns accordingly.
   * Turn count is updated and displayed on LCD.
3. If no obstacle is detected, the robot moves forward.
4. IR sensor adds an extra layer of obstacle detection.

---

## How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/Obstacle-Avoidance-Robot.git
   cd Obstacle-Avoidance-Robot/code
   ```
2. Open `obstacle_avoidance_robot.ino` in **Arduino IDE**.
3. Install required libraries:

   * Servo.h (pre-installed)
   * LiquidCrystal\_I2C.h (via Library Manager)
4. Connect Arduino, select correct COM port, and upload code.
5. Power the robot and press the button to start.

---

## Future Improvements

* Add Bluetooth or Wi-Fi control
* Implement PID for smoother turns
* Multi-sensor fusion for better obstacle avoidance
* Speed control using PWM

---

