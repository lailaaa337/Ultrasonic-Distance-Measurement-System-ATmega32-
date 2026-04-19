

---

# Distance Measurement System using ATmega32 & Ultrasonic Sensor

##  Overview

This project implements a **distance measurement system** using an **ATmega32 microcontroller** and an **HC-SR04 ultrasonic sensor**, with real-time output displayed on an **LCD screen**.

The system dynamically responds to distance changes by:

* Displaying measured distance on LCD
* Controlling multiple LEDs based on distance thresholds

This project combines **embedded programming, hardware interfacing, and real-time signal processing**.

---

##  Features

*  Real-time distance measurement
*  LCD display output (distance in cm)
*  LED indicators based on distance levels
*  Timer-based signal measurement (Input Capture Unit)
*  Continuous real-time updates
*  Full hardware implementation

---

##  Project Demo

<p align="center">
  <img src="demo.gif" alt="Distance Measurement Demo" width="400"/>
</p>
<p align="center"><em>Real-time distance measurement displayed on LCD with LED indicators</em></p>

---

##  System Design

###  Main Components

* **ATmega32 Microcontroller**
* **HC-SR04 Ultrasonic Sensor**
* **16x2 LCD Display**
* **LED Indicators (4 LEDs)**
* **Potentiometer (for LCD contrast)**

---

###  Sensor Working Principle

* Ultrasonic sensor sends a pulse (Trigger)
* Echo signal returns after hitting object
* Time difference is measured
* Distance is calculated using:

```math
Distance = \frac{Time \times Speed\ of\ Sound}{2}
```

---

###  Microcontroller Logic

* Uses **Timer1 + Input Capture Unit (ICP1)**
* Measures duration of echo signal
* Converts time → distance

---

### LED Control Logic

LEDs indicate distance levels:

| Distance Range | LEDs ON |
| -------------- | ------- |
| < 5 cm         | 4 LEDs  |
| < 10 cm        | 3 LEDs  |
| < 15 cm        | 2 LEDs  |
| < 20 cm        | 1 LED   |

---

###  LCD Interface

* Data pins connected to **Port C**
* Control pins connected to **Port D**
* Displays formatted distance output

---

##  How It Works

1. Trigger pulse is sent to ultrasonic sensor
2. Echo signal is received
3. Timer measures signal duration
4. Distance is calculated
5. LCD displays distance
6. LEDs update based on thresholds

---

##  Technologies Used

* **Embedded C (AVR)**
* **ATmega32 Microcontroller**
* **Proteus (simulation)**
* **Hardware (Breadboard Implementation)**

---

##  Project Structure

```
project/
│── report.pdf
│── demo.gif
│── README.md
```

---

##  Project Documentation

Full report available here:
[View Report](compOrgProject.pdf)

---

##  What I Learned

* Interfacing sensors with microcontrollers
* Using timers and interrupts (ICU)
* LCD communication protocols
* Embedded C programming
* Real-time system design
* Debugging hardware circuits

---

##  Limitations

* Limited measurement range
* No filtering for noisy signals
* Basic UI

---

##  Future Improvements

* Add buzzer for alerts
* Improve accuracy using filtering
* Add wireless monitoring (IoT)
* Display graph of distance changes
* Use more advanced sensors

---

##  Team Members

* Laila Tarek
* Miran Samer
* Lojaine Mohamed
* Hana Mabrouk

---

