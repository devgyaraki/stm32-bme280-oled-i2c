# STM32 BME280 & OLED I2C Weather Station

This project is a demonstration of embedded firmware development using the STM32F446RE (Nucleo-64) platform. The system interface reads environmental data (temperature, humidity, pressure) from a BME280 sensor via I2C and displays the results on an SSD1306 OLED screen. Additionally, the system provides real-time telemetry via UART to a PC for debugging and monitoring.

-------------------------------------------------------------------------------------------------------------------

## Project Objectives
- System Integration: Implementing reliable communication between the STM32, BME280 sensor, and SSD1306 OLED display using I2C protocols.

- Firmware Development: Managing data acquisition, processing, and real-time visualization.

- Telemetry & Monitoring: Streaming sensor data via UART for PC-side monitoring and verifying communication integrity using PuTTY.

- Debugging & Verification: Using a Logic Analyzer (Kingst LA1010) to monitor and verify bus communication and data timing.

-------------------------------------------------------------------------------------------------------------------

## Features
- Real-time environmental data acquisition.

- OLED display visualization for local status monitoring.

- UART serial telemetry for remote data logging and debugging.

- Bare-metal/HAL environment setup with efficient modular code structure.

-------------------------------------------------------------------------------------------------------------------

##Technical Implementation
- IDE: STM32CubeIDE

- Hardware: STM32 Nucleo-F446RE, BME280 Sensor, SSD1306 OLED Display.

- Drivers: Integrated established open-source drivers for BME280 and SSD1306, focusing on system-level integration and custom data processing.

- Verification: Serial console data verification via PuTTY and protocol analysis via Kingst LA1010.

-------------------------------------------------------------------------------------------------------------------

## Documentation
The `Dokumentation/` directory contains detailed technical resources:
* **Hardware Design:** [Schematic_V1.0.pdf](Dokumentation/Schematic_V1.0.pdf)
* **Prototype:** [Prototype_Photo.jpg](Dokumentation/Figure_01_Prototype_Photo.jpg)
* **Communication Analysis:** 
    * [I2C Cycle Analysis](Dokumentation/Figure_02_I2C_Cycle_Analysis.png)
    * [BME280 Protocol Details](Dokumentation/Figure_03_BME280_Protocol_Details.png)
    * [SSD1306 Protocol Details](Dokumentation/Figure_04_SSD1306_Protocol_Details.png)

-------------------------------------------------------------------------------------------------------------------

## Project Structure
```text
/Core           - Main application source and header files
/Drivers        - CMSIS and HAL library files
/Dokumentation  - Schematics, technical logs, and component specifications
/Debug          - Compilation and binary output files

-------------------------------------------------------------------------------------------------------------------

## Credits & References
- BME280 Driver: [Bosch BME280 Sensor API](https://github.com/BoschSensortec/BME280_driver) - Official Bosch Sensortec implementation for sensor data acquisition.

- SSD1306 Driver: [afiskon/stm32-ssd1306](https://github.com/afiskon/stm32-ssd1306) - A widely used, lightweight library for SSD1306 OLED displays on STM32 platforms.
