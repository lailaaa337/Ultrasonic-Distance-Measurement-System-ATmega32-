# Distance Measurement System using ATmega32 & Ultrasonic Sensor

## Overview

This project implements a distance measurement system using an ATmega32 microcontroller and an HC-SR04 ultrasonic sensor, with real-time output displayed on an LCD screen.

The system responds dynamically to distance changes by displaying the measured distance and controlling LEDs based on different distance thresholds. It combines embedded programming, hardware interfacing, and real-time signal processing.

---

## Features

* Real-time distance measurement
* LCD display output (distance in cm)
* LED indicators based on distance levels
* Timer-based signal measurement (Input Capture Unit)
* Continuous real-time updates
* Full hardware implementation

---

## Project Demo

<p align="center">
  <img src="demo.gif" alt="Distance Measurement Demo" width="400"/>
</p>
<p align="center"><em>Real-time distance measurement displayed on LCD with LED indicators</em></p>

---

## System Design

### Main Components

* ATmega32 Microcontroller
* HC-SR04 Ultrasonic Sensor
* 16x2 LCD Display
* LED Indicators (4 LEDs)
* Potentiometer (for LCD contrast)

---

### Sensor Working Principle

* The ultrasonic sensor sends a trigger pulse
* The echo signal returns after hitting an object
* The time difference is measured
* Distance is calculated using:

Distance = (Time × Speed of Sound) / 2

---

### Microcontroller Logic

* Uses Timer1 with Input Capture Unit (ICP1)
* Measures duration of echo signal
* Converts time into distance

---

### LED Control Logic

LEDs indicate distance levels:

* Less than 5 cm → 4 LEDs
* Less than 10 cm → 3 LEDs
* Less than 15 cm → 2 LEDs
* Less than 20 cm → 1 LED

---

### LCD Interface

* Data pins connected to Port C
* Control pins connected to Port D
* Displays the calculated distance

---

## How It Works

1. A trigger pulse is sent to the ultrasonic sensor
2. The echo signal is received
3. Timer measures the signal duration
4. Distance is calculated
5. LCD displays the result
6. LEDs update based on distance

---

## Technologies Used

* Embedded C (AVR)
* ATmega32 Microcontroller
* Proteus (simulation)
* Hardware (Breadboard implementation)

---

## Project Structure

project/
│── compOrgProject.pdf
│── demo.gif
│── README.md

---

## Project Documentation

Full report available here:
compOrgProject.pdf

---

## What I Learned

* Interfacing sensors with microcontrollers
* Using timers and interrupts (ICU)
* LCD communication
* Embedded C programming
* Real-time system design
* Debugging hardware circuits

---

## Limitations

* Limited measurement range
* No filtering for noisy signals
* Basic user interface

---

## Future Improvements

* Add buzzer for alerts
* Improve accuracy using filtering
* Add wireless monitoring (IoT)
* Display graphs of distance changes
* Use more advanced sensors

---

## Author

Laila Tarek
Miran Samer
Lojaine Mohamed
Hana Mabrouk
