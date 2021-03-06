Data exchange over a serial line 
================================

This folder contains the source files for the demonstration project on data
exchange over a serial line between two devices.

Both the sender and receiver stations are implemented in the REX Control System
but any of them can be replaced by arbitrary device supporting serial 
communication. 

The Sender station transmits 4 signals of various types to the Receiver station. 
See the source **.c* files to understand how the data is processed and 
transmitted.

The received data is recorded in the TRND block which allows displaying of the 
trends (graphs) in the Watch mode of *RexDraw* or in the *RexView* diagnostic tool. 

## Timing of the project ##

The algorithm runs each 500 milliseconds (0.5 s). See the EXEC function block,  
tick x ntick0 = 0.05 x 10 = 0.5 

## Prerequisities ##
- RexCore must be installed and running on the target devices.
- The serial line must be available.

## Running the examples ##
- The **exec.mdl* file is the project main file.
- Open it with *RexDraw*.
- Edit the p0 parameter of the REXLANG function block to specify the serial 
communication device to use (e.g. */dev/ttyS0* in Linux or *COM1* in Windows).
- Compile and download each project to the corresponding target device.
- Switch to Watch mode and observe the algorithm in real time.
- Enable monitoring of the REXLANG block (right-click it and select 
Monitor selection from the context menu).
- Change the constants in the Sender station on-the-fly and check if it reaches 
the Receiver station.

## Documentation ##

- **Press F1 for help** on the selected function block in the *RexDraw* program.
- [REXLANG function block documentation](http://www.rexcontrols.com/media/HTML/DOC/ENGLISH/REXLANG.html)
- [Function blocks of the REX Control System](http://www.rexcontrols.com/media/HTML/DOC/ENGLISH/index.html)
- [Complete documentation of the REX Control System](http://www.rexcontrols.com/documentation-and-support)

## Additional information ##

- Visit the [REX Controls company webpage](http://www.rexcontrols.com) 
for more information about the example projects and developing advanced 
automation and control solutions using the REX Control System.