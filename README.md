# Advanced Student Safety Car System with a Windshield Wiper Subsystem
### by Alexander Ramos-Rodriguez & Tzimpilis Konstatinos
The system is divided into two parts: the engine ignition subsystem and the wiper subsystem.
## Engine Ignition Subsystem Behavior
For the engine ignition sequence, both the passenger and the driver must be seated and have their seat belts fastened before starting the engine. In our system, the driver and passenger sitting down are represented by continuously pressing two buttons (one for the driver’s seat and one for the passenger’s seat), while fastening their seat belts is represented by turning on two switches (one for the driver's seat belt and one for the passenger’s seat belt). These four actions must be completed before the engine ignition button can be pressed.

Once the sequence is completed, a green LED turns on, allowing the driver to press the engine ignition button, which then starts the engine (indicated by a blue LED turning on). If the sequence is not completed, the green LED will not turn on. If the engine ignition button is pressed without completing the sequence, an alarm will go off, signaling that the sequence must be completed.

## Ignition Subsystem
| Behavior  | Test Result | Comment |
| ------------- | ------------- |--------------|
| When driver seats a welcome message appears | PASS | 100% Sucess at the message showing in the terminal|
| Ignition Enabled LED (green LED) (Required both seat buttons pressed and both seatbelt switches in ON position)  | PASS  | 100% success for LED lighting when both buttons and switches are HIGH and for when at least one is LOW |
| Engine Started LED (blue LED)  | PASS  | 100% sucess when starting the engine  | PASS  | 100% success in keeping engine ON regardless of any button presses or senor inputs other than the ignition button |
| Engine OFF once ignition button pressed while engine running | PASS  | 100% success in shutting OFF ignition with a second button press. Is not affected by seated or seat belt button states. |
| Engine Stays ON even if anyone steps off the car| PASS | 100% Sucess at keeping the engine light ON after a succesful ignition|

## Wiper Subsystem Behavior

For the wipers subsystem, the wipers can only be used when the engine is successfully started. There are four different speed settings:

1. OFF – The wipers do not move at all when the potentiometer reading is below 0.3.
2. SLOW – The wipers move consistently at a slow speed (30 RPM) when the potentiometer reading is below 0.6.
3. HIGH – The wipers move consistently at a fast speed (40 RPM) when the potentiometer reading is below 0.9.
4. INT – The wipers complete one full wipe and then pause before the next cycle. This mode is activated when the potentiometer reading is above 0.9.

INT mode also has three different delay options determined by the reading of a second potentiometer.
1. SHORT mode – 3-second delay (activated when the potentiometer reading is below 0.33).
2. MEDIUM mode – 6-second delay (activated when the potentiometer reading is below 0.66).
3. LONG mode – 8-second delay (activated when the potentiometer reading is above 0.66).

Lastly, our system includes a display that shows the current wiper mode (HIGH, SLOW, INT, or OFF). When in INT mode, the display also indicates the current delay setting (LONG, MEDIUM, or SHORT). The display turns on only when the engine is running and turns off when the engine is off.

## Ignition Subsystem
| Behavior  | Test Result | Comment |
| ------------- | ------------- |--------------|
| Wipers returns to 0 degrees when in OFF mode from any mode and does nothing when already in OFF mode| PASS | 100% success  |
| Wipers move at 30 RPM in SLOW and 40 RPM in HIGH mode in a oscillating pattern | PASS  | 100% success  |
| Wipers move at 30 RPM in INT mode and has a the appropiated selected delay time (SHORT, MEDIUM, LONG) | PASS  | 100% sucess |
| Wipers only run when the Ignition and stop  | PASS  | 100% success |
| Display showcases the selected mode when the ignition is ON and in INT mode it also showcases the selected delay| PASS  | 100% success |





