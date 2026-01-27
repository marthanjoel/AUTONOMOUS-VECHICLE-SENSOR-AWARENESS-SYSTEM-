Autonomous Vehicle Sensor Fusion Platform 



Project Overview
This project is an educational sensor fusion platform for autonomous vehicle concepts. It combines multiple sensors to monitor the environment, prioritizes alerts, and provides visual feedback to the driver using an RGB LED.

The system demonstrates real-time environmental awareness, sensor prioritization, and adjustable settings using a rotary encoder for brightness and system control.

Components Used (Real Project)
Component	Purpose
IR Obstacle Sensor	Detects objects in front of the vehicle
Optical Break Beam Sensor	Detects beam interruptions (like a virtual tripwire)
Flame Sensor	Detects fire or high-temperature hazards
Rotary Encoder	Adjusts RGB LED brightness and toggles system ON/OFF
Push Button (Encoder Switch)	Toggles system ON/OFF
RGB LED (Common Cathode)	Visual feedback for sensor status
Arduino UNO	Microcontroller for processing sensor data
Wires / Breadboard	Connections for hardware
System Behavior
Condition	LED Output	Description
System OFF	All LEDs OFF	No monitoring
System ON (idle)	Green	System powered ON, environment clear
IR Obstacle detected	Red	Warning: obstacle detected
Optical beam blocked	Blue	Warning: path blocked
Flame detected	White	High-priority alert
All sensors clear	Green	Safe environment

Rotary encoder:

Clockwise → increases LED brightness

Counterclockwise → decreases LED brightness

Press → toggles system ON/OFF

Priority logic: Flame > IR > Optical > All Clear

Wiring / Connections
IR Sensor

VCC → 5V

GND → GND

OUT → D2

Optical Sensor

VCC → 5V

GND → GND

OUT → D3

Flame Sensor

VCC → 5V

GND → GND

OUT → D7

Rotary Encoder

CLK → D4

DT → D5

Switch → D6

RGB LED (Common Cathode)

Cathode → GND

Red → D9 (220Ω)

Green → D10 (220Ω)

Blue → D11 (220Ω)

How It Works
Power ON/OFF: Press the rotary encoder button to turn the system ON. Press again to turn it OFF.





Sensor Monitoring:
IR sensor detects obstacles → Red LED
Optical sensor detects blocked beam → Blue LED
Flame sensor detects fire → White LED (highest priority)
All Clear: If no sensors are triggered → Green LED lights
Brightness Adjustment: Rotate the rotary encoder to change RGB LED brightness.
Serial Monitor: Prints sensor status and LED brightness in real-time.






Features
Real-time sensor fusion logic
Priority-based alerts (Flame > IR > Optical)
Adjustable LED brightness using rotary encoder
Push-button toggle for system power
Visual feedback with RGB LED
Easy to replicate with off-the-shelf sensors




Future Improvements
Add buzzer alarm for high-priority alerts (fire)
Add LCD display for sensor readings
Add startup LED animation for better system feedback
Integrate with actual vehicle prototype for real testing





Notes
Flame sensor always takes highest priority
Ir and optical sensors act as secondary alerts
Rotary encoder provides both system control and brightness adjustment
Green LED shows either system ON or all clear depending on sensor readings
