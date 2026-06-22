# Wiring Connections Guide 🔌

## Main Circuit Diagram
![Circuit Diagram](circuit/circuit_diagram.jpg)

---

## Ultrasonic Sensor Connections (HC-SR04)

| Sensor Pin | Arduino Pin |
|-----------|------------|
| TRIG | A0 |
| ECHO | A1 |
| VCC | 5V |
| GND | GND |

---

## Servo Motor Connections

| Servo Pin | Arduino Pin |
|-----------|------------|
| Signal (Yellow) | Pin 10 |
| VCC (Red) | 5V |
| GND (Brown) | GND |

---

## Motor Driver Shield (L298N)

### Motor Connections:
- **Motor 1 (Front Left)** → OUT1, OUT2
- **Motor 2 (Front Right)** → OUT3, OUT4
- **Motor 3 (Rear Left)** → OUT1, OUT2 (Channel B)
- **Motor 4 (Rear Right)** → OUT3, OUT4 (Channel B)

### Power:
- GND → Arduino GND
- +12V → External Power Supply

---

## Battery Connections

- **Positive (+)** → Motor Driver Shield Power Input
- **Negative (-)** → Motor Driver Shield GND & Arduino GND

**Recommended: 9V or 12V Battery**

---

## Connection Summary Table

| Component | Description | Pin |
|-----------|------------|-----|
| **Arduino Uno** | Main board | - |
| **Ultrasonic Sensor** | Obstacle detection | A0, A1 |
| **Servo Motor** | Sensor rotation | Pin 10 |
| **Motor Driver** | Motor control | - |
| **DC Motors (4x)** | Movement | - |
| **Battery** | Power supply | 9V-12V |

---

## Checklist ✅

- [ ] Ultrasonic Sensor connected to A0 and A1
- [ ] Servo Motor connected to Pin 10
- [ ] All motors connected to Motor Driver
- [ ] Battery properly connected
- [ ] All connections secure before power on

---

## Common Mistakes to Avoid ⚠️

- ❌ Reverse polarity on battery
- ❌ Loose connections
- ❌ Short circuits
- ❌ Wrong pin connections

**Follow the diagram carefully! 🎯**
