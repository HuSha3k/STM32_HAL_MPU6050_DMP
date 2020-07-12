# STM32_HAL_MPU6050_DMP
Implemented MPU6050 DMP by STM32CubeMX HAL lib using **CPP** with the latest DMP Firmware Version 6.12. The code is modified from [**STM32_DMP_Driver**](https://github.com/fMeow/STM32_DMP_Driver/tree/I2Cdev) and arduino lib [**I2Cdevlib-MPU6050**](https://github.com/jrowberg/i2cdevlib).

# headers

`MPU6050_6Axis_MotionApps20.h` Based on an old InvenSense DMP driver with Detailed comments

`MPU6050_6Axis_MotionApps_V6_12.h` DMP Firmware Version 6.12 Latest as of today with many features and bug fixes:

- MPU6050 Registers have not changed just the DMP Image so that full backwards compatibility is present
- Run-time calibration routine is enabled which calibrates after no motion state is detected
- once no motion state is detected Calibration completes within 0.5 seconds

**Just include  either  of them**

# Example

**Connection:**

| stm32 | arduino |     pin      |
| :---: | :-----: | :----------: |
|  PB8  |   A5    |     SCL      |
|  PB9  |   A4    |     SDA      |
|  PB6  |    0    | TX（USB-RX） |
|  PB7  |    1    | RX（USB-TX） |

Code generated by CubeMX and  remains similar to arduino example `MPU6050_DMP6`
