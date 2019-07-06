# Plantower PMS5003 Dust Sensor ESP-IDF Component

## Brief Overview

This is an esp-idf module for using the plantower pms5003 dust sensor. This collects dust concentration in terms of PM1.0, PM2.5 and PM10 concentrations in standard and atmospheric conditions.

## Wiring

The PMS5003 module connects to ESP32 via serial 9600 baud, 8N1. You can use any serial port of the ESP32, only the TX pin of the PMS5003 is needed, the RX pin is left unconnected.

In the examplem, I connected the tx pin of the sensor to GPIO 2 (or to any input pin of the ESP32), note the default assignments for the rx pin.

	PMS5003 TX <--> ESP32 Pin GPIO2


## Configuration and Build

Clone this repository on your esp-idf projects components subdirectory. 
		
		>cd project
		>mkdir components
		>cd compnents
		>git clone https://github.com/vpcola/plantower5003

Optionally look in the examples folder for referrence on how to use this component. With the example project, you can then issue:

		make menuconfig

You can fine tune the parameters for the PMS5003 dust sensor parser task by selecting "Component config -> Dustsensor Parser". 

Set the GPIO for the RX pin and the UART port to use. After that, build the project with:

		make flash monitor

To flash and start monitoring the dust sensor data.
