# Hotel Automation Controller
- Problem

## Problem
A very prestigious chain of Hotels is facing a problem managing their electronic equipments.
Their equipments, like lights, ACs, etc are currently controlled manually, by the hotel staff, using
switches. They want to optimise the usage of Power and also ensure that there is no
inconvenience caused to the guests and staff.
So the Hotel Management has installed sensors, like Motion Sensors, etc at appropriate places
and have approached you to program a Controller which takes inputs from these sensors and
controls the various equipments.

The way the hotel equipments are organised and the requirements for the Controller is below:
- A Hotel can have multiple floors
- Each floor can have multiple main corridors and sub corridors
- Both main corridor and sub corridor have one light each
- Both main and sub corridor lights consume 5 units of power when ON
- Both main and sub corridor have independently controllable ACs
- Both main and sub corridor ACs consume 10 units of power when ON
- All the lights in all the main corridors need to be switched ON between 6PM to 6AM,
which is the Night time slot
- When a motion is detected in one of the sub corridors the corresponding lights need to
be switched ON between 6PM to 6AM (Night time slot)
- When there is no motion for more than a minute the sub corridor lights should be
switched OFF
- The total power consumption of all the ACs and lights combined should not exceed
(Number of Main corridors * 15) + (Number of sub corridors * 10) units of per floor. Sub
corridor AC could be switched OFF to ensure that the power consumption is not more
than the specified maximum value
- When the power consumption goes below the specified maximum value the ACs that
were switched OFF previously must be switched ON

- Motion in sub corridors is input to the controller. Controller need to keep track and optimise the
power consumption.
- Write a program that takes input values for Floors, Main corridors, Sub corridors and takes
different external inputs for motion in sub corridors and for each input prints out the state of all
the lights and ACs in the hotel. For simplicity, assume that the controller is operating at the night
time. Sample input and output below.

Initial input to the controller:
Number of floors: 2
Main corridors per floor: 1

Sub corridors per floor: 2


Subsequent Inputs from Sensors | Output from controller for corresponding sensor input
------------ | -------------
Default state (when the program is first run) | Floor 1 <br> Main corridor 1 <br> Light 1 : ON <br> AC : ON <br> Light 1 : OFF <br> Sub corridor 2 <br> Light 2 : OFF <br> Floor 2 <br> Main corridor 1 <br> Light 1 : ON <br> AC : ON <br> Sub corridor 1 <br> Light 1 : OFF <br> AC : ON <br> Sub corridor 2 <br> Light 2 : OFF <br> AC : ON
Movement in Floor 1, Sub corridor 2 | Floor 1 <br> Main corridor 1 <br> Light 1 : ON <br> AC : ON <br> Sub corridor 1 <br> Light 1 : OFF <br> AC : OFF <br> Sub corridor 2 <br> Light 2 : ON <br> AC : ON <br> Floor 2 <br> Main corridor 1 <br> Light 1 : ON <br> AC : ON <br> Sub corridor 1 <br> Light 1 : OFF  <br> AC : ON <br> Sub corridor 2 <br> Light 2 : OFF <br> AC : ON
No movement in Floor 1, Sub corridor 2 for a minute | Floor 1 <br> Main corridor 1 <br> Light 1 : ON <br> AC : ON <br> Sub corridor 1 <br> Light 1 : OFF <br> AC : ON <br> Sub corridor 2 <br> Light 2 : OFF <br> AC : ON <br> Floor 2 <br> Main corridor 1 <br> Light 1 : ON <br> AC : ON <br> Sub corridor 1 <br> Light 1 : OFF <br> AC : ON <br> Sub corridor 2 <br> Light 2 : OFF <br> AC : ON <br 
