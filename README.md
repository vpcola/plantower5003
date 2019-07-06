# Plantower PMS5003 Dust Sensor ESP-IDF Component

## Brief Overview

This is an esp-idf module for using the plantower pms5003 dust sensor. This collects dust concentration in terms of PM1.0, PM2.5 and PM10 concentrations in standard and atmospheric conditions.

## Wiring

Connect the tx pin of the sensor to any input pin of the ESP32, note the default assignments for the rx pin.

## Configuration and Build

Clone this repository on your esp-idf projects components subdirectory. Optionally look in the examples folder for referrence on how to use this component. With the example project, you can then issue:

		make menuconfig

Set the GPIO for the RX pin and the UART port to use. After that, build the project with:

		make flash monitor

To flash and start monitoring the dust sensor data.
