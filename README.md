# Hybrid Test Stand Instrumentation

Hybrid instrumentation is a part of the hybrid test stand support project. A LabJack U6 Data Acquisition unit (DAQ) collects the output voltage of the pressure transducers, load cells, and thermocouples placed on the test stand as well as within the combustion chamber and injector. These are sent to a Raspberry Pi 3, where voltages are processed, logged, and displayed by the instrumentation software written in the block diagram coding program LabVIEW. 

## Installing LabJack UD Drivers and Test Applications

First go to the links below to install the following programs

Download LabJack UD drivers for LabVIEW: 
https://labjack.com/support/software/examples/ud/labview

Download LabJack UD series testing applications package :
https://labjack.com/support/software/installers/ud

The LJUD test applications will require you to run the executable and download to User>Program Files (x86)>LabJack.
For our testing purposes, the two useful applications are LJStreamUD and LJControlPanel. As recommended by LabJack, it's easiest to extract the .zip file containing the LJ_UD drivers directly into the same 
folder your test applications are stored. 

Running any of UVR's instrumentation VI's that contain LJ_UD drivers will prompt you to find them within the drivers folder manually. However, you will only need to do this the first time that file is opened. It is best practice to, whenever a new instrunetation VI requiring LJ_UD drivers is created, to copy the driver VI's into the folder containing the instrumentation VI

The "Signal Manipulation" VI can be found in the "Old Instrumentation" Folder (In new instrumentation as a reference for sensor gain/offset)
