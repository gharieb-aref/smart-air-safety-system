# Smart Air Safety System

A smart Arduino-based safety and environmental monitoring system designed to detect hazardous gases, smoke, fire, and high temperature conditions while automatically ventilating the area and alerting users using alarms and LCD notifications.

---

## Features

- Real-time temperature monitoring using DHT11
- Gas leakage detection
- Flame/fire detection
- Automatic smoke and gas ventilation
- LCD status display
- Automatic buzzer alarm system
- Safe/Danger condition monitoring
- Smart environmental safety control

---

## Components Used

| Component | Quantity |
|---|---|
| Arduino UNO | 1 |
| DHT11 Temperature Sensor | 1 |
| MQ Gas Sensor | 2 |
| Flame Sensor | 2 |
| 16x2 LCD I2C Display | 1 |
| Buzzer | 1 |
| Ventilation Fan | 1 |
| Jumper Wires | Multiple |
| Breadboard | 1 |

---

## Pin Configuration

| Component | Arduino Pin |
|---|---|
| Ventilation Fan | D2 |
| DHT11 Sensor | D3 |
| Flame Sensor 1 | D5 |
| Flame Sensor 2 | D6 |
| Buzzer | D7 |
| Gas Sensor 1 | D9 |
| Gas Sensor 2 | D10 |

---

## System Operation

### Temperature Monitoring
The system continuously reads temperature values using the DHT11 sensor.

- If temperature exceeds the safe threshold:
  - Ventilation fan turns ON
  - LCD displays warning message

---

### Gas Leakage Detection
The MQ gas sensors monitor air quality and gas concentration.

- If gas leakage is detected:
  - Alarm buzzer activates
  - Ventilation fan starts automatically
  - LCD displays GAS ALARM warning

---

### Fire Detection
Flame sensors continuously monitor for fire presence.

- If fire is detected:
  - Buzzer alarm activates
  - LCD displays FIRE ALARM
  - System remains in alert state until fire disappears

---

## LCD Display Messages

| Status | LCD Message |
|---|---|
| Normal Condition | SAFE |
| High Temperature | HIGH TEMP |
| Fire Detected | FIRE ALARM |
| Gas Leakage | GAS ALARM |

---

## Libraries Used

```cpp
#include <Wire.h>
#include <LiquidCrystal_I2C.h>
#include <DHT.h>
```

---

## Arduino Code File

```text
air_quality_monitor.ino
```

---

## Project Structure

```text
smart-air-safety-system/
│
├── air_quality_monitor.ino
├── README.md
├── LICENSE
└── images/
    ├── circuit.jpg
    └── project.jpg
```

---

## Installation

1. Install Arduino IDE
2. Install required libraries:
   - DHT Sensor Library
   - LiquidCrystal_I2C
3. Connect all components
4. Upload the code to Arduino UNO
5. Power the system

---

## Future Improvements

- ESP32 IoT integration
- Mobile app notifications
- WiFi monitoring dashboard
- GSM alert system
- Air quality percentage display
- Battery backup system

---

## Applications

- Smart homes
- Laboratories
- Factories
- Server rooms
- Kitchens
- Industrial safety systems

---

## Project Preview

Add your project images inside the `images` folder.

```md
![Project Image](images/project.jpg)
```

---

## License

This project is licensed under the MIT License.

---

## Author

Developed by Genius Coder Academy

GitHub:
https://github.com/

---

## Keywords

Arduino, IoT, Embedded Systems, Gas Detection, Fire Alarm, Safety System, Smart Home, Air Monitoring, Ventilation System, DHT11, LCD I2C
