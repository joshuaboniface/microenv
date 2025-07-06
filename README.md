# MicroEnv v1.x

The MicroEnv is a compact and simplistic environmental monitoring sensor,
based on the ESP32-C3 and the Sensirion SGP41 and SHT45 sensors, using
ESPHome for integration with HomeAssistant

Use a MicroEnv near a source of emissions to monitor air quality, or as
a general room environmental tracking sensor. It is, in effect, a cut
down version of the environmental sensor package of my [Supersensor 2.x](https://github.com/joshuaboniface/supersensor2)
project in a much smaller footprint.

Power is provided by USB-C, though a very slim connector is required when
using SMD soldering without a buffer.

The Sensirion sensors are elevated with through-hole pins, to ensure
optimal distance between the (warm) board and the sensors themselves.
You can either directly solder the sensors to the board or, as I do,
use 4-pin female sockets for easy changing should it be necessary.

![MicroEnv Board Design](/board/pcb.svg)

## Parts List

| Qty   | Component           | Cost (mid-2025 CAD, ex. shipping) | Links |
|-------|---------------------|-----------------------------------|-------|
| 1     | GY-SGP41            | $9.58                             | [AliExpress](https://www.aliexpress.com/item/1005007958589642.html)  |
| 1     | GY-SHT45            | $5.67                             | [AliExpress](https://www.aliexpress.com/item/1005008175340220.html)* |
| 1     | ESP32-C3            | $3.12                             | [AliExpress](https://www.aliexpress.com/item/1005007205044247.html)  |
| 2     | Female 4-pin header | $0.37 ($14.99/40)                 | [Amazon](https://www.amazon.ca/dp/B08LF3S5S8) |
| 1     | Custom PCB (JLC)    | $0.50 ($5.00/10)                  | [GitHub](https://github.com/joshuaboniface/microenv/tree/master/board) |
| **TOTAL** |                    | **$19.24**                           |       |

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

## Home Assistant View

This image shows the various available sensors in Home Assistant.

![MicroEnv Home Assistant](/microenv-homeassistant.png)
