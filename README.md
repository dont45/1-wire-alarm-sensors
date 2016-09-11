# 1-wire-alarm-seniors
Collection of 1-wire sensor devices

The typical 'closure' sensor such as a typical magnetic reed switch is connected to the photonAlarm 
by use of a 1-wire device such as a ds2406 or ds2413.  These devices provide two gpio 'pins' controlled
by 1-wire commands from the photonAlarm.  The gpio pins are generally labled PIO pins, PIO-A and PIO-B
for the two devices mentioned.  These are bi-directional open drain pins which can serve to detect a 
switch closure or drive a device for output.
