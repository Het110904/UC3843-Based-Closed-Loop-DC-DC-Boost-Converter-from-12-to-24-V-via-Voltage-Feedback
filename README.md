# Closed-Loop 12 V to 24 V Boost Converter using UC3843AN

## Overview
This project demonstrates the design and implementation of a closed-loop DC-DC boost converter using the UC3843AN PWM controller. The converter was built entirely on a breadboard using discrete components and is capable of stepping up a 12 V DC input to an adjustable regulated output. 

Unlike an open-loop converter, the output voltage is continuously monitored through a feedback network, allowing the controller to automatically adjust the PWM duty cycle and maintain the selected output voltage.

## Features
* Closed-loop voltage regulation
* Adjustable output using a potentiometer
* 12 V DC input
* Output voltage adjustable from 15.4 V to 28 V (no-load)
* Successfully regulated 24.0 V while powering a 24 V BLDC fan
* Demonstrated DC motor speed control by varying armature voltage
* Stable continuous operation for over 32 minutes

## Components Used
* **UC3843AN** PWM Controller
* **IRFZ44N** MOSFET
* **220 µH** Toroidal Inductor
* **1N5819** Schottky Diode
* **4700 µF / 50 V** Output Capacitor
* **100 nF** Ceramic Capacitor
* Feedback Resistor Network
* Potentiometer
* 12 V DC Power Adapter

## Testing Phase

### No-Load Test
The converter produced an adjustable output voltage between 15.4 V and 28.0 V with smooth regulation across the entire range.

### BLDC Fan Test
The converter successfully maintained 24.0 V while powering a 24 V BLDC cooling fan, confirming proper closed-loop voltage regulation under load.

### DC Motor Test
A permanent magnet DC motor was connected to demonstrate a practical application of the converter. By adjusting the output voltage with the potentiometer, the motor speed changed smoothly. This provided a practical demonstration of armature voltage control, a commonly used DC motor speed control technique.

### Continuous Operation
The converter was operated continuously for approximately 32 minutes. Throughout the test, the output voltage remained stable between 22.1 V and 22.3 V. Only the inductor became moderately warm, while the remaining components continued operating normally.

## Video Demonstration
*Note: This video demonstrates the DC Motor Test phase. **Please turn on your sound!** You can hear the motor's pitch and speed changing as the armature voltage is varied, while the multimeter displays the real-time voltage.*

https://github.com/user-attachments/assets/41e2a490-813e-499f-b78e-8405f5dae897

## UC3843AN Measurements
*Measured while regulating 24.0 V with the BLDC fan connected.*

| Pin | Function | Voltage |
| :--- | :--- | :--- |
| 1 | COMP | 5.78 V |
| 2 | VFB | 2.43 V |
| 3 | ISENSE | 0.28 V |
| 4 | RT/CT | 1.95 V |
| 6 | OUTPUT | 5.50 V |
| 7 | VCC | 11.17 V |
| 8 | VREF | 5.00 V |

## Key Learnings
Throughout this project, I gained practical experience with:
* PWM control using the UC3843AN
* Closed-loop voltage regulation
* Feedback compensation
* MOSFET switching
* Inductor-based energy transfer
* Hardware debugging and troubleshooting
* Thermal testing
* DC motor speed control through armature voltage variation

One of the most rewarding parts of this project was seeing a concept I had previously studied only in MATLAB/Simulink—DC motor speed control by varying armature voltage—working successfully in real hardware.

## Conclusion
This project successfully demonstrates the implementation of a closed-loop boost converter using the UC3843AN. The converter achieved stable voltage regulation, powered a 24 V BLDC fan, demonstrated variable-speed DC motor control, and operated reliably during extended testing. Beyond building a working converter, the project provided valuable hands-on experience in power electronics, closed-loop control, and practical hardware development.
