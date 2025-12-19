# Specifications

## v1

- USB HID scroll wheel
- BT HID scroll wheel
- Battery Charging with protections:
  - Overvoltage
  - Undervoltage
  - Overcurrent
  - Over temp
  - Reverse battery protection
- Motor

## Future

- FFB
- High resolution scrolling
- Set battery charge level limits
- Load sharing/Power path
- Coulomb counting

- LSE for STM32?

## RF

- Is this antenna suitable?
- Do we need two pi filters?
- Are the pi filter values a good start point?
- Do we need test points for calibration?

# Review Notes 2025/08/11

- ~~move the motor current sense from low side to the switched line~~
- ~~current sensor is 680uA - too high for long term storage (ok?)~~
  - Low power is not priority at the moment
- ~~why 27 ohm gate resistors? suggest 6V/600mA = 10ohm~~
  - Max gate driver current is 250mA
- add decouple to +2V5
- ~~lower the Hall effect sensor data series resistor, suggest 100ohm~~
  - Setting R46 to be DNP instead
- ~~USB diode protection U2 is connected wrong~~
- ~~recommend use TPS61041 rather than TPS61040 (250mA peak rather than 400mA peak - we don't need that much)~~
- ~~C18 is far too high ( I think 33pF ok )~~
  - Using 10pF as recommended by datasheet
