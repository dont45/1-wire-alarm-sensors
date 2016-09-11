# 1-wire-alarm-seniors
Collection of 1-wire sensor devices

A switch 'closure' sensor such as a typical magnetic reed switch is connected to the photonAlarm 
by use of a 1-wire device such as a ds2406 or ds2413.  These devices provide two gpio 'pins' controlled
by 1-wire commands from the photonAlarm.  The gpio pins are generally labled PIO pins, PIO-A and PIO-B
for the two devices mentioned.  These are bi-directional open drain pins which can serve to detect a 
switch closure or drive a device for output.  The advantage of this design is that a single wire (and a ground)
connects all the alarm sensors, with the 1-wire devices being connected in a varity of topologies, i.e. star,
multi-drop, or straight line.

Since in the simplest configuration there is no voltage supplied to the sensor, just the 1-wire data line,
there is no voltage to detect by the sensor switch closing.  In order to keep the sensor network in the
spirit of 1-wire, a method, called parasitic power, can be used to power the detection circuit of the
reed switch.  This method is implemented by a parasitic charge circuit which taps the 1-wire data line
to keep a capacitor charged.  The charge on this capacitor is used to drive the voltage detection at the
device's PIO port.  This design is attached as sensor-2406p+.  Included are Eagle files as well as the .pdf's.
