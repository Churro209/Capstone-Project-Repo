# Lab Entry – 2026-01-09

## Metadata
- Date: 2026-01-09
- Project:Off Grid Solar Battery Charger
- Board / Rev:
- Scope: 

## Objective
Solder INA219 break out PCB and run continuity test.
## Setup
Use soldering iron and Klein digital multimeter. Use flux to help solder flow and prevent over heating. Use isopropyl alcohol to clean up left over flux. 
## Measurements
Use the continuity function to test solder points to verify 
a solid connection and check for shorts. 
## Scope Captures
N/A
## Observations
![INA219 breakout PCB after clean up and continuity test](../1-09-2026-Solder-INA219-Breakout-PCB/photos/INA219_Breakout.png)

Each input passed continuity test. 
##  Next Steps
Verify that the PCB function by running a quick test with a microcontroller to see if we can communicate with the INA219 chip using I2C. If Chip ACKS our request, 
calibrate and test the functionality using a 9V battery and and 100 ohm resistor. 

