# Obstacle Avoiding Car - Arduino Uno 🚗

A smart self-driving car that automatically avoids obstacles using Arduino Uno.

## Project Overview 📋
A smart car that uses an Ultrasonic Sensor to detect obstacles and avoid them automatically. The car is equipped with a servo motor that rotates the distance sensor to scan the surrounding environment.

## Components Used 🔧
- **Arduino Uno** - Main microcontroller board
- **Ultrasonic Sensor (HC-SR04)** - For detecting obstacles and measuring distances
- **DC Motors (4x)** - Movement motors
- **Motor Driver Shield (L298N)** - For controlling the motors
- **Servo Motor** - To rotate the distance sensor
- **9V Battery** - Power source
- **Wheels & Chassis** - Frame and wheels

## Circuit Diagram 📐
![Obstacle Avoiding Car Circuit](https://cdn.corenexis.com/f/v2UiPsSxMh3.png)

The circuit diagram above shows all the connections:
- **Servo Motor** - Controls the direction of the ultrasonic sensor
- **Ultrasonic Sensor (HC-SR04)** - Measures distance to obstacles
- **Motor Driver Shield (L298N)** - Manages the 4 DC motors
- **4 DC Motors** - Drive the car forward, backward, and turns
- **9V Battery** - Powers the entire system
- **Switch** - On/Off control

## How It Works ⚙️

1. **Detection Phase**: The ultrasonic sensor continuously measures the distance in front of the car
2. **Decision Phase**: 
   - If distance < 15 cm → Obstacle detected
   - If distance ≥ 15 cm → Continue forward
3. **Obstacle Avoidance**:
   - Stop the car
   - Move backward slightly
   - Rotate the sensor left and right to scan
   - Choose the direction with more space
   - Turn in that direction
4. **Continue**: Resume moving forward

## Required Libraries 📚

Before uploading the code, install these 3 libraries:

1. **AFMotor Library**
   - https://learn.adafruit.com/adafruit-motor-shield/library-install

2. **NewPing Library**
   - https://github.com/livetronic/Arduino-NewPing

3. **Servo Library**
   - Pre-installed with Arduino IDE ✅

See `INSTALLATION.md` for detailed installation steps.

## Quick Start 🚀

### 1. Install Libraries
Follow the instructions in `INSTALLATION.md`

### 2. Upload Code
- Open `code/ARDUINO_OBSTACLE_AVOIDING_CAR.ino` in Arduino IDE
- Select Board: **Arduino Uno**
- Select correct COM Port
- Click **Upload**

### 3. Assembly
- Follow the circuit diagram above
- Connect all components as shown
- Ensure all connections are secure

### 4. Test
- Power on the car
- Place it on the ground
- It should move forward and avoid obstacles automatically!

## Pin Configuration 📌

| Component | Pin |
|-----------|-----|
| Ultrasonic Sensor TRIG | A0 |
| Ultrasonic Sensor ECHO | A1 |
| Servo Motor | Pin 10 |
| Motor 1 | Motor Driver OUT1/OUT2 |
| Motor 2 | Motor Driver OUT3/OUT4 |
| Motor 3 | Motor Driver OUT1/OUT2 (Ch B) |
| Motor 4 | Motor Driver OUT3/OUT4 (Ch B) |

## Features ✨

- ✅ Automatic obstacle detection
- ✅ Smart path finding
- ✅ 360-degree scanning with servo
- ✅ Smooth acceleration/deceleration
- ✅ Low power consumption
- ✅ Works in any lighting condition

## File Structure 📁

```
obstacle-avoiding-car/
├── README.md                           # This file
├── INSTALLATION.md                     # Library installation guide
├── WIRING.md                          # Detailed wiring connections
├── code/
│   └── ARDUINO_OBSTACLE_AVOIDING_CAR.ino
└── circuit/
    └── circuit_diagram.jpg            # Circuit diagram image
```

## Troubleshooting 🔧

### Car doesn't move
- Check battery voltage (should be 9V+)
- Verify motor connections
- Check if all motors have power

### Sensor doesn't detect obstacles
- Verify A0 and A1 connections
- Check sensor orientation (facing forward)
- Test sensor with multimeter

### Servo doesn't rotate
- Check Pin 10 connection
- Verify servo power supply
- Calibrate servo in code if needed

### Code won't upload
- Install all required libraries
- Select correct board and port
- Check USB cable connection

## Future Enhancements 🚀

- [ ] Add LED indicators
- [ ] Add buzzer for alerts
- [ ] Bluetooth remote control
- [ ] Speed adjustment
- [ ] Line following capability
- [ ] Object size detection

## Author 👨‍💻
**logyaser-max**

## License 📄
This project is open source and free to use for educational purposes.

---

**Enjoy building and customizing your obstacle avoiding car! 🎉**

For questions or improvements, feel free to open an issue or submit a pull request!
