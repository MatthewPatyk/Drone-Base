# Drone Base Firmware

**IMPORTANT:**

- This is still work in progress.
- Some libraries are released under `MIT license`, some have `Copyright © 2018 Mateusz Patyk`, I am working on it to write documentation for most libraries, and release them under MIT or LGPL license.

## Features
- original flight controller core
- Android app via Bluetooth for on-field parameters changing, eg. PID tuning, made with Qt framework
- Windows app via Serial interface for in-door testing, made with Qt framework
- sensors fusion made with Madgwick's or Mahony's filters,
- magnetometer calibration for soft and hard iron compensation parameters, made with MATLAB,
- original protocol based on Modbus-like protocol for long and short range communication via RF and BT - prevention of data corruption,
- 200 Hz loop control (due to maximum magnetometer data rate) can be higher,

## Hardware major components:
- Arduino Due is the heart of drone,
- GY-80 IMU board:
  - ADXL345 accelerometer,
   - L3G4200D gyroscope,
   - HMC5883L magnetometr,
   - BMP085 barometer,
- any ATmega 328P board (Uno and Pro Mini in my setup) on remote,
- nRF24L01 2.4GHz RF transceivers.

## Frame, motors, ESC and power supply:
- Tarot 650mm quadcopter frame TL65B01,
- Tarot low KV, 6S motors TL68P07,
- FVT LittleBee 30A ESC,
- 13" and 15" proppelers,
- 3S 5000mAh or 6S 5000mAh (I'm using 2x3S in series) for 13" and 15" propellers.

## What affecting flying performance? I guess:
- low IMU quality? - there ale a lot of better IMUs e.g. MPU9250
- sensors weak calibration?,
- PID module?
- ?

## TODO
- **improve flying performance...**
- connect pitch, roll, yaw sticks to remote and calibrate them,
- add pitch, roll control feature (after connecting sticks to remote),
- add yaw control feature (use heading from IMU filters),
 

## Author 
* 2018, **Mateusz Patyk**, <matpatyk@gmail.com> 
 
## License 
- MIT License, unless it states otherwise. **Check files notes.**
