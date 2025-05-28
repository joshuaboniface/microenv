# MicroEnv v1.x

MicroEnv is a compact and simplistic environmental monitoring sensor,
based on the ESP32-C3 and the Sensirion SGP30 and SHT45 sensors, using
ESPHome for integration with HomeAssistant

Use a MicroEnv near a source of emissions to monitor air quality, or as
a general room environmental tracking sensor.

Power is provided by USB-C, though a very slim cable is required when
using SMD soldering without a buffer.

The Sensirion sensors are elevated with through-hole pins, to ensure
optimal distance between the (warm) board and the sensors themselves.

For more details, please [see my blog post on the MicroEnv project](https://www.boniface.me/the-microenv/).

## Parts List

| Qty   | Component          | Cost (2025/05 CAD, ex. shipping) | Links |
|-------|--------------------|----------------------------------|-------|
| 1     | GY-SGP30           | $5.73                            | [AliExpress](https://www.aliexpress.com/item/1005008473372972.html)  |
| 1     | GY-SHT45           | $5.67                            | [AliExpress](https://www.aliexpress.com/item/1005008175340220.html)* |
| 1     | ESP32-C3           | $3.12                            | [AliExpress](https://www.aliexpress.com/item/1005007205044247.html)  |
| 1     | Custom PCB (JLC)   | $0.50 ($5.00/10)                 | [GitHub](https://github.com/joshuaboniface/microenv) |
| **TOTAL** |                    | **$15.02**                           |       |

`*` Ensure you select the correct device on the page as it shows multiple options.

## Configurable Options

There are several UI-configurable options with the MicroEnv to help you get
the most out of the sensor for your particular use-case.

### Temperature Offset (selector, -30 to +10 @ 0.1, -5 default)

Allows calibration of the SHT45 temperature sensor with an offset from -30 to +10
degrees C. Useful if the sensor is misreporting actual ambient tempreatures. Due
to internal heating of the SHT45 by the ESP32, this defaults to -5; further
calibration may be needed for your sensors and environment.

### Humidity Offset (selector, -20 to +20 @ 0.1)

Allows calibration of the SHT45 humidity sensor with an offset from -20 to +20
percent relative humidity. Useful if the sensor is misreporting actual humidity.

