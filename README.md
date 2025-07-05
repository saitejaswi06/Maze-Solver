# 🔍 Maze Solver Robot | Arduino Uno + Ultrasonic Sensors + Differential Drive

An autonomous robot designed to navigate mazes using distance sensing and real-time decision-making. Built on a differential drive platform, it uses ultrasonic sensors for wall detection and implements the **Right-Hand or Left-Hand Rule** to solve mazes.

## ⚙️ Technologies & Components Used
| Component                 | Purpose                                      |
|----------------------------|----------------------------------------------|
| Arduino Uno                | Main microcontroller                         |
| HC-SR04 Ultrasonic Sensors | Detect walls and measure distances           |
| L293D / L298N Motor Driver | Controls two DC motors for differential drive|
| DC Gear Motors             | Drive the left and right wheels              |
| LiPo Battery (7.4V / 11.1V)| Provides stable power to motors and control |
| Buck Converter             | Regulates voltage for safe 5V operation      |
| Chassis & Castor Wheel     | Supports robot frame                         |

## 🛠️ Working Principle
- Uses **front, left, and right ultrasonic sensors** to measure distances to maze walls.
- Implements a **Right-Hand or Left-Hand Algorithm** for maze solving:
   - If there is space to the right, turn right.
   - If front is clear, move forward.
   - If blocked ahead and right, turn left.
- Continuously updates navigation based on real-time sensor readings.

## 🔋 Power System
- Powered by a LiPo battery regulated through a buck converter for consistent 5V supply to the Arduino and motor drivers.
- Ensures stable operation across variable load conditions.

## 🧠 Control Logic
- Ultrasonic sensors connected to Arduino digital pins trigger distance measurement using pulseIn().
- Logic-based decision tree selects motion direction.
- PWM-based speed control adjusts motor speeds during sharp turns.

## ✅ Features
- Autonomous navigation and obstacle avoidance.
- Accurate distance measurement (~±1 cm error).
- Modular code structure for easy algorithm changes.
- Efficient LiPo battery power with voltage regulation.

## 🔧 Possible Future Enhancements
- Add PID control for smoother navigation in tight spaces.
- Map the maze dynamically using a grid array or SLAM.
- Replace Arduino Uno with an ESP32 or Raspberry Pi for advanced processing.

