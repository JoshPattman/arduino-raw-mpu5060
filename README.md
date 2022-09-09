# arduino-raw-mpu5060 - Simple sketch to send raw MPU6050 data over serial
## What this does
It will repeatedly send accelerometer and gyro data over a serial connection in the form `[<gyroX,<gyroY>,<gyroZ>,<accX>,<accY>,<accZ>]`. It has does no proscessing of the data other than converting the gyro data into `deg/s` and the acc data into `g`s. It does NOT ever use the onboard dmp of the mpu.
## Hardware
* MPU `VCC` and arduino `3.3v`
* MPU `GND` and arduino `Gnd`
* MPU `SDA` and arduino SDA pin (on nanos this is `A4`)
* MPU `SCL` and arduino SCL pin (on nanos this is `A5`)
## Why no complex features?
This is so that all the processing, filtering, and calibration can be done in you prefered language instead of on the arduino (I am personally not very good at making arduinos do what I want :))