Overview

The Weather Monitoring System with GSM Alert is a real-time embedded system developed using the ARM7 LPC2129 microcontroller. The project continuously monitors environmental temperature, displays real-time temperature and clock information on a 16×2 LCD, and automatically sends SMS alerts through a GSM module whenever the temperature crosses predefined safety limits.
The system integrates multiple embedded peripherals, including an RTC module, SPI-based ADC, GSM module, LCD, buzzer, and cooling motor, using I2C, SPI, UART, and GPIO interfaces.

Problem Statement

Environmental temperature variations can negatively impact industrial equipment, agricultural systems, and electronic devices. Manual monitoring is inefficient and may delay corrective action during abnormal conditions.
An automated embedded monitoring system is required to continuously measure temperature and generate immediate alerts whenever unsafe conditions are detected.

Solution

The system continuously measures ambient temperature using a temperature sensor connected through an SPI ADC. The LPC2129 processes the sensor data, displays the current temperature and time on the LCD, and automatically performs the following actions based on predefined thresholds:
Sends SMS alerts using the GSM module.
Activates a cooling motor/fan when the temperature exceeds the upper limit.
Activates a buzzer when the temperature falls below the lower limit.
This enables real-time environmental monitoring with minimal human intervention.

Features

Real-time temperature monitoring
Real-time clock display using DS1307 RTC
GSM-based SMS alert system
16×2 LCD display
Automatic cooling motor/fan control
Low-temperature buzzer alert
Continuous environmental monitoring
I2C, SPI, UART, and GPIO peripheral interfacing

Hardware Components

ARM7 LPC2129 Microcontroller
DS1307 RTC Module
LM35 Temperature Sensor
MCP3208 SPI ADC
SIM900 GSM Module
16×2 LCD Display
DC Motor/Fan
Buzzer
Power Supply
Software Tools
Embedded C
Keil µVision IDE
Flash Magic

System Implementation

The LM35 temperature sensor measures the ambient temperature.
The MCP3208 ADC converts the analog sensor signal into digital data.
The LPC2129 reads the ADC data using SPI communication.
The DS1307 RTC provides real-time date and time using the I2C protocol.
The LCD continuously displays the current temperature and time.
If the temperature exceeds the upper threshold, the system:
Sends an SMS alert using the GSM module.
Activates the cooling motor/fan.
If the temperature falls below the lower threshold, the system:
Activates the buzzer.
The monitoring process repeats continuously to provide real-time updates.
Technologies and Concepts Used
Embedded C Programming
ARM7 LPC2129 Microcontroller
GPIO Programming
I2C Communication (RTC Interface)
SPI Communication (ADC Interface)
UART Communication (GSM Interface)
LCD Interfacing
Sensor Data Acquisition
Real-Time Embedded Systems
Embedded Automation

Applications

Weather Monitoring Stations
Smart Agriculture
Greenhouse Monitoring
Industrial Temperature Monitoring
Cold Storage Monitoring
Server Room Temperature Monitoring
Environmental Monitoring Systems
Remote Alert Systems
Future Enhancements
Add humidity sensing using DHT11/DHT22.
Integrate cloud monitoring through Wi-Fi or IoT.
Develop a mobile application for remote monitoring.
Store historical sensor data on an SD card.
Support multiple environmental sensors.

Author

Harshavarthani M

Electronics and Communication Engineering
