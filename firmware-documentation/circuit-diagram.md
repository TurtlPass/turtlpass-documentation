# 🏗️ Circuit Diagram

```
  RP2040-Zero               Touch Sensor
 +-----------+              +----------+
 |           | GND -------- | GND      |
 |  RGB-LED  |              |          |
 | (GPIO 16) | GPIO 2 ----- | I/O      |
 |           |              |          |
 |           | 3.3V ------- | VCC      |
 +-----------+              +----------+
```

**Connect the Touch Sensor (TTP-223) to RP2040-Zero:**

1. Connect the GND pin of the touch sensor to a ground (GND) pin on the RP2040-Zero board.
2. Connect the I/O pin of the touch sensor to GPIO 2 on the RP2040-Zero board.
3. Connect the VCC pin of the touch sensor to a 3.3V power source on the RP2040-Zero board.
