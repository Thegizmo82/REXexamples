﻿Integration of Siemens LOGO! in REX
======================================================

This folder contains the source files for the demonstration project on data
exchange between Siemens LOGO! 0BA8 and the REX control algorithm.

There is a project for LOGO! which must run in the device. See the *logo_integration.lsc* project. The 
LOGO! acts as a server.

There is also a project for REX, which illustrates the access
to Inputs (I, AI), Outputs (Q) and Variable Memory Table (V) from the control 
algorithm. REX acts as a client and connects to the LOGO! base module via Ethernet.

The pulses on input I6 of the LOGO! device are counted. When 10 is reached, the 
counter is reset to 0 and the relays Q1 to Q3 are triggered for a specified 
period. The duration of the pulses can be altered from the REX control algorithm.
While the Q1 and Q2 relays are activated by the algorithm in the LOGO! itself, 
the Q3 relay is activated from the REX control algorithm.

The Q4 relay is activated according to an external analog signal, which is 
generated by the REX control algorithm (sine wave).

Analog inputs of the LOGO! are read and stored in the TRND block in the REX 
control algorithm, which provides a time-plot of the measured data in real-time.

Moreover, a connection watchdog is implemented to monitor the connection with 
REX.

## Prerequisities ##
- RexCore and S7Drv modules are installed on the target device
- The LOGO! device is in RUN mode (*logo_integration.lsc* attached)
- The IP address 192.168.1.111 is assumed in the LOGO! device. If the IP address 
differs, **remember to change it** in the configuration dialog of the IO driver file according to your
LOGO! base module. As was already mentioned, LOGO! acts as a server the clients 
connect to. 

## Running the example ##
- The **exec.mdl* file is the project main file
- Open it with RexDraw, compile and download it to the target device

## User interface (HMI) ##
The example is accompanied by a graphical user interface generated from RexHMI Designer.

## Documentation ##

- [S7Drv - S7 communication driver](https://www.rexcontrols.com/media/2.50.5/doc/ENGLISH/MANUALS/S7Drv/S7Drv_ENG.html)
- [Function blocks of REX](https://www.rexcontrols.com/media/2.50.5/doc/ENGLISH/MANUALS/BRef/BRef_ENG.html)
- [RexDraw User Guide](https://www.rexcontrols.com/media/2.50.5/doc/ENGLISH/MANUALS/RexDraw/RexDraw_ENG.html)
- [Complete documentation of REX](http://www.rexcontrols.com/documentation-and-support)

## Additional information ##

- Siemens and LOGO! are trademarks of [Siemens AG](http://www.siemens.com).
- The S7Drv driver of REX uses the [Snap7 communication suite](http://sourceforge.net/projects/snap7).
- Visit the [REX Controls company webpage](http://www.rexcontrols.com) 
for more information about the example projects and developing advanced 
automation and control solutions using REX.
